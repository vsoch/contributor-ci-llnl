# Comments

These are notes that I'm taking during the CFAs. I am putting them here so
I can have them in one place.

## Spindle

At face value, Spindle seems like it's undervalued, and I say this because the problem seems very real and overlooked, although I haven't encountered it myself. The reason is that it might not be given enough attention is that the software presents itself very technically - "a tool for improving the performance of dynamic library and python loading in HPC enviornments." If I'm a user of such an environment, I don't directly see how this relates to me, or if it does, that using Spindle will improve doing my research. But being able to frame this problem in a way that is relatable to the general HPC user depends on if the general HPC user really faces this problem: "We encountered cases where it took over ten hours for a dynamically-linked MPI application running on 16K processes to reach main." So step 1 is identifying the audience for Spindle, describing (in a little more detail) the different use cases (not once in a long time or simulated, but actual day to day, and is it only MPI? What percentage of users use MPI?) and then deciding if there could be more interest in the community. I have quite a few suggestions to make the contributor friendliness (CF) of the project better if we decide it should be. For example, it would be very useful to provide a dummy cluster with containers, and then install spindle for a user to quickly interact. Spindle also uses LGPL which is OSI approved, but has "special cases" for [Google](https://opensource.google/docs/thirdparty/licenses/#LinkingRequirements) (which might suggest that they don't readily use or contribute as they would MIT or Apache, etc.). 

## Spot

For the series of spot repos (there is one for a front end, a back end, and a container) it would be much easier to navigate if there
was a single documentation interface that puts them all in context.
