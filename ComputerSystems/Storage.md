# Storage

## Why do we need secondary storage?
Secondary storage is the permenant storeage on your computer.
It is used to store the OS, programs and files.

## How much storage do I need?
All data on a computer is stored in binary.
This means data that we input needs to be storaged as 1s and 0s, and then we need to be able to read it again.
Storing text, images, music and other files as binary is called binary representation
We need to understand how a computer stores file to know how much storage we need

### Text
#### ASCII
ASCII stands for 'American Standard Code for Information Interchage'.
It was the first standard for representing letters in binary.
Before this everyone had a different system, so products from different manufactures could not 'talk' to each other.
ASCII was originally 7-bit, meaning that there are 128 possible combinations.
Not all of these 128 combinations are used for english letters. There are also 'non printing' characters link backspace, shift on, shift off, etc.
Symbols and numbers are also represented in ascii.

<div id="tt">
Here is just the printing ASCII characters. <i>skip to <a href="#tb">bottom</a></i>
</div>

ASCII | 8-bin binary | Denary
------|--------------|-------
32 | 0100000 | space
33 | 0100001 | !
34 | 0100010 | "
35 | 0100011 | #
36 | 0100100 | $
37 | 0100101 | %
38 | 0100110 | &
39 | 0100111 | '
40 | 0101000 | (
41 | 0101001 | )
42 | 0101010 | *
43 | 0101011 | +
44 | 0101100 | ,
45 | 0101101 | -
46 | 0101110 | .
47 | 0101111 | /
48 | 0110000 | 0
49 | 0110001 | 1
50 | 0110010 | 2
51 | 0110011 | 3
52 | 0110100 | 4
53 | 0110101 | 5
54 | 0110110 | 6
55 | 0110111 | 7
56 | 0111000 | 8
57 | 0111001 | 9
58 | 0111010 | :
59 | 0111011 | ;
60 | 0111100 | <
61 | 0111101 | =
62 | 0111110 | >
63 | 0111111 | ?
64 | 01000000 | @
65 | 01000001 | A
66 | 01000010 | B
67 | 01000011 | C
68 | 01000100 | D
69 | 01000101 | E
70 | 01000110 | F
71 | 01000111 | G
72 | 01001000 | H
73 | 01001001 | I
74 | 01001010 | J
75 | 01001011 | K
76 | 01001100 | L
77 | 01001101 | M
78 | 01001110 | N
79 | 01001111 | O
80 | 01010000 | P

<div id="tb">
<i>go to table <a href="#tt">top</a></i>
</div>

Using ascii you can represent words so **72 101 108 108 111 44 32 87 111 114 108 100 33** would be **Hello, World!**

#### Extended ASCII
ASCII was not big enough.
People needed ways to encode mathmatical symbols etc. on  acomputer, so Extended ASCII was invented.
This was an 8-bit verision on ASCII with 256 code.
(I won't put them all here, but with a quick internet search i'm sure you can find an extended ASCII table)
This made sence as computers process data in 8-bit bytes.

#### Unicode
Extended ASCII still had its issues.
It did not allow counties that use diffrent writing schemes to communicate.
With all of the latin alphabet, the Cyrillic script, and the thousands of japaneese characters a new solution was needed.
This was why the Unicde Consortium was founded. It's job was to maintain and popularises Unicode.
Unicode has space of characters from most (if not all) writing systems and even has space for emoji!

The first hundrard or so characters of unicode are the same as that of ASCII, to allow cross compatibitly with older devices

#### How big is an ASCII file?
In extended ASCII (we will not just refer to this as ASCII, as noone use 7-bit ASCII anymore), each character is represented as 1 byte.
This means that to calcuate the file of a plain text file, you just get the amount of characters (include spaces) and that is your amount of bytes.
So, **Hello, World! I am learning Computer Science.** has 45 characters so is 45 bytes in size.

### Images
Text isn't the only thing computers store.
Images can also be represented in binary.
Images are made up of lots of pixels (or picture elements).
You often desribe an image by how many pixels it has.
So an 2048 x 1536 image would mean that the image had 3145728 pixels.

As the amount of pixels used to represent an image increases, so does the file size (and quality). This works the other way around.

The reolution of an image is how many pixels is has per quare inch on the computer screen. If the resolution is higher, the image looks better.

#### Colour Depth
The colour depth of an image is how many bits that are used to represent a pixel.
If the color depth is one, there is 1 bit per pixel, meaning that a pixel can be black or white.

Increasing the colour depth increase how many colour a pixel could be, but also increases the file size. A color depth of 3 allow 8 colours to be used (2<sup>2</sup>).

If the colour depth is 8, then you can hase 256 different colors or red green and blue, meaing 16777216 different colours.
This is known as True Colors.

#### How big is an image file.

To calculate the size of an image file you fist need to know how many pixels are in an image.
Lets say that it is a very small 10x5 image, so there are 50 pixels.

Next you need to know how many bits represent each pixel. If there are 8 different colours you know that each pixel is 3 bits.

Now multiply the amount of pixels by the space take up by each pixel to get the file size.
In our case 50x3 = 150 bits, meaning the image size is 150B

#### Image MetaData
An image file does not just store the image itself. Often data about the data (or meta data) is also stored. This can be:
* The GPS location of where the image was taken
* the camera make / model
* the camera aperture setting
* the speed settings
* the dimentions of the image file

Other meta data can be added by the user such as
* titles
* captions
* headlines
* descriptions

### Sound
To know how computers represent sound, we first need to know what sound is.

Sound is just vibrations that travel through a medium.
The most common mediums for sound to travel through is air; water; materials like wood, metal and glass.

When these vibrations hit tiny hairs in our earsm out brain turns it into sound.

A wave can be plotted to represent sound. the the wavelength is wider, then the frequency is lower.

Analouge recoding devices record the height of the sound wave as it changes.
However, a computer is digital and cannot store continuous data.
This is why we need sampling.
If the sample rate is 5Hz that means that 5 samples are taken per second.

A sample just a snapshot of the sound wave at that moment in time.

Having a digital sound file allows you to edit and maninpulate the sound with computer equiptment.

CDs have a smaple rate of 44.1KHz, or 44100 samples per second.

![sample rate diagram](https://proxy.duckduckgo.com/iu/?u=http%3A%2F%2Fwww.bluefoxvideo.com%2Fimages%2Farticles%2Fsamplerate.jpg&f=1)

Bit depth is the amount of bits used to represent each sample.
If the bit depth is higher, the digital file will be more accureate.

#### Calculating file size.
To calculate the file size, you need the sample rate, bit depth, number of channels (mono / stero) and the length of the recording.
You then multiply all of these values to get the file size

## Types of storage
There are three main types of storage
* Optical
* Magnetic
* Solid State

Each type of storage has pros and cons that relate to their: capacity, portability, durability, reliablility and cost.

Factor       | Optical | Magnetic | Solid State
-------------|---------|----------|------------
Capacity     | CDs 700MB; DVDs 4.7GB; Blu-ray 128GB; | 1-2TB | 1TB
Portablility | Fairly large; More portable that magnetic | Not very portable; Physcial knocks can cause data corruption | Very portable; Inside cameras, phones etc
Durability   | Scratchs cause data loss; no rewrite | Very durable | Limited read/write cycles
Reliability  | if not scratched, very reliable | Very reliable | magnetic fields do not effect reliablitys
Cost         | Cheap | Cheap | More expensive, getting cheaper
