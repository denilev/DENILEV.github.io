---
title: "Пирамида логических уровней Роберта Дилтса."
author:
  name: "Денис"
  link: https://youtu.be/xafw2cqQP7E
date: 2022-05-18 14:10:00 +0800
categories: [Публикации]
tags: [осознание]
image:
  src: dilts.jpg
  width: 800
  height: 500
pin: true
---

Пирамида Дилтса является одной из важнейших моделей НЛП и коучинга.  

Она показывает то, каким образом наши представления о себе, ценности и убеждения оказывают непосредственное влияние на наши поступки, решения и окружающую действительность.  

Пирамида помогает разобраться в себе, лучше понять себя, предлагая найти ответы на вопросы: "Кто я?" и "Зачем" что-то есть или чего-то нет в моей жизни.
Это должен знать каждый.  

**Задание:** 
Личность или бизнес через пирамиду Дилтса. `Построить, ответить на вопросы.`



<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <!-- script and style block -->
            <script type="text/javascript" src="lib/jquery/1.10.2/jquery-1.10.2.min.js" ></script>
            <!-- audio -->
                <script type="text/javascript" src="lib/jPlayer.2.6.0/js/jquery.jplayer.min.js"></script>
                <script type="text/javascript" src="lib/jPlayer.2.6.0/js/jplayer.playlist.min.js"></script>
                <link href="lib/jPlayer.2.6.0/skin/vkontakte/vkontakte.css" rel="stylesheet" type="text/css" />
            <!-- audio -->
        <!-- /script and style block -->
        
        <!-- pour cette page -->
        <link 
            href="example.css" 
            media="all" 
            rel="stylesheet" />
        
    </head>
    <body >
        <div id="jquery_jplayer_1" class="jp-jplayer"></div>
        <div id="jp_container_1" class="jp-audio">

            <div class="jp-type-playlist">
                <div class="jp-gui jp-interface">
                    <ul class="jp-controls">
                        <li>
                            <label id="name-of-the-song-that-plays"></label>
                        </li>
                        <li><a href="javascript:;" class="jp-play" tabindex="1">play</a></li>
                        <li><a href="javascript:;" class="jp-pause" tabindex="1">pause</a></li>
                        <li><a href="javascript:;" class="jp-previous" tabindex="1">previous</a></li>
                        <li><a href="javascript:;" class="jp-next" tabindex="1">next</a></li>
                        <div class="clear"></div>
                    </ul>
                    <!-- Прогресс бар -->
                    <div class="jp-progress">
                        <div class="jp-seek-bar">
                            <div class="jp-play-bar"></div>
                        </div>
                    </div>
                    <!-- Регулятор громкости -->
                    <div class="jp-volume-bar">
                        <div class="jp-volume-bar-value"></div>
                    </div>
                    <!-- Остаток времени -->
                    <div class="jp-time-holder">
                        <div class="jp-current-time"></div>
                    </div>

                    <div class="clear"></div>

                    <!-- Кнопки повторения и перемешивания плейлиста -->
                    <ul class="jp-toggles">
                        <li>
                            <a href="javascript:;" class="jp-shuffle" tabindex="1" title="shuffle">shuffle</a>
                        </li>
                        <li>
                            <a href="javascript:;" class="jp-shuffle-off" tabindex="1" title="shuffle off">shuffle off</a>
                        </li>
                        <li>
                            <a href="javascript:;" class="jp-repeat" tabindex="1" title="repeat">repeat</a>
                        </li>
                        <li>
                            <a href="javascript:;" class="jp-repeat-off" tabindex="1" title="repeat off">repeat off</a>
                        </li>
                    </ul>
                    <div class="clear"></div>
                </div>
                <!-- Будущий плейлист -->
                <div class="jp-playlist">
                    <ul>
                        <li></li>
                    </ul>
                </div>
                <!-- Сообщение об ошибке -->
                <div class="jp-no-solution">
                    <span>Update Required</span>
                    To play the media you will need to either update your browser to a recent version or update your 
                    <a href="http://get.adobe.com/flashplayer/" target="_blank">
                        Flash plugin
                    </a>.
                </div>
            </div>
        </div>
    </body>
</html>



<script
//<![CDATA[
$(document).ready(function(){

    var cssSelector = {
        jPlayer: "#jquery_jplayer_1", 
        cssSelectorAncestor: "#jp_container_1"
    };

    var playlist = [
        {
            author:"TSP",
            title:"Cro Magnon Man",
            discription: "Текст песни / описание",
            mp3:"http://www.jplayer.org/audio/mp3/TSP-01-Cro_magnon_man.mp3",
            oga:"http://www.jplayer.org/audio/ogg/TSP-01-Cro_magnon_man.ogg"
        },
        {
            author:"TSP",
            title:"Your Face",
            discription: "Текст песни / описание",
            mp3:"http://www.jplayer.org/audio/mp3/TSP-05-Your_face.mp3",
            oga:"http://www.jplayer.org/audio/ogg/TSP-05-Your_face.ogg"
        },
        {
            author:"TSP",
            title:"Cyber Sonnet",
            discription: "Текст песни / описание",
            mp3:"http://www.jplayer.org/audio/mp3/TSP-07-Cybersonnet.mp3",
            oga:"http://www.jplayer.org/audio/ogg/TSP-07-Cybersonnet.ogg"
        },
        {
            author:"Miaow",
            title:"Tempered Song",
            discription: "Текст песни / описание",
            mp3:"http://www.jplayer.org/audio/mp3/Miaow-01-Tempered-song.mp3",
            oga:"http://www.jplayer.org/audio/ogg/Miaow-01-Tempered-song.ogg"
        },
        {
            author:"Miaow",
            title:"Hidden",
            discription: "Текст песни / описание",
            mp3:"http://www.jplayer.org/audio/mp3/Miaow-02-Hidden.mp3",
            oga:"http://www.jplayer.org/audio/ogg/Miaow-02-Hidden.ogg"
        },
        {
            author:"Miaow",
            title:"Lentement",
            free:true,
            discription: "Текст песни / описание",
            mp3:"http://www.jplayer.org/audio/mp3/Miaow-03-Lentement.mp3",
            oga:"http://www.jplayer.org/audio/ogg/Miaow-03-Lentement.ogg"
        },
        {
            author:"Miaow",
            title:"Lismore",
            discription: "Текст песни / описание",
            mp3:"http://www.jplayer.org/audio/mp3/Miaow-04-Lismore.mp3",
            oga:"http://www.jplayer.org/audio/ogg/Miaow-04-Lismore.ogg"
        },
        {
            author:"Miaow",
            title:"The Separation",
            discription: "Текст песни / описание",
            mp3:"http://www.jplayer.org/audio/mp3/Miaow-05-The-separation.mp3",
            oga:"http://www.jplayer.org/audio/ogg/Miaow-05-The-separation.ogg"
        },
        {
            author:"Miaow",
            title:"Beside Me",
            discription: "Текст песни / описание",
            mp3:"http://www.jplayer.org/audio/mp3/Miaow-06-Beside-me.mp3",
            oga:"http://www.jplayer.org/audio/ogg/Miaow-06-Beside-me.ogg"
        },
        {
            author:"Miaow",
            title:"Bubble",
            free:true,
            discription: "Текст песни / описание",
            mp3:"http://www.jplayer.org/audio/mp3/Miaow-07-Bubble.mp3",
            oga:"http://www.jplayer.org/audio/ogg/Miaow-07-Bubble.ogg"
        },
        {
            author:"Miaow",
            title:"Stirring of a Fool",
            discription: "Текст песни / описание",
            mp3:"http://www.jplayer.org/audio/mp3/Miaow-08-Stirring-of-a-fool.mp3",
            oga:"http://www.jplayer.org/audio/ogg/Miaow-08-Stirring-of-a-fool.ogg"
        },
        {
            author:"Miaow",
            title:"Partir",
            free: true,
            discription: "Текст песни / описание",
            mp3:"http://www.jplayer.org/audio/mp3/Miaow-09-Partir.mp3",
            oga:"http://www.jplayer.org/audio/ogg/Miaow-09-Partir.ogg"
        },
        {
            author:"Miaow",
            title:"Thin Ice",
            discription: "Текст песни / описание",
            mp3:"http://www.jplayer.org/audio/mp3/Miaow-10-Thin-ice.mp3",
            oga:"http://www.jplayer.org/audio/ogg/Miaow-10-Thin-ice.ogg"
        }
    ];

    var options = {
        swfPath: "js",
        supplied: "oga, mp3",
        wmode: "window",
        smoothPlayBar: false,
        keyEnabled: true
    };

    new jPlayerPlaylist(cssSelector, playlist, options);
});
//]]>
></script>



