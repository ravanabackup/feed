https://github.com/ravanabackup/feedlater/edit/main/README.md 

// ==UserScript==
// @name         Youtube Unblocker
// @namespace    YTUB
// @version      6.4
// @description  Automatically forwards country-blocked YouTube videos to clipzag.com and unblocks the video.
// @author       drhouse
// @include      https://www.youtube.com/watch*
// @require      http://code.jquery.com/jquery-3.4.1.min.js
// @require      https://cdnjs.cloudflare.com/ajax/libs/babel-standalone/6.18.2/babel.js
// @require      https://cdnjs.cloudflare.com/ajax/libs/babel-polyfill/6.16.0/polyfill.js
// @license      CC-BY-NC-SA-4.0
// @icon https://www.google.com/s2/favicons?sz=64&domain=youtube.com
// @locale       en
// ==/UserScript==
 
this.$ = this.jQuery = jQuery.noConflict(true);
(function($){
 
    setTimeout(function(){
        if($("#subreason").text() === 'The uploader has not made this video available in your country'){
            location.replace('https://clipzag.com/watch' + location.search);
        }
    }, 1000); 
 
})(jQuery);
