# About
 X11 protocol client for node.js

# status

soon to be released at stage 2) ( see [roadmap.txt](node-x11/blob/master/roadmap.txt) )

# example

    var x = require('x11');

    var s = x.createConnection().defaultScreen();
    var wnd = s.createWindow(10, 10, 100, 100); 
    // adding event callback also selects event on server
    wnd
      .on('expose', function(exposeevent)
      {
          this.drawString(10, 50, 'Hello');
      })
      .on('keypress', function(keyevent) 
      {
          process.exit(0);
      });



# Protocol documentation

  - http://www.x.org/releases/X11R7.6/doc/
  - http://www.x.org/releases/X11R7.6/doc/xproto/x11protocol.pdf

# Other implementations

  - C: XLib - http://codesearch.google.com/codesearch/p?hl=en#xEHUuo8Crmg/sites/ftp.x.org/pub/X11R7.2/src/update/everything/libX11-X11R7.2-1.1.1.tar.bz2%7CnOqwAyDlYlo/libX11-X11R7.2-1.1.1/src/OpenDis.c&q=XOpenDisplay&d=3
  - C: XCB - http://xcb.freedesktop.org/
  - Python/twisted:  https://launchpad.net/twisted-x11
  - Perl: http://search.cpan.org/~smccam/X11-Protocol-0.56/Protocol.pm
