#Thoughts on a watch app

Platform: Garmin (probably only platform with sufficient battery life and APIs)

Calculate mileage — trail miles, actual miles
Miles to next shelter, water
Compute trip stats in app
Scroll through upcoming trail features
Town mileage math

One use case where users just use the app to show distance to waypoints — doesn’t have to record any information or know where they’re going.

Another use case for thru-hikers who want stats and to be able to go back and see what they’ve done.

Probably have to load the section to the watch (unlikely it can hold whole trail).

Create a watch face with the upcoming shelter and water information? Which trail mile? (Can watch faces use GPS? Should be a widget?)

Show GPS status — currently locked, searching, or not searching. Use colored dot?

Show time last GPS updated (if out of date).

Show distance from trail (if sufficiently far from trail).

Make a version for the non-watch Garmin GPS units, which are common on the trail.

Have a setup-less mode where it detects the trail and direction without any configuration. Have a stable direction so that it doesn’t switch back and forth.

Have a “going the wrong way” notification if you hike too far in the opposite direction (need to be careful to avoid false positives).

Have a "trail maker" mode where you can add points of interest directly on the watch.

Most likely will have to sync with phone app to get nearby trail. Could do a sync without any explicit selection if it uses the local trail(s) and infers direction.

Have an algorithm and process for downsampling GPS tracks while still keeping accurate mileage. Use high res GPS track to calculate mileage points, then figure out how to throw away intermediate points while minimizing average and maximum errors. Can find optimal solution to maximize space savings given fixed maximum error tolerance?

How much storage can a Garmin watch app use?

Initial imagined architecture:

Launch phone app. Nearest trail is automatically selected, can be overwritten in the phone UI. (Be smart about remembering old trails.)

Launch watch app (can one of the apps automatically launch the other?). Sync with phone app, or show warning if it can't connect.

Watch app shows warning if it get get a current or cached location. If it can, it defaults to the screen showing the upcoming and / or previous POIs.

Other screens include estimates for trail and total mileage on the day, based on first trail location for the day or last the previous night (or manually selected location in app).

Maybe details on the specific upcoming POIs?

Elevation snippet… might have to be calculated / rendered on phone.
