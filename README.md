# AI生图网站说明书

## 网站目标

这个网站能够根据你输入的文字描述，自动生成相应的图片。

## 使用方法

1. 在输入框中填写你想要生成的图片描述，例如“一只飞翔的猫咪”。
2. 点击“生成图片”按钮。
3. 稍等片刻，网站就会显示生成的图片。

## 核心功能

* **文本输入**: 用户可以在这里输入生成图片的描述。
* **图片生成**: 根据用户输入的文本生成对应的图片。
* **图片展示**: 将生成的图片显示给用户。

## 技术组成 (简单理解)

* **前端 (你看到的部分)**: 负责展示网页，让你输入文字和看到图片。使用 **Next.js** 框架构建。
* **后端 (幕后工作者)**: 接收你的指令，告诉 AI 去生成图片，并把图片传回来。
* **AI模型 (魔法大脑)**: 真正理解你的文字，并画出图片的“大脑”。

## 当前项目技术栈

* **前端框架**: **Next.js**
    * **App Router**: 使用 Next.js 13 引入的 App Router 进行页面路由和布局管理。
    * **TypeScript**: 使用 **TypeScript** 作为主要的编程语言，为 JavaScript 代码添加静态类型检查，提高代码质量和可维护性。
    * **ESLint**: 使用 **ESLint** 进行代码静态分析，确保代码风格统一，并尽早发现潜在的错误。
    * **Turbopack**: 使用 **Turbopack** 作为开发服务器的构建工具，以提升本地开发的启动和热更新速度。
* **后端**: （待定，目前后端逻辑可能在 Next.js 的 API 路由中实现）
* **AI模型**: （待定，例如 Stable Diffusion）
* **服务器**: （待定）

## 目录结构

项目的主要代码位于根目录下。

* **`app`**: 使用 App Router 时，页面 (routes) 和布局 (layouts) 文件会放在这个目录下。
* **`public`**: 存放静态资源文件，例如图片。
* **`node_modules`**: 存放项目依赖的第三方库。
* **`package.json`**: 记录项目依赖和脚本命令。
* **`tsconfig.json`**: TypeScript 的配置文件。
* 其他配置文件 (例如 `.eslintrc.cjs`)。

## 快速开始

1. 确保你已经安装了 **Node.js** 和 **npm** (或者 **pnpm**, **yarn**)。
2. 克隆本项目到本地。
3. 在项目根目录下，运行 `npm install` (或者 `pnpm install`, `yarn install`) 安装依赖。
4. 运行 `npm run dev` (或者 `pnpm dev`, `yarn dev`) 启动开发服务器。
5. 在浏览器中访问 `http://localhost:3000` 查看效果。

## 关于技术选型的说明

* **TypeScript**: 你选择了使用 **TypeScript**。TypeScript 是一种 JavaScript 的超集，添加了静态类型检查。这可以帮助你在开发过程中更早地发现错误，并提高代码的可读性和可维护性。虽然学习曲线会稍微陡峭一些，但对于长期项目来说，这是一个很好的选择。
* **`src` 目录**: 你没有选择使用 `src` 目录。这意味着你的 `app` 目录（存放页面和路由）以及其他项目代码将直接位于项目的根目录下。虽然这是一种可行的项目结构，但使用 `src` 目录通常被认为是更好的实践，因为它更清晰地划分了源代码和配置文件。
* **Turbopack**: 你选择了使用 **Turbopack** 作为开发服务器的构建工具。Turbopack 据称可以提供更快的本地开发体验。由于它是一个相对较新的工具，可能会遇到一些未知的 bug 或不兼容性。如果你在开发过程中遇到问题，可以考虑切换回 Next.js 默认的构建工具。

## 后续开发注意事项

* 由于你选择了 **TypeScript**，你需要学习 TypeScript 的基本语法和类型定义。
* 你的页面文件将会放在 `app` 目录下，利用 Next.js 的 **App Router** 进行路由管理。
* 你可以通过修改 `app/page.tsx` (注意文件扩展名是 `.tsx`，因为使用了 TypeScript) 文件来修改网站的首页内容。
* 如果遇到任何问题，可以查阅 Next.js 的官方文档：[Next.js 文档](https://nextjs.org/docs)。
