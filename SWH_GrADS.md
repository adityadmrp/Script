#Script - Significant Wave Height with GrADS
sdfopen C:\Users\ASUS\Documents\metmar\gelombang.nc
#Use your directory 
set lat -10 -2
set lon 105 115
set mpdset hires
set timelab off
set grads off
set grid off
swh=ave(vhm0,t=1,t=5)
swh1=ave(vhm0,t=5,t=9)
set gxout shaded
set ccols 4 3 7 8 2 9 6
set clevs 0.5 1.25 2.5 4 6 9   
set csmooth on
#d swh
d swh1
cbar
draw title Tinggi Gelombang Signifikan
printim C:\Users\ASUS\Documents\metmar\Gel2.png white
#Use your directory
