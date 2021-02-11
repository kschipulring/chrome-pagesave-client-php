# Chrome page saving client with PHP

### a tool to get saved webpages rendered with chrome-pagesave-server-nodejs (Chromedriver / Selenium based) on a remote server via HTTP(s)

This tool works typically by command line, but it can likely also be called via the browser.

The tool may also initiate a remote Chromedriver / Selenium tool to render.

### To get a rendered page rendered remotely from Chrome-pagesave-server-NodeJS endpoint:

(extremely basic) from your command line, within the directory of this project type or paste:

```
php index.php 
```
- this is a default call that calls the remotely rendered web page. 

NOTE: without any additiona parameters here, you will need a .env setup with at least the following settings:
- CHROMEPAGE_RENDERED_URL -> the URL location on the chrome-pagesave-server-nodejs server. This is the source.
- CHROMEPAGE_SAVE_FILENAME -> file name of what the script will save the file as. Relative to the script directory as.

But without depending on such .env settings, to do the same, you could then use:
```
php index.php --chromepage_rendered_url:https://{chrome-pagesave-server-nodejs service URL} --chromepage_save_filename:save-file.html
```


Without additional parameters for this op, you will minimally need .env settings for:

- ORIGIN_URL -> the raw origin web page URL.  Can literally be any public web page that a normal web browser can see.
- CHROMEPAGE_BASE_URL_RENDERER -> The URL for the chrome-pagesave-server-nodejs service. This will perform the work.

But without depending on such .env settings, to do the same, you could then use:
```
php index.php --origin_url:https://www.google.com --chromepage_base_url_renderer:https://{chrome-pagesave-server-nodejs service URL}/chromesave/
```
