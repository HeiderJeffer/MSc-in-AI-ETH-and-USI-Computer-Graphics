<body>
<img src = "https://github-vistors-counter.onrender.com/github?username=https://github.com/HeiderJeffer/MSc-in-AI-ETH-and-USI-Computer-Graphics" alt = "Visitors-Counter"/>
</body>

#### <span class="smallcaps">ETH Zurich and UNIVERSITÀ DELLA SVIZZERA ITALIANA</span>
#### FACULTY OF COMPUTER SCIENCE - Master in Artificial Intelligence
#### Topic: Computer Graphics \[2014\]
#### Speakers: Heider Jeffer and Prof. Kai Hormann 
#### Instructor: Mehdi Jazayeri
#### Assistant: Sasa Nesic

# Summary

Computer graphics are graphics created using computers and, more
generally, the representation and manipulation of image data by a
computer. The development of computer graphics, simply referred to as
CG, has made computers easier to interact with, and better for
understanding and interpreting many types of data. Developments in
computer graphics have had a profound impact on many types of media and
have revolutionized the animation and video game industry.

The term computer graphics has been used in a broad sense to describe”
almost everything on computers that is not text or sound, Typically, the
term computer graphics refers to several different things:

“The representation and manipulation of image data by a computer the
various technologies used to create and manipulate images the images so
produced, and the sub-field of computer science which studies methods
for digitally synthesizing and manipulating visual content.”

Today, computers and computer-generated images touch many aspects of our
daily life. Computer imagery is found on television, in newspapers, for
example in their weather reports, or for example in all kinds of medical
investigations and surgical procedures. A well-constructed graph can
present complex statistics in a form that is easier to understand and
interpret.

In the media “such graphs are used to illustrate papers, reports,
theses”, and other presentation material. Many powerful tools have been
developed to visualize data. Computer-generated imagery can be
categorized into several different types: 2D, 3D, and animated graphics.
As technology has improved, 3D computer graphics have become more
common, but 2D computer graphics are still widely used.

Computer graphics has emerged as a sub-field of computer science that
studies methods for digitally synthesizing and manipulating visual
content. Over the past decade, other specialized fields have been
developed like information visualization, and scientific visualization
more concerned with “the visualization of three-dimensional phenomena
(architectural, meteorological, medical, biological, etc.), where the
emphasis is on realistic renderings of volumes, surfaces, illumination
sources, and so forth, perhaps with a dynamic (time) component”.

# 2D computer graphics 

2D computer graphics are the computer-based generation of digital images
mostly from two-dimensional models, such as 2D geometric models, text,
and digital images, and by techniques specific to them. The word may
stand for the branch of computer science that comprises such techniques,
or for the models themselves.

# Pixel art 

Pixel art is a form of digital art, created through the use of raster
graphics software, where images are edited on the pixel level. Graphics
in most old (or relatively limited) computer and video games, graphing
calculator games, and many mobile phone games are mostly pixel art.

# Vector graphics

Vector graphics formats are complementary to raster graphics, which is
the representation of images as an array of pixels, as it is typically
used for the representation of photographic images. There are instances
when working with vector tools and formats is best practice, and
instances when working with raster tools and formats is best practice.
There are times when both formats come together. An understanding of the
advantages and limitations of each technology and the relationship
between them is most likely to result in the efficient and effective use
of tools.

# 3-D computer graphics

3D computer graphics in contrast to 2D computer graphics are graphics
that use a three-dimensional representation of geometric data that is
stored in the computer to perform calculations and render 2D images.
Such images may be for later display or real-time viewing. Despite these
differences, 3D computer graphics rely on many of the same algorithms as
2D computer vector graphics in the wireframe model and 2D computer
raster graphics in the final rendered display. 3D is occasionally
blurred; 2D applications may use 3D techniques to achieve effects such
as lighting, and primarily 3D may use 2D rendering techniques.

# Computer animation

Computer animation is the art of creating moving images via the use of
computers. It is a subfield of computer graphics and animation.
Increasingly it is created using 3D computer graphics, though 2D
computer graphics are still widely used for stylistic, low bandwidth,
and faster real-time rendering needs. Sometimes the target of the
animation is the computer itself, but sometimes the target is another
medium, such as film. It is also referred to as CGI (Computer-generated
imagery or computer-generated imaging), especially when used in films.

# Examples using Python:

These examples provide a basic understanding and implementation of each aspect mentioned in the research paper on Computer Graphics. Depending on specific requirements or applications, these examples can be expanded and customized further.

To provide a comprehensive code implementation for each section mentioned in the research paper on Computer Graphics, I'll break down the implementation into several key components: 2D graphics, pixel art, vector graphics, 3D graphics, and computer animation. Each section will include a basic example in Python to illustrate the concepts.

### 1. 2D Computer Graphics

```python
import matplotlib.pyplot as plt

# Example of plotting a simple 2D graph using matplotlib
x = [1, 2, 3, 4, 5]
y = [2, 3, 5, 7, 11]

plt.plot(x, y)
plt.title('Simple 2D Graph')
plt.xlabel('X axis')
plt.ylabel('Y axis')
plt.show()
```

### 2. Pixel Art

```python
from PIL import Image, ImageDraw

# Creating a simple pixel art image using PIL (Python Imaging Library)
image = Image.new('RGB', (100, 100), color='white')
draw = ImageDraw.Draw(image)

# Drawing a smiley face
draw.rectangle([(30, 30), (70, 70)], fill='yellow')  # face
draw.rectangle([(40, 40), (50, 50)], fill='black')   # left eye
draw.rectangle([(60, 40), (70, 50)], fill='black')   # right eye
draw.line([(40, 60), (60, 60)], fill='black', width=3)  # mouth

image.show()
```

### 3. Vector Graphics

```python
import matplotlib.pyplot as plt
import numpy as np

# Example of drawing vector graphics using matplotlib
fig, ax = plt.subplots()

# Drawing a vector arrow
ax.arrow(0, 0, 3, 4, head_width=0.5, head_length=0.5, fc='blue', ec='black')
ax.set_xlim(-1, 5)
ax.set_ylim(-1, 5)
ax.grid(True)
plt.title('Vector Arrow Example')
plt.show()
```

### 4. 3D Computer Graphics

```python
import matplotlib.pyplot as plt
from mpl_toolkits.mplot3d import Axes3D

# Example of plotting 3D graphics using matplotlib
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')

# Creating data
x = [1, 2, 3, 4, 5]
y = [2, 3, 5, 7, 11]
z = [1, 4, 9, 16, 25]

# Plotting a 3D scatter plot
ax.scatter(x, y, z, c='r', marker='o')
ax.set_xlabel('X axis')
ax.set_ylabel('Y axis')
ax.set_zlabel('Z axis')
plt.title('3D Scatter Plot Example')
plt.show()
```

### 5. Computer Animation

For computer animation, a basic example using libraries like Pygame or Matplotlib's animation module would be suitable. Here’s an example using Matplotlib:

```python
import matplotlib.pyplot as plt
from matplotlib.animation import FuncAnimation
import numpy as np

# Example of creating a simple animation using matplotlib
fig, ax = plt.subplots()

x = np.linspace(0, 2*np.pi, 100)
y = np.sin(x)

line, = ax.plot(x, y)

def animate(frame):
    line.set_ydata(np.sin(x + frame / 10.0))
    return line,

ani = FuncAnimation(fig, animate, frames=100, interval=50)
plt.title('Simple Sine Wave Animation')
plt.show()
```

