This index.html is one we got working with the National Geographic  - Every Issue Since 1888.

NOTE:  THIS IS WORK IN PROGRESS and can allow users who had purchased the National Geographic - All Issues DVD's to work with a simple index.html once the images are extracted from the DVDs which tools are available to do (ie: CNG2JPG). It isn't perfect but it is workable.

The following are dependences based on how we are testing the index.html files and this is just for testing.

Dependencies:

1) Use cng2jpg to convert and save all CNG files to JPG.
    This will create a structure similar to: ./CNG/discs/images, directories based on years ie: 188x, 189x, 190x to 200x,
    directories names based on YYYYMMDD
2) Copy or move all the YYYYMMDD directories to one directory  ie: ./CNG/images
3) Copy the index.html file to the same directory (ie: ./CNG/images/index.html)

Directory we used:
root@pc: /home/user1/Documents/CNG/images# ls -1
18881001
18890401
18890701
18891001
18900401
18900501
18900701
18900801
18910328
18910401
18910430
<snip>
index.html
root@pc: /home/user1/Documents/CNG/images#

root@Lenovo-Red:/home/michelle/Documents/CNG/images# ls 20071201
'2007_12_Dinosaurs_side 2.jpg'             NGM_2007_12_080_4.jpg   NGM_2007_12_161_4.jpg
'2007_12_Planet of Dinosaurs_side 1.jpg'   NGM_2007_12_081_4.jpg   NGM_2007_12_162_4.jpg
 NGM_2007_12_001_4.jpg                     NGM_2007_12_082_4.jpg   NGM_2007_12_163_4.jpg
 NGM_2007_12_002_4.jpg                     NGM_2007_12_083_4.jpg   NGM_2007_12_164_4.jpg
 NGM_2007_12_003_4.jpg                     NGM_2007_12_084_4.jpg   NGM_2007_12_165_4.jpg
 NGM_2007_12_004_4.jpg                     NGM_2007_12_085_4.jpg   NGM_2007_12_166_4.jpg
<snip>
root@pc: /home/user1/Documents/CNG/images#


If when viewing the magazines, the images go off the right or left sides, increase the size of your browser window if it isn't full screen. Some images on the dvds are quite large.

When you open the index.html the view of the National Geographic images will include scroll buttons for year and month on the top left, 
and page scroll buttons on the bottom left.

Here are some samples of what the viewing looks like:



<img width="2626" height="1906" alt="front1" src="https://github.com/user-attachments/assets/d0dbf37e-b97a-4646-a926-8e9f89965639" />


<img width="2820" height="1920" alt="screen1" src="https://github.com/user-attachments/assets/a37c1950-f797-4432-b09a-7d3cb0a2798d" />


<img width="3288" height="1914" alt="screen2" src="https://github.com/user-attachments/assets/a37e8255-a2e5-4ad5-aa65-3519cb3bd5b0" />
