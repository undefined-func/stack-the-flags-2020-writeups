# What is he working on? Some high value project?
1000 points (790 points at the end of the competition due to dynamic scoring)<br>
29 solves<br>
Codename: osint-challenge-1

## DESCRIPTION
The lead Smart Nation engineer is missing! He has not responded to our calls for 3 days and is suspected to be kidnapped! Can you find out some of the projects he has been working on? Perhaps this will give us some insights on why he was kidnapped…maybe some high-value projects! This is one of the latest work, maybe it serves as a good starting point to start hunting.

Flag is the repository name!

[Developer's Portal - STACK the Flags] (https://www.developer.tech.gov.sg/communities/events/stack-the-flags-2020)

Note: Just this page only! Only stack-the-flags-2020 page have the clues to help you proceed. Please do not perform any scanning activities on www.developer.tech.gov.sg. This is not part of the challenge scope!

This challenge:
- Unlocks other challenge(s)
- Is eligible for Awesome Write-ups Award

## WRITEUP
We look at the Developer's Portal and nothing seems out of the ordinary. We then view the page source and see that there is a comment in the HTML source (line 858).

```
<!-- Will fork to our gitlab - @joshhky -->
```

This gives us a clue to pivot to gitlab and search for the user named [joshhky](https://gitlab.com/joshhky).

We then trawl through his gitlab activity, especially the ones on the [KoroVax group](https://gitlab.com/korovax), since that is the organization targeted.

We then find in the README.md of [Korovax/korovax-employee-wiki](https://gitlab.com/korovax/korovax-employee-wiki) an interesting note.

```
README
Extracted wiki template from GitLab pages examples.
This POC will be complementary to the whole suite of offerings which KoroVax will use internally.
Todo:
- The employee wiki will list what each employee is responsible for, eg, Josh will be in charge of the krs-admin-portal
- Please note that not all repository should be made public, relevant ones with business data should be made private
POC Site: https://korovax.gitlab.io/korovax-employee-wiki
```

We can then infer that `krs-admin-portal` is our high value project repository name.

## FLAG
`govtech-csg{krs-admin-portal}`
