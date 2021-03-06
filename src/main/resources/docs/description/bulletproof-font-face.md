When using @font-face to declare multiple font types for cross browser compatibility, you can see 404's in old versions of IE
due to a bug in the way that IE parses the font declarations. For example, this syntax:

     @font-face {
       font-family: 'MyFontFamily';
       src: url('myfont-webfont.eot') format('embedded-opentype'),
         url('myfont-webfont.woff') format('woff'),
         url('myfont-webfont.ttf')  format('truetype'),
         url('myfont-webfont.svg#svgFontName') format('svg');
     }

Will cause a 404 in IE 6, 7, and 8. The fix is to add a question mark after the first font URL, so IE sees
the rest of the property value as a query string. This is a correct example:

     @font-face {
       font-family: 'MyFontFamily';
       src: url('myfont-webfont.eot?#iefix') format('embedded-opentype'),
         url('myfont-webfont.woff') format('woff'),
         url('myfont-webfont.ttf')  format('truetype'),
         url('myfont-webfont.svg#svgFontName') format('svg');
     }

[More information](http://www.fontspring.com/blog/the-new-bulletproof-font-face-syntax)

[Source](https://github.com/CSSLint/csslint/wiki/Bulletproof-font-face)
      