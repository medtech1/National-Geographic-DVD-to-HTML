This index.html is one we got working with the National Geographic  - Every Issue Since 1888.

The following are dependences based on how we are testing the index.html files and this is just for testing.

Dependencies:

1) Use cng2jpg to convert and save all CNG files to JPG.
    This will create a structure similar to: ./CNG/discs/images, directories based on years ie: 188x, 189x, 190x to 200x,
    directories names based on YYYYMMDD
2) Copy or move all the YYYYMMDD directories to one directory  ie: ./CNG/images
3) Copy the index.html file to the same directory (ie: ./CNG/images/index.html)

When you open the index.html the view of the National Geographic images will include scroll buttons for year and month on the top left, 
and page scroll buttons on the bottom left.

Here are some samples of what the viewing looks like:



<img width="2626" height="1906" alt="front1" src="https://github.com/user-attachments/assets/d0dbf37e-b97a-4646-a926-8e9f89965639" />


<img width="2820" height="1920" alt="screen1" src="https://github.com/user-attachments/assets/a37c1950-f797-4432-b09a-7d3cb0a2798d" />


<img width="3288" height="1914" alt="screen2" src="https://github.com/user-attachments/assets/a37e8255-a2e5-4ad5-aa65-3519cb3bd5b0" />
