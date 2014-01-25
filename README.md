# Custom Apache autoindex

To make apache autoindex pages look good, with a little help of bootstrap and jquery.

## Installation

### Local files

+ Create ".autoindex" folder in your webserver's root directory.
+ Copy files from repository to the ".autoindex" folder.
+ Add bootstrap.min.js and bootstrap.min.css files from [bootstrap distribution](https://github.com/twbs/bootstrap)
+ Add [jquery from distribution](https://github.com/jquery/jquery)
+ Customize header.html and footer.html to suit your needs.

You can link bootstrap and jquery from online CDN, but I recomend to make local copies for dev server.

### Apache config

+ Add instructions to apache config file.
Ie /etc/httpd/conf/extra/httpd-autoindex.conf or your custom apache config file.

```
IndexOptions FancyIndexing XHTML HTMLTable FoldersFirst SuppressHTMLPreamble SuppressDescription  SuppressRules IgnoreCase IconsAreLinks Charset=UTF-8 NameWidth=*
HeaderName "/.autoindex/header.html"
ReadmeName "/.autoindex/footer.html"
```

+ Restart apache.

