---
layout: post
title:  "JAVASCRIPT HTML Element 생성"
date:   2020-04-08
categories: 코드
tags: html js
comments: 1
---
JAVASCRIPT HTML Element 생성

아래와 같은 DIV 요소가 있다. 
{% highlight html %}
<div id="box"></div>
{% endhighlight %}
<div id=box> 하위요소로<br>
<div id=menu> 요소를 만들고<br>
id=menu의 하위요소에 p태그를 만들고 그안에 rice라는 html을 삽입 하겠다.<br>

JavaScript :
{% highlight javascript %}
window.onload = function(){
    let box = document.getElementById('box');// box element 담아두기
    let menuElement = document.createElement('div'); // menu div 생성
    menuElement.id = 'menu'; // id를 menu로 지정
    box.appendChild(menuElement); // 박스의 자식요소로 menuElement를 삽입
    let riceElement = document.createElement('p'); // p 생성
    riceElement.innerHTML = 'rice'; // 생성된 p 태그에 rice를 삽입 
    menuElement.appendChild(riceElement)//menuElement의 자식요소로 생성된 p태그 삽입      
}
{% endhighlight %}

위의 자바스크립트가 실행되면 div만 있던 코드가 아래와 같이 변경된다
{% highlight html %}
<div id="box">
    <div id="menu">
      <p>rice</p>
    </div>
</div>
{% endhighlight %}

