# about_Terminal_command
***
## 파일 및 디렉토리 관리
- ls : 현재 디렉토리의 파일과 디렉토리 목록을 나열한다.
    ```
    ls             # 현재 디렉토리 파일/디렉토리 목록
    ls -l          # 상세 정보 (파일 권한, 크기, 수정 날짜 등)
    ls -a          # 숨김 파일 포함 목록
    ```
- cd : 디렉토리 이동 (Change Directory)
    ```
    cd /path/to/directory   # 절대 경로로 이동
    cd ..                   # 상위 디렉토리로 이동
    cd ~                    # 홈 디렉토리로 이동
    cd -                    # 마지막 디렉토리로 이동
    ```
- pwd : 현재 작업 중인 디렉토리의 절대 경로 출력 (Print Working Directory)
    ```
    pwd   # 현재 디렉토리 경로 출력
    ```
- mkdir : 새 디렉토리 생성
    ```
    mkdir new-directory     # 새 디렉토리 생성
    mkdir -p path/to/dir    # 상위 디렉토리가 없으면 함께 생성
    ```
- rmdir : 빈 디렉토리 삭제
    ```
    rmdir directory-name    # 빈 디렉토리 삭제
    ```
- rm : 파일 삭제
    ```
    rm file-name            # 파일 삭제
    rm -r directory-name    # 디렉토리 삭제 (디렉토리 내부의 파일 포함)
    rm -f file-name         # 강제로 파일 삭제 (경고 없이)
    rm -rf directory-name   # 강제로 디렉토리 및 그 안의 모든 파일 삭제
    ```
- cp : 파일 복사
    ```
    cp file1.txt file2.txt     # 파일 복사
    cp -r dir1 dir2            # 디렉토리 복사
    ```
- mv : 파일/디렉토리 이동 또는 이름 변경 
    ```
    mv old-name.txt new-name.txt   # 파일 이름 변경
    mv file.txt /path/to/directory # 파일 이동
    ```
- touch: 새로운 빈 파일 생성
    ```
    touch newfile.txt           # 새로운 빈 파일 생성
    ```

## 파일 내용 보기 및 편집
- cat: 파일의 내용을 출력
    ```
    cat file.txt            # 파일 내용 출력
    ```
- less: 파일 내용을 페이지 단위로 보기 (스크롤 가능)
    ```
    less file.txt           # 파일 내용 페이지 단위로 보기
    ```
- head: 파일의 첫 몇 줄 출력
    ```
    head file.txt           # 파일의 처음 10줄 출력
    head -n 20 file.txt     # 파일의 처음 20줄 출력
    ```
- tail: 파일의 마지막 몇 줄 출력
    ```
    tail file.txt           # 파일의 마지막 10줄 출력
    tail -n 20 file.txt     # 파일의 마지막 20줄 출력
    ```
- nano, vim, vi: 텍스트 파일 편집기
    ```
    nano file.txt           # nano 편집기 열기
    vim file.txt            # vim 편집기 열기
    vi file.txt             # vi 편집기 열기
    ```

## 프로세스 및 시스템 관리
- ps: 현재 실행 중인 프로세스 보기
```
ps           # 현재 쉘에서 실행 중인 프로세스
ps aux       # 모든 사용자와 모든 프로세스 보기
ps -ef       # 전체 프로세스 정보 출력
```
- top: 실시간 시스템 리소스 사용량과 프로세스 상태 보기
```
top          # 실시간 CPU, 메모리 사용 상태 확인
```
- kill: 프로세스 종료
```
kill 1234    # PID가 1234인 프로세스를 종료
kill -9 1234 # 강제로 프로세스 종료 (SIGKILL)
```
- df: 파일 시스템의 디스크 공간 사용 상태 보기
```
df           # 전체 파일 시스템의 디스크 사용 현황
df -h        # 사람이 읽기 쉬운 형태로 디스크 사용 현황 (GB, MB 등)
```
- free: 시스템의 메모리 사용 현황 보기
```
free         # 메모리 사용 상태 확인
free -h      # 사람이 읽기 쉬운 형태로 메모리 사용 현황
```
- uptime: 시스템 부팅 이후 경과 시간 및 시스템 부하 확인
```
uptime       # 시스템의 현재 시간, 부팅 시간, 부하 상태 표시
```

## 네트워크 관련 명령어
- ping: 네트워크 연결 확인
```
ping google.com         # google.com에 ping 요청
ping 192.168.1.1        # IP 주소에 ping 요청
```
- ifconfig: 네트워크 인터페이스 정보 보기 (보통 리눅스에서 사용)
```
ifconfig     # 네트워크 인터페이스 정보 출력
```
- ip: 네트워크 인터페이스 및 라우팅 테이블 관리
```
ip a         # IP 주소 및 네트워크 인터페이스 정보
ip route     # 라우팅 테이블 확인
```
- curl: 서버와 HTTP 요청/응답 테스트
```
curl http://example.com   # 웹사이트 접속 (응답 내용 출력)
curl -O http://example.com/file.zip   # 파일 다운로드
```

## 파일 압축 및 압축 해제
- tar: 파일 압축 및 압축 해제
```
tar -czvf archive.tar.gz directory/     # 디렉토리 압축 (gzip)
tar -xzvf archive.tar.gz                # gzip 압축 파일 해제
```
- zip: ZIP 파일 생성 및 압축 해제
```
zip archive.zip file1.txt file2.txt    # 파일을 ZIP으로 압축
unzip archive.zip                      # ZIP 파일 압축 해제
```
- gzip: GZIP 파일 압축
```
gzip file.txt           # file.txt 파일을 .gz로 압축
gunzip file.txt.gz      # .gz 파일 압축 해제
```

## 기타
- man: 명령어의 매뉴얼 페이지 보기
```
man ls         # ls 명령어의 매뉴얼 페이지
man tar        # tar 명령어의 매뉴얼 페이지
```
- history: 이전에 입력한 명령어 목록 보기
```
history       # 이전에 입력한 명령어 목록
```
- clear: 터미널 화면 지우기
```
clear         # 터미널 화면을 깨끗하게 지운다
```
