
# LusterShop
## Modern E-Commerce Platform (Chandelier & Lighting Store)

A **scalable, clean-layered e-commerce system** built with **ASP.NET Core MVC** on **.NET 9**, following **Domain-Driven Design (DDD)** and **Clean Architecture** principles.  
Initially developed as a **chandelier online store** for a university project, but designed to support **any product category** with full extensibility.

---

## Features
- Full product catalog with categories, filters, and search
- Shopping cart & multi-step checkout
- Admin dashboard (CRUD for products, categories, orders)
- Responsive UI with Bootstrap 5
- Layered architecture: **Domain → Application → Data → Web**
- Dependency Injection (IoC) via built-in container
- Entity Framework Core with SQL Server
- Migration-based database setup
- Ready for future extensions (payment gateway, inventory, reviews, etc.)

---

## Technologies
- **.NET 9** – Latest LTS version with performance improvements
- **ASP.NET Core MVC** – Server-side rendered views with Razor
- **Entity Framework Core 9** – Code-First ORM with migrations
- **SQL Server** – Production-ready relational database
- **Bootstrap 5** – Responsive and mobile-first frontend
- **Clean Architecture** – Separation of concerns across layers

---

## Project Purpose
This project was created as part of a **software development course** to demonstrate:
- Building a **real-world e-commerce platform** using modern .NET practices
- Applying **layered architecture** with clear responsibilities
- Using **EF Core migrations** for database evolution
- Creating a **reusable, maintainable, and extensible** codebase

> While submitted as a **chandelier store**, the system is **fully generic** and can sell furniture, electronics, clothing, or any product.

---

## Project Structure
```
LusterShop/
├── LusterShop.Web/              (ASP.NET Core MVC - Presentation Layer)
├── LusterShop.Application/      (Use Cases, DTOs, Interfaces)
├── LusterShop.Domain/           (Entities, Value Objects, Domain Logic)
├── LusterShop.Data/             (EF Core, DbContext, Repositories)
├── LusterShop.Tests/            (xUnit / NUnit tests - optional)
├── README.md
└── LusterShop.sln
```

---

## Prerequisites
- [.NET 9 SDK](https://dotnet.microsoft.com/download/dotnet/9.0)
- [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-downloads) (LocalDB or full instance)
- Visual Studio 2022/2025, Rider, or VS Code

---

## Setup

### 1. Clone the repository
```bash
git clone https://github.com/benAliAlizadeh/LusterShop.git
cd LusterShop
```

### 2. Restore packages
```bash
dotnet restore
```

### 3. Configure database
Update connection string in `LusterShop.Web/appsettings.json`:
```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=(localdb)\\mssqllocaldb;Database=LusterShopDb;Trusted_Connection=True;MultipleActiveResultSets=true"
  }
}
```

### 4. Apply migrations
```bash
cd LusterShop.Web
dotnet ef migrations add InitialCreate --project ../LusterShop.Data
dotnet ef database update --project ../LusterShop.Data
```

### 5. Run the project
```bash
dotnet run
```
> Open browser: `https://localhost:5001`

---

## Usage
- **Customers**: Browse products → Add to cart → Checkout
- **Admin**: Login at `/Admin` → Manage products, categories, orders
- **Seed Data**: Initial data (sample chandeliers) added on first migration

---

## Screenshots (Add later)
```
screenshots/
├── home.png
├── product-detail.png
├── cart.png
├── admin-dashboard.png
└── admin-products.png
```

---

## Contributing
Contributions, bug reports, and feature suggestions are welcome!  
Open an [Issue](https://github.com/benAliAlizadeh/LusterShop/issues) or submit a [Pull Request](https://github.com/benAliAlizadeh/LusterShop/pulls).

---

## Persian Description (توضیحات فارسی)
این پروژه یه **فروشگاه آنلاین لوستر و روشنایی** هست که با **دات نت ۹** و **ASP.NET Core MVC** نوشته شده. از **معماری لایه‌ای تمیز** (Domain, Application, Data, Web) استفاده می‌کنه و کاملاً **قابل گسترش** برای فروش هر نوع محصولیه.  
برای درس توسعه نرم‌افزار دانشگاه ساخته شده، ولی کدش **حرفه‌ای، عمومی و آماده استفاده در رزومه** هست.  
دیتابیس با **SQL Server** و **EF Core** مدیریت میشه و از **مهاجرت‌ها (Migrations)** برای ساخت دیتابیس استفاده شده.

---

**Developed by [Ali Alizadeh](https://alizadeh82.ir/)**
