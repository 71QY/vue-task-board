Vue3 能源管理平台
基于 Vue3 + TypeScript + Vite 开发的能源管理前端系统，针对充电站日常运维、设备监控、能耗统计、运营数据分析等业务场景开发。项目功能完整、代码结构规范，适合作为实战练手、课程设计、毕业设计项目

项目介绍
本系统是一套基于 Vue 3 + TypeScript 构建的企业级充电站能源管理前端解决方案。项目深度聚焦场站监控、设备运维、数据可视化及权限管控等核心业务场景，摒弃冗余装饰，坚持实战导向。得益于 Vite 的高效构建与全量 TypeScript 类型约束，系统兼具极速启动体验与卓越的代码稳定性。内置完善的本地 Mock 数据服务，无需后端依赖即可完整预览全流程业务效果，是快速搭建能源管理平台的理想基石

核心优势
 极速开发体验：Vite 构建工具，秒级启动，热更新快速
 类型安全：全程 TypeScript 强类型约束，减少运行时错误
 现代化 UI：Element Plus 组件库，美观且易用
 数据可视化：ECharts 图表展示，直观呈现运营数据
 权限控制：完善的 RBAC 权限管理体系
 地图集成：高德地图可视化展示站点分布
 开箱即用：Mock 数据支持，无需后端即可完整预览

主要功能
数据可视化大屏
 实时展示设备运行状态、能耗数据、收益统计
 多维度数据趋势图表分析
 关键指标一目了然

充电站管理
 实时监控场站、充电桩运行状态
 设备故障信息记录与追踪
 场站收益数据统计与分析

地图点位展示
 集成高德地图 API
 可视化展示充电站地理位置
 站点分布情况一目了然

设备告警管理
 统一收集设备异常、离线、故障告警
 支持多条件筛选与分类
 方便运维快速排查问题

运营数据管理
 全量充电订单管理
 日常运营数据统计
 支持 Excel 表格数据导出

文档管理
 内置 TinyMCE 富文本编辑器
 在线编辑、保存运维文档
 操作说明归档管理

权限管理
 基于角色的访问控制（RBAC）
 页面路由级别权限拦截
 按钮级别权限显示/隐藏

个人中心
 账号信息管理
 密码修改功能
 系统操作日志记录

核心技术
 框架：[Vue 3.5.10](https://vuejs.org/) - 渐进式 JavaScript 框架
 语言：[TypeScript 5.5.3](https://www.typescriptlang.org/) - JavaScript 的超集
 构建工具：[Vite 5.4.8](https://vitejs.dev/) - 下一代前端构建工具

路由与状态管理
 路由：[Vue Router 4.4.5](https://router.vuejs.org/) - Vue.js 官方路由
 状态管理：[Pinia 2.2.4](https://pinia.vuejs.org/) - Vue 官方推荐的状态管理库

UI 与可视化
 UI 框架：[Element Plus 2.8.5](https://element-plus.org/) - 基于 Vue 3 的组件库
 图标：[@element-plus/icons-vue](https://element-plus.org/en-US/component/icon.html)
 图表：[ECharts 5.5.1](https://echarts.apache.org/) - 强大的数据可视化库

工具库
 HTTP 客户端：[Axios 1.7.7](https://axios-http.com/) - 基于 Promise 的 HTTP 客户端
 Mock 数据：[MockJS](http://mockjs.com/) - 生成随机数据，拦截 Ajax 请求
 Excel 处理：[XLSX](https://sheetjs.com/) + [FileSaver](https://github.com/eligrey/FileSaver.js/)

第三方集成
 地图服务：[@amap/amap-jsapi-loader](https://lbs.amap.com/api/javascript-api/summary) - 高德地图 JS API
 富文本编辑器：[@tinymce/tinymce-vue](https://www.tiny.cloud/docs/integrations/vue/) - TinyMCE 编辑器

样式处理：
CSS 预处理器：[Less 4.2.0](https://lesscss.org/)


项目结构
Vue3能源管理平台项目实战/
├── src/
│   ├── api/                    # API 接口统一管理
│   │   ├── alarm.ts           # 告警相关接口
│   │   ├── chargingstation.ts # 充电站相关接口
│   │   ├── dashboard.ts       # 仪表盘相关接口
│   │   ├── document.ts        # 文档相关接口
│   │   ├── map.ts             # 地图相关接口
│   │   ├── operation.ts       # 运营相关接口
│   │   ├── system.ts          # 系统相关接口
│   │   └── user.ts            # 用户相关接口
│   ├── components/            # 全局公共组件
│   │   ├── TopHeader/         # 顶部导航栏
│   │   ├── map/               # 地图组件
│   │   ├── navMenu/           # 导航菜单
│   │   └── stepForm/          # 步骤表单
│   ├── directives/            # 自定义指令
│   │   └── permission.ts      # 权限指令
│   ├── hooks/                 # 组合式函数
│   │   ├── useChart.ts        # 图表相关 Hook
│   │   ├── useHttp.ts         # HTTP 请求 Hook
│   │   └── usePagination.ts   # 分页 Hook
│   ├── layouts/               # 布局组件
│   │   ├── DefaultLayout.vue  # 默认布局
│   │   └── TabsLayout.vue     # 标签页布局
│   ├── mock/                  # Mock 数据
│   │   └── index.ts           # Mock 配置
│   ├── router/                # 路由配置
│   │   ├── basicRouteMap.ts   # 基础路由映射
│   │   ├── guard.ts           # 路由守卫
│   │   └── index.ts           # 路由入口
│   ├── store/                 # Pinia 状态管理
│   │   ├── auth.ts            # 认证状态
│   │   ├── station.ts         # 站点状态
│   │   └── tabs.ts            # 标签页状态
│   ├── types/                 # TypeScript 类型定义
│   │   ├── station/           # 站点相关类型
│   │   └── user/              # 用户相关类型
│   ├── utils/                 # 工具函数
│   │   ├── axios.ts           # Axios 封装
│   │   ├── http.ts            # HTTP 工具
│   │   ├── toThousands.ts     # 千分位格式化
│   │   └── transformMenu.ts   # 菜单转换工具
│   ├── views/                 # 业务页面
│   │   ├── alarm/             # 告警管理
│   │   ├── chargingstation/   # 充电站管理
│   │   ├── dashboard/         # 数据仪表盘
│   │   ├── document/          # 文档管理
│   │   ├── equipment/         # 设备管理
│   │   ├── map/               # 电子地图
│   │   ├── operations/        # 运营管理
│   │   ├── personal/          # 个人中心
│   │   ├── system/            # 系统设置
│   │   ├── Login.vue          # 登录页面
│   │   └── NotFound.vue       # 404 页面
│   ├── App.vue                # 根组件
│   └── main.ts                # 应用入口
├── public/                    # 静态资源
├── index.html                 # HTML 模板
├── package.json               # 项目依赖
├── tsconfig.json              # TypeScript 配置
├── vite.config.ts             # Vite 配置
└── README.md                  # 项目说明

 
 快速开始
环境要求
 Node.js >= 16.0.0
 npm >= 7.0.0 或 yarn >= 1.22.0

安装步骤
 1 克隆项目
bash
git clone https://github.com/your-username/energy-management-platform.git
cd energy-management-platform

2 安装依赖
bash
使用 npm
npm install

或使用 yarn
yarn install

或使用 pnpm
pnpm install


3 启动开发服务器
bash
npm run dev
或
yarn dev

浏览器访问：[http://localhost:5173](http://localhost:5173)

4 构建生产版本
bash
npm run build
或
yarn build
构建完成后，dist 目录即为可部署的生产环境文件。

5 预览生产构建
bash
npm run preview
或
yarn preview


配置说明
环境变量配置
在项目根目录创建 `.env` 文件：
env

开发环境
VITE_APP_BASE_API=/api
VITE_APP_MAP_KEY=你的高德地图Key

生产环境
VITE_APP_BASE_API=https://api.yourdomain.com
VITE_APP_MAP_KEY=你的高德地图Key


Mock 数据开关
在 `src/main.ts` 中控制 Mock 启用：
typescript
// 开发环境启用 Mock
if (import.meta.env.DEV) {
  import('./mock')
}

高德地图密钥配置
1. 前往 [高德开放平台](https://lbs.amap.com/) 注册账号
2. 创建应用并获取 Web 端 Key
3. 在环境变量文件中配置 `VITE_APP_MAP_KEY`


常见问题
Q1: 地图无法加载？
A: 请检查以下几点：
 是否正确配置了高德地图 Key
 网络连接是否正常
 浏览器控制台是否有报错信息

Q2: 如何对接真实后端？
A:
1. 关闭 Mock 数据，注释掉 `src/main.ts` 中的 mock 导入
2. 修改 `src/utils/axios.ts` 中的 `baseURL` 配置
3. 根据实际后端接口调整 API 路径

Q3: 如何修改主题颜色？
A: Element Plus 支持主题定制，可在 `vite.config.ts` 中配置：
typescript
css: {
  preprocessorOptions: {
    less: {
      modifyVars: {
        'primary-color': '#409EFF',
      },
    },
  },
}

Q4: 生产环境部署注意事项？
A:
 确保关闭 Mock 数据
 配置正确的 API 代理或 CORS
 如使用 History 模式，需配置服务器重定向规则
 建议启用 Gzip 压缩优化加载速度

Q5: 如何添加新页面？
A:
1. 在 `src/views/` 下创建新页面组件
2. 在 `src/router/index.ts` 中添加路由配置
3. 如需菜单显示，在路由 meta 中配置菜单信息


贡献指南
欢迎提交 Issue 和 Pull Request！

贡献步骤
1. Fork 本仓库
2. 创建特性分支 `git checkout -b feature/AmazingFeature`
3. 提交更改 `git commit -m 'Add some AmazingFeature'`
4. 推送到分支 `git push origin feature/AmazingFeature`
5. 开启 Pull Request

代码规范
 遵循 [Vue 风格指南](https://cn.vuejs.org/style-guide/)
 使用 TypeScript 严格模式
 组件命名采用 PascalCase
 提交信息遵循 [Conventional Commits](https://www.conventionalcommits.org/)


许可说明
本项目采用 [MIT License](LICENSE) 开源协议。

使用范围：
 允许个人学习与练习
 允许课程设计与毕业设计
 允许企业内部项目参考
 禁止直接用于商业项目
 禁止违规用途


联系方式
如有问题或建议，欢迎通过以下方式联系：
 邮箱：1396587508@qq.com
 CSDN：https://blog.csdn.net/name_1111
如果这个项目对你有帮助，欢迎 star、fork、share
