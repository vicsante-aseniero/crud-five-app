# CRUD Five App

A full-stack CRUD sample application using **Next.js 15** (TypeScript) for the front-end and **.NET 8.0** for the back-end services, with DevContainer support for streamlined development.

---

## 🏗️ Project Structure

```
crud-five-app/
├── .devcontainer/          # DevContainer configuration
│   ├── devcontainer.json   # Dev container settings
│   ├── docker-compose.yml  # Container orchestration
│   ├── Dockerfile          # .NET 8.0 base image
│   ├── mssql/              # SQL Server tools & scripts
│   └── postCreateCommand.sh
├── ui/                     # Front-end (Next.js 15 + TypeScript)
│   ├── app/                # App Router pages
│   ├── public/             # Static assets
│   └── package.json        # Node dependencies
├── api/                    # REST API (.NET 8.0 Minimal API)
│   ├── Program.cs          # API entry point
│   └── crud-api.csproj     # Project file
├── grpc/                   # gRPC Service (.NET 8.0)
│   ├── Program.cs          # Service entry point
│   ├── Services/           # gRPC service implementations
│   ├── Protos/             # Protocol buffer definitions
│   └── crud-grpc.csproj    # Project file
└── crud-app.sln            # Solution file
```

---

## 🚀 Technology Stack

### Front-end (`ui/`)

| Technology  | Version | Purpose                         |
| ----------- | ------- | ------------------------------- |
| Next.js     | 15.5.2  | React framework with App Router |
| React       | 19.1.0  | UI library                      |
| TypeScript  | ^5      | Type safety                     |
| TailwindCSS | ^4      | Utility-first styling           |
| ESLint      | ^9      | Code linting                    |

### Back-end (`api/`)

| Technology               | Version | Purpose           |
| ------------------------ | ------- | ----------------- |
| .NET                     | 8.0     | Runtime framework |
| ASP.NET Core Minimal API | 8.0     | RESTful API       |
| Swagger/OpenAPI          | 8.0.18  | API documentation |
| Swashbuckle              | 6.6.2   | Swagger UI        |

### gRPC Service (`grpc/`)

| Technology       | Version | Purpose             |
| ---------------- | ------- | ------------------- |
| .NET             | 8.0     | Runtime framework   |
| Grpc.AspNetCore  | 2.57.0  | gRPC server         |
| Protocol Buffers | proto3  | Service definitions |

---

## 🛠️ Development Environment

### Prerequisites

- Docker Desktop
- VS Code with Remote - Containers extension

### Quick Start

1. **Clone the repository**

   ```bash
   git clone <repository-url>
   cd crud-five-app
   ```

2. **Open in DevContainer**
   - Open VS Code
   - Press `F1` → "Dev Containers: Reopen in Container"
   - Wait for container build and setup

3. **Start the Front-end**

   ```bash
   cd ui
   npm install
   npm run dev
   ```

   Access at: http://localhost:3000

4. **Start the API**

   ```bash
   cd api
   dotnet run
   ```

   Swagger UI: https://localhost:5001/swagger

5. **Start gRPC Service**
   ```bash
   cd grpc
   dotnet run
   ```

---

## 📦 DevContainer Features

The development container includes:

- **Languages & Runtimes**: .NET 8.0, Node.js LTS, TypeScript
- **Database Tools**: PostgreSQL Client, SQL Server Tools
- **API Tools**: Postman, REST Client, Protobuf Compiler
- **Testing**: Jest, Playwright, Cypress
- **Cloud**: LocalStack, AWS CLI, Dapr CLI
- **VS Code Extensions**: C# DevKit, ESLint, Prettier, GitHub Copilot, Docker

### Resource Limits

| Resource | Limit   | Reserved |
| -------- | ------- | -------- |
| CPU      | 8 cores | 2 cores  |
| Memory   | 8 GB    | 2 GB     |
| Swap     | 16 GB   | -        |

### Forwarded Ports

| Port | Service    |
| ---- | ---------- |
| 3000 | Next.js    |
| 5432 | PostgreSQL |
| 8080 | API        |
| 6379 | Redis      |

---

## 🔧 Available Scripts

### Front-end (`ui/`)

```bash
npm run dev      # Start development server (Turbopack)
npm run build    # Production build
npm run start    # Start production server
npm run lint     # Run ESLint
```

### Back-end (Solution)

```bash
dotnet build     # Build all projects
dotnet run       # Run specific project
dotnet test      # Run tests
```

---

## 📚 Additional Documentation

- [ANALYSIS.md](./ANALYSIS.md) - Detailed technical analysis
- [API README](./api/README.md) - API-specific documentation
- [gRPC README](./grpc/README.md) - gRPC service documentation
- [UI README](./ui/README.md) - Front-end documentation

---

## 📄 License

This project is for educational and demonstration purposes.
