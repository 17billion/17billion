---
layout: post
title:  "Github와 연동하여 Jekyll 프로젝트 호스팅하기"
date:   2017-05-27 09:51:42 +0900
categories: Jekyll github
---

> **Jekyll**과 **Github**를 연동하여 자신의 프로젝트 페이지나 블로그, 웹사이트를 무료로 GitHub에 호스팅을 할 수 있습니다. <br>
 이번 글에서는 지난번에 생성한 로컬의 Jekyll 프로젝트를 Github를 이용하여 호스팅하는 것까지 알려드리겠습니다.
 
> 아래 설명 중 Command Console은 대부분 Git Bash를 설치하여 진행했으며 <br>
> $ .. 부분의 명령어를 실행하여 진행해주시면 됩니다.

 
#### 1. github 가입 (<https://github.com/>)
![1_signup_github](/images/Jekyll_github/1_signup_github.jpg)
#### 1-2. public repository 선택 후 Continue 클릭 (private repository는 유로)
![1_2_signup_github](/images/Jekyll_github/1_2_signup_github.jpg)
#### 1-3. 사용자 정보 기입 (기입을 원하지 않을 경우 아래 skip the step 클릭)
![1_3_signup_github](/images/Jekyll_github/1_3_signup_github.jpg)
#### 1-4. 가입 완료
![1_4_signup_github](/images/Jekyll_github/1_4_signup_github.jpg)
#### 1-5. 가입할때 입력한 E-mail에 로그인하여 인증 (Verify email address 클릭)
![1_5_signup_github_email](/images/Jekyll_github/1_5_signup_github_email.jpg)
#### 2. repository 생성
##### repository name을 원하는 name으로 입력 후 Create repository 클릭 (private는 유료)
![2_make_github_repository](/images/Jekyll_github/2_make_github_repository.jpg)
#### 3. 로컬에 있는 Jekyll 프로젝트를 생성한 github repository로 commit 후 push
##### 중간에 인증을 위해 로그인 화면이 나타나는데 가입한 정보로 로그인해주면 됩니다.
##### 저는 Jekyll 프로젝트를 Jekyll_site/17billion에 생성했었습니다. 아래 과정은 각자 생성한 프로젝트에서 진행해주시면 됩니다.
> $ cd /c/Jekyll_site/17billion
> $ git init
```
Initialized empty Git repository in C:/Jekyll_site/17billion/.git/
```
> $ git remote add origin https://github.com/17billion/17billion.github.io.git <br>
> $ echo "# 17billion" >> README.md <br>
> $ git init
```
Reinitialized existing Git repository in C:/Jekyll_site/17billion/.git/
```
> $ git add README.md
```
warning: LF will be replaced by CRLF in README.md.
The file will have its original line endings in your working directory.
```
> $ git commit -m "first commit"
```
[master (root-commit) 528fa52] first commit
 8 files changed, 174 insertions(+)
 create mode 100644 .gitignore
 create mode 100644 Gemfile
 create mode 100644 Gemfile.lock
 create mode 100644 README.md
 create mode 100644 _config.yml
 create mode 100644 _posts/2017-05-03-welcome-to-Jekyll.markdown
 create mode 100644 about.md
 create mode 100644 index.md
```
> $ git remote add origin https://github.com/17billion/17billion.git
```
fatal: remote origin already exists.
```
> $ git push -u origin master
```
Counting objects: 11, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (9/9), done.
Writing objects: 100% (11/11), 3.48 KiB | 0 bytes/s, done.
Total 11 (delta 0), reused 0 (delta 0)
Branch master set up to track remote branch master from origin.
To https://github.com/17billion/17billion.git
 * [new branch]      master -> master
```
##### 아래는 제가 진행했을때의 git bash 화면입니다. (중간에 인증을 위해 로그인을 하는 과정이 있습니다.)
![3_github_Jekyll_commit](/images/Jekyll_github/3_github_Jekyll_commit.jpg)

#### 3. push 된 Jekyll 프로젝트 확인
![3_2_github_Jekyll_commit](/images/Jekyll_github/3_2_github_Jekyll_commit.jpg)

#### 4. 호스팅된 주소로 접속확인 (https://{Owner}.github.io/{Repository Name})
![4_end_github_Jekyll_conn](/images/Jekyll_github/4_end_github_Jekyll_conn.jpg)

 
[Jekyll-docs]: https://Jekyllrb.com/docs/home
[Jekyll-gh]:   https://github.com/Jekyll/Jekyll
[Jekyll-talk]: https://talk.Jekyllrb.com/
