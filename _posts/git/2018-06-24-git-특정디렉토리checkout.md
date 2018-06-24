---
layout: post
title:  "git 특정 디렉토리 checkout"
date: 2018-06-24 16:48:00
comments: true
categories: git
---
<br/>

#### 1. git 저장소 생성
<pre><code>git init my-proj
cd my-proj

</code></pre>
<br/>

#### 2. core.sparseCheckout 옵션 추가
<pre><code>git config core.sparseCheckout true
</code></pre>
<br/>

#### 3. git remote 추가
<pre><code>git remote add -f origin {REMOTE_URL}
</code></pre>
<br/>

#### 4. checkout(clone)할 파일 or 디렉토리를 sparse-checkout 파일에 작성
<pre><code>echo "project/myDirectory" >> .git/info/sparse-checkout
</code></pre>
<br/>

#### 5. pull!
<pre><code>git pull origin master
</code></pre>
<br/>

---

#### Ref
https://www.lesstif.com/pages/viewpage.action?pageId=20776761

