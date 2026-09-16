project-ideas 

---
## Questions to explore 

The tools in this tutorial (generate PSTHs, assess response classification, attention modulation index) can be reused to answer further questions across the units, brain areas, and sessions in this dataset. Here are a few questions that could start a few research projects: 

#### Sensory responses across the brain
- Which brain regions have the largest fraction of visually responsive neurons? Which are most auditory responsive?
- Do frontal cortical areas(e.g. `MOs`, `ACA`, `PL`) show sensory responses? If so, are they more often visual, auditory, or mixed?

#### Attention modulation
- Compare how neurons are modulated by attention across brain areas
- Where in the trial does the attention effect peak? Recompute AMI in sliding response windows (e.g. 0–100 ms, 100–250 ms, 250–500 ms) and compare across areas.
- Does the size of the AMI depend on behavioral performance? Split trials by hit vs miss (for targets) or false alarm vs correct reject (for non-targets) and see how that affects attention modulation. 
- Are there spatial gradients or clusters with respect to response profiles? The `units` table has coordinates for every unit - try plotting every unit's AMI as a scatterplot colored by AMI. 

#### Other kinds of context-dependent modulation

The AMI compares two contexts — attend-visual vs attend-auditory blocks. The same formula (or a slight variation) can quantify *any* pair of contexts you can define from the `trials` table. Propose a new "modulation index" of your own, then test it. Some starting points:

- Reward-history modulation. Compare the response on a given stimulus following a rewarded trial vs following an unrewarded trial. Does prior outcome bias sensory responses?
- Running / arousal modulation. Running speed and pupil size is also available - split trials into "high arousal" and "low arousal" and compute a modulation index. This is a useful control for the AMI we computed before. 