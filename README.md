# Testing o3 mini with coding tasks

In this repository you'll find some test I ran on o3 mini, promped via Claude - Composer. o3 mini was able too to handle prompts and file and code generation.

Prompts are organised in steps as given. Results are noted under results

Debugging was done with o3mini when possible. Due to impossibility of sharing images with o3 mini, I used claude-3.5 sonnet for some steps that required image recognition

## Prompts given


1. write a js program that shows a ball bouncing inside a spinning hexagon. The ball should be affected by gravity and friction, and it must bounce off the rotating walls realistically

2. @index.html add another 20 balls

3. now make it so that the balls should also collide against each other and affect each other

*NOTE* here the balls get stuck within themselves and pull each other out of the boundaries

4. @index.html looks good, now add some limits so balls cannot scape the boundaries of the polygon, as during the first frames all balls get cluttered and push each other drastically out of the boundaries and collapse to the infinite bottom , only a few manage to stay within the boundaries and behave normally

*NOTE* this doesn't fully correct the issue, although balls are confined to the boundaries of the polygon

5. seems like the balls get stuck with each other just revolting energetically in a cluster, not being able to scape the clump , fix that so balls bounce naturally when colliding with each other and the boundaries of the polygon, also without scaping the polygon @index.html 


## Results

1. Success on the first attempt. Polygon drawn, rotation smooth, one bouncing ball added with natural physics.

2. Success. First Attempt. Several balls added.

3. Fail. Several balls seem to build a revolting clump that brings itself outside of the boundaries of polygon

4.  Fails to solve the issue so I changed model to be able to send it an image (o3 mini to claude)

5. Success. First Attempt. Smooth simulation.