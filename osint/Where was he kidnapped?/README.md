# Where was he kidnapped?
1000 points (790 at the end of the competition due to dynamic scoring)<br>
29 solves<br>
Codename: osint-challenge-2

## DESCRIPTION
The missing engineer stores his videos from his phone in his private cloud servers. We managed to get hold of these videos and we will need your help to trace back the route taken he took before going missing and identify where he was potentially kidnapped!

You only have limited number of flag submissions!

Download

Flag Format: govtech-csg{postal_code}

This challenge:
- Is eligible for Awesome Write-ups Award

## WRITEUP
Abstract: This writeup uses Google Street View heavily. Some background knowledge that are useful, but not essential when solving this challenge is in _italics_.

From `video-1.mp4`, our main observations is the overground MRT station in the background and bus 117 towards Punggol Int. The `finallllyyyyyyy...` suggests that the engineer is boarding bus 117.

We look at the [bus route](https://www.transitlink.com.sg/eservice/eguide/service_route.php?service=117) and we see that it passes by a few overground MRT stations (such as Sembawang, Canberra, Yishun and Khatib). _It might be useful to know that the MRT station in the video is Yishun._ Nonetheless, we can verify which MRT it is from Google Street View.

![gsw1](Images/gsw1.png)
![vid1](Images/vid1.png)

We verified that the MRT is indeed `Yishun`.

We then trace the bus route of bus 117 towards Punggol Int using Google Street View and the bus route hyperlinked above. From this we are trying to identify a similar architecture of the bus stop as in `video-2.mp4`.

We find this at bus stop `59501 Block 871`.

![gsw2](Images/gsw2.png)
![vid2](Images/vid2.png)


We then look through (again, using Google Street View) the vicinity of block 871 for a similar place to `video-3.mp4`. We are mainly looking at the garden in the background, the round table and bench, and the floor tiles.

We find this at nearby `block 870`.

![gsw3](Images/gsw3.png)
![vid3](Images/vid3.png)

## FLAG
`govtech-csg{760870}`

## ACKNOWLEDGEMENT
This writeup contains a lot of content from my friend @[codekrodile](https://github.com/codekrodile)
