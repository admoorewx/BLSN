BLOWING SNOW SITE README

Blowing Snow V 1.0

Author: Andrew Moore - NWS Grand Forks
Contact: andrew.moore@noaa.gov

PURPOSE:

The purpose of this web-based tool is to help relate current conditions to the probability of 
visibility reduction due to blowing snow. Additionally, this tool will help give forecasters an 
idea about how sensitive visibilities are to the ongoing conditions (i.e. what is the chance that
a 25 knot wind will cause 1/2 mile visibilities compared to a 30 knot wind?). 

Although there are many caveats to using this tool, it should help forecasters maintain
situtational awareness and help key in to the possibility of visibility reductions due to blowing
snow. 


BLOWING SNOW MODEL:

The blowing snow model used in this tool is the Baggaley Blowing Snow model - the same model used
in GFE as of November 2018. In theory, there is a probability (given in %) that a given wind speed,
temperature, falling snow rate, and/or snow pack age will cause visibility reductions down to a given 
threshold. While impact studies have been performed for the impacts down to 1/2 mile, this tool gives
probabilities for 1/2, 1, and 3 miles. 

One additional feature particular to this tool is that the Snowfall Rate is capped at 1"/hour. This is done 
because it is assumed that after snowfall rates exceed 0.55"/hour that visibility will already be reduced to
~1/2 mile just due to the falling snow (even without any wind!). (Why not cap it at 1"/hour then? We figured 
1"/hour is an nicer cut off rate to work with than 0.55"/hour - the important number here is 0.55"/hour though.)

How does this tool compare to the blowing snow percentages given by the equivalent GFE tool? They're very close, 
though not always a 100% match. Usually this tool will be within 1-2% of the GFE tool. On rare occasions you may 
notice that this tool is 3% off from the GFE tool. 


For full documentation/details on the Baggaley Blowing Snow Model, please consult:

Baggaley, D., Hanesiak, J., 2005, "An Empirical Blowing Snow Forecast Technique for the Canadian Arctic
and the Prairie Provinces", Bull. Amer. Met. Soc. Feb. 2005, vol 20, 51-62


INSTALLATION: 

Installation of the Blowing Snow Site should be relatively simple - just make sure that the 
BlowingSnowSite.html and BlowingSnow.js scripts are in the same directories on your web server!

The encoding for both scripts is Unicode, but this may need to be changed to ANSI or UTF-8 depending
on your web server configuration. 


USEAGE:

This site is designed to be relatively straightforward to use: 

1) Enter in the desired temperature and wind speed into their respective entry boxes. 

2) Select the desired snowfall rate in units of inches/hour. (Not sure how to best determine snowfall rate? We aren't either... 
   Our best advice is to collect frequent obs or make a reasonable guess based on GFE snow grids or radar observations.) 

3) Simply click on "RUN BLSN MODEL" and the two tables below will populate. 


SITE LAYOUT:

Just to the right of the "Input Data" section you will see three visibility buttons (1/2 Mile, 1 Mile, and 3 Miles). 
You can click between each of these to view the probability table for each visibility threshold. 

Now for the tables themselves:

Each of these tables are describing the probability of visibility being reduced to X Mile(s) given certain wind speed, 
temperature, snowfall rate, and snow age conditions. 

The table on the left shows the sensitivity of the visibility to changes in wind speed. The temperature is kept constant, 
as denoted by the "Constant Temperature = #F" in blue in the upper left portion of the table (notice that this is the user's 
input temperature). The wind speeds in the table range from 10 knots below the user's input wind speed to 10 knots above the
user's input wind speed. The input wind speed can be found in bold text in the middle row of the table. The "Falling Snow" 
column incorporates the snowfall rate input by the user and does not take into account the presence (or lack thereof) of a snow
pack. To the right of this is the "No Falling Snow (Snow Age)" section. This shows the probability of visibility reductions due 
simply to wind speed, temperature, and the age of a snow pack.

The table on the right is analogous to the left table except that it is showing the sensitivity of visibility reduction to 
different temperatures. The user's input wind speed is held constant as noted in the "Constant Wind Speed = # kts" in blue in 
the upper left portion of the table. The temperatures range from 10 degrees F below the user's input temperature to 10 
degrees F above the user's input temperature. The input temperature can be found in bold text in the middle row of the table. 
The "Falling Snow" and "No Falling Snow (Snow Age)" columns serve the same purpose as described above. 

The cells/probabilities are color-coded based on the level of potential impacts. For the 1/2 mile visibility threshold, these 
impacts are colored based off of impact studies. The 1 and 3 Mile tables are color-coded based on thresholds set within GFE. 
For 1 mile visibility, any percentage greater than 30% is comparable to the "Areas of Blowing Snow" wording used in GFE. For 
3 mile visibility, any percentage greater than 10% is comparable to the "Patchy Blowing Snow" wording used in GFE. 


NOTES AND CAVEATS

A few things to note:

1) This tool does not take into account any melting/refreezing on the snow pack (i.e. crunchy ice layers on the top
   that you can often fall through). 

2) Assumes blowable snow is on the ground. 

3) Assumes blowing snow is not possible if the temperature is > 37 F. 

4) Does not take into account depth of the snow pack. 

5) Further research is still needed to connect the 1 & 3 mile probabilities with real impacts. 

6) IMPORTANT: Typically, when the sustained winds are near 25-30 knots, an increase in wind speed of 1-3 knots is enough to drop visibilities from 1/2 to 1/4 mile 
   during most blowing snow/heavy snowfall scenarios! This may have important implications for forecasting blizzard
   conditions.


If there are any questions, comments, suggestsions, or you want to yell at someone for poor commenting, please 
email the contact listed at the top of this document. 

Good luck!
 




