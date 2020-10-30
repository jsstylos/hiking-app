#Thoughts on OpenStreetMaps

Right now the limiting factor for creating a widely used hiking app (especially if trying to make it free) is serving the map tiles. Even when the source is free (USGS), just the bandwidth is expensive, and annoyingly slow for users to download.

A related problem, crowdsourced changes to maps can’t easily feedback into the maps used in the applications.

The solution is to use a vectorized mapping platform, based on OpenStreetMaps.

There are three main challenges.

First, technical. MapBox has a vector based solution for OpenStreetMaps, and it’s open source, but their full solution is not, I think. Getting a full solution working for iPhone and Android (and ideally web) will take some work, possibly serious work.

Second, relevant information on the maps. USGS maps are popular for hiking because they have information that other map sources often don’t. This can be remedied by making contributions to OpenStreetMaps, but it will take a large effort to improve OpenStreetMaps around the trails hikers care about. Luckily, non-hikers can do a lot of this work, but it will require coordinating them, and incentivizing them by already having an app where they can see and take advantage of the results of their labors. Part of this is data collection about the trail, part is areas, map features, near the trail.

Third, artistic. Right now most OpenStreetMap renderings are ugly. Creating a visualization that is both pleasing and functional will take a lot of work, ideally by a graphic designer.
