# Open Blog App 项目说明

## 项目简介
Open Blog App 是一个基于 Spring Boot 的开源博客应用程序。该项目旨在提供一个简单、高效且易于扩展的博客系统，支持文章发布、用户评论、邮件通知等功能。

## 技术栈
- **Spring Boot**: 快速开发框架
- **MyBatis Plus**: ORM 框架，简化数据库操作
- **FastJSON2**: 阿里巴巴的 JSON 处理库
- **Hutool**: Java 工具类库
- **Transmittable Thread Local**: 支持线程上下文传递的本地线程工具
- **Lombok**: 简化 Java 代码编写
- **Redis**: 用于缓存和消息队列
- **MySQL**: 数据库存储

## 项目结构
```
open-blog-app/
├── deploy/                  # 部署相关文件
│   └── sql/
│       └── init.sql         # 初始化 SQL 脚本
├── src/
│   └── main/
│       ├── java/
│       │   └── cloud/
│       │       └── abaaba/
│       │           └── BlogApplication.java # 主启动类
│       └── resources/
│           └── application.yml              # 配置文件
├── README.md                # 项目说明文档
└── pom.xml                  # Maven 项目配置文件
```


## 功能特性
- 文章管理：支持文章的创建、编辑、删除和展示
- 用户评论：用户可以对文章进行评论
- 邮件通知：支持邮件发送功能，可用于注册、评论提醒等
- Redis 缓存：提升系统性能，减少数据库压力
- 多数据源支持：通过 MyBatis Plus 实现灵活的数据访问层

## 安装与部署

### 环境要求
- JDK 1.8 或以上版本
- MySQL 8.0 或以上版本
- Redis 3.0 或以上版本

### 步骤
1. **克隆项目**
   ```bash
   git clone https://github.com/yourname/open-blog-app.git
   cd open-blog-app
   ```


2. **数据库初始化**
    - 导入 `deploy/sql/init.sql` 文件到 MySQL 数据库中，创建相应的表结构。

3. **配置修改**
    - 修改 `src/main/resources/application.yml` 文件，配置数据库连接、Redis 连接、邮件服务器等信息。

4. **构建项目**
   ```bash
   mvn clean package
   ```


5. **运行项目**
   ```bash
   java -jar target/open-blog-app-1.0-SNAPSHOT.jar
   ```


6. **访问应用**
    - 打开浏览器，访问 `http://localhost:8080` 即可使用博客系统。

## 开发者指南
- **代码风格**：遵循阿里巴巴 Java 开发规范
- **日志输出**：使用 Spring Boot 自带的日志框架（如 Logback）
- **异常处理**：统一的全局异常处理器
- **单元测试**：使用 JUnit 和 Mockito 进行单元测试覆盖

## 贡献指南
欢迎贡献代码！请遵循以下步骤：
1. Fork 仓库
2. 创建新分支 (`git checkout -b feature/new-feature`)
3. 提交更改 (`git commit -m 'Add new feature'`)
4. 推送分支 (`git push origin feature/new-feature`)
5. 提交 Pull Request

## 许可证
本项目采用 MIT 许可证，请查看 [LICENSE](LICENSE) 文件了解详细信息。

## 联系方式
- 作者：Pig-Gua
- 邮箱：pig_gua@example.com
- GitHub：[https://github.com/yourname/open-blog-app](https://github.com/yourname/open-blog-app)

---

感谢您选择使用 Open Blog App！如果您有任何问题或建议，请随时联系我。