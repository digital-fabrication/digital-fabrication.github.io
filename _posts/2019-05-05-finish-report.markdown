---
layout: post
title:  "It's done, was fun"
date:   2019-05-05 21:10:00 +0200
categories: blinds
---
Report of projects last week

# "Wait, we're missing the routes for the led!"

We are planning to mill two shield pcb's for the Huzzah controller, and we started with the simpler one that will house connections for the buttons and led (the other one will have the dc-dc converter and singaling for the servo, but will be fashioned later on our spare time and is outside of this course). The pcb work started with a logical layout in Eagle based on our TinkerCad model. When we had the initial logical model we ran the Eagles autoroute function to get the physical layout and we were beaming with delight as it managed to wrestle out a fully connected layout. We were almost taking this straight to the mill, but fortunately had the sense to step through each route only to find that we had omitted a couple of connections. We added them dutifully but then ran in to problems with the autoroute function. The added routes made getting a full connectivity with the autoroute algorithm seemingly impossible. With some fiddling of the components we managed to free just enough space for the algorithm to barely squeeze out a single fully connetected solution, and though it was not the prettiest, we took it to the bank.

The milling process had it's kinks also. In the first draft we did not drill the lanes deep enough, and in the cut out phase the board slipped free off the base and the drill head took it for a walk. The second attempt was a fail also, but the third one gave us a beautifyll board!

![sunday-editions]
*Fig. 1: The two failed pcbs*

![success1]
*Fig. 1: The success pcb front/up*

![success1]
*Fig. 1: The success pcb back/down with pins attached*

[sunday-editions]: /assets/pcb/sunday_editions.jpg
[success1]: /assets/pcb/success1.jpg
[success2]: /assets/pcb/success2.jpg
[success3]: /assets/pcb/success_soldered.jpg
[success4]: /assets/pcb/success_attached.jpg
[success5]: /assets/pcb/success_formfactor_comparison.jpg
