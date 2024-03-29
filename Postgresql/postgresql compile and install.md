# Postgresql source 코드 컴파일 및 설치

## 0. postgresql 제거
  * 기존에 package를 이용해 설치한 postgresql을 제거한다.
    ```
    $ sudo apt purge postgresql postgresql-contrib
    ```
    <br><img src="https://github.com/RainingCodes/Industry-Academic-Cooperation1/blob/main/img/img73.JPG" width="300px" height="90px" alt="purge postgresql"><br/>

## 1. source 코드 다운로드 & 컴파일
  * https://www.postgresql.org/ftp/source/v15.1/ 에 접속해서 postgresql-15.1.tar.gz 다운로드
<br><img src="https://github.com/RainingCodes/Industry-Academic-Cooperation1/blob/main/img/img71.JPG" width="800px" height="750px" alt="source download"><br/>

  * 압축 해제
  <br><img src="https://github.com/RainingCodes/Industry-Academic-Cooperation1/blob/main/img/img74.JPG" width="300px" height="200px" alt="tar"><br/>

  * 폴더 이동 후 configure
  ```
  $ mv postgresql-15.1 ..
  $ cd ~/postgresql-15.1
  $ ./configure
  ```
 <img src="https://github.com/RainingCodes/Industry-Academic-Cooperation1/blob/main/img/img75.JPG" width="480px" height="400px" alt="configure"><br/>

  * error 확인
  <br><img src="https://github.com/RainingCodes/Industry-Academic-Cooperation1/blob/main/img/img72.JPG" width="600px" height="200px" alt="first error"><br/>

  * readline 설치
  ```
  $ sudo apt install libreadline-dev
  ``` 
  <img src="https://github.com/RainingCodes/Industry-Academic-Cooperation1/blob/main/img/img72.JPG" width="600px" height="350px" alt="install readline"><br/>

  * configure 후 생기는 두 번째 error 확인
  ```
  $ ./configure
  ```
   <img src="https://github.com/RainingCodes/Industry-Academic-Cooperation1/blob/main/img/img76.JPG" width="600px" height="350px" alt="second error"><br/>
  * zlib 설치
  ```
  $ sudo apt-get install zlib1g-dev
  ```
  <img src="https://github.com/RainingCodes/Industry-Academic-Cooperation1/blob/main/img/img77.JPG" width="600px" height="350px" alt="install zlib"><br/>

  * configure 성공
  ```
  $ ./configure
  ```
<img src="https://github.com/RainingCodes/Industry-Academic-Cooperation1/blob/main/img/img78.JPG" width="600px" height="450px" alt="configure completed"><br/>

  * make
  ```
  $ make
  ```
  <img src="https://github.com/RainingCodes/Industry-Academic-Cooperation1/blob/main/img/img79.JPG" width="600px" height="450px" alt="make"><br/>
  