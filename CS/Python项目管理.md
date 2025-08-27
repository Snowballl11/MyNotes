## Python 官方管理工具流程：

1. 创建虚拟环境（解决项目之间的依赖冲突）：`python -m venv .venv`

2. 激活虚拟环境：`source .venv/bin/activate`

3. 安装依赖：

   ```bash
   pip install flask
   ```

   使别人能复现环境：`pip freeze > requirements.txt`[^1]

   通过`pip install -r requirements.txt`命令来安装

4. 在 pyproject.toml 中声明项目的直接依赖[^2]：

   ```toml
   [project]
   name = "proj"
   version = "0.1.0"
   dependencies = [
       "flask>=3.1.1"
   ]
   ```

   通过 `pip install -e .` 命令来安装

5. 流程回顾：

   ```bash
   python -m venv .venv
   source .venv/bin/activate
   edit project.toml
   pip install -e .
   ```

## 使用 uv 做项目管理：

1. 初始项目中只有 main.py 和只包含项目名称和版本号的 pyproject.toml

2. 安装依赖

   ```bash
   uv add flask
   ```

   这条命令会自动修改 pyproject.toml 文件，检查并自动创建 .venv 虚拟环境，把这个包和它所有的间接依赖全都安装到虚拟环境中

3. 如果我是项目的协作者

   ```bash
   uv sync
   ```

4. 运行代码

   ```bash
   uv run main.py
   ```

   $\Leftrightarrow $

   ```bash
   source .venv/bin/activate
   python main.py
   ```

[^1]: requirements.txt 中混合了所有的直接和间接依赖，为了解决这个问题，社区转向了 pyproject.toml 文件

[^2]: 手动编辑 pyproject.toml 文件太麻烦了，催生了像 uv 这样高层的项目管理工具
