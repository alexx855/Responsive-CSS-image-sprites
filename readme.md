### How it works?

| Attribute     | How to calculate             |
| ------------- |:-------------|
| Padding bottom     | (icon height / icon width) * 100% | $1600 |
| Background size      | (sprite width / icon width) x 100       | 
| Background pos x | (x pixel pos / (sprite width - icon width)) x 100       |   
| Background pos Y | (y pixel pos / (sprite height - icone height)) x 100      |   

So, our SCSS should look like this:

```scss
.icon{
  display: inline-block;
  &::before{
    content: '';
    display: block;
    width: 100%;
    height: 0;
    background: url('../images/goggles_features.png') no-repeat;
  }
}

.icon--one{
  width: 20%;
  &::before{
    background-position: 59.111% 50%;
    padding-bottom: 92.42%;
    background-size: 440.91%;
  }
}

```

### Example
You can found two examples what ive used on my projects in this repo, but if you want to play with it, [here is a codepen example]

#### Notes
Any comment, suggestion or star are apreciate :)

