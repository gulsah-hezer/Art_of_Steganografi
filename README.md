# Art_of_Steganografi

***Steganography is the art of hiding secret data in any file.
The secret data can be data of any format like text or even a file. 
the main motive of steganography is to hide the intended information within any file, usually an image, audio, or video, without actually changing the external appearance of the file, i.e. 
it should look the same as before.
we will be focussing on learning image-based steganography, i.e. hiding secret data in an image.
But before diving a little deeper into it, let’s look at what an image comprises of.
Pixels are the building blocks of an image.
Every pixel contains three values: (red, green, blue) also known as RGB values.
Every RGB value ranges from 0 to 255.
This much information is enough to get started.
Now, let’s look at how we can encode and decode data into our image.


***There are a lot of algorithms that can be used to encode data into the image.
The one being used in there,is easy to understand and implement, as well.

The algorithm is as follows:

1) For each character in the data, its ASCII value is taken and converted into 8-bit binary.

2) Three pixels are read at a time having a total of 3*3=9 RGB values.
The first eight RGB values are used to store one character that is converted into an 8-bit binary.

3) Corresponding RGB value and binary data are compared. 
If the binary digit is 1 then the RGB value is converted to odd and, otherwise, even.

4) The ninth value determines if more pixels should be read or not. 
If there is more data to be read, i.e. encoded or decoded, then the ninth pixel changes to even.
Otherwise, if we want to stop reading pixels further, then make it odd.



