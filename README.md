# bitcoin-donate

Add simple donate buttons to any website

![A screenshot of the popover bubble](https://raw.githubusercontent.com/danielquinn/bitcoin-donate/master/screenshot.png "Screenshot")

It seems like a simple thing, yet after a bunch of browsing through
[/r/bitcoin](http://www.reddit.com/r/bitcoin) and basic web searches, I couldn't
find anything like it: a quick and easy way to have a "gimme bitcoins" button on
a website.

Most sites that solicit donations simply write the address out and expect you to
copy/paste it into a desktop bitcoin client in order to make use of it -- hardly
reasonable in an age of smart phones where most of us carry are to-use cash in
our pockets and our nest-eggs in some form of hard to access storage.

What the community needs is a means of getting a QR code to show up easy for
anyone with a phone so they can donate a small amount just by pointing that
phone at the screen.

So here's how you do it:

```html
<html>
  <head>
    <link rel="stylesheet" href="/path/to/css/btcdonate.css">
  </head>
  <body>

    <h1>My Awesome Web Page</h1>

    <p>Some stuff on your page and <a href="bitcoin:A_BITCOIN_ADDRESS">a donation link</a></p>
    <p>Some more stuff on your page</p>
    <p>
      Even more stuff on your page and
      <a href="bitcoin:ANOTHER_BITCOIN_ADDRESS?amount=0.01">
        another donation link, this time with a suggested amount
      </a>.
    </p>

    <script type="text/javascript" src="/path/to/js/jquery.js"></script>
    <script type="text/javascript" src="/path/to/js/jquery.qrcode.js"></script>
    <script type="text/javascript" src="/path/to/js/btcdonate.js"></script>

  </body>
</html>
```

What you end up with is a standard link with an on-mouseover popup containing a
QR code.  Just point your phone, and tap "send" in whatever app you're using.


## Working Demo

This code has been wrestled into a [jsfiddle](http://jsfiddle.net/T5uSN/2/) to see how it works, but the implementation there (due to a lack of CDN for these files) is not ideal.  The best way to use this is laid out above.


## 3rd-party libraries

Bitcoin-donate is licensed under the GPL3, but depends on two other Free
software projects [jQuery](https://github.com/jquery/jquery) (MIT license) and
[jQuery-QRCode](https://github.com/lrsjng/jQuery.qrcode) (as-is license). 


## Maturity

This is *very* young code and has only been tested in Firefox 30 when 
interacting with [Andreas Schildbach's popular Bitcoin Wallet](https://play.google.com/store/apps/details?id=de.schildbach.wallet)
app available in the Google Play store.  If you have tried this out under other
circumstances please feel free to say as much in the issue queue and I'll update
the status here.
