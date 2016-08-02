A Pen created at CodePen.io. You can find this one at http://codepen.io/alexmwalker/pen/VYoNVM.

 Hit the 'animate' radio button.

Experimenting with animating linear gradients across the image surface to fake a static light source as the model moves. 

At the moment:
- 1 animation for the rotation
- 1 animation for lighting effect, but applied across 3 surfaces

I'm animating the gradient's background-pos, which is always the top layer in a multiple background. 

Why am I using empty background layers on the surfaces? 

Each face needs a different background-position to position the cover, spine and back in it's frame (right, center, left). I want them to share the gradient animation, but NOT the cover image's background position. So I assign positioning to each layer (right, center, left), and then only render the cover image into the layer with the positioning i need. 

Might sound a little convoluted, but it's probably better than creating a different animation for each side.

Fun Fact: -webkit-filter applied to a HTML elements kills their pseudo elements (before and after). Weird, huh?.