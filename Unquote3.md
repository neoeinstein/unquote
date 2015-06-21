# Introduction #

It's been over two years since the last release of Unquote. Partly because it is version 2.2.2 is very stable, partly because breaking changes in vs2012 and F# 3.0 delayed value in upgrading from vs2010 and F# 2.0. However, things have stabilized around vs2013 and F# 3.1, so we are due for some new bits!

# Planned Features #

The following are the main features planned for Unquote 3.0.0.
  1. (breaking change) Drop support for Silverlight4.
  1. Add support for net45 and portable profile 259 (upgrade main solution and projects to vs2013 / F# 3.1)
  1. Continue support for net40 (maintain secondary vs2010 solution file and projects)
  1. (breaking change) Deprecate '?' suffixed operators (they conflict with F# 3.1 nullable operators) and replace with '!' suffixed operators
  1. Add xUnit.net 2.x integration
  1. Add Fuchu integration
  1. (breaking change) `Swensen.Unquote.Operators.unquote` to return first-class object rather than print to stdout (will use `StructuredFormatDisplay` for FSI pretty printing)
  1. (minor breaking change - needs tests around reduction) introduced `ReductionException` for distinguishing between exceptions raised during reduction vs. non-raised exception values. Use this information to do smarter decompilation. Namely, only print stack traces for raised exceptions.

# TODO #
  * (out of scope) Possibly do better automating testing, building, and packing with fake
  * (no - can have issues) Possibly add FSharp.Core dependencies in NuGet package