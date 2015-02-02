---
layout: page
mathjax: true
permalink: /
---

## Drawing ConvNets (just for fun)
Hate overfitting? Well, here overfitting is finally 'useful'! Three ConvNets with 8 hidden layers are treating the pixels of an image as a learning problem: they take the (x,y) position on a grid and learn to predict the color at that point using regression to (r,g,b).
We are comparing three different activator functions (ReLU, maxout and tanh) and see how fast they overfit (it trains live in your browser!). Which Neural Net is your favorite artist? 

<style type="text/css">
canvas { 
    border: 1px solid #555;
    margin-top: 10px;
}
#wrap {
  width: 800px;
  margin-right: auto;
  margin-left: auto;
  margin-bottom: 200px;
}
#gallery img {
  width: 50;
  height: 50px;
  display: inline-block;
}
</style>

<div style="background-color: #EEE; padding: 10px; margin-top: 10px;">
<div style="float: left; margin-left: 10px;">
  Original Image<br>
  <canvas id="canv_original"></canvas>
</div>
<div style="float: left; margin-left: 10px;">
  ConvNet (ReLU) <br>
  <canvas id="canv_net"></canvas>
</div>
<div style="float: left; margin-left: 10px;">
  ConvNet (maxout) <br>
  <canvas id="canv_net2"></canvas>
</div>
<div style="float: left; margin-left: 10px;">
  ConvNet (tanh) <br>
  <canvas id="canv_net3"></canvas>
</div>


<div style="clear:both;"></div>
</div>

<br>
<div>
  Click on one of the pics to load a new picture ...
</div>

<div id="gallery">
  <img src="imgs/david.png" class="ci" title="itse me!"/>
  <img src="imgs/iris.png" class="ci" title="iris!"/>
  <img src="imgs/seb.png"  class="ci" title="seb!"/>
  <img src="imgs/alexis.png" class="ci" title="my prof!"/>
  <img src="imgs/tum_logo_color.png"  class="ci" title="my lovely uni!"/>
  <img src="imgs/brml_logo.png"  class="ci" title="machine learning!"/>
</div>
<div style="float: left;">
or upload your own picture
<input id="f" type="file" />
</div>
<br>
<br>

<div style="background-color: grey; padding: 10px; margin-top: 10px;">
<b>ConvNet (ReLU)</b>
<div id="report"></div>
<br>

<div id="lr">Learning rate:</div>
<div id="slider"></div>

<br>
<b>ConvNet (maxout)</b>
<div id="report2"></div>
<br>

<div id="lr2">Learning rate:</div>
<div id="slider2"></div>

<br>
<b>ConvNet (tanh)</b>
<div id="report3"></div>
<br>

<div id="lr3">Learning rate:</div>
<div id="slider3"></div>
</div>


<script src="bundle.js"></script>
<script src="convnet2.js"></script>
<script src="convnet3.js"></script>

Written in nodejs using browserify convnetjs