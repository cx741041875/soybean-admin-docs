## 目录规范

```bash
soybean-admin
├── .husky                     //git commit提交钩子，提交前检查代码格式和提交commit内容的格式
├── .vscode                    //vscode插件和设置
├── build                      //vite构建相关配置和插件
│   ├── define                 //定义的全局常量，通过vite构建时注入
│   ├── env                    //.env环境文件内容加载插件
│   └── plugins                //构建插件
│       ├── html.ts            //html插件(注入变量，压缩代码等)
│       ├── iconify.ts         //iconify图标插件
│       ├── visualizer.ts      //构建的依赖大小占比分析插件
│       ├── vue.ts             //vue相关vite插件
│       └── windicss.ts        //css框架插件
├── public                     //公共目录(文件夹里面的资源打包后会在根目录下)
│   ├── resource               //资源文件夹
│   └── favicon.ico            //网站标签图标
├── src
│   ├── assets                 //静态资源
│   ├── components             //全局组件
│   │   ├── business           //业务相关组件
│   │   ├── common             //公共组件
│   │   └── custom             //自定义组件
│   ├── composables            //组合式函数(从外部引入状态+内部状态)
│   │   ├── business           //业务相关composables
│   │   └── common             //通用composables
│   ├── config                 //全局常量配置
│   │   ├── business           //业务相关常量
│   │   └── common             //通用常量
│   ├── context                //上下文(通过provide和inject实现，用于组件之间的状态共享)
│   │   ├── app                //从app.vue注入的上下文
│   │   └── part               //局部组件注入的上下文
│   ├── directives             //vue指令
│   ├── enum                   //TS枚举
│   │   ├── business           //业务相关枚举
│   │   └── common             //通用枚举
│   ├── hooks                  //组合式的函数hooks(状态从函数里面产生)
│   │   ├── business           //业务相关hooks
│   │   └── common             //通用hooks
│   ├── interface              //TS类型接口
│   │   ├── business           //业务相关类型接口
│   │   └── common             //通用类型接口
│   ├── layouts                //布局组件
│   │   ├── BasicLayout        //基本布局(包含全局头部、多页签、侧边栏、底部等公共部分)
│   │   ├── BlankLayout        //空白布局组件(单个页面)
│   │   └── RouterViewLayout   //路由组件(作为多级路由之间的桥接)
│   ├── plugins                //插件
│   │   └── assets.ts          //各种依赖的静态资源导入(css、scss等)
│   ├── router                 //vue路由
│   │   ├── constant           //路由的名称、路径、标题声明
│   │   ├── modules            //按模块划分的路由页面
│   │   ├── guard              //路由守卫
│   │   ├── routes         		 //声明的路由
│   │   └── setup              //路由挂载函数
│   ├── service                //网络请求
│   │   ├── api                //接口api
│   │   ├── middleware         //请求结果的处理中间件
│   │   └── request            //封装的请求函数
│   ├── settings               //项目初始配置
│   │   └── theme.ts           //项目主题初始配置
│   ├── store                  //pinia状态管理
│   │   └── modules            //状态管理划分的模块
│   ├── styles                 //全局样式
│   │   ├── css                //css
│   │   └── scss               //scss
│   ├── typings                //TS类型声明文件(*.d.ts)
│   ├── utils                  //全局工具函数
│   │   ├── auth               //用户鉴权
│   │   ├── common             //通用工具函数
│   │   ├── package            //npm依赖
│   │   ├── router             //路由
│   │   ├── service            //请求相关的工具函数
│   │   └── storage            //存储
│   ├── views                  //页面
│   │   ├── about              //关于
│   │   ├── component          //插件、组件
│   │   ├── dashboard          //仪表盘
│   │   ├── document           //文档
│   │   ├── feat               //功能示例
│   │   ├── multi-menu         //多级菜单
│   │   └── system             //系统内置页面：登录、异常页等
│   ├── App.vue                //vue文件入口
│   ├── AppProvider.vue        //配置naive UI的vue文件(国际化,loadingBar、message等组件)
│   └── main.ts                //项目入口ts文件
├── .cz-config.js              //git cz提交配置
├── .editorconfig              //统一编辑器配置
├── .env                       //环境文件
├── .env.development           //环境文件(开发模式)
├── .env.production            //环境文件(生产模式)
├── .env.staging               //环境文件(自定义staging模式)
├── .eslintignore              //忽略eslint检查的配置文件
├── .eslintrc.js               //eslint配置文件
├── .gitignore                 //忽略git提交的配置文件
├── .prettierrc.js             //prettier代码格式插件配置
├── CHANGELOG.md               //项目变更日志
├── commitlint.config.js       //commitlint提交规范插件配置
├── index.html
├── package.json               //npm依赖描述文件
├── pnpm-lock.yaml             //npm包管理器pnpm依赖锁定文件
├── README.md                  //项目介绍文档
├── tsconfig.json              //TS配置
├── vite.config.ts             //vite配置
└── windi.config.ts            //windicss框架配置
```
