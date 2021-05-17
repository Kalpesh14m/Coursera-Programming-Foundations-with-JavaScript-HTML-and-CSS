1. Consider the following code that declares two variables x and y. 

  ```
  var x = 8 ;
  var y = 4 ;
  x = 3 ;
  y = 2 + x ;
  print(y);
  ```

Which one of the following is the correct value printed out when this code runs?

=> 5

---

2. Consider writing a function named phrase3words that puts three words together into a phrase that is of type string with blanks between the words. The function phrase3words has three parameters named value1, value2 and value3. This function concatenates the words together into one string that has value1 first, followed by a blank, followed by value2, followed by a blank, and followed by value3.
For example, the call phrase3words("smile","at","everyone") would calculate and return the string "smile at everyone".
The function phrase3words has been started below for you but is missing code where it says [code here].

  ```
  function phrase3words(value1, value2, value3) {
      var answer = [code here] ;          
      return answer;
  }
  ```
Which one of the following is the correct code to replace the line containing  [code here] ?

=> `var answer = value1 + " " + value2 + " " + value3 ;`

---

3. Consider a function named phrase3words that puts three words together into a phrase that is of type string with blanks between the words. The function phrase3words has three parameters named value1, value2 and value3. This function concatenates the words together into one string that has value1 first, followed by a blank, followed by value2, followed by a blank, and followed by value3.
For example, the call phrase3words("smile","at","everyone") would calculate and return the string "smile at everyone".
Consider the following code that uses the phrase3words function. 

  ```
  var result1 = phrase3words("smile","at","everyone");
  var result2 = phrase3words("everyone","wave", "back");
  var result3 = phrase3words("that", "might", "make");
  var result4 = phrase3words(result1, result3, result2);
  print(result4);
  ```

Which one of the following is the phrase that is printed when this code runs?

=> smile at everyone that might make everyone wave back

---

4. Consider a function named reformatName that puts a name together in a specific format.  The function reformatName has two parameters named first and last, representing the first and last names. This function puts the names together into one string that has the last name first, followed by a comma and blank, and then followed by the first name. 
For example, the call reformatName("Susan", "Rodger") returns the string "Rodger, Susan", and the call reformatName("Robert", "Duvall") returns the string "Duvall, Robert".
Which one of the following is NOT a correct implementation of this function?

=>

```
function reformatName(first, last) {
    var name = last + ", " ;
    name = first + name ;
    return name;
}
```

---

5. Consider writing a function named numberPixels that calculates the total number of pixels in an image. The function numberPixels has one parameter named namefile, which is a string that is the name of an image file. This function calculates and returns the total number of pixels in the specified image filename.
For example, consider the image named chapel.png that has 231 pixels in width and 308 pixels in height. The call numberPixels("chapel.png") returns 71148. 
This function has been started for you and has missing code:

    ```
    function numberPixels(namefile) {
        var someImg = new SimpleImage(namefile);
        var height = someImg.getHeight();
        // missing code
    }
    ```

Which one of the following has the correct missing code so that the function numberPixels works correctly?

=>

```
var width = someImg.getWidth();
var total = height * width:
return total;
```

---

6. Consider writing a function named perimeter that calculates the number of pixels in the perimeter of an image. The perimeter is the number of pixels on the edge of the image, from all four sides. The function perimeter has one parameter named imageName, which is a string that is the name of an image file. This function calculates and returns the perimeter in the specified image filename.
For example, the image "rodger.png" has 315 pixels in width and 424 pixels in height. That means it has 315 pixels on the bottom, 315 on the top, 424 on the right side and 424 on the left side. The perimeter of this image is 315 + 315 + 424 + 424 =  1478. The call perimeter("rodger.png") returns 1478.
Which one of the following is NOT a correct implementation of this function?

=>

```
function perimeter(imageName) {
    var someImg = new SimpleImage(imageName);
    var value = 2 * (someImg.getHeight() * someImg.getWidth());
    return value;
}
```

---

7. Consider writing a function named printPixel that prints the red, blue and green values of a pixel, in that order, one on each line, and identifies each one. The function printPixel has three parameters,  namefile, which is a string that is the name of an image file, and xpos and ypos that are numbers representing the x and y coordinates of the pixel location. Consider using the SimpleImage methods getRed, getGreen, and getBlue. Since this function is printing values, it does NOT need a return statement. 
Consider the call: printPixel("drewgreen.png",10, 10);
Note that in the image drewgreen.png, Drew is standing in the middle and the background is bright green. So the pixel at (10,10) is near the edge and is bright green. For its red, green and blue values, it has all green (255), no blue (0)  and only a tiny bit of red (1). The corresponding output should be:

red is 1

green is 255

blue is 0

This function has been started for you and has missing code:

```
function printPixel(nameImage, xpos, ypos) {
    // missing code
}
```

Which one of the following has the correct missing code so that the function printPixel works correctly and displays the output in the format above?

=>

```
function printPixel(nameImage, xpos, ypos) {
    var someImage = new SimpleImage(nameImage) ;
    print("red is " + someImage.getRed(xpos,ypos));
    print("green is " + someImage.getGreen(xpos,ypos));
    print("blue is " + someImage.getBlue(xpos,ypos));
}
```

---

8. Write a function named sumPixel that calculates and returns the sum of the red, blue and green values of a pixel.  The function sumPixel has three parameters,  namefile, which is a string that is the name of an image file, and xpos and ypos that are numbers representing the x and y coordinates of the pixel location.
Consider the image drewgreen.png.  The pixel at location (250,500) has red component 102, green component 90 and blue component 80. The call  sumPixel("drewgreen.png", 250, 500) should return 102+90+80 = 272.
Which one of the following is the correct code for sumPixel?

=>

```
function sumPixel(nameOfImage, xpos, ypos) {
    var theImage = new SimpleImage(nameOfImage) ;
    var redNumber = theImage.getRed(xpos,ypos);
    var blueNumber = theImage.getBlue(xpos,ypos);
    var greenNumber = theImage.getGreen(xpos,ypos);
    return redNumber + blueNumber + greenNumber;
}
```
