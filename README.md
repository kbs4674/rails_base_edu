# Ruby on Rails Base For Education

## 1. 루비/레일즈 정보
* Ruby : 2.4.0
* Rails : 5.1.6
    

## 2. 인수인계 사항
* Gem : jquery-rails 설치
* Gem : Rails DB 설치
* Gem : Devise 설치
* 부트스트랩 V4.1 적용
* Scaffold 적용 (Post)
* 간단한 디자인 (홈페이지 메인, Scaffold:Post Index 등)
* Turbolinks 제거 (사유 : Jquery와의 충돌)


## 3. 첫 시작 (프로젝트 생성)
* 첫 레일즈 셋팅 (C9에서 Ruby on Rails Tutorial 프로젝트를 선택하세요.)
    ```
    git init
    rm -rf README.md
    git remote add origin https://github.com/kbs4674/rails_base_edu
    git pull origin master
    gem install rails --version=5.1.6
    gem update --system
    bundle install
    rake db:drop;rake db:migrate;rake db:seed
    rails s -b $IP -p $PORT
    ```


## 4. Ruby on Rails 간단 설명
* 이론
    * Ruby on Rails은 Ruby 기반의 웹 프레임워크임. (Python의 Django 혹은 Java의 Spring 같은 개념)
    * Ruby on Rails은 MVC 패턴으로 이루어져 있으며, 디자인 작업은 보통 V(View)에서 이루어짐
        * M : Model(DB 및 DB 관계를 다룸) / V : View (페이지를 다루며, HTML/CSS/Javascript/Rails 코드와 병합되어 사용) / C : Controller (DB를 어떻게 처리할건지 관리)
    * Javascript, CSS는 ```app/assets/javascript``` 혹은 ```app/assets/stylesheets```에 넣어두면 됨.
        * ```<script src="...">``` 혹은 ```<link rel="...">```을 정의하지 않아도 알아서 적용됨.
        * 캐싱에 영향을 안받음. (F12로 보면 파일 이름 뒤에 난수가 붙는걸 확인 가능)
    * ```<%= ... %>``` 혹은 ```<% ... %>```은 레일즈 코드임.
    * ```<%= render '...' %>```은 ```'...'``` 위치의 View를 불러오는 역할을 맡음 (Default : ```app/views/```)
    * 모든 View에 있어 공통적으로 보여지는 View(예 : 상단 메뉴, 기본 글꼴 style) ```app/views/layouts/application.html.erb``` 
    * 홈페이지 View 코드 수정은 ```app/views/(모델명)``` 에서 이루어짐.<br/><br/>
    * Ruby on Rails에는 크게 3가지 모드가 존재함 : Development, Test, Production
        * Development : 주로 개발용 모드로서 오류를 일으킬 시 오류메세지 및 디버그를 알려줌.
        * Production : 서비스를 릴리즈할 때 쓰이는 모드로서, 링크를 잘못 입력하거나 오류 발생 시 404 에러페이지 혹은 500 에러페이지로 리다이렉트 시킴.
            * 404 혹은 505 페이지 view는 ```public``` 폴더 안에 있음.

* 명령어 및 위치 모음
    * 서버 ON 명령어 : ```rails s -b $IP -p $PORT```
    * DB추가, 애트리뷰트 추가 등으로 인한 업데이트 시( 기존의 데이터 삭제) : ```rake db:drop;rake db:migrate```
    * 미리 입력된 DB 불러오기(app/db/seeds.rb) ```rake db:seed```


## 5. 알아두면 좋은 사이트
* 코딩 지식인 - Stackoverflow <a href="http://stackoverflow.com" target="_blank">클릭</a>
* Rails Gem 추천 사이트 <a href="https://www.ruby-toolbox.com/" target="_blank">클릭</a>
* Rails 사용설명 블로그 <a href="http://blog.naver.com/kbs4674" target="_blank">클릭</a>