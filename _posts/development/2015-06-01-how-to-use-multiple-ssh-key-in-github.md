---
layout: page
sidebar: no
subheadline: Tip
title:  "Github 에서 여러 계정의 ssh 인증을 사용하는 방법"
teaser:
header: no
tags:
    - github
    - ssh
categories:
    - development
comments: true
breadcrumb: true
---
Github 에서 여러개의 계정을 사용할 경우에는 키체인을 이용한 https 인증을 사용하기 어렵습니다.
이럴 경우에 여러개의 ssh 키를 사용함으로써 여러개의 계정을 동시에 사용할 수 있습니다.
일단 [ssh 키](https://help.github.com/articles/generating-ssh-keys/)를 만들고 Github계정에 등록을합니다.
Github은 서로 다른 계정에 똑같은 키를 사용하는것을 허용하지 않으므로 두개의 키를 생성해야 합니다.
각각의 키 이름을 `~/.ssh/id_rsa_foo`, `~/.ssh/id_rsa_bar` 라고 합시다.

`vi` 등을 사용하여 `~/.ssh/config` 파일을 생성합니다.

~~~
# Default account
Host github.com
    User git
    IdentityFile ~/.ssh/id_rsa_foo
# 두번째 계정의 인증서
Host github.com-bar
    User git
    IdentityFile ~/.ssh/id_rsa_bar
~~~

이제 repository를 클론할때나 remote를 지정해줄때 도메인 네임을 `github.com` 대신에 ssh config에서 지정한 호스트 네임인 `github.com-bar` 를 사용하면 두번째 키를 이용하여 인증을 하게 됩니다.
예를들어,

```
git clone git@github.com-bar:bar/testrepo.git testrepo
```

로 클론을 하면 bar의 인증을 사용하게 됩니다.


## Other Post Formats
{: .t60 }
{% include list-posts.html tag='development' %}
