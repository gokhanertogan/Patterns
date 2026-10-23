# Patterns

Small, self-contained C# console apps illustrating 15 of the classic Gang of Four design patterns.

> **📦 Archived** — this is an early learning project (2020), kept for reference only. It is not maintained.

![.NET Framework](https://img.shields.io/badge/.NET%20Framework-4.6.1-512BD4?logo=dotnet)
![C#](https://img.shields.io/badge/C%23-7.3-239120?logo=csharp)
![Status](https://img.shields.io/badge/status-archived-lightgrey)

## Overview

Each pattern lives in its own console project with a single `Program.cs` that contains the participants and a short demo in `Main`. Console output and some sample data are in Turkish.

| Category | Project | Example scenario |
|---|---|---|
| Creational | `AbstractFactory` | Content + publisher families (video/Facebook, blog/Twitter) |
| Creational | `BuilderMethod` | Building greeting messages step by step |
| Creational | `FactoryMethod` | Roles that create their own permission sets |
| Creational | `ProtoTypeMethod` | Cloning a prototype car via `ICloneable` |
| Creational | `SingletonDesignMethod` | Single `DbHelper` instance |
| Structural | `AdapterMethod` | Adapting a bank POS reader to a common interface |
| Structural | `BridgeMethod` | Reports decoupled from their output format (web/desktop) |
| Structural | `CompositeDesignMethod` | Generic tree of book categories and books |
| Structural | `DecoratorMethod` | Adding signing/encryption to a mail |
| Structural | `FacadeMethod` | One `OrderFacade` over order, order-detail and stock managers |
| Structural | `FlyweightMethod` | Sharing balloon objects per colour (`System.Drawing`) |
| Structural | `ProxyPatern` | Proxy in front of a product service |
| Behavioral | `ChainResponsibility` | Meeting-room search passed along country handlers |
| Behavioral | `CommandMethod` | Order operations wrapped as commands |
| Behavioral | `IteratorMethod` | Custom iterator over a category collection |

## Tech stack

- C# console applications, .NET Framework 4.6.1 (classic, non-SDK-style `.csproj`)
- No external NuGet dependencies

## Project structure

```
Patterns.sln
├── AbstractFactory/        Program.cs, App.config, Properties/
├── AdapterMethod/
├── ...                     one folder per pattern, same layout
└── SingletonDesignMethod/
```

## Getting started

Prerequisites: Windows with Visual Studio 2017+ (or Build Tools) and the .NET Framework 4.6.1 Developer Pack.

1. Open `Patterns.sln`.
2. Set the pattern you want to see as the startup project and run it (most demos wait for a key press before exiting).

On macOS/Linux the solution does not build as-is because the .NET Framework 4.6.1 reference assemblies are missing; the source files themselves compile unchanged when placed in an SDK-style console project.

## Notes and limitations

- `FlyweightMethod` contains the pattern classes but its `Main` is empty, so it prints nothing.
- The singleton is the simple lazy version and is not thread-safe.
- These are minimal teaching examples, without tests or error handling.
