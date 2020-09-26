# Repro for GCP Functions alpha package

Trying to build a library while having the package as a dep fails.

The project file: 

```xml
  <PropertyGroup>
    <TargetFramework>netcoreapp3.1</TargetFramework>
  </PropertyGroup>

  <ItemGroup>
    <PackageReference Include="Google.Cloud.Functions.Hosting" Version="1.0.0-alpha12" />
  </ItemGroup>
```

```sh
14:03 $ dotnet build
Microsoft (R) Build Engine version 16.6.0+5ff7b0c9e for .NET Core
Copyright (C) Microsoft Corporation. All rights reserved.

  Determining projects to restore...
  Restored /Users/bruno/temp/repro-gcp-func/repro-gcp-func.csproj (in 349 ms).
CSC : error CS2017: Cannot specify /main if building a module or library [/Users/bruno/temp/repro-gcp-func/repro-gcp-func.csproj]

Build FAILED.

CSC : error CS2017: Cannot specify /main if building a module or library [/Users/bruno/temp/repro-gcp-func/repro-gcp-func.csproj]
    0 Warning(s)
    1 Error(s)
```