/* 

padding bottom = (image height / image width) * 100%
background size = (total image width / display image width) x 100 
background position x = (x pixel pos / (total image width - display image width)) x 100 
background position y = (y pixel pos / (total image height - display image height)) x 100

*/

.icon::before {
  content: '';
  background: url('images/sprite.png') no-repeat 0 94.565%;
  height: 0;
  padding-bottom: 130%;
  width: 100%;
  display: inline-block;
  background-size: 953%; 
}
