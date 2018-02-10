/*****************************************************************************
 * Assignment 05: Drawing App         //  Date: January 29, 2018
 * ARTG 2260: Programming Basics      // Instructor: Jose
 * Written By: Richard Tu             // Email: tu.r@husky.neu.edu
 * Title: Drawing App that took a very long time
 ****************************************************************************/
 
Description: This is a drawing app that takes in mouse input to draw colors
			 and shapes - is TLDR version.
			  
Controls (In code, see "keypressed" section):
<+>/<=> - Display draw panel
<->/<-> - Hide draw panel
<?>/</> - Show/Hide help panel
<s> - Save the entire screen to a file
<S> - Save the canvas part of the screen to a file
<g>/<G> - Create a gradient
<f>/<F> - Create a background fill
<c>/<C> - Clear the canvas/screen
<r>/<R> - Activate/Deactivate "Random" for fill/stroke colors
<x> - Save the current frame/canvas
<z> - Load the saved frame/canvas
			  
This app has multiple features:
-Brush Color
-Brush Size
-GradientBG
-FillBG
-ClearBG
-Circle		[Shapes]
-Ellipse	[Shapes]
-Square		[Shapes]
-Rectangle	[Shapes]
-Triangle	[Shapes]
-Line		[Shapes]
-Random Coloring
-Save/Load
-Screen Capture
-Help

NOTE: It is recommended you run the application to better know what the
following are describing.

							***Brush Color***
The current Primary Brush Color can be seen as the color of the word 
"Brush Color". The Secondary (Alternative) Brush Color can be seen as the
background of the word "Brush Color".
<Left Click>s will draw with the primary brush color
<Right Click>s will draw with the secondary brush color

Brush Color is split up into three bars. 
-The first bar represents an HSB (Hue, saturation, Brightness) color spectrum. 
-The second bar represents HSB but only the shades between black and white
 since the other spectrum (1st bar) did not have black or white. 
-The third bar represents the alpha of the brush and will affect how 
 "see through" your brush strokes are.

For each bar, there is a line representing where in the spectrum you clicked
-The first bar has a black line representing the primary brush color and
 white line representing the secondary brush color.
-The second bar has a red line representing the primary brush color and
 white line representing the secondary brush color.
-The third bar has a black line representing the primary brush color and
 white line representing the secondary brush color.
 
Brush Color can be set to white to simulate an eraser tool
 
You will see later on that brush color also affects other features.

							***Brush Size***
The current Primary Brush Size can be seen as the black number to the left
of the Brush-Size Triangle. The Secondary (Alternative) Brush Color can be
seen as the white number to the left of the Brush-Size Triangle.

Brush Size is determined by clicking/dragging along the triangle. A vertical
bar will show up displaying visually what size your primary/secondary brush
are - you can also see it numerically as described earlier.

You will see later on that brush size also affects other features.

							***GradientBG***
GradientBG or Gradient Background will set a gradient background onto the
canvas of the drawing. If the draw panel is not there, it will draw from one
corner of the screen to the other, but if the draw panel is there, it will
create a background in only the canvas part of the screen.

GradientBG will make the gradient based on the primary brush color.

GradientBG will also have a "strength" of the gradient that is based on the
x position of your mouse when you click it.

Can be activated with <g> or <G>

							  ***FillBG***
FILLBG or Fill Background will fill a background with a single solid color. 
 
FillBG will fill the background based on the primary brush color.
 
Can be activated with <f> or <F>

							  ***ClearBG***
ClearBG or Clear Background will clean the canvas by setting the background
back to white.

Can be activated with <c> or <C>

							  ***Shapes***
A Shape can be a:
-Circle
-Ellipse (Oval)
-Square
-Rectangle
-Triangle
-Line

All shapes darken to indicate they are active. 

Different Shapes can be drawn simultaneously.

Shapes are drawn with a fill of the primary brush color and stroke of the 
secondary brush color.

Shapes will be drawn at the clicked mouseX and mouseY positions


Circle: The circle tool will create a circle based on the primary brush size

Ellipse: The ellipse tool will create an ellipse based on the primary brush
		 size (width) and the secondary brush size (height).
		 
Square: The square tool will create a square based on the primary brush size

Rectangle: The rectangle tool will create a rectangle based on the primary
		 brush size (width) and secondary brush size (height).

Triangle: The triangle tool will create a triangle based on the primary
		 brush size - as equilateral of a triangle as possible
		 
Line: The line tool will create a line based on the primary brush size

							***Random Color***
Random Color will override the brush color and force the brush to have a
randomly picked color for every single "frame" or stroke you are drawing

Random Color + GradientBG makes a rainbow HSB color spectrum on a gradient

Random Color + FillBG makes a rainbow HSB color spectrum

Random Color + [Shape] gives the shape a random fill and stroke

							 ***Save/Load***
This drawing app also has a save/load feature. The <x> button will save
the current state of the drawing and the <z> button will load the state.
You can only store one state.

If you mess up, and saved before you messed up, you can "undo" it by loading
-Save frequently!

						   ***Screen Capture***
The drawing app also comes with a screen capture feature. 
Using <s> will capture the full screen while using <S> (<Shift> + <s>) will
capture just the canvas (not the draw panel)

								***Help***
This app also has a help feature that will notify you what things do on
the drawing panel. Use it by simple pressing </> or <?>.