## 리눅스 명령어

1. pwd
- 현재 작업중인 디렉토리 정보 출력
- 사용예시
: pwd

2. ls
- 현재 디렉토리 목록 확인
- -a로 숨겨진 파일이나 디렉토리를 볼 수 있음
- -l로 자세한 내용을 출력
- 사용예시
: ls, ls -l, ls -a, ls -al


3. cd
- 경로 이동
- 사용예시
: cd .. (상위 폴더로 이동)
: cd /home, cd/home/etc 

4. mkdir/rmdir
- 디렉토리 생성/제거
- -p 옵션으로 하위 디렉토리까지 생성 가능(mkdir -p dir1/dir2)
- -m 옵션으로 생성시 모드까지 지정 가능(mkdir -m 700 testdir)
- 사용예시
: mkdir testdir
: rmdir testdir

5. ps
- 현재 실행중인 프로세스 목록과 상태를 보여줌
- 사용예시
: ps [option]

6. kill
- 실행중인 프로세스를 죽일 때 사용
- 사용예시
: kill [options] [pid(프로세스 id)]
: kill -3 [pid] (해당 프로세스 종료. 보통 사용되지 않으며 덤프 파일을 남김)
: kill -9 [pid] (해당 프로세스 강제종료. 저장되지 않은 데이터는 소멸. 프로세스가 무시 불가)
: kill -15 [pid] (해당 프로세스 종료. 메모리상의 데이터와 기타 파일을 저장 후 프로세스 종료. 프로세스가 무시 가능)

7. touch
- 파일이나 디렉토리의 최근 업데이트 일자를 현재 시간으로 변경. 존재하지 않을 경우 빈 파일을 만듦
- 사용예시
: touch testfile1

8. cp
- 파일 혹은 디렉토리 복사. 디렉토리 복사시 -r 옵션
- 사용예시
: cp testfile1 testfile_cp, 
: cp -r testdir testdir_cp

9. mv
- 파일 혹은 디렉토리 이동 or 이름 변경
- 사용예시
: mv file1 file2 (file1의 이름을 file2로 변경)
: mv file1 dir1/ (file1을 dir1 디렉토리로 이동)
: mv file1 file2 dir1/ (file1, file2를 동시에 dir1로 이동)
: mv dir1 dir2 (dir1의 이름을 dir2로 변경)

10. wget
- Web GET의 약어로 웹 상의 파일을 다운로드 할 때 사용
- 사용예시
: wget [download Url] (해당 url의 )

11. find
- 특정 파일이나 디렉토리를 검색
- 사용예시
: find [검색경로] -name [파일명]
: find ./ -name 'file1'
: find ./ -name "*.jpg" (확장자가 jpg인 것을 모두 찾음)*
: find ./ -name "*.jpg" -exec rm {} \;  (확장자가 .jpg인 것을 찾고 모두 제거)*
: find ./ -type d (디렉토리만 탐색), find ./ -type f(파일만 탐색)

12. grep
- 파일 내 특정 문자열 찾기
- 사용예시
: grep [옵션][패턴][파일명]
: grep 'test' 파일명 (특정 파일에서 'test' 문자열 찾기)
: grep 'test' 파일명1 파일명2 (여러 파일에서 'test' 문자열 찾기)
: grep 'test' * (현재 디렉토리의 모든 파일에서 'test' 문자열 찾기)
: grep 'test' *.log (특정 확장자를 가진 모든 파일에서 'test'문자열 찾기)*
: grep '^[ab]' 파일명 (특정 파일에서 문자열이 포함된 행을 찾음)
: grep 'a*' 파일명 (특정 파일에서 a로 시작하는 모든 단어를 찾음)
- 정규식을 사용하거나 옵션을 사용하는 경우가 많아 여기까지 작성

13. clear
- 터미널의 내용을 모두 지움
- 사용예시
: clear

14. echo
- 텍스트나 문자열을 보여줌
- 사용예시
: echo [옵션] [string]
: echo "teststring"

15. sudo
- 현재 계정에서 root 권한을 이용하여 명령어를 실행할 때 사용. 실행하기 전 현재 사용자의 비밀번호를 요구
- 사용예시
: sudo apt-get update 

16. su
- 현재 계정을 로그아웃 하지 않고 다른 계정으로 전환
- 사용예시
: su (root 사용자로 변경. root 암호 입력 필요)
: su user1 (user1으로 사용자 변경)
: su - user1 (다른 사용자로 변경하며 환경변수까지 적용)

17. whoami
- 현재 사용자 출력
- 사용예시
: whoami

18. logout(or exit)
- 이전 계정으로 돌아옴
- 사용예시
: logout (or exit)

19. sort
- 입력된 내용을 정렬하는 명령어(옵션없이 실행시 오름차순. -r시 내림차순, -f시 대소문자 구분 x, -b시 공백 무시)
- 사용예시  
: sort input.txt (input.txt의 내용을 정렬)

20. chmod
- 파일, 디렉토리의 권한(읽기r, 쓰기 w, 실행 x) 변경
- 사용예시
: chmod [숫자] file.txt 
: 세 자리 숫자가 들어가며, 앞에서 부터 사용자, 그룹, 다른 사용자의 권한을 의미
: rwx를 이진법으로 나타내며 모든 권한 허용시 7, 모든 권한 비허용시 0, 읽기만 허용시 4, 이런 식으로 이진법으로 나타낸다.
: chmod 000 file.txt (사용자, 그룹, 다른 사용자의 모든 권한을 제거)
: chmod 777 file.txt (사용자, 그룹, 다른 사용자의 모든 권한 추가)
: chmod 700 file.txt (사용자에게만 모든 권한 부여)

21. tar
- 여러 개의 파일을 하나의 파일로 묶거나 풀 때 사용
- 사용예시
: tar -cvf [파일명.tar] [폴더명] (해당 폴더를 파일명.tar로 압축)
: tar -xvf [파일명.tar] (파일명.tar 파일을 압축풀기)
: tar -zcvf [파일명.tar] [폴더명] (해당 폴더를 파일명.tar.gz로 압축)
: tar -zxvf [파일명.tar] (파일명.tar.gz 파일을 압축풀기)

22. cat
- 단순히 파일의 내용을 출력하거나 파일 여러개를 합쳐 하나의 파일을 만들거나, 기존 파일에 내용 덧붙이기도 가능
- 사용예시
: cat file1 (단순 출력)
: cat file1 file2 > file1_2(새로운 파일 생성) 
: cat file1 >> file2(file2에 file1내용 붙이기)

23. head
- 파일의 앞부분을 보고싶은 줄 수 만큼 보여줌(미지정시 상위 10줄)
- 사용예시
: head -3 testfile, head testfile

24. tail
- 파일의 뒷부분을 보고싶은 줄 수 만큼 보여줌(미지정시 하위 10줄)
- 사용예시
: tail -3 testfile, tail testfile

25. man (--help로 대체 가능(간단한 사용법))
- 명령어의 메뉴얼을 알려줌
- man [명령어 종류]
- 사용 예시
: man rm (rm 명령어의 메뉴얼을 확인)


## ELF?
#### elf란?
- ELF는 리눅스 시스템에서 사용되는 중요 실행 파일 형식이다.  
- 사용자 어플리케이션, 공유 라이브러리, 커널 모듈, 커널 자체 모두 ELF 형식으로 저장된다. 
#### 형태
![image](https://user-images.githubusercontent.com/70579655/156350562-9f1618dd-fc16-447d-8734-b283d8a0cc0a.png)

