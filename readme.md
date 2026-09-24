# 🏗️ .NET Clean Architecture Template

Proudction ready template for creating mircoservices using .NET with Clean Architecture.

### Koryagin Roman

**👨‍💻 GitHub:** [@softwarekoryaginrs-rgb](https://github.com/softwarekoryaginrs-rgb)  

## 📋 What does this template create?

After running the command `dotnet new Capi -n MyProject` the following structure is created:

```bash
MyProject/
├── README.md                 
├── MyProject.API/            
├── MyProject.Application/    
├── MyProject.Domain/         
└── MyProject.Infrastructure/ 
```

## 🚀 Quick Start

### 1. Add Nuget Source GitHub Packages

Create **[Personal Access Token](https://github.com/settings/tokens/new)** on GitHub with rights
`read:packages` and run following commands:

### Template
```bash
dotnet nuget add source https://nuget.pkg.github.com/<GITHUB_USERNAME>/index.json \
  --name <CUSTOM_NUGET_NAME> \
  --username <YOUR_GITHUB_USERNAME> \
  --password <YOUR_PERSONAL_ACCESS_TOKEN> \
  --store-password-in-clear-text
```

### Example
```bash
dotnet nuget add source https://nuget.pkg.github.com/iksergey/index.json \
  --name github-iksergey \
  --username iksergey \
  --password PCH2Y60YqR7qg8lfyZcjCP3BQ4yr \
  --store-password-in-clear-text
```

### 2. Install the template

```bash
dotnet new install softwarekoryaginrs.cleanarchitecture.template
```

### 3. Using template

```bash

dotnet new Capi -n MyMicroservice

cd MyMicroservice
dotnet build
dotnet run --project MyMicroservice.API
```

## 🔧 Local template development

```bash

git clone https://github.com/softwarekoryaginrs-rgb/dotnet-clean-architecture-template
cd dotnet-clean-architecture-template

cd working
dotnet new install .

dotnet new Capi -n TestProject


dotnet new uninstall "/полный/путь/к/working"
```

## 📋 Creating the project

```bash
dotnet new web -n "Capi.API"   
dotnet new classlib -n "Capi.Domain"  
dotnet new classlib -n "Capi.Application"  
dotnet new classlib -n "Capi.Infrastructure"

dotnet new gitignore   
```

## 🛠️ Dependencies

### Swagger

1. Libraty installation:
   ```bash
   dotnet add package "Swashbuckle.AspNetCore"
   ```
2. Services injection:
   ```csharp
   builder.Services.AddEndpointsApiExplorer();
   builder.Services.AddSwaggerGen();
   ```
3. Application configuration:
   ```csharp
    app.UseSwagger();
    app.UseSwaggerUI();
   ```

### For using `IServiceCollection`

```bash
dotnet add package "Microsoft.Extensions.DependencyInjection.Abstractions"
```

### For using `IConfiguration`

```bash
dotnet add package "Microsoft.Extensions.Configuration"
```
