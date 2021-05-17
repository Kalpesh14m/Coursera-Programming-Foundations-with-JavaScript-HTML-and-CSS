1. Which of the following commands creates a variable x and assigns it the value of the x coordinate of a pixel?

=> `var x = pixel.getX();`

---

2. A variable x has been initialized to have the value 2. What is the value of x after the following line of code has been executed?

`x = x*3;`

=> 6

---

3. Consider the following code segment:  

```
var x = 3;
print("x");
```
What is the output?

=> x

---

4. Which of the following lines of code includes a method call? Select all that apply.

=> Which of the following lines of code includes a method call? Select all that apply.

=> px.setRed(200);

---

5. Consider the following code. What does a call to i1.getHeight() return?
  ```
  var i1 = new SimpleImage(name);
  var i2 = new SimpleImage(name2);
  ```

=>   The height of image i1

---

6. Consider the code you just wrote in the last programming exercise to modify Drew’s picture shown on the left by making a red, green and blue vertical stripe as shown in the image on the right.

![](https://user-images.githubusercontent.com/25608527/118560101-96e4a680-b786-11eb-89a6-491b1a953476.JPG)

Which two of the following code segments are the correct loop to make this modification to the image named image? The red stripe is made by changing the red of all the pixels in the left vertical third to 255, the green of all the pixels in the middle vertical to 255, and the the blue of all the pixels in the right vertical third to 255.

  =>
  ```
  w = image.getWidth();
  for (var pixel of image.values()) {
       x = pixel.getX();
       if (x < w/3) {
            pixel.setRed(255);
       }
       if (x >= w/3 && x < 2*w/3) {
            pixel.setGreen(255);
       }
       if (x >= 2*w/3 && x <= w) {
            pixel.setBlue(255);
       }
  }
  ```
  
  =>
  ```
    w = image.getWidth();
  for (var pixel of image.values()) {
       x = pixel.getX();
       if (x < w/3) {
            pixel.setRed(255);
       }
       else if (x < 2*w/3) {
            pixel.setGreen(255);
       }
       else {
            pixel.setBlue(255);
       }
  }
  ```

---

7. The function swapRedGreen has one parameter, a pixel. This function swaps the red and green values and returns the resulting red, green and blue values somehow. Which one of the following is the correct code for this function?

=>
  ```
  function swapRedGreen(pixel) {	
       var newGreen = pixel.getRed();	
       var newRed = pixel.getGreen();	
       pixel.setGreen(newGreen);	
       pixel.setRed(newRed);	
       return pixel;
  }
  ```
  
---
  
8. Your friend is writing code to change the Duke blue devil to be yellow, as in the following example:

![](https://user-images.githubusercontent.com/25608527/118560102-9815d380-b786-11eb-9457-df3618fb9911.JPG)
  
=> They have made all pixels with a blue value of greater than 220 yellow, forgetting that white pixels have blue values of 255.


