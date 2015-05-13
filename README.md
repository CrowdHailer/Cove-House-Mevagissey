Cove House Mevagissey
=====================
A luxury holiday cottage with stunning views over the Mevagissey harbour, village and along the beautiful Cornish coast.

http://www.covehousemevagissey.com/

![View over Mevagissey harbour](http://covehousemevagissey.co.uk/images/DSC_1607.JPG)

License
=======
This page can be view for the purpose of openess. However all copyright is reserved to either [Workshop 14 Limited](http://workshop14.io) or appropriate content producer.

---

Update
======
This site is being moved to a more appropriate static hosting. During this process I will incorperate several optimisations and record impact.

Initial Page Speed Insights
Mobile speed: 0
Mobile user experience: 87
Desktop speed: 0  


### 1 Switch to Divshot
Effecient build steps useful for static
```sh
mkdir www www/images
for file in images/*; do convert $file -resize 500 ./www/$file; done
./node_modules/.bin/imagemin www/images/* www/images/
cat css/foundation.css css/layout.css | ./node_modules/.bin/cleancss > www/css/main.min.css
divshot push
```

### 2 Resize images
`for file in images/*; do convert $file -resize 500 ./www/$file; done`

Page Speed Insights
Mobile speed: 51
Mobile user experience: 87
Desktop speed: 55  

### 3 Optimise images
Compress images with imagemin
install
```sh
npm i --save-dev imagemin
```

Page Speed Insights
Mobile speed: 75
Mobile user experience: 87
Desktop speed: 86

### 4 Clean Css
Clean css with clean css
install
```sh
npm i --save-dev clean
```

Page Speed Insights
Mobile speed: 77
Mobile user experience: 87
Desktop speed: 87
