## BoM: A Program to do Bill of Materials analysis
For instance if a hypothetical fan assembly requires four screws, a fan
housing, a motor and a fan impeller, and a motor requires a stator, eight
screws and a rotor, and a rotor requires four screws an armature and two coils,
and a stator requires two armatures, eight screws and four coils then the
completely expanded Bill of Materials will show the following:

- 24 screws
- 1 fan housing
- 1 fan impeller
- 3 armatures
- 6 coils

BoM is envisaged primarily for use in planning complex modded Minecraft builds.
It should be useful for evaluating the cost of different technology paths. As
such it should support multiple different recipes and ingredients that are
needed but not consumed, for example a macerator. Recipes should be filterable
by ingredients on hand, so for example you can look at recipes that don't
include the use of a machine you don't have yet.

Future plans include support for directly extracting recipes from your modded
Minecraft install, including displaying icons, etc., from a properly licensed
Minecraft install. The author takes no responsibility in regards to your rights
to use these assets.

Although the primary use for BoM is envisaged to be for planning complex builds
in modded Minecraft, although the author hopes it will be more generally useful
in the planning of other creative endeavours.

BoM is currently in the planning stage, and no working code has yet been
written.

BoM was created because at the time of its creation the only Bill of Materials
software available were extremely expensive engineering programs which were not
freely customisable; or huge and frankly baffling ERP programs, most of which
were similarly costed in the five figure range and similarly not freely modifiable.

Ad hoc solutions were tried with some success, such as spreadsheets that used
two sheets and matrix multiplications and sums. But such solutions were tedious
to set up, not automated and like many complex spreadsheets quite brittle.

BoM is licensed under the terms of the GPL 2, which encourages you to add and
modify while guaranteeing any future versions come with the same freedoms in 
the future. This can only be achieved by requiring that any modifications that
you make must be distributed with the same freedom to share and modify as the
original.

If you have made some cool enhancement or bug fix, then by all means contribute
back to the main branch by submitting a pull request!