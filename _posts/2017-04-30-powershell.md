---
title: PowerShell
code: |-
  - 0.1 + 0.2
  - 0.1 + 0.2 -eq 0.3
  - [decimal]0.1 + [decimal]0.2 -eq [decimal]0.3
  - 0.1d + 0.2d -eq 0.3d
result: |-
  - 0.3
  - False
  - True
  - True
---

PowerShell by default uses double type, but because it runs on .NET it has the
same types as C# does. Thanks to that the [Decimal type][1] can be used -
directly by providing the type name `[decimal]` or via [suffix `d`][2].

More about that in the [C# section][3].

[1]: https://docs.microsoft.com/en-us/dotnet/api/system.decimal?view=net-5.0
[2]: https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_numeric_literals?view=powershell-7.1#real-literals
[3]: #csharp

