#Experiment no:- 1
#Experiment name:- Use different colour scales on the Rainfall prediction dataset
import matplotlib.pyplot as plt

years=list(range(1901,2017))
jan_mm=[51.8,4.6,5.3,6.3,16,14.4,1.3,14.7,7,2.4,9.4,5.5,0,0.2,8.2,0.6,2.7,0.6,40.2,0,26.8,12.2,1.3,2.5,7.7,16.3,24.4,41.2,51.6,11.6,1.3,0,28.3,30.1,21,7.7,0,12.4,5,0.9,16.2,34.4,34.7,27.3,50.7,0,5.6,11.1,16.5,9.8,7.3,1.1,29.7,12.5,20,19.3,75.2,16,81.2,1.4,11.7,13,3.4,1.4,0.4,21.2,0.2,29.1,5.2,22.1,17.3,12.9,22.9,3.9,9.1,2.3,5.3,13.4,23.4,4.7,31.3,4.4,13,128.6,8.8,1.1,0.7,1.2,8.9,0.3,14.5,2.6,9.4,28.3,6.8,26,10.5,8.4,0.1,0.5,1,13.4,22.7,13.9,0.1,0.2,25.6,0.3,0.1,4.2,18.1,5.1,17,12.8,9.3,0.7]
feb_mm=[19.6,0.7,4.7,1.7,30.1,56.9,55.2,38.6,6.3,4.8,0.1,8.5,38,22.7,57.1,16.5,19.7,0.1,7.7,19.2,0.6,4.6,35.1,12.7,1.8,0.6,36.4,21.5,1.1,7.6,32.4,8.2,13.1,13.7,19.6,6.9,66.3,17,42.3,43.8,2.8,43.5,16.9,32.6,24,21.3,5.6,7.5,42.8,11.8,1.5,10.3,4.2,8.4,6.7,4.7,2.8,2.7,1.5,0.1,35.8,7.8,1.7,3.3,1.2,6.9,0.1,1.7,9.3,13.4,14.6,38,10.2,0.7,4.1,12.4,2.9,27.8,19.4,2.4,5.7,6.1,1.7,33.9,0.5,13.9,3.7,15.3,8.7,30.26,3,3.1,4,29.1,11.6,21.7,1.1,11.2,0.2,12.1,0.5,11.3,39.7,2.1,14.3,0,34.2,4.4,0.4,1.1,7.7,2.7,22.6,33.5,1.8,0.6]
mar_mm=[2,3.5,32.6,8.6,39.4,6.1,0,6.6,2.2,23.9,18.1,8,22.5,0.3,7.9,1.8,3.8,31,6.5,0,1.5,1.8,7.7,29.7,31.9,0.1,11.4,13.6,11.4,0.5,0.7,3,0.6,4.6,0.8,0,11.3,65.5,0.7,14.7,0.2,42,0.2,42,1.4,5,10.2,3.6,5.7,22.1,5.8,20.1,8.7,0.8,2.3,9.6,11.6,4.7,9.4,42.7,1.4,9.5,9.4,2.4,15.7,0.1,38.6,7,9.7,3.2,5.1,2.7,3.8,21.9,12,0.9,1.3,16.8,2.3,9.5,14.3,28.2,8,1.3,0.5,5.4,27.3,6.9,13.8,7.9,0.1,24.5,1,2,0.2,2.9,23.6,0.4,3.6,3,2.2,10.2,2.2,12.1,1.9,25.4,3.2,1.1,0.2,9.2,7.3,0.6,8.4,27.2,5.6,22.8]
apr_mm=[17.3,4.7,5.3,21.4,0.9,27,2.2,72.8,5.7,13.1,25.4,1.4,29,6.4,25.3,5.8,29.5,11.6,2.6,21.2,9.6,13.5,8.8,52.9,12.8,3.1,18.3,16.2,6.6,1.6,14.8,62.1,9.1,0.7,7.7,10.7,2.9,1.7,5,4.6,18.2,40.7,34.1,32.4,52.3,7.5,11.3,35.5,2.2,8.2,24.6,16.7,0.6,11.9,5.3,0.5,26.4,18.6,5.2,2,20.8,17.5,21.9,7.1,0.9,30.6,3,20.7,17.9,91.4,3.2,4.4,9.9,11,8.9,17,24.5,21.3,7.9,47.9,14.7,45,11.2,8,16,37.7,46.9,0.2,14,8.9,2.6,24.5,7,0.1,3,29.3,26.6,3.8,37.2,12.6,25,21.9,32,7.7,19.2,20.3,10.4,2.9,6.5,23.9,20.4,32.3,0.7,38.7,3.9,21.8]
may_mm=[65.6,66.3,28.2,118.7,77.5,44.7,32.9,36.7,25.8,51.5,41.7,62.7,106.1,77,72.5,25.1,103.3,105.4,42.3,28.8,26.3,22,38.1,14.8,36.8,47,52.9,54.3,28.6,27.5,26.6,90.3,22,84.3,80,115.5,41.5,31.9,67.1,28.1,37,21.9,57.8,88.6,57.7,46.3,93.1,43.3,22.8,57,37.4,40.9,28.2,75.4,1.3,16.1,35.7,49.9,33.9,33.9,38.8,78.9,59.3,7.7,39.5,23.6,17.3,64.4,39.2,81.5,3.4,65,39.1,34.4,80.1,83.7,51.8,6.2,80.9,86.3,31,81.1,65.5,69.2,94.3,40.1,46.2,100.3,83.3,31.2,61.1,51.1,32.7,6.7,18.2,42.2,38.2,83.6,96.2,98.4,74.8,41.4,72.7,28.6,73.2,94.4,48.9,98.5,44.4,74.5,18.8,89.5,103.9,39.5,84,79.7]
jun_mm=[66.3,118.2,192.9,191.6,50.5,191.3,232.2,94,446,297.5,312.3,146.8,379.9,84.4,149.1,270.3,227.8,251.6,195,108.9,132.4,345.8,171.7,170.6,130.4,48.1,115.9,208,190.2,144.6,75.9,152.1,197,165.5,127.9,188.9,113.6,382.4,230.4,114.6,177.7,174.7,169.8,223.9,120.5,168.7,89.4,114.6,202.2,346.5,144.5,272.5,224.7,166.6,172.5,319.4,115.6,120.7,132.3,117.6,239.7,156.4,154,134.7,98.8,114.5,80.7,261.8,193.1,194.6,278,56.7,200.9,129.4,147.1,102.5,190.4,90.6,160.2,107.9,222.4,101.2,353.4,163.2,168.4,143.6,174.5,152.9,156.6,176.2,83.9,154.8,130.9,162.9,220.1,211,96.6,265.1,267.2,224.4,116.6,230.9,246.8,82.5,200,170.4,291.2,67.7,80.9,211,96.2,183.3,115.2,122.1,128.7,84.6]
jul_mm=[492.1,245.9,361,115,394.4,409.1,366.2,282.4,202.3,256.2,365.1,362.4,258.8,269.1,321.3,445.6,328.7,240.3,417.8,361.6,303.8,427.3,253.9,514,322.9,451.5,377.2,328.8,298.2,441.3,164.3,377.3,423.6,193.8,462.2,217.9,362.1,315,317.6,248.8,253.5,296,253.3,226.9,354.7,394.4,409,341.7,257,307.8,212.5,431.8,366.1,505.7,200.6,334.5,222.8,245.8,357.4,211.6,244.3,375.4,453.6,302.2,155.5,278.2,329.6,348.4,284.2,307,163.4,185.1,451.6,403.1,221,375.5,313.6,435.5,389.9,580.1,227.2,355.8,476.4,481.5,395.7,452,364.5,446,485.5,179.7,284.8,209.1,217.7,227.5,238.5,463.9,465.1,380.8,264.3,224.7,386.1,356.8,418.4,300,290.7,549.4,397.2,213.6,191.2,241.1,354,182,265.4,231.5,356.4,379.9]
aug_mm=[319.4, 225.5, 342.6, 351.3, 495.3, 430.1, 242.2, 167.3, 352.4, 328.8, 425.5, 302.9, 363, 460.4,415, 325.2, 249.3, 519.2, 228.5, 422, 363.5, 243.2, 295.7, 331.5, 276, 242.7, 272.9, 326.3, 247.8, 218.8, 249.3, 377.8, 251.3, 481.7, 261.5, 441.8, 385.1, 277.1, 314.9, 466, 330.4, 322.1, 322.8, 265.6, 267.8, 244.6, 329.8, 386.5, 313.3, 204.5, 291.9, 263.3, 308.6, 268.7, 286.3, 295.8, 451.1, 264.2, 285.5, 317.5, 395.4, 273.5, 157.7, 328.3, 308.3, 282.1, 293.1, 379.4, 235.6, 367.9, 154.9, 258.9, 317.5, 155.2, 292.8, 266, 252.6, 166.1, 375.3, 311.3, 164.5, 195.8, 216.9, 238, 263.5,539.8, 459.4, 171.9, 204.4, 324.2, 219.2, 357.3, 257.6, 335.7, 350.9, 287.6, 377.4, 347.5, 201.4, 225.9, 247.7, 310.6, 175.9, 309.1, 160.4, 340.6, 278.1, 298.9, 158.4, 278.7, 240.4, 213.6, 307.6, 287, 150.8, 342.8]
sept_mm=[155.1, 358.7, 173.9, 84.4, 353.9, 118.7, 149.9, 175.4, 258.5, 279.1, 104.7, 270.3, 98.4, 185.1, 265.2, 272.1, 254.4, 244.8, 337.6, 295.8, 241.3, 148.9, 320.3, 269.4, 211.6, 231.4, 83.3, 124.7, 290.9, 248.2, 191.2, 167.8, 231.2, 370.3, 449.2, 179.3, 201.4, 262, 171.6, 190.2, 347.2, 215.4, 221.3, 305.5, 271.8, 215.3, 248.9, 217.9, 113.4, 114.3, 297.7, 342.2, 129.5, 192.2, 359.8, 115.2, 224.2, 157.1, 348.1, 157.5, 216.3, 255.7, 219, 215, 83.1, 253.8, 79.2, 219.1, 229.5, 129.2, 209.7, 271.4, 229.2, 245.3, 372.6, 121, 248.6, 113, 190.5, 168.8, 170.5, 220.6, 219, 289, 221.1, 379.7, 153.2, 330.9, 201.2, 270.5, 85.9, 320, 226.5, 279.1, 162.5, 185.8, 188, 199.6, 314.8, 274.8, 192.8, 183.9, 115.3, 105.1, 285.2, 309, 117.1, 127.6, 105.7, 234.1, 233.8, 143.3, 160.3, 101.7, 357.9, 129.6]
oct_mm=[8.3, 28.5, 147, 98.1, 11.6, 32.9, 25.4, 43.1, 73.8, 61, 122.8, 14, 10.1, 75.3, 130.1, 116.5, 8.6, 58.6, 5.6, 37, 15.7, 74.4, 53.1, 17.6, 17.6, 21.5, 164.3, 231.4, 30.4, 76.1, 32.4, 77.6, 55.2, 2.6, 88.8, 194.6, 27.1, 56.9, 4.9, 47.8, 7, 37, 48.5, 154.8, 148.7, 61.5, 81, 103.4, 3, 28.7, 15.4, 18.4, 15.1, 35.7, 168.8, 11.6, 81.5, 233.8, 37.9, 236, 72.5, 138.7, 66.3, 22.2, 18.3, 10.3, 113.3, 15.3, 34.5, 138.6, 48.4, 158.2, 28, 51.7, 22.4, 147.1, 142.8, 88.5, 29.5, 1, 42.1, 69.9, 15.4, 188, 124.2, 52.8, 33.7, 28.2, 49.7, 7.2, 52.4, 34.3, 32.9, 11.4, 66.2, 27.8, 83, 114.1, 9.6, 181.3, 33.8, 142, 56.4, 34.3, 17.6, 39.6, 21.4, 72.6, 33.6, 10, 34.3, 197.1, 47.8, 10.4, 60.8, 50.1]
nov_mm=[7.3, 1.1, 0.1, 10.6, 0, 0.4, 0, 0, 0, 21.7, 17.8, 72.6, 0, 36.7, 0.4, 0, 0.1, 0, 0, 0, 0.7, 0.7, 61.7, 11, 1.8, 38.6, 0.9, 0, 24, 11.2, 78.7, 0.3, 9.8, 0.1, 0.4, 0.3, 0.8, 0, 0, 1.1, 0, 0, 0.2, 0, 14.9, 0.1, 36.2, 1.1, 0.1, 4.7, 3.4, 0.9, 0.2, 0.3, 36, 0, 0.7, 0, 2, 0.8, 0, 17.8, 2.7, 1.8, 17.1, 0.1, 0, 23.6, 0.4, 1.9, 24.6, 8.3, 0.3, 0, 0.7, 8.1, 4.8, 25.2, 0.2, 6.1, 21.5, 0, 1.5, 1.2, 1.3, 2.7, 1.5, 1, 0, 0, 1.4, 19.3, 4.4, 44.4, 0, 11, 14.5, 6.9, 0, 0.5, 1.4, 0.2, 3.1, 0, 2.9, 9.1, 0.1, 5.1, 5, 2, 6.4, 0.4, 0, 0, 0, 0]
dec_mm=[0.1, 0, 0, 3.8, 0.6, 0, 2.1, 0.3, 5.6, 0, 0, 0, 32.8, 0.6, 0, 0.2, 0, 0.7, 0, 0, 6.5, 0.4, 0.2, 0, 8.7, 0.2, 7.6, 44.4, 10.4, 0.7, 8.9, 0.3, 2.8, 0.1, 10.3, 1.1, 0, 0, 17.5, 0, 0.9, 0, 0.8, 3.2, 0, 0.3, 0, 0, 2.1, 0.1, 0.4, 0.8, 1.3, 0.1, 8.1, 2.7, 0.6, 0.1, 0, 10.1, 3.2, 0.2, 0, 2.4, 1.6, 1.5, 4.9, 0.3, 0, 0, 0, 0, 3.7, 0, 0.5, 17.3, 3.7, 10.3, 1, 3.9, 1, 14.1, 3, 7.1, 22.1, 2.3, 13.8, 14, 0.2, 19.2, 0.4, 0.1, 1.2, 23.8, 0, 30.6, 0, 0.6, 0.1, 0, 0.7, 3, 0, 0.2, 1.6, 7.5, 0, 0.8, 2.1, 0.9, 0, 0, 1.2, 0, 0, 0]
plt.title("Rainfall prediction in bihar between 1901 and 2017")
plt.xlabel("year")
plt.ylabel("Rainfall(in MMs)")
plt.xticks(rotation=90)
plt.plot(years,jan_mm,color="b")
plt.plot(years,feb_mm,color="r")
plt.plot(years,mar_mm,color="g")
plt.plot(years,apr_mm,color="m")
plt.plot(years,may_mm,color="y",ls=":")
plt.plot(years,jun_mm,color="g",ls="-.")
plt.plot(years,jul_mm,color="y",ls=":")
plt.plot(years,aug_mm,color="k")
plt.plot(years,sept_mm,color="c")
plt.plot(years,oct_mm,color="r",ls="--")
plt.plot(years,nov_mm,color="c")
plt.plot(years,dec_mm,color="m",ls="--")
plt.show()


#Experiment no:- 2 
#Experiment name:- Create different bars plots for variables in any dataset 
#AC ELECTIONS
import matplotlib.pyplot as plt
import numpy as np
barwidth=0.1
fig,ax=plt.subplots(figsize=(20, 9))

years=["1977","1980","1985","1990","1993","1998","2003","2008","2013","2018"]
BJP =[0,18.6,21.2,25.3,38.6,33.2,39.2,34.3,46.0,39.3]
INC=[31.5,43.0,46.6,33.6,38.3,45.0,35.6,36.8,33.7,39.8]
IND=[ 16.0,13.1,11.9,14.9,12.9,14.4,11.4,15.0,8.4,9.6]
BSP=[ 0,0,0,0,0,2.2,4.0,7.6,3.4,4.0]  
CPM=[0.7,0,0,1.0,1.0,0,0,1.6,0,0]
INLD=[0,0,0,0,0,0,2.6,0,0,0]    
JD =[0,0,0,21.6,6.9,2.0,0,0,0,0]
LKD=[ 0,0,11.9,0,0,0,0,0,0,0]
JNP=[ 50.4,7.3,5.9,0,0,0,0,0,0,0]  

br1=np.arange(len(BJP))
br2=[x+barwidth for x in br1]
br3=[x+barwidth for x in br2]
br4=[x+barwidth for x in br3]
br5=[x+barwidth for x in br4]
br6=[x+barwidth for x in br5]
br7=[x+barwidth for x in br6]
br8=[x+barwidth for x in br7]
br9=[x+barwidth for x in br8]

plt.bar(br1,BJP,color="r",width=barwidth,edgecolor="grey",label="BJP")
plt.bar(br2,INC,color="#FF00FF",width=barwidth,edgecolor="grey",label="INC")
plt.bar(br3,IND,color="#0000CC",width=barwidth,edgecolor="grey",label="IND")
plt.bar(br4,BSP,color="#9ACD32",width=barwidth,edgecolor="grey",label="BSP")
plt.bar(br5,CPM,color="#660000",width=barwidth,edgecolor="grey",label="CPM")
plt.bar(br6,INLD,color="g",width=barwidth,edgecolor="grey",label="INLD")
plt.bar(br7,JD,color="#FFFF33",width=barwidth,edgecolor="grey",label="JD")
plt.bar(br8,LKD,color="#33FFFF",width=barwidth,edgecolor="grey",label="LKD")
plt.bar(br9,JNP,color="#00FF00",width=barwidth,edgecolor="grey",label="JNP")

plt.xlabel("YEARS ---------->",fontweight="bold",fontsize=15)
plt.ylabel("VOTES(in %) ---------->",fontweight="bold",fontsize=15)
plt.xticks([r+barwidth for r in range(len(BJP))],years)
plt.legend()
plt.show()

#PC ELECTIONS
import matplotlib.pyplot as plt
import numpy as np
barwidth=0.1
fig,ax=plt.subplots(figsize=(20, 9))

years=["1984","1989","1991","1996","1998","1999","2004","2009","2014","2019"]
BJP=[7.4,11.4,20.1,20.3,25.6,23.8,22.2,18.8,31.3,37.7]
INC=[48.1,39.5,36.4,28.8,25.8,28.3,26.5,28.6,19.5,19.7]
BSP=[0,2.1,1.8,4.0,4.7,4.2,5.3,6.2,4.2,3.7]
CPI=[5.7,6.5,6.1,6.1,5.2,5.4,5.7,5.3,3.3,1.8]
API=[0,0,0,0,0,0,0,0,0,0.1]
IND1=[9.4,5.3,4.2,6.3,2.4,2.7,4.2,5.2,3.1,2.7]
IND2=[9.4,5.3,4.2,6.3,2.4,2.7,4.2,5.2,3.1,2.7]
JSVP=[0,0,0,0,0,0,0,0,0,0]
HND=[0,0,0,0,0,0,0,0,0,0]

br1=np.arange(len(BJP))
br2=[x+barwidth for x in br1]
br3=[x+barwidth for x in br2]
br4=[x+barwidth for x in br3]
br5=[x+barwidth for x in br4]
br6=[x+barwidth for x in br5]
br7=[x+barwidth for x in br6]
br8=[x+barwidth for x in br7]
br9=[x+barwidth for x in br8]

plt.bar(br1,BJP,color="r",width=barwidth,edgecolor="grey",label="BJP")
plt.bar(br2,INC,color="#FF00FF",width=barwidth,edgecolor="grey",label="INC")
plt.bar(br3,BSP,color="#0000CC",width=barwidth,edgecolor="grey",label="BSP")
plt.bar(br4,CPI,color="#9ACD32",width=barwidth,edgecolor="grey",label="CPI")
plt.bar(br5,API,color="#660000",width=barwidth,edgecolor="grey",label="API")
plt.bar(br6,IND1,color="g",width=barwidth,edgecolor="grey",label="IND1")
plt.bar(br7,IND2,color="#FFFF33",width=barwidth,edgecolor="grey",label="IND2")
plt.bar(br8,JSVP,color="#33FFFF",width=barwidth,edgecolor="grey",label="JSVP")
plt.bar(br9,HND,color="#00FF00",width=barwidth,edgecolor="grey",label="HND")


plt.xlabel("YEARS -------->",fontweight="bold",fontsize=15)
plt.ylabel("VOTES(in %) ---------->",fontweight="bold",fontsize=15)
plt.xticks([r+barwidth for r in range(len(BJP))],years)
plt.legend()
plt.show()


#Experiment no:- 3 
#Experiment name:- Illustrate the usage of different color codes.
import matplotlib.pyplot as plt
import numpy as np
barwidth=0.1
fig=plt.subplots(figsize=(20,9))
ax=plt.axes()

In_number=["50000000","100000000","150000000","200000000","250000000","300000000","350000000","400000000","450000000","500000000","550000000","600000000"]
y=[50000000,100000000,150000000,200000000,250000000,300000000,350000000,400000000,450000000,500000000,550000000,600000000]
AN_Island=[498279.0,15242.0,505398.0,16206.0,1.43,6.32]
AndhraPradesh=[194767874.0,281083.0,237051508.0,280356.0,21.71,-0.26]
ArunachalPradesh=[512436.0,7653.0,555639.0,7825.0,8.43,2.25]
Assam=[4710617.0,15592.0,5447805.0,26878.0,15.65,72.38]
Bihar=[33621613.0,1087971.0,33990038.0,1093141.0,1.1,0.48]
Chandigarh=[1538796.0,39681.0,1563795.0,44132.0,1.62,11.22]
Chhattisgarh=[19329501.0,14399.0,17304506.0,6817.0,-10.48,-52.66]
Dadra_NagarHaveli=[609435.0,1608.0,618330.0,1666.0,1.46,3.61]
Daman_Diu=[898824.0,5694.0,897804.0,5703.0,-0.11,0.16]
Delhi=[29114423.0,2740502.0,36467598.0,2983436.0,25.26,8.86]
Goa=[7081559.0,933841.0,7127287.0,937113.0,0.65,0.35]
Gujrat=[54369873.0,513113.0,58864661.0,595607.0,8.27,16.08]
Haryana=[4888952.0,73977.0,4549017.0,48046.0,-6.95,-35.05]
HimachalPradesh=[6093935.0,356568.0,16829231.0,382876.0,4.57,7.38]
Jharkhand=[35408822.0,175801.0,35580768.0,176043.0,0.49,0.14]
Jammu_Kashmir=[17076315.0,139520.0,16163330.0,57920.0,-5.35,-58.49]
Karnataka=[214306456.0,543716.0,227934714.0,608754.0,6.36,11.96]
Kerala=[15604661.0,1096407.0,18384233.0,1189771.0,17.81,8.52]
Lakshadweep=[10435.0,1313.0,6985.0,820.0,-33.06,-37.55]
Ladakh=[25486.0,21984.0,241285.0,38652.0,197654.0,23451.0]
MadhyaPradesh=[83969799.0,375476.0,88707139.0,327958.0,5.64,-12.66]
Maharashtra=[119191539.0,5078514.0,149294703.0,5528704.0,25.26,8.86]
Manipur=[176109.0,6391.0,167560.0,13608.0,-4.85,112.92]
Meghalaya=[1198340.0,18114.0,1245633.0,25813.0,3.95,42.5]
Mizoram=[76551.0,967.0,163762.0,2249.0,113.93,132.57]
Nagaland=[101588.0,5010.0,125949.0,5577.0,23.98,11.32]
Odisha=[15208540.0,110818.0,15307637.0,115128.0,0.65,3.89]
Puducherry=[1616660.0,141133.0,1713248.0,149919.0,5.97,6.23]
Punjab=[44595061.0,1200969.0,47385387.0,1101343.0,6.26,-8.3]
Rajasthan=[50235643.0,1754348.0,52220431.0,1605560.0,3.95,-8.48]
Sikkim=[1426127.0,71172.0,1421823.0,133388.0,-0.3,87.42]
TamilNadu=[385909376.0,6074345.0,494865257.0,6866327.0,28.23,13.04]
Telengana=[92878329.0,318154.0,83035894.0,323326.0,-10.6,1.63]
Tripura=[414388.0,102861.0,437201.0,154405.0,5.51,50.11]
UttarPradesh=[285079848.0,3780752.0,535855162.0,4745181.0,87.97,25.51]
Uttarakhand=[35609650.0,151320.0,37585920.0,152273.0,5.55,0.63]
WestBengal=[85657365.0,1617105.0,92366025.0,1656145.0,7.83,2.41]
Total=[1853787719.0,28851130.0,2321982663.0,31408666.0,25.3,8.9]

br1=np.arange(len(AN_Island))
br2=[x+barwidth for x in br1]
br3=[x+barwidth for x in br2]
br4=[x+barwidth for x in br3]
br5=[x+barwidth for x in br4]
br6=[x+barwidth for x in br5]
br7=[x+barwidth for x in br6]
br8=[x+barwidth for x in br7]
br9=[x+barwidth for x in br8]
br10=[x+barwidth for x in br9]
br11=[x+barwidth for x in br10]
br12=[x+barwidth for x in br11]
br13=[x+barwidth for x in br12]
br14=[x+barwidth for x in br13]
br15=[x+barwidth for x in br14]
br16=[x+barwidth for x in br15]
br17=[x+barwidth for x in br16]
br18=[x+barwidth for x in br17]
br19=[x+barwidth for x in br18]
br20=[x+barwidth for x in br19]
br21=[x+barwidth for x in br20]
br22=[x+barwidth for x in br21]
br23=[x+barwidth for x in br22]
br24=[x+barwidth for x in br23]
br25=[x+barwidth for x in br24]
br26=[x+barwidth for x in br25]
br27=[x+barwidth for x in br26]
br28=[x+barwidth for x in br27]
br29=[x+barwidth for x in br28]
br30=[x+barwidth for x in br29]
br31=[x+barwidth for x in br30]
br32=[x+barwidth for x in br31]
br33=[x+barwidth for x in br32]
br34=[x+barwidth for x in br33]
br35=[x+barwidth for x in br34]
br36=[x+barwidth for x in br35]
br37=[x+barwidth for x in br36]


plt.bar(br1,AN_Island,color="r",width=barwidth,edgecolor="grey",label="A&N Island")
plt.bar(br2,AndhraPradesh,color="#191970",width=barwidth,edgecolor="grey",label="Andhra Pradesh")
plt.bar(br3,ArunachalPradesh,color="#5F9EA0",width=barwidth,edgecolor="grey",label="Arunachal Pradesh")
plt.bar(br4,Assam,color="#9ACD32",width=barwidth,edgecolor="grey",label="Assam")
plt.bar(br5,Bihar,color="#B8860A",width=barwidth,edgecolor="grey",label="Bihar")
plt.bar(br6,Chandigarh,color="c",width=barwidth,edgecolor="grey",label="Chandighar")
plt.bar(br7,Dadra_NagarHaveli,color="#FFFF33",width=barwidth,edgecolor="grey",label="Dara & nagar haveli")
plt.bar(br8,Daman_Diu,color="#33FFFF",width=barwidth,edgecolor="grey",label="Daman & Diu")
plt.bar(br9,Delhi,color="#20B2AA",width=barwidth,edgecolor="grey",label="Delhi")
plt.bar(br10,Goa,color="#5F9EA0",width=barwidth,edgecolor="grey",label="Goa")
plt.bar(br11,Gujrat,color="#FF7F50",width=barwidth,edgecolor="grey",label="Gujrat")
plt.bar(br12,Haryana,color="#00008B",width=barwidth,edgecolor="grey",label="Harayana")
plt.bar(br13,HimachalPradesh,color="#6495ED",width=barwidth,edgecolor="grey",label="Himachal Pradesh")
plt.bar(br14,Jharkhand,color="#006400",width=barwidth,edgecolor="grey",label="Jharkhand")
plt.bar(br15,Jammu_Kashmir,color="#E9967A",width=barwidth,edgecolor="grey",label="Jammu & Kashmir")
plt.bar(br16,Karnataka,color="#DC143C",width=barwidth,edgecolor="grey",label="Karnataka")
plt.bar(br17,Kerala,color="#F0E68C",width=barwidth,edgecolor="grey",label="Kerela")
plt.bar(br18,Lakshadweep,color="#20B2AA",width=barwidth,edgecolor="grey",label="Lakashadeep")
plt.bar(br19,Ladakh,color="#CD5C5C",width=barwidth,edgecolor="grey",label="Ladakh")
plt.bar(br20,MadhyaPradesh,color="#778899",width=barwidth,edgecolor="grey",label="Madhya Pradesh")
plt.bar(br21,Maharashtra,color="#800000",width=barwidth,edgecolor="grey",label="Maharashtra")
plt.bar(br22,Manipur,color="#FFE4E1",width=barwidth,edgecolor="grey",label="Manipur")
plt.bar(br23,Meghalaya,color="#AFEEEE",width=barwidth,edgecolor="grey",label="Meghalaya")
plt.bar(br24,Mizoram,color="#CD853F",width=barwidth,edgecolor="grey",label="Mizoram")
plt.bar(br25,Nagaland,color="#DB7093",width=barwidth,edgecolor="grey",label="Nagaland")
plt.bar(br26,Odisha,color="#B0E0E6",width=barwidth,edgecolor="grey",label="Odisha")
plt.bar(br27,Puducherry,color="#DB7093",width=barwidth,edgecolor="grey",label="Puducherry")
plt.bar(br28,Punjab,color="#FFD700",width=barwidth,edgecolor="grey",label="Punjab")
plt.bar(br29,Rajasthan,color="#F4A460",width=barwidth,edgecolor="grey",label="Rajasthan")
plt.bar(br30,Sikkim,color="#FA8072",width=barwidth,edgecolor="grey",label="Sikkim")
plt.bar(br31,TamilNadu,color="#008080",width=barwidth,edgecolor="grey",label="Tamil Nadu")
plt.bar(br32,Telengana,color="#D8BFD8",width=barwidth,edgecolor="grey",label="Telengana")
plt.bar(br33,Tripura,color="#FF6347",width=barwidth,edgecolor="grey",label="Tripura")
plt.bar(br34,UttarPradesh,color="#FFB6C1",width=barwidth,edgecolor="grey",label="Uttar Pradesh")
plt.bar(br35,Uttarakhand,color="#00CED1",width=barwidth,edgecolor="grey",label="Uttra Khand")
plt.bar(br36,WestBengal,color="#2F4F4F",width=barwidth,edgecolor="grey",label="West Bengal")
plt.bar(br37,Total,color="#F08080",width=barwidth,edgecolor="grey",label="Total")



plt.title("State/UT wise Domastic Tourists visited in 2019",loc="left")
plt.ylabel("In Number",fontweight="bold",fontsize=15)
plt.xlabel("State/UT",fontweight="bold",fontsize=15)
ax.set_xticklabels=(["AN_Island","AndhraPradesh","ArunachalPradesh","Assam","Bihar","Chandigarh","Dadra_NagarHaveli","Daman_Diu","Delhi","Goa,Gujrat","Haryana","HimachalPradesh","Jharkhand","Jammu_Kashmir","Karnataka","Kerala","Lakshadweep","Ladakh",
"MadhyaPradesh","Maharashtra","Manipur","Meghalaya","Mizoram","Nagaland","Odisha","Puducherry","Punjab","Rajasthan","Sikkim","TamilNadu","Telengana","Tripura","UttarPradesh","Uttarakhand","WestBengal","Total"])
plt.yticks=(y)
ax.set_yticklabels(["50000000","100000000","150000000","200000000","250000000","300000000","350000000","400000000","450000000","500000000","550000000","600000000"])
plt.legend()
plt.show()


#Experiment no:- 4 
#Experiment name:-Build a scatterplot. 
import numpy as np
import matplotlib.pyplot as plt


y1 = [135874461,197234442,203233706,66288611,60836479,48033871]
y2 = [941239310,801519667,723566822,568237850,317141652,214206477]
x = ["2016","2017","2018","2019","2020","2021"]
ax=plt.axes()

plt.xlabel("Nature of project ------->")
plt.ylabel("Years --------->")


plt.scatter(y1,x,color='green',marker='*', label="Hostel")
plt.scatter(y2,x,color='red',marker='^', label="Residential School")
ax.set_xticklabels([100000000,200000000,300000000,400000000,500000000,600000000,700000000,800000000,900000000,1000000000])

plt.show()
