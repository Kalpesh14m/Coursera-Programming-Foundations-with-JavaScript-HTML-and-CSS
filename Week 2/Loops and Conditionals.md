1. Consider writing code  that turns the red part of every pixel in “chapel.png” to the highest red value possible. The image changes from the picture on the left to the redder picture on the right. 
 
 ![](https://user-images.githubusercontent.com/25608527/118557081-57b45680-b782-11eb-89fe-bd4dfb7715aa.JPG)
 
 ```
  var image = new SimpleImage("chapel.png");
  // missing code
  print(image);
  ```
  
  Which one of the following is the best choice for the correct missing code to turn the chapel red?

  =>
  ```
    for (var pixel of image.values()) {
        pixel.setRed(255);
    }
  ```

---

2. Consider writing code that starts with the image “chapel.png” shown below on the left and removes all the red from the image, resulting in the picture on the right below. 
 
 ![](https://user-images.githubusercontent.com/25608527/118557084-58e58380-b782-11eb-97cb-280aa53d1f69.JPG)

  ```
    var image = new SimpleImage("chapel.png");
    // missing code
    print(image);
  ```
  Which one of the following is the best choice for the correct missing code to remove all the red from the image?

  =>
  ```
  for (var pixel of image.values()) {
      pixel.setRed(0);
  }
  ```

---

3. Consider writing code that starts with the image “eastereggs.jpg” shown below on the left and replaces all the red pixel values higher than 70 with 70, resulting in the picture on the right below. 

  ![](https://user-images.githubusercontent.com/25608527/118557089-5a16b080-b782-11eb-8028-be0f2eb4e058.JPG)
  ```
    var image = new SimpleImage("eastereggs.jpg");
    // missing code
    print(image);
  ```
  Which one of the following is the best choice for the correct missing code to replace all the red values higher than 70 with 70?

=>
  ```
    for (var pixel of someImage.values()) {
        if (pixel.getRed() > 70) {
            pixel.setRed(70);
        }
    }
```

---

4. Consider writing code that starts with the image “astrachan.jpg” shown below on the left and replaces the bottom 10 rows of pixels with black pixels, resulting in the picture on the right below. 

![](https://user-images.githubusercontent.com/25608527/118557090-5a16b080-b782-11eb-9d94-f79260e7a97e.JPG)

```
  var image = new SimpleImage("astrachan.jpg");
  // missing code
  print(image);
```
Which one of the following is the best choice for the correct missing code to replace the bottom 10 rows with black pixels?

=>
```
  var height = someImage.getHeight();
  for (var pixel of someImage.values()) {
      if (pixel.getY() >= height - 10) {
          pixel.setRed(0);
          pixel.setGreen(0);
          pixel.setBlue(0);
      }
  }
```

---

5. Consider writing code that starts with the image “chapel.png” shown below on the left and replaces the top left corner with an all green square of size 50 by 50, resulting in the picture on the right below. 

![](https://user-images.githubusercontent.com/25608527/118557094-5aaf4700-b782-11eb-90eb-bb90e18b544b.JPG)
 
 ```
    var image = new SimpleImage("chapel.png");
    // missing code
    print(image);
  ```
 
 Which one of the following is NOT the correct missing code to add the green square to the top left corner of the image?

=>
  ```
  for (var pixel of someImage.values()) {
      if (pixel.getX() < 50) {
          pixel.setRed(0);
          pixel.setGreen(255);
          pixel.setBlue(0);
      }
      if (pixel.getY() < 50) {
          pixel.setRed(0);
          pixel.setGreen(255);
          pixel.setBlue(0);
      }
  }
  ```
---

6. Consider writing a function named topRightCorner that puts a rectangle of a specified color and size in the top right corner of the image. The function topRightCorner has six parameters named cornerWidth, cornerHeight, someImage, red, green, and blue. This function replaces the top right corner of the image someImage with a rectangle of height cornerHeight and width cornerWidth, and color that has red, green and blue numeric values.
For example, the call result = topRightCorner(30, 60, picture, 255, 255, 0)
where picture is the simpleImage on the left below, followed by print(result) results in a yellow rectangle (all red and all green makes yellow) of width 30 and height 60  in the top right corner.

  ![](https://user-images.githubusercontent.com/25608527/118557099-5be07400-b782-11eb-9449-a18de7ff54d5.JPG)
 
 This function has been started for you and is missing the body of the for loop. Also shown below the function is code that calls the function that results in the picture on the right with the yellow rectangle. 

```
  function topRightCorner(cornerWidth, cornerHeight, someImage, red, green, blue) {
      var width = someImage.getWidth();
      for (var pixel of someImage.values()) {
          // missing code
      }
      return someImage;
  }
  var picture = new SimpleImage("chapel.png");
  var result = topRightCorner(30, 60, picture, 255, 255, 0);
  print(result);
  ```

Which one of the following is the correct missing code for the for loop in the function topRightCorner?

=>
  ```
    if (pixel.getY() < cornerHeight) {
              if (pixel.getX() > cornerWidth - width) {
                  pixel.setRed(red);
                  pixel.setGreen(green);
                  pixel.setBlue(blue);
              }
          }
  ```

---

7. Consider a function named topRightCorner that puts a rectangle of a specified color and size in the top right corner of the image. The function topRightCorner has six parameters named cornerWidth, cornerHeight, someImage, red, green, and blue. This function replaces the top right corner of the image someImage with a rectangle of height cornerHeight and width cornerWidth, and color that has red, green and blue numeric values.
For example, the call result = topRightCorner(30, 60, picture, 255, 255, 0)
where picture is the simpleImage on the left below, followed by print(result) results in a yellow rectangle (all red and all green makes yellow) of width 30 and height 60  in the top right corner.

  ![](https://user-images.githubusercontent.com/25608527/118557102-5d11a100-b782-11eb-95ce-e131269e9ac3.JPG)

Consider calling the topRightCorner function repeatedly to change the chapel image into the image on the right below where each of the three colored squares is 30 by 30.

  ![](https://user-images.githubusercontent.com/25608527/118557106-5daa3780-b782-11eb-94cb-8940339727c8.JPG)

=>
  ```
  var picture = new SimpleImage("chapel.png");
  var result = topRightCorner(30, 60, picture, 255, 255, 0);
  var result2 = topRightCorner(60, 30, result, 0, 0, 255);
  var result3 = topRightCorner(30, 30, result2, 0, 255, 0);
  print(result3);
  ```

---

8. Consider the function named changeRed that draws a rectangle of width 256 showing all the changes of the color red, from left to right repeatedly, while blue and green are both set to 0. With height set to 200, the resulting image is shown here.

  ![](https://user-images.githubusercontent.com/25608527/118557111-5e42ce00-b782-11eb-97ea-4d6b15dfed1d.JPG)

The function changeRed has two parameters named width and height for the width and height of the rectangle. This function should start at the first pixel with red set to 0 and increment red by 1 with each new pixel it processes. After the red reaches 255, it should be reset back to 0 for the next row. This function returns the newly created image. The function has been started below. 

  **CODE:**
  ```
  function changeRed(width, height) {
      var picture = new SimpleImage(width, height);
      var red = 0;
       // missing code
      return picture;
  }
  var result = changeRed(256,200);
  print(result);
  ```
  **OUTPUT:**

  ![](https://user-images.githubusercontent.com/25608527/118557111-5e42ce00-b782-11eb-97ea-4d6b15dfed1d.JPG)

Which of the following is the correct code for the missing code for this function?

  =>
  ```
      for (var pixel of picture.values()) {
          pixel.setRed(red);
          pixel.setGreen(0);
          pixel.setBlue(0);
          if (pixel.getRed() < 255) {
              red = red + 1;
          }
          if (pixel.getRed() == 255) {
              red = 0;
          }
  }
  ```

---

9.Consider the function named changeRed that creates a rectangular image of width 256 showing all the changes of the color red, from left to right repeatedly, while blue and green are both set to 0. With height set to 200, the resulting image is shown here.

  ![](https://user-images.githubusercontent.com/25608527/118557111-5e42ce00-b782-11eb-97ea-4d6b15dfed1d.JPG)
 
 The function changeRed has two parameters named width and height for the width and height of the rectangle. This function should start at the first pixel with red set to 0 and increment red by 1 with each new pixel it processes. After the red reaches 255, it should be reset back to 0 for the next row. This function returns the newly created image. The function header is shown below. 
 
 `function changeRed(width, height) {`

Now consider allowing different values of blue and green. For example, if blue was 200 and green was 100, then as red changed from 0 to 255 the resulting image would change from a green color to an orange color as shown here:
  
  ![](https://user-images.githubusercontent.com/25608527/118557114-5edb6480-b782-11eb-8aa0-aee9713a7a1d.JPG)

Which of the following best describes how to modify the changeRed function so that different values of blue and green could easily be used when the function is called?

=> Add two parameters, one for the blue color and one for the green color. Then in the code set blue to be the blue number passed in and green to be the green number passed in. 


