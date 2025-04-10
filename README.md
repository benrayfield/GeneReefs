# GeneReefs
the tools that built the GeneReefs art collection. Each GeneReef is a tiny html file that uses a canvas live and could be modded to fit into video games, multi touch screens, etc. Hundreds are on Cardano. Make your own locally.

The html in ReefEditor dir made them all. It takes json as input and output. It also outputs html and zip.

Video: https://www.youtube.com/watch?v=2cKOYv4vIBw

<img src=https://github.com/benrayfield/GeneReefs/blob/main/pics/GeneReefExperiment_686.html.png>

from the discord chatroom:
Bullet-point description of the reefs, but not about the charity and DAPP:
* 8888 reefs, most or all of them visually unique even without the metadata.
* Graphics uses a html canvas and 2d voxels, painting voxels from the curvy line, with variable time speed, forward or rewinding to the past, then forward again to try an alternate timeline, back and forth in many combos.
* The curvy line is a physics sim of potential-energy between all pairs of near points. Each of 300 species has different numbers in its potential-energy equation. Between each 2 points on the curve, its a 2d potential-energy curve between straight line distance vs distance along the curve, which allows complex nonlinear growth patterns to emerge, especially as this potential-energy curve changes over time.
* On-chain. Each reef is a html file that fits in a 16kB cardano transaction metadata, packed extra tight by 2 javascript minifiers, the last of which took 5 days of compute time. Shared thumbnail is on IPFS.
* 300 species, that each choose how it curves from one moment to the next. Each species has between 1 and 51 reefs. The first 5 reefs have only 1 per species. Second 5 species (10 reefs) have 2 per species, and so on.
* 202 patterns of color (seeds), that each chooses neuralnet weights. We picked those that look good.
* 56% are curvy-surface, that uses a curvy-line as a paintbrush. 44% looked better just as a curvy-line.
* 47 unique starting shapes, including circle, triangle, square, pentagon,  star, knots, spiral, random radius per angle, tiltedSineWaveCrossesItselfInCenter, fatBone, coil, and some hard to describe. The starting shape affects how it grows. 
* most reefs have a unique background color.
* Most variables that affect how a reef curves and moves, vary over time and look like a wave, a record groove, or a mechanical cam moving them, instead of a constant behavior.
* Variable speed of color change.
* Variable max speed per point on the curvy line paintbrush.
* Variable amount of random jumpyness.
* A few species use an acceleration field (which can push in directions or be hills and valleys) so reefs grow around these hills or are bent and moved.
* Variable pointyness of surfaces, anywhere between a sharp point to a smooth circle.
* Variable total length of the curve or range of allowed length.
* Of the 300 species/prototypes, some were manually designed, and some were evolved by harmony-search, and then repeat for the next generation, combining the best parts from multiple reefs into new reefs. All 300 look good and work as expected.
* Color is a smooth cellular automata of the nearest 11 points on the curvy line to its center point, red green and blue of all that, a 3 node-layer feedforward tanh neuralnet with sizes 34 (1const + red green and blue of plus/minus near 5 points on curvy line) -> 51 -> 3 (red green and blue). Sometimes this converges to 1 or a few colors, sometimes it goes back and forth, sometimes it slides colors around, and sometimes it has complex patterns. 
