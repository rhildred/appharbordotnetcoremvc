# appharbordotnetcoremvc
dotnet core mvc 2.0 on appharbor

1. `dotnet new mvc`
2. `dotnet new sln`
3. `dotnet sln add <>.csproj`

Then you want to change the <>.csproj from

```

<Project Sdk="Microsoft.NET.Sdk.Web">

  <PropertyGroup>
    <TargetFramework>netcoreapp2.0</TargetFramework>
  </PropertyGroup>

  <ItemGroup>
    <PackageReference Include="Microsoft.AspNetCore.All" Version="2.0.5" />
  </ItemGroup>

  <ItemGroup>
    <DotNetCliToolReference Include="Microsoft.VisualStudio.Web.CodeGeneration.Tools" Version="2.0.2" />
  </ItemGroup>

</Project>

```

to this


```

<Project Sdk="Microsoft.NET.Sdk.Web" DefaultTargets="Publish">

  <PropertyGroup>
    <TargetFramework>netcoreapp2.0</TargetFramework>
    <PublishDir>$(OutDir)_PublishedWebsites\NetCoreApp\</PublishDir>
  </PropertyGroup>

  <ItemGroup>
    <PackageReference Include="Microsoft.AspNetCore.All" Version="2.0.5" />
  </ItemGroup>

  <ItemGroup>
    <DotNetCliToolReference Include="Microsoft.VisualStudio.Web.CodeGeneration.Tools" Version="2.0.2" />
  </ItemGroup>

</Project>

```

Push to bitbucket or github, deploy on appharbor
