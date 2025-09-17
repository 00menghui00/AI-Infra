# AI-Infra


# smolagents
- 模型资源：在huggingface中建一个token，使用codeagent时用该token，可以免费使用开源编码模型


---

## codeagent
smolagents中有一个codeagent类（ https://huggingface.co/blog/smolagents#code-agents ），这个类可以实现编码并执行（接入了E2B沙盒环境 https://e2b.dev/ ）  

- CodeAgent 里，默认是一个 受限沙盒环境，为了安全，它不允许随便 import 库。如果希望 Agent 在生成代码时能导入特定库，就必须 提前声明允许的库。

---

## tools

- 沙盒环境无法直接访问本地数据，可以将本地数据封装到tool中作为一个接口供沙盒环境访问（当执行程序需要本地数据支持时可以这样操作）
