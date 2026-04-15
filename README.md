This index.html is one we got working with the National Geographic  - Every Issue Since 1888.

NOTE:  THIS IS WORK IN PROGRESS and can allow users who had purchased the National Geographic - All Issues DVD's and an index.html once the images are extracted from the DVDs which tools are available to do (ie: CNG2JPG). It isn't perfect (it does have glitches! - Help make this project better!) but it is workable.

The following are dependences based on how we are testing the index.html files and this is just for testing.

Dependencies:

1) Use cng2jpg to convert and save all CNG files to JPG.
    This will create a structure similar to: ./CNG/discs/images, directories based on years ie: 188x, 189x, 190x to 200x,
    directories names based on YYYYMMDD
2) Copy or move all the YYYYMMDD directories to one directory  ie: ./CNG/images
3) Copy the index.html file to the same directory (ie: ./CNG/images/index.html)


 <img width="1486" height="1086" alt="filelayout1" src="https://github.com/user-attachments/assets/f204fc4b-b3ec-46b5-998b-27277a752be2" />



If when viewing the magazines, the images go off the right or left sides, increase the size of your browser window if it isn't full screen. Some images on the dvds are quite large.

When you open the index.html the view of the National Geographic images will include scroll buttons for year and month on the top left, 
and page scroll buttons on the bottom left.

Here are some samples of what the viewing looks like:



<img width="2626" height="1906" alt="front1" src="https://github.com/user-attachments/assets/d0dbf37e-b97a-4646-a926-8e9f89965639" />


<img width="2820" height="1920" alt="screen1" src="https://github.com/user-attachments/assets/a37c1950-f797-4432-b09a-7d3cb0a2798d" />


<img width="3288" height="1914" alt="screen2" src="https://github.com/user-attachments/assets/a37e8255-a2e5-4ad5-aa65-3519cb3bd5b0" />






Here’s a clear, structured overview of what this flipbook viewer can do based on the index.html code :


📖 Core Viewer Features


🗂️ Magazine Issue Selection

* Dropdowns for **year (1888–2008)** and **month (01–12)**
* Automatically reloads content when changed
* Builds image paths dynamically based on selection


📄 Page Display

* **Page 1 shown as a single page**
* All subsequent pages shown as **two-page spreads**
* Handles:

  * Missing pages → displays **“No Page” placeholder**
* Responsive layout using full viewport


🔢 Page Detection (Smart)

* Automatically detects how many pages exist
* Works even if:

  * Pages are **missing in between**
* Uses:

  * ⚡ **Batched requests** (faster than sequential)
  * 🧠 **Caching per issue** (instant reload when revisiting)


⏭️ Navigation

* Buttons:

  * `<` previous
  * `>` next
* Keyboard:

  * ⬅️ Arrow Left → previous
  * ➡️ Arrow Right → next
* Navigation logic:

  * Page 1 → then jumps in spreads (2,4,6…)
* Prevents overflow past last page


🔍 Zoom & Interaction

🖱️ Mouse Wheel Zoom

* Smooth zoom in/out
* **Zoom centered on cursor position**

  * behaves like:

    * Google Maps
    * Image viewers
* Zoom limits:

  * Minimum: 1x (fit view)
  * Maximum: 5x


✋ Click + Drag Pan

* Click and drag to move the image
* Cursor changes:

  * grab → grabbing


🔄 Double-Click Reset

* Double-click anywhere on image:

  * Resets zoom to original view
  * Resets pan position
  * Smooth animated transition


⚡ Performance Features

🚀 Preloading

* Automatically preloads next pages:

  * `page + 1`
  * `page + 2`
* Makes navigation feel instant


🧠 Caching

* Stores detected page counts per issue
* Switching back to a viewed issue:

  * ⚡ Instant load
  * No re-scanning


🔄 Efficient Rendering

* Clears and rebuilds DOM per page change
* Avoids memory leaks:

  * Uses global mouse handlers (not duplicated)


📊 UI Enhancements


📄 Page Indicator

* Displays:

  * `Page 1 of X`
  * or `Pages 10–11 of X`


🎨 Clean UI

* Dark theme viewer
* Minimal controls:

  * top-left selectors
  * bottom-left navigation
  * bottom-right page info


🧩 Robustness


🛠️ Error Handling

* Missing images:

  * replaced with fallback block
* No crashes on missing pages


📁 Flexible File Support

* Works with:

  * Gaps in numbering
  * Incomplete datasets
* No need for perfect sequences


🏁 Summary

Viewer is:

* 📖 **Functional** — full flipbook browsing
* ⚡ **Fast** — batched + cached loading
* 🧠 **Smart** — handles missing pages gracefully
* 🖱️ **Interactive** — zoom, pan, reset
* 🧹 **Stable** — no event leaks or glitches
* 🎯 **User-friendly** — intuitive controls + feedback


🚀 If you want to go further

Next-level upgrades could include:

* 📖 Thumbnail sidebar / page grid
* 📱 Touch gestures (pinch + swipe)
* 🔍 Zoom-to-fit / zoom buttons
* 📂 Server-side index (instant load, no probing)
* 📚 Multi-issue navigation (like archive browser)
