<style scoped lang='stylus'>
.player {
    width: 100%;
    position: fixed;
    top: 0;
    left: 0;
    z-index: 1;
    header {
        width: 100%;
        height: 50px;
        position: relative;
        text-align: center;
        line-height: 50px;
        z-index: 6;
        color: #fff;
        font-size: 14px;
        background: rgba(0, 0, 0, 0.3);
        .icon-houtui1 {
            width: 50px;
            height: 50px;
            text-align: center;
            font-size: 26px;
            text-align: center;
            line-height: 50px;
            display: block;
            position: absolute;
            top: 0;
            left: 0;
        }
    }
    .content_player {
        position: relative;
        overflow: hidden;
        padding-top: 20px;
        .cd {
            width: 80%;
            margin: 24px auto;
            margin-bottom: 0;
            position: relative;
            img {
                width: 100%;
            }
            .playerAlbumImage {
                position: absolute;
                top: 49%;
                left: 50%;
                transform: translate(-50%, -50%);
                width: 65%;
                border-radius: 50%;
                animation-name: donghua;
                animation-duration: 8s;
                animation-timing-function: linear;
                animation-play-state: paused;
                animation-iteration-count: infinite;
            }
            .playerAlbumImage.cur {
                animation-play-state: running;
            }
            @keyframes donghua {
                from {
                    transform: translate(-50%, -50%) rotate(0deg);
                }
                to {
                    transform: translate(-50%, -50%) rotate(360deg);
                }
            }
        }
        .swith {
            position: absolute;
            top: -23px;
            left: 63%;
            transform: translateX(-50%) rotate(-23deg);
            transform-origin: 24px 27px;
            width: 110px;
            transition: 1s linear all 0s;
            height: 165px;
            img {
                width: 100%;
            }
        }
        .swith.cur {
            transform: translateX(-50%) rotate(-9deg);
        }
    }
    .options {
        margin-top: 30px;
        ul {
            overflow: hidden;
            width: 80%;
            margin: 0 auto;
            li {
                float: left;
                width: 25%;
                color: rgba(255, 255, 255, 0.7);
                height: 50px;
                line-height: 50px;
                font-size: 30px;
                text-align: center;
            }
            li.icon-xin1 {
                font-size: 26px;
            }
        }
    }
    .kongzhiqi {
        height: 60px;
        line-height: 60px;
        color: rgba(255, 255, 255, 0.7);
        p:nth-child(1) {
            width: 15%;
            text-align: right;
        }

        p:nth-child(2) {
            width: 66%;
            margin: 0 2%;
            span.duration {
                width: 100%;
                display: block;
                height: 2px;
                background: rgba(255, 255, 255, 0.7);
                position: relative;
                top: 29px;
                span.currentTime {
                    position: absolute;
                    top: 0;
                    left: 0;
                    background: #c20c0c;
                    height: 2px;
                    width: 50%;
                    display: block;
                }
            }
        }
        p:nth-child(3) {
            width: 15%;
            text-align: left;
        }
    }
    .more {
        ul {
            overflow: hidden;
            li {
                float: left;
                width: 20%;
                color: rgba(255, 255, 255, 0.6);
                font-weight: normal;
                height: 50px;
                line-height: 50px;
                font-size: 32px;
                text-align: center;
            }
            li.icon-bofang,
            li.icon-pause-20 {
                font-size: 48px;
            }
        }
    }
    .audioPlayerList.cur {
        bottom: 0px;
    }
    .audioPlayerList {
        bottom: -300px;
        left: 0;
        width: 100%;
        background: #fff;
        height: 300px;
        z-index: 8;
        transition: 1s ease all 0s;
        ul {
            height: 250px;
            overflow-y: scroll;
        }
        .close {
            font-size: 28px;
            line-height: 50px;
            height: 50px;
            width: 50px;
            text-align: center;
            display: block;
            width: 100%;
        }
        div.index {
            width: 50px;
            line-height: 50px;
            text-align: center;
            font-size: 24px;
        }
        div {
            height: 50px;
            .musicName {
                color: #4b4c4d;
                height: 25px;
                line-height: 25px;
                /*下面4句话是 超出部分显示...*/
                overflow: hidden;
                display: -webkit-box;
                /*显示一行*/
                -webkit-line-clamp: 1;
                -webkit-box-orient: vertical;
            }
            .musicSinger {
                color: #888;
                font-size: 12px;
                height: 25px;
                line-height: 25px;
            }
        }
        .icon-bofang {
            font-size: 28px;
            line-height: 50px;
            height: 50px;
            width: 50px;
            text-align: center;
        }
        li.cur {
            color: #c20c0c;
            .musicName {
                color: #c20c0c;
            }
            .musicSinger {
                color: #c20c0c;
            }
        }
    }
    .popWindow {
        width: 100%;
        position: fixed;
        top: 0;
        left: 0;
        z-index: 7;
        background: rgba(0, 0, 0, 0.5);
    }
}

.lyric {
    overflow: hidden;
    ul {
        position: relative;
        transition: 0.6s all ease 0s;
        li {
            text-align: center;
            color: #fff;
            font-size: 14px;
            height: 26px;
            line-height: 26px;
            .animationLyric_origin {
                position: relative;display: inline-block;height: 26px;
                line-height: 26px;
                .animationLyric_current {
                    position: absolute;
                    top: 0;height: 26px;
                    line-height: 26px;
                    left: 0;
                    width: 100%;overflow: hidden;
                    white-space: nowrap;display: inline-block;
                    
                    
                }
            }
        }
        li.cur {
            .animationLyric_current {
                color: red;
                animation-name:lyricDonghua;
                animation-timing-function:linear;
            }
        }
        @keyframes lyricDonghua{
            from {width:0%;}
            to {width:100%;}
        }
    }
}

</style>
<template>
    <div class="player" v-height :style="{background:`#114b61 url(${player.playerbg}) 0 0 /100% 100% no-repeat`}">
        <header>
            <span class="iconfont icon-houtui1" @click="goback"></span>{{typeof player.index == 'number' ? player.album[player.index].musicName : "播放器"}}
        </header>
        <span v-if="typeof player.index == 'number'">
            <audio :src="player.album[player.index].musicUrl" autoplay @timeupdate="play" id="audio"></audio>
        </span>
        <div class="content_player" v-show="!isShowLyric" @click="showLyric" v-height="270">
            <div class="cd">
                <img src="../../resource/images/cd.png">
                <img :src="player.albumImage" class="playerAlbumImage" :class="{cur : isPlay}">
            </div>
            <div class="swith" :class="{cur : isPlay}">
                <img src="../../resource/images/swith.png">
            </div>
        </div>
        <div class="lyric" v-show="isShowLyric" v-height="250" @click="hideLyric">
            <ul>
                <li v-for="(item, index) in lyric" :class="{cur : currentTime > lyric[index][0] && currentTime + (lyric[index][0] - lyric[ index <= 0 ? 0 : index + 1 > lyric.length - 1 ? lyric.length - 1 : index + 1][0]) < lyric[index][0] }">
                    <span class="animationLyric_origin">
                        {{item[1]}}
                        <span class="animationLyric_current" :style="[{'animation-duration' : parseFloat(lyric[index + 1 > lyric.length - 1 ? lyric.length - 1 : index + 1]) - parseFloat(lyric[index]) + 's'},{'animation-play-state':isPlay ? 'running' : 'paused'}]">{{item[1]}}</span>
                        <!-- :time="parseFloat(lyric[index + 1 > lyric.length - 1 ? lyric.length - 1 : index + 1]) - parseFloat(lyric[index]) + 's'" -->
                    </span>
                </li>
            </ul>
        </div>
        <div class="options">
            <ul>
                <li class="iconfont icon-xin1"></li>
                <li class="iconfont icon-icon--"></li>
                <li class="iconfont icon-BAI-pinglun"></li>
                <li class="iconfont icon-more-vert"></li>
            </ul>
        </div>
        <div class="kongzhiqi ovh">
            <p class="fl">{{currentTime | zhuanhuan}}</p>
            <p class="fl">
                <span class="duration" @click="goTime($event)">
                    <span class="currentTime" :style="{width : currentTime / duration * 100 + '%'}"></span>
                </span>
            </p>
            <p class="fl">{{duration | zhuanhuan}}</p>
        </div>
        <div class="more">
            <ul>
                <li class="iconfont" :class="[{'icon-bofangye-caozuolan-suijibofang' : playState == 'random'},{'icon-xunhuan' : playState == 'all'},{'icon-singlecycle' : playState == 'once'}]" @click="changePlayState"> </li>
                <li class="iconfont icon-previous" @click="goPrev"> </li>
                <li class="iconfont " :class="[isPlay == false ? 'icon-bofang' : 'icon-pause-20']" @click="paused_played"> </li>
                <li class="iconfont icon-next" @click="goNext"> </li>
                <li class="iconfont icon-icon8" @click="showAudioList"> </li>
            </ul>
        </div>
        <div class="popWindow" v-height v-if="isShowAudioPlayerList"></div>
        <div class="audioPlayerList poa" :class="{cur : isShowAudioPlayerList}">
            <ul>
                <li v-for="(item, index) in player.album" class="ovh" :class="{cur : index == playerIndex}" @click="changeMusic(index)">
                    <div class="fl index iconfont" :class="{'icon-laba' : index == playerIndex}"></div>
                    <div class="fl" v-width="100">
                        <p class="musicName">{{item.musicName}}</p>
                        <p class="musicSinger">{{item.musicSinger}}</p>
                    </div>
                    <span class="iconfont icon-bofang fr"></span>
                </li>
            </ul>
            <footer>
                <span class="close iconfont icon-guanbi" @click="close"></span>
            </footer>
        </div>
    </div>
</template>
<script>
export default {
    props: ["player"],
    data() {
        return {
            isShowAudioPlayerList: false,
            currentTime: 0,
            duration: 0,
            isPlay: true,
            isAddClass: true,
            playState: 'all',
            isShowLyric: false,
            lyric: []
        }
    },
    computed: {
        playerIndex() {
            return this.$store.state.player.index
        },
        albumIndex() {
            return this.$store.state.player.albumIndex
        }
    },
    watch: {
        playerIndex() {
            var vm = this;
            $.get(this.player.album[this.playerIndex].musicLyric, function(data) {
                vm.lyric = vm.parseLyric(data)
            });
        },
        albumIndex() {
            var vm = this;
            $.get(this.player.album[this.playerIndex].musicLyric, function(data) {
                vm.lyric = vm.parseLyric(data)
            });
        }
    },
    methods: {
        goback() {
            this.$store.commit("HIDEPLAYER", {
                isShowPlayer: false
            })
        },
        showLyric() {
            var vm = this;
            this.isShowLyric = !this.isShowLyric;
            // 点击显示歌词
            $.get(this.player.album[this.playerIndex].musicLyric, function(data) {
                vm.lyric = vm.parseLyric(data)
            });
        },
        parseLyric(lyric) {
            var lines = lyric.split(/\n/);
            // 匹配时间的
            var getLyricTime = /\[\d{2}:\d{2}.\d{2}\]/g;
            var arr = [];
            while (!getLyricTime.test(lines[0])) {
                lines = lines.splice(1);
                // 得到有时间的歌词语句
            }
            //去掉最后的空行
            if (lines[lines.length - 1].length === 0) {
                lines.pop()
            }
            lines.forEach(function(item) {
                var index = item.indexOf("]");
                var time = item.substr(1, index - 1);
                var timeArr = time.split(":")
                var geci = item.substr(index + 1);
                arr.push([timeArr[0] * 60 + parseFloat(timeArr[1]), geci])
            });

            arr.sort((a, b) => {
                return a[0] - b[0]
            });
            console.log(arr);
            return arr
        },
        hideLyric() {
            this.showLyric()
        },
        changePlayState() {
            if (this.playState == 'all') {
                this.playState = 'random'
            } else if (this.playState == 'random') {
                this.playState = 'once'
            } else if (this.playState == 'once') {
                this.playState = 'all'
            }
        },
        goNext() {
            if (this.playerIndex < this.player.album.length - 1) {
                this.changeMusic(this.playerIndex + 1)
            } else {
                return
            }
        },
        goPrev() {
            if (this.playerIndex > 0) {
                this.changeMusic(this.playerIndex - 1)
            } else {
                return
            }
        },
        paused_played() {
            this.isPlay = !this.isPlay
            if (this.isPlay == true) {
                $("#audio")[0].play()

            } else if (this.isPlay == false) {
                $("#audio")[0].pause()
                this.isAddClass = true
            }
        },
        showAudioList() {
            this.isShowAudioPlayerList = !this.isShowAudioPlayerList
        },
        close() {
            this.showAudioList()
        },
        changeMusic(index) {
            if (this.player.albumIndex == null) {
                this.$store.commit("CHANGEMUSIC", {
                    index: index,
                    playerbg: this.player.album[index].playerbg,
                    albumImage: this.player.album[index].albumImage
                })
            } else if (typeof this.player.albumIndex == 'number') {
                this.$store.commit("CHANGEMUSIC", {
                    index: index,
                    playerbg: this.player.playerbg,
                    albumImage: this.player.albumImage
                })
            }
        },
        play() {
            this.currentTime = $("#audio")[0].currentTime
            this.duration = $("#audio")[0].duration

            if (!$("#audio")[0].paused && this.isAddClass) {
                // 如果是暂停 返回true
                this.isPlay = true
                this.isAddClass = false
            }
            if ($("#audio")[0].ended) {
                if (this.playState == 'all') {
                    this.goNext()
                } else if (this.playState == 'random') {
                    var randomIndex;
                    do {
                        randomIndex = ~~(Math.random() * this.player.album.length - 1);
                    } while (randomIndex == this.playerIndex);

                    this.changeMusic(randomIndex)
                } else if (this.playState == 'once') {
                    this.changeMusic(this.playerIndex)
                    $("#audio")[0].load()
                }
            }

            for (var i = 0; i < this.lyric.length - 1; i++) {
                if (this.currentTime > this.lyric[i][0]) {
                    $(".lyric ul").css({
                        "top": $(".lyric").height() / 2 - 26 * (i + 1)
                    });
                }
            }
        },
        goTime(event) {
            $("#audio")[0].currentTime = (event.offsetX / $(".duration").width()) * $("#audio")[0].duration;
        }
    },
    filters: {
        zhuanhuan(s) {
            var t;
            if (s > -1) {
                var min = Math.floor(s / 60) % 60;
                var sec = s % 60;
                if (min < 10) { t = "0"; }
                t += min + ":";
                if (sec < 10) { t += "0"; }
                t += ~~sec;
            }
            return t;
        }
    }
}

</script>
