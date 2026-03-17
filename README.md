# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# NAME : SHREEJA R S
# REF.NO : 25017561


# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
import matplotlib.pyplot as plt
%matplotlib inline
import numpy as np
```
```
## Simple Examples

x=np.arange(0,10)
y=np.arange(11,21)
```
```
a=np.arange(40,50)
b=np.arange(50,60)

```

```
##plotting using matplotlib 

##plt scatter

plt.scatter(x,y,c='g')
plt.xlabel('X axis')
plt.ylabel('Y axis')
plt.title('Graph in 2D')
plt.savefig('Test.png')
```

<img width="636" height="597" alt="Screenshot 2026-03-13 084852" src="https://github.com/user-attachments/assets/131172da-5120-471c-bd55-f0cc295b8189" />

<img width="748" height="861" alt="Screenshot 2026-03-13 084908" src="https://github.com/user-attachments/assets/c1cf4209-4b3b-491a-bdc8-148ab8d79c85" />

```
y=x*x
```



```
## plt plot

plt.plot(x,y,'r*',linestyle='dashed',linewidth=2, markersize=12)
plt.xlabel('X axis')
plt.ylabel('Y axis')
plt.title('2d Diagram')
plt.show()
```
<img width="725" height="845" alt="Screenshot 2026-03-13 084922" src="https://github.com/user-attachments/assets/4df27b30-2251-4be3-970b-81c1ba20ff5f" />


```
## Creating Subplots

plt.subplot(2,2,1)
plt.plot(x,y,'r--')
plt.subplot(2,2,2)
plt.plot(x,y,'g*--')
plt.subplot(2,2,3)
plt.plot(x,y,'bo')
plt.subplot(2,2,4)
plt.plot(x,y,'go')
plt.show()
```
<img width="732" height="853" alt="Screenshot 2026-03-13 084932" src="https://github.com/user-attachments/assets/cc440dd6-c410-4ed7-b6ca-0ef44b28671d" />

```
x = np.arange(1,11) 
y = 3 * x + 5 
plt.title("Matplotlib demo") 
plt.xlabel("x axis caption") 
plt.ylabel("y axis caption") 
plt.plot(x,y) 
plt.show()
```
<img width="734" height="799" alt="Screenshot 2026-03-13 084943" src="https://github.com/user-attachments/assets/8c4c2bab-89dc-4941-9fcd-4f8c9cefac2d" />

```
np.pi
```
<img width="294" height="128" alt="Screenshot 2026-03-13 084953" src="https://github.com/user-attachments/assets/cfc1a390-4d71-488a-ba80-c144c4bde8ce" />

```
# Compute the x and y coordinates for points on a sine curve 
x = np.arange(0, 4 * np.pi, 0.1) 
y = np.sin(x) 
plt.title("sine wave form") 

# Plot the points using matplotlib 
plt.plot(x, y) 
plt.show() 
```

<img width="735" height="813" alt="Screenshot 2026-03-13 085000" src="https://github.com/user-attachments/assets/6a481891-ed83-4e20-bbb9-f787dbed6d30" />


```
#Subplot()
# Compute the x and y coordinates for points on sine and cosine curves 
x = np.arange(0, 5 * np.pi, 0.1) 
y_sin = np.sin(x) 
y_cos = np.cos(x)  
   
# Set up a subplot grid that has height 2 and width 1, 
# and set the first such subplot as active. 
plt.subplot(2, 1, 1)
   
# Make the first plot 
plt.plot(x, y_sin,'r--') 
plt.title('Sine')  
   
# Set the second subplot as active, and make the second plot. 
plt.subplot(2, 1, 2) 
plt.plot(x, y_cos,'g--') 
plt.title('Cosine')  
   
# Show the figure. 
plt.show()
```
<img width="729" height="842" alt="Screenshot 2026-03-13 085010" src="https://github.com/user-attachments/assets/83a805dc-cdfa-465c-97da-9ec7eb9a443a" />

<img width="737" height="303" alt="Screenshot 2026-03-13 085020" src="https://github.com/user-attachments/assets/e41f91f6-55c4-4537-9edb-8fac88f34a40" />

```
#Subplot()
# Compute the x and y coordinates for points on sine and cosine curves 
x = np.arange(0, 5 * np.pi, 0.1) 
y_sin = np.sin(x) 
y_cos = np.cos(x)  
   
# Set up a subplot grid that has height 2 and width 1, 
# and set the first such subplot as active. 
plt.subplot(2, 1, 1)
   
# Make the first plot 
plt.plot(x, y_sin,'r--') 
plt.title('Sine')  
   
# Set the second subplot as active, and make the second plot. 
plt.subplot(2, 1, 2) 
plt.plot(x, y_cos,'g--') 
plt.title('Cosine')  
   
# Show the figure. 
plt.show()
```
<img width="410" height="377" alt="Screenshot 2026-03-13 085027" src="https://github.com/user-attachments/assets/32939df5-3005-4775-84a3-5a5443009db3" />
<img width="755" height="637" alt="Screenshot 2026-03-13 085036" src="https://github.com/user-attachments/assets/6c9a9e95-5136-4c72-b911-312ca89cdfc7" />

```
a = np.array([22,87,5,43,56,73,55,54,11,20,51,5,79,31,27]) 
plt.hist(a) 
plt.title("histogram") 
plt.show()
```
<img width="746" height="743" alt="Screenshot 2026-03-13 085045" src="https://github.com/user-attachments/assets/6db39660-04a2-451c-a097-a05559c0574b" />

```
data = [np.random.normal(0, std, 100) for std in range(1, 4)]

# rectangular box plot
plt.boxplot(data,vert=True,patch_artist=False);  
plt.show()
```
<img width="765" height="731" alt="Screenshot 2026-03-13 085052" src="https://github.com/user-attachments/assets/db50039f-ca63-4cac-b421-0e8951b888f6" />

```
data = [np.random.normal(0, std ,100) for std in range (1,4)]

plt.boxplot(data,vert=True , patch_artist=True);
plt.show()
```
<img width="774" height="751" alt="Screenshot 2026-03-13 085059" src="https://github.com/user-attachments/assets/a5c22abc-f19d-4a0e-b725-c719cde9c532" />

```
data
```
<img width="782" height="840" alt="Screenshot 2026-03-13 085107" src="https://github.com/user-attachments/assets/0db5543f-a972-4aad-9d9a-c4b0490a9bf5" />

```
# Data to plot
labels = 'Python', 'C++', 'Ruby', 'Java'
sizes = [215, 130, 245, 210]
colors = ['gold', 'yellowgreen', 'lightcoral', 'lightskyblue']
explode = (0.4, 0, 0, 0)  # explode 1st slice

# Plot
plt.pie(sizes, explode=explode, labels=labels, colors=colors,
autopct='%1.1f%%', shadow=False)

plt.axis('equal')
plt.show()
```
<img width="710" height="848" alt="Screenshot 2026-03-13 085120" src="https://github.com/user-attachments/assets/357815f3-45f9-4476-988d-f57331de36f7" />




# Result:

   Thus, Data Visualization using matplotlib python library for the given datasets has been 
successfully performed
