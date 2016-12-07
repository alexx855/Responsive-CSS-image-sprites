### How it works?

For example, our sprite its a 291x73 and the icon its a 66x61 and it's -133px horizontal  and -6px vertical.

| Attribute     | How to calculate             |
| ------------- |:-------------|
| Padding bottom     | (icon height / icon width) * 100% | $1600 |
| Background size      | (sprite width / icon width) x 100       | 
| Background pos x | (x pixel pos / (sprite width - icon width)) x 100       |   
| Background pos Y | (y pixel pos / (sprite height - icone height)) x 100      |   

So, our SCSS would look like this:

```scss
.icon{
  display: inline-block;
  position:relative;
  flex-direction: column;  
  &::before{
    content: '';
    width: 100%;
    display: inline-block;
    background: url('../images/goggles_features.png') no-repeat;
  }
}

.icon--free-returns {
  &::before{
    background-position: 59.111% 50%;
    padding-bottom: 92.42%;
    background-size: 440.91%;
  }
  width: 20%;
}
```

Do you want it on CSS?:

```css
.icon{
  display: inline-block;
  position:relative;
  flex-direction: column;  
  &::before{
    content: '';
    width: 100%;
    display: inline-block;
    background: url('../images/goggles_features.png') no-repeat;
  }
}

.icon--free-returns {
  &::before{
    background-position: 59.111% 50%;
    padding-bottom: 92.42%;
    background-size: 440.91%;
  }
  width: 20%;
}
```

/* 

### Example
You can found two examples what ive used on my projects in this repo, but if you want to play with it, [here is a codepen example]


Any comment, suggestion or star are apreciate :)

