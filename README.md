### Description
Clone of Google Maps InfoBubble Library by **Luke Mahe** and **Chris Broadfoot** with some optimizations and new features. I developed these chanegs to provide a more capable customziation ability for this library. This library allows you to add css3 based infoWindows along with tabbing. My modifications enable you to specify tab coloring for active, and inactive tabs. As well as defining seperate padding for tabs and removed the lockout for `borderWidth = 0`.

You can see the entire library in its original code at: http://google-maps-utility-library-v3.googlecode.com/svn/trunk/infobubble/examples/example.html

### New Features

  * Active Tab CSS Class Definition
  * Tab Padding Definition
    * Default tab padding is set to 10px, like the InfoBubble
  * Removed the outerArrow lockout for no borderWidth
  
### Planned Features

 * segregate the ArrowColor and borderColor

### Documentation
The new features can be defined the same way all the other options are defined by adding them when you call a new `InfoBubble` class.

```Javascript
infoBubble2 = new InfoBubble({
    position: myLatlng,
    minWidth: 240,
    minHeight: 220,
    shadowStyle: 1,
    padding: 0,
    /**
     * Padding around the tabs, now set seperately
     * from the InfoBubble padding
     **/
    tabPadding: 12,
    /** 
     * You can set the background color to transparent, 
     * and define a class instead
     **/
    backgroundColor: 'transparent',
    borderRadius: 4,
    arrowSize: 10,
    borderWidth: 0,
    /**
     * Now that there is no borderWidth check, 
     * you can define a borderColor and it will 
     * apply to Just the arrow
     **/
    borderColor: '#AB2424',
    disableAutoPan: true,
    hideCloseButton: false,
    arrowPosition: 30,
    /** 
     * use the .phoney class to define all styling 
     * for your InfoBubble
     **/
    backgroundClassName: 'phoney',
    /**
     * define a CSS class name for all, this is 
     * technically the "inactive" tab class
     **/
    tabClassName: 'tabClass',
    /**
     * define a CSS class name for active tabs only
     **/
    activeTabClassName: 'activeTabClass',
    /**
     * define a custom src and/or className for close icon
     **/
    closeSrc: '//domain.com/img/myClose.png',
    closeClassName: 'infobubble-close',
    arrowStyle: 0
  });
```

### Credits
I would like to give props to the following people, as the majority of this work is built and maintained by them and not me. I have only made a few key modifications to the library for my needs and shared with the world.

* Luke Mahe @lukemahe
* Chris Broadfoot
* Many others on the Google Maps Team
