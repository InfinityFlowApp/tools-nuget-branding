# InfinityFlow NuGet Branding

[![GitHub Actions Workflow Status](https://img.shields.io/github/actions/workflow/status/InfinityFlowApp/tools-nuget-branding/release.yml)](https://github.com/InfinityFlowApp/tools-nuget-branding/actions?query=branch%3Amain)
[![GitHub Release](https://img.shields.io/github/v/release/InfinityFlowApp/tools-nuget-branding)](https://github.com/InfinityFlowApp/tools-nuget-branding/releases)
[![GitHub License](https://img.shields.io/github/license/InfinityFlowApp/tools-nuget-branding)](https://github.com/InfinityFlowApp/tools-nuget-branding?tab=MIT-1-ov-file)

A NuGet package that sets the MSBuild properties such as Authors,
PackageIcon, PackageLicenseFile, PackageReadmeFile, Copyright,
and puts assets for Package Icon.

Please ensure to revise the License and Readme files taken
from the Solution before proceeding with the MSBuild.

## Installation
To install this package, use the NuGet Package Manager Console:

```shell
PM> Install-Package InfinityFlow.Tools.Branding
```
Or you can search for "InfinityFlow.Tools.Branding" in the NuGet Package Manager UI and install it from there.

## Usage
After installing the package, the MSBuild properties will be set automatically.
You can modify the properties by updating the values in your .csproj or .vbproj file.

For example, to set the Authors property, add the following to your .csproj or .vbproj file:

```xml
<PropertyGroup>
    <Authors>John Doe;Jane Smith</Authors>
</PropertyGroup>
```

## MSBuild Properties
This package sets the following MSBuild properties:

- Authors
- PackageIcon
- PackageLicenseFile
- PackageReadmeFile
- Copyright

You can modify these properties by updating your .csproj or .vbproj file as described in the Usage section.

## Assets
This package includes the following assets:

- PackageIcon: `assets/packageIcon.png`
- License: `LICENSE`
- Readme file: `README.md`

To access the assets, use the relative paths shown above.

Except the PackageIcon, License and Readme are taken from Solution Root folder, unless specified differently.

```xml
<ItemGroup>
  <None Pack="true" PackagePath="" Include="$(SolutionDir)/LICENSE" />
  <None Pack="true" PackagePath="" Include="$(SolutionDir)/README.md" />
</ItemGroup>
```

## Contributing
If you find a bug or have a feature request, please create an issue in the GitHub repository.

## License
This package is released under the MIT License. See the LICENSE file for details.

