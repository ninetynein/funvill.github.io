---
layout: post
title: Cakephp - Session->setFlash is not working any more. 
date: 2009-11-25 12:13
author: funvill
comments: true
categories: [cakephp, session, setflash, tips, Tips and Tricks, Web development]
---
<strong>Question:</strong>
<em>setFlash()</em> no longer showing up on the page. Why ?
<code>$this-&gt;Session-&gt;setFlash("Hello world");</code>

<strong>Answer</strong>
As of CakePHP version 1.2 you need to tell the template where to put the flash message

<code>&lt;?php
$session-&gt;check('Message.flash')) {
$session-&gt;flash();
}
?&gt;</code>
