# 音视频文件上传系统

这是一个基于Vue3和Spring Boot的音视频文件上传管理系统，支持音视频文件的上传、下载、播放和管理功能。

## 技术栈

### 前端
- Vue 3
- TypeScript
- Vue Router
- Pinia
- Element Plus
- Axios

### 后端
- Spring Boot
- MySQL
- JdbcTemplate
- 阿里云OSS

## 功能特性

- 文件上传：支持上传音频和视频文件到阿里云OSS
- 文件管理：分类显示音频和视频文件列表
- 文件播放：支持在线播放音频和视频文件
- 文件删除：支持删除已上传的文件

## 项目结构

```
├── media-upload-backend/    # 后端项目
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/org/example/
│   │   │   │   ├── controller/    # 控制器
│   │   │   │   ├── service/       # 服务层
│   │   │   │   ├── repository/    # 数据访问层
│   │   │   │   ├── entity/        # 实体类
│   │   │   │   ├── vo/            # 视图对象
│   │   │   │   ├── utils/         # 工具类
│   │   │   │   └── MediaUploadApplication.java  # 启动类
│   │   │   └── resources/
│   │   │       ├── application.yml  # 配置文件
│   │   │       └── schema.sql       # 数据库初始化脚本
│   └── pom.xml                     # Maven配置文件
│
└── media-upload-frontend/  # 前端项目
    ├── src/
    │   ├── api/            # API接口
    │   ├── components/     # 组件
    │   ├── router/         # 路由配置
    │   ├── views/          # 页面视图
    │   ├── App.vue         # 根组件
    │   └── main.ts         # 入口文件
    ├── index.html          # HTML模板
    ├── package.json        # NPM配置
    └── vite.config.ts      # Vite配置
```

## 快速开始

### 后端启动

1. 确保安装了Java 8+和Maven
2. 创建MySQL数据库`media_upload`
3. 修改`application.yml`中的数据库连接信息
4. 修改`AliOssUtil.java`中的阿里云OSS配置
5. 在后端目录中执行命令：
```
mvn spring-boot:run
```

### 前端启动

1. 确保安装了Node.js 14+
2. 在前端目录中执行命令：
```
npm install
npm run dev
```

## 访问地址

- 前端：http://localhost:3000
- 后端：http://localhost:8080