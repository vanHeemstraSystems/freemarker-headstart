freemarker-headstart
# Freemarker - Headstart

Based on "Freemarker.js" at https://freemarker.js.org/

Based on "The truth is in the code" at https://www.freecodecamp.org/news/the-truth-is-in-the-code-86a712362c99

## 100 - Introduction

*FreeMarker is a "template engine". It's a Java package, a class library for Java programmers.*

Freemarker.js is bridge API for [fmpp](http://fmpp.sourceforge.net/) to make [Freemarker](http://freemarker.org/) available with node.js.

100% language support like Freemarker on Java.

## 200 - References

- [Freemarker Manual](http://freemarker.org/docs/index.html)
- [FMPP Manual](http://fmpp.sourceforge.net/manual.html)

## 300 - Install

```
$ npm install freemarker.js
```

## 400 - How to Use

```
var Freemarker = require('freemarker.js');
var fm = new Freemarker({
  viewRoot: '/template',
  options: {
    /** for fmpp */
  }
});

// Single template file
fm.render(tpl, dataObject, function(err, html, output) {
  //...
});

// Use fmpp configuration file, see `http://fmpp.sourceforge.net/configfile.html`
fm.renderBulk(cfgFile, function(err) {
  //...
});

// Other
Freemarker.exec(['--version'], function(err, output) {
  //
});
```

## 500 - Configurations

Avaliable options for fmpp:

- **sourceEncoding**: The encoding of textual sources (templates). Use the special value "host"(-E host) if the default encoding of the host machine should be used. The default is "ISO-8859-1".
- **tagSyntax**: Sets the tag syntax for templates that doesn't start with the ftl directive. Possible values are: angleBracket, squareBracket, autoDetect.
- **timeFormat**: The format used to show time values. The default is locale dependent.
- **timeZone**: Sets the time zone in which date/time/date-time values are shown. The default is the time zone of the host machine. Example: GMT+02
- **numberFormat**: The number format used to show numerical values. The default is 0.############
- **dateFormat**: The format used to show date (year+month+day) values. The default is locale dependent.
- **booleanFormat**: The boolean format used to show boolean values, like "Yes,No". Not "true,false"; use ${myBool?c} for that. The default is error on ${myBool}.
- **datetimeFormat**: The format used to show date-time values. The default is locale dependent.
- **locale**: The locale (as ar_SA). Use the special value "host" (-A host) if the default locale of the host machine should be used. The default value of the option is en_US.
