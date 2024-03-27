FROM ubuntu:latest
# 가져오기

RUN apt-get update && apt-get install -y -q nginx
#패키지 설치

COPY index.html /usr/share/nginx/html
#copy시 파일시스템에 변화되고, 적는만큼 이런거 하나하나가 이미지 레이어가 됨

CMD ["nginx", "-g", "daemon off;"]
# 컨테이너 안에 들어가는 프로세서는 포그라운드로 꼭 돌리기

