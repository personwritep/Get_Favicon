// ==UserScript==
// @name        Get Favicon 🔵
// @namespace        http://tampermonkey.net/
// @version        0.8
// @description        各種のサイトでファビコンを取得 「F2」でポップアップを表示
// @author        You
// @match        https://*/*
// @exclude        https://blog.ameba.jp/ucs/entry/srventry*
// @noframes
// @grant        none
// @updateURL        https://github.com/personwritep/Get_Favicon/raw/main/Get_Favicon.user.js
// @downloadURL        https://github.com/personwritep/Get_Favicon/raw/main/Get_Favicon.user.js
// ==/UserScript==



if(!location.hostname.includes('example.com')){
    let popup;

    window.addEventListener('keydown', check_key);
    function check_key(event){
        if(event.keyCode==113){ // ショートカット「F2」
            event.preventDefault();
            event.stopImmediatePropagation();
            let left_p=screen.width -340;
            let win_apper='left='+ left_p +',  top=100, width=240, height=290';
            let exam_q='https://example.com/?'+ location.href;

            if(!popup){
                popup=window.open(exam_q, null , win_apper); }
            else{
                popup.close();
                popup=window.open(exam_q, null , win_apper); }
        }}}



if(location.hostname.includes('example.com')){ // ファビコン取得ウインドウ
    env();
    let page_location=get_query(); // 目的ページのURL
    main(page_location); }



function env(){
    let head=document.head;
    if(head){
        let lang='<meta http-equiv="Content-Language" content="ja">';
        head.insertAdjacentHTML('beforeend', lang);

        let pre_style=head.querySelector('style');
        if(pre_style){
            pre_style.remove(); }}

    let pre_div=document.querySelector('body > div');
    if(pre_div){
        pre_div.remove(); }}



function get_query(){
    let query=window.location.search.slice(1); // 文頭?を除外
    return query; }



function main(page_location){
    let fav_request; // ファビコンを取得するためのURL
    let f_size; // ファビコンの指定サイズ
    let back=0; // パネル背景色の黒白


    fav_request=
        'https://t1.gstatic.com/faviconV2?client=SOCIAL'+
        '&type=FAVICON&fallback_opts=TYPE,SIZE,URL&url='+ page_location;


    let help_url='https://ameblo.jp/personwritep/entry-12860094754.html';

    let GF_help=
        '<a href="'+ help_url +'" target="_blank" rel="noopener noreferrer">'+
        '<svg id="gf_help" viewBox="0 0 150 150">'+
        '<path d="M66 13C56 15 47 18 39 24C-12 60 18 146 82 137C92 135 '+
        '102 131 110 126C162 90 128 4 66 13M68 25C131 17 145 117 81 125C16 '+
        '133 3 34 68 25M69 40C61 41 39 58 58 61C66 63 73 47 82 57C84 60 '+
        '83 62 81 65C77 70 52 90 76 89C82 89 82 84 86 81C92 76 98 74 100 66'+
        'C105 48 84 37 69 40M70 94C58 99 66 118 78 112C90 107 82 89 70 94z">'+
        '</path></svg></a>';


    let ifr=
        '<div class="fav_div">'+
        '<div class="fav_frame">'+
        '<img alt="" src='+ fav_request +'></div>'+
        '<div id="fav_menu">'+
        'Back：<input id="back_color" type="submit" value=" ">'+
        'Size：<input id="fav_size" type="number" min="4" max="256" step="4">'+
        GF_help +
        '</div>'+

        '<style>.fav_div { position: fixed; top: 0; left: 0; z-index: 1; '+
        'width: 100vw; height: 100vh; overflow: hidden; background: #000; } '+
        '.fav_frame { display: flex; justify-content: center; width: 240px; height: 240px; '+
        'overflow: hidden; } '+
        '.fav_frame img { align-self: center; } '+
        '#fav_menu { width: 100%; padding: 10px 0; color: #000; text-align: center; '+
        'font: normal 16px/24px Meiryo; letter-spacing: 0; '+
        'border-top: 1px solid #666; background: #fff; } '+

        '#fav_menu input { display: revert; box-sizing: border-box; min-width: unset; '+
        'font: normal 16px/24px Meiryo; letter-spacing: 0; '+
        'outline: none; box-shadow: unset; appearance: auto; transform: none; } '+
        '#back_color { width: 30px; height: 30px; margin-right: 8px; padding: 0; '+
        'vertical-align: 1px; '+
        'border: 1px solid #666; border-radius: 3px; background: #000; cursor: pointer; } '+
        '#fav_size { width: 60px; height: 30px; margin: 0; padding: 2px 2px 0; '+
        'vertical-align: 0; text-align: center; color: #000; '+
        'border: revert; border-radius: revert; background: revert; } '+
        '#fav_size::-webkit-inner-spin-button { -webkit-appearance: auto; } '+
        '#gf_help { height: 18px; width: 18px; margin: 0 0 -4px 8px; padding: 0; fill: #777; '+
        'vertical-align: 0; cursor: pointer; display: inline; }'+
        '</style></div>';

    if(!document.querySelector('.fav_div')){
        document.body.insertAdjacentHTML('beforeend', ifr); }


    setTimeout(()=>{
        let fav_size=document.querySelector('#fav_size');
        if(fav_size){
            fav_size.value=test_size(0);
            f_size=fav_size.value; }
    }, 800);



    get_favicon();
    clicked_focus();
    back_color_set();



    function scan(f_size){
        let que=fav_request.split('&');
        if(que[que.length-1] && que[que.length-1].indexOf('size=')==0){
            que.pop();
            fav_request=que.join('&') +'&size='+ f_size; }
        else{
            fav_request=fav_request +'&size='+ f_size; }

        let fav_frame=document.querySelector('.fav_frame');
        if(fav_frame){
            fav_frame.innerHTML='<img alt="" src='+ fav_request +'>'; }

    } // scan(f_size)


    function test_size(n){
        let img=document.querySelector('.fav_frame img');
        if(img){
            let img_width=img.getBoundingClientRect().width;
            if(n==1){
                if(img_width && img_width>16){
                    return Math.round(img_width); }} // 24px以上のファビコンが取得できたらサイズを返す
            else{
                if(img_width){
                    return Math.round(img_width); }} // ファビコンが取得できたら サイズを返す

        }} // test_size(n)



    function get_favicon(){
        let fav_size=document.querySelector('#fav_size');
        if(fav_size){
            let interval;

            fav_size.addEventListener('keydown', (event)=>{

                if(event.keyCode==13){
                    event.preventDefault();
                    event.stopImmediatePropagation();

                    if(event.shiftKey || event.ctrlKey){ //「Shift+Enter」「Ctrl+Enter」
                        scan(256);
                        setTimeout(()=>{
                            if(test_size(1)){
                                fav_size.value=test_size(1);
                            }
                        }, 200); }
                    else{ //「Enter」
                        f_size=fav_size.value;
                        scan(f_size);
                        setTimeout(()=>{
                            fav_size.value=test_size(0);
                        }, 200); }}

                else if(event.keyCode==38){ //⇧
                    event.preventDefault();
                    let f_size_d=fav_size.value/1;
                    f_size=f_size_d - f_size_d%8; // 8の整数倍
                    if(15<f_size && f_size<257){
                        scan_up(); }
                    else if(f_size<16){
                        f_size=16;
                        scan(f_size);
                        setTimeout(()=>{
                            fav_size.value=test_size(0);
                        }, 200); }}

                else if(event.keyCode==40){ //⇩
                    event.preventDefault();
                    let f_size_d=fav_size.value/1;
                    f_size=f_size_d - f_size_d%8; // 8の整数倍
                    if(25<f_size && f_size<257){
                        scan_down(); }
                    else if(f_size==24){
                        f_size=16;
                        scan(f_size);
                        setTimeout(()=>{
                            fav_size.value=test_size(0);
                        }, 200); }
                    else if(f_size==16){
                        f_size=12;
                        scan(f_size);
                        setTimeout(()=>{
                            fav_size.value=test_size(0);
                        }, 200); }}

            }); // keydown


            function scan_up(){
                clearInterval(interval);
                interval=setInterval(wait_img_up, 200);

                function wait_img_up(){
                    f_size +=8;

                    if(f_size>256){ // スキャン最大サイズ制限
                        f_size=256;
                        setTimeout(()=>{
                            if(test_size(0)){
                                fav_size.value=test_size(0); }
                        }, 200);
                        clearInterval(interval); }

                    fav_size.value=f_size;
                    scan(f_size);
                    setTimeout(()=>{
                        if(test_size(1)){
                            fav_size.value=test_size(1);
                            clearInterval(interval); }
                    }, 180); }

            } // scan_up()


            function scan_down(){
                clearInterval(interval);
                interval=setInterval(wait_img_down, 200);

                function wait_img_down(){
                    f_size -=8;

                    if(f_size<25){ // スキャン最大サイズ制限
                        f_size=24;
                        scan(f_size);
                        setTimeout(()=>{
                            fav_size.value=test_size(0);
                        }, 200);
                        clearInterval(interval); }

                    fav_size.value=f_size;
                    scan(f_size);
                    setTimeout(()=>{
                        if(test_size(1)){
                            fav_size.value=test_size(1);
                            clearInterval(interval); }
                    }, 180); }

            } // scan_down()

        } // if(fav_size)
    } // get_favicon()



    function clicked_focus(){
        let fav_div=document.querySelector('.fav_div');
        let fav_size=document.querySelector('#fav_size');
        if(fav_div && fav_size){
            fav_div.onclick=function(){
                fav_size.focus(); }}}



    function back_color_set(){
        let fav_div=document.querySelector('.fav_div');
        let back_color=document.querySelector('#back_color');
        if(fav_div && back_color){
            back_color.onclick=()=>{
                if(back==0){
                    back=1;
                    fav_div.style.background='#fff';
                    back_color.style.background='#fff'; }
                else{
                    back=0;
                    fav_div.style.background='#000';
                    back_color.style.background='#000'; }}}

    } // back_color_set()

} // main()
