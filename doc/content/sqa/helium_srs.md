!template load file=sqa/app_srs.md.template app=Helium category=helium

!template! item key=system-purpose
{{app}} is a module to compute the fluid properties of helium gas using Spline-Based Table lookups (SBTL) for MOOSE applications.
SBTL is a fast method of computing properties from pre-generated tables of fluid properties. The {{app}} can compute properties such as
density, specific heat, or viscosity over the range of validity in pressure and temperature that the input data was defined on.
Helium fluid properties are useful to perform thermal hydraulic simulations of certain Gas-cooled Fast Reactors (GFRs). GFRs are
an advanced reactor concept currently under investigation in the United States by several private companies with support from
national laboratories.

!template! item key=system-scope
{{app}}'s scope is somewhat open-ended, as fluid properties are an important but generally not central part of a given simulation.
The initial scope of the development of {{app}} was to support Gas Fast Reactor analysis.
!template-end!

!template! item key=assumptions-and-dependencies
The {{app}} application is designed with the fewest possible constraints on hardware and software. It
inherits the assumptions and dependencies for its own dependencies - namely, the MOOSE framework,
MOOSE physics modules, and {{app}} submodule applications - which are listed at the beginning of this
document. Any physics-based assumptions in code simulations and code objects are highlighted in their
respective documentation pages.
!template-end!

!template! item key=user-characteristics
Like [!ac](MOOSE), there are three kinds of users working on the {{app}} application:

- +{{app}} application Developers+: These are the core developers of the {{app}} application.
  They are responsible for following and enforcing the software development standards of the application,
  as well as designing, implementing, and maintaining the software.
- +Developers+: A scientist or engineer that uses the {{app}} application alongside [!ac](MOOSE)
  and the {{app}} dependencies to build their own application. This user will typically have a
  background in modeling or simulation techniques (and perhaps numerical analysis) but may only have
  a limited skillset when it comes to code development using the C++ language. This is the primary
  focus group of the application. In many cases, these developers will be encouraged to contribute
  generally-appropriate code back to {{app}} application, or to one of its dependencies.
- +Analysts+: These are users that will run the code and perform analysis on the simulations they perform.
  These users may interact with developers of the system requesting new features and reporting bugs
  found and will typically make heavy use of the input file format.
!template-end!

!template! item key=reliability
The regression test suite will cover at least 50% of all lines of code within the {{app}} application
at all times. Known regressions will be recorded and tracked (see [#maintainability]) to an
independent and satisfactory resolution.
!template-end!

!template! item key=information-management
The {{app}} application and all dependencies in their entirety will be made available on an appropriate
repository hosting site accessible to {{app}} licensees, commensurate to their access level. Day-to-day
backups and security services will be provided by the hosting service.
!template-end!

!template! item key=policies-and-regulations
!include framework_srs.md start=policies-and-regulations-begin end=policies-and-regulations-finish
!template-end!

!template! item key=packaging
All export control restrictions must be adhered to when packaging and shipping media containing the
{{app}} application or its dependencies.
!template-end!
