
# Code for Datumless Topography: Dominance, Jut, Submission, and Rut
**Kai Xu, Yale University**

This repo provides the Google Earth Engine scripts (in JavaScript) for computing the datumless measures of topographic relief: *dominance*, *jut*, *submission*, and *rut*. These concepts are explained in my research paper [here](https://arxiv.org/abs/2208.01600). For much friendlier explanations, check out these five-minute explanations of [dominance](https://www.reddit.com/r/Mountaineering/comments/wfmrxw/a_new_way_to_measure_the_height_of_a_mountain/), [jut](https://www.reddit.com/r/Mountaineering/comments/wup76h/a_new_way_to_quantify_the_impressiveness_of_a/), and [dominant points](https://www.reddit.com/r/Mountaineering/comments/ww1wtw/on_top_of_the_world_a_new_mountain_metric/) (related to submission).

To compute the datumless measures, the first step is to create a Google Earth Engine account [here](https://earthengine.google.com/new_signup/). For the question "What would you like to accomplish with Earth Engine?", say that you are interested in computing the datumless measures of topographic relief, and include the link of the research paper (https://arxiv.org/abs/2208.01600) to increase your chances of approval. Your account should be approved within a few hours to a few days.

After your account is approved, you can access and run the code [here](https://code.earthengine.google.com/e2c0e4d0f21bdec0bd80ec9e392cd958). Instructions are provided in the code as comments.

# What Are the Datumless Measures?

On Earth, the relief of a mountain or other surface feature is measured with elevation, or height above sea level. However, for elevation to work on planets without a sea level, scientists have to define a "fake sea level" corresponding to zero elevation, also known as a *datum*. On such planets, the datum doesn't correspond to real surface features, hence the elevation of a point doesn't describe much by itself. Take Mt. Sharp on Mars, whose summit elevation of 728 meters reveals nothing by itself about the approximately 5 kilometer rise of the mountain above the floor of the Gale Crater that it rests within.

Instead, on other planets, the local relief of a point is assessed by comparing its elevation with that of its surroundings. For instance, the height of mountains on other planets is usually listed as base-to-peak height. However, what exactly counts as the base of a mountain? The current approach is to choose a point that "feels like" the base—a method that is undoubtedly arbitrary.

Introducing the datumless measures: a new way of quantifying relief that is based not on elevation, but purely on gravity and the planetary surface. The datumless measures provide a universally consistent way to quantify relief on any terrestrial planet or asteroid, including Earth. The four datumless measures are as follows:
 1. ***[Dominance](https://www.reddit.com/r/Mountaineering/comments/wfmrxw/a_new_way_to_measure_the_height_of_a_mountain/)*** measures how much a point rises above its surroundings. Among its applications, it provides a non-arbitrary base-to-peak measure of the height of any mountain on any planet. A point with a dominance of 0 is known as a *submissive point*, and is akin to a local low point. After releasing the paper, it was made known to me that the concept for dominance was actually first invented by the mountaineers Jerry Brekhus and Andy Martin in 2006 in a private online forum.
 2. ***[Jut](https://www.reddit.com/r/Mountaineering/comments/wup76h/a_new_way_to_quantify_the_impressiveness_of_a/)*** measures how sharply/impressively a point rises above its surroundings, accounting for both height and steepness. Jut is inspired by the *omnidirectional relief and steepness* (ORS) measure, also known as the *spire measure*, which was invented by Edward Earl and David Metzler to quantify the perceived impressiveness of a protruding landform such as a mountain or cliff. Jut achieves a similar goal using a much simpler formulation.
3. ***Submission*** measures how much a point dips below its surroundings. A point with a submission of 0 is known as a *[dominant point](https://www.reddit.com/r/Mountaineering/comments/ww1wtw/on_top_of_the_world_a_new_mountain_metric/)*, and is akin to a local high point.
4. ***Rut*** measures how sharply/impressively a point dips below its surroundings, accounting for both height and steepness.
