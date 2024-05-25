cmake_minimum_required(VERSION 3.14)

set(PROJECT_NAME cmake_project_example) #set은 변수세팅 키워드. Project_Name 이라는 변수에  cmake_project_example 의 string 을 넣어준다.

set(CMAKE_CXX_STANDARD 17) #CMAKE 로 시작하는 변수는 전역변수이다. 컴파일 옵션등을 바꿀 때 사용됨. 여기서는 CXX(C++) StanDard 17을 사용한다는 말.


project(${PROJECT_NAME}) # ${} 중괄호 안에 변수 이름을 넣으면 변수에 저장된 값을 꺼내 쓸 수 있다. 그냥 Project_Name 을 넣으면 string 으로 들어감. project 키워드는 프로젝트를 실행한다는 말이다.

add_executable(${PROJECT_NAME} src/main.cpp) #${PROJECT_NAME} 이름으로 src/main.cpp 에 있는 모든 파일을 컴파일해서 실행파일로 만든다는 명령어이다.



#터미널에 cmake -Bbuild . -DCMAKE_BUILD_TYPE=Debug 로 vs실행파일 만듦.

# -B : 빌드 할 폴더를 지정 , build 라는 폴더가 생기고 그 안에 sln파일이 생김

# 그 뒤에 . 은 CMAKELIST.txt 의 루트 디렉토리를 지정해주는건데 .이 현재 디렉토리를 가리키니깐 따로 주소를 입력하지 않고 . 으로 지정해준다..



