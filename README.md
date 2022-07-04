# 별도의 설치 없이 가능한 한글 C언어
별도의 설치없이 한글로 코딩해보세요
이 프로젝트는 나무위키에서 영감을 받아 2일만에 만들어졌습니다
3분의 2는 잠과 먹는것에 사용했다는건 안비밀입니다.

# 튜토리얼
## 코드
```
int -> 정수
char -> 문자
printf -> 출력
return -> 반환
main -> 진입점
auto -> 자동
break -> 반복문끝
auto -> 자동
break -> 반복문끝
case -> 선택지
const -> 변함없는
continue -> 진행
default -> 기본
else -> 아니면
enum -> 열거형
extern -> 타파일전역변수
float -> 실수형
for -> 위해
goto -> 이동
if -> 만일
inline -> 인라인
long -> 긴
register -> 등록
restrict -> 제한
return -> 돌아가
short -> 짧다
signed -> 서명
sizeof -> 크기
static -> 고정
struct -> 구조물
switch -> 스위치
typedef -> 형식정의
union -> 연합
unsigned서명안함
void -> 공허
volatile -> 변덕
while -> 동안
scanf -> 입력받기
```

## 사용법
밑의 코드를 맨 위에 붙여넣는다 그 후 위의 튜토리얼을 보고 코드를 짜면 끝!

```
typedef int 정수;
typedef char 문자;
#define 출력 printf
#define 반환 return
#define 진입점 main
#define 자동 auto
#define 반복문끝 break
#define 선택지 case
#define 변함없는 const
#define 진행 continue
#define 기본 default
#define 더블 double
#define 아니면 else
#define 열거형 enum
#define 타파일전역변수 extern
#define 실수형 float
#define 위해 for
#define 이동 goto
#define 만일 if
#define 인라인 inline
typedef long 긴;
#define 등록 register
#define 제한 restrict
#define 돌아가 return
#define 짧다 short
#define 서명 signed
#define 크기 sizeof
#define 고정 static
#define 구조물 struct
#define 스위치 switch
#define 형식정의 typedef
#define 연합 union
#define 서명안함 unsigned
#define 공허 void
#define 변덕 volatile
#define 동안 while
#define 입력받기 scanf 
```

## 예제
### hello world 출력
```
정수 진입점(정수 매개변수개수, 문자 **매개변수목록)
{	출력("안녕 세상!");
	반환 0;
}
```

### 문자 5개를 입력받아서 입력받아서 소문자면 대문자로, 대문자면 소문자로 출력
```
정수 진입점()
{
    문자 ch[6];
 
    정수 i;
 
    출력 ("문자 5개를 입력하세요 : ");
    scanf ("%s", ch);


    위해 (i=0; i<6; i++) {
        만일 (ch[i] >= 'A' && ch[i] <='Z') {
            ch[i] = ch[i] + ('a' - 'A');

        }

        아니면 만일 (ch[i] >= 'a' && ch[i] <='z') {
            ch[i] = ch[i] - ('a' - 'A');

        }
    }

    출력 ("%s", ch);

    반환 0;
 }
 ```
 
 ### 업다운게임
 ```
 #include <stdio.h>
#include <stdlib.h>
#include <time.h>

typedef int 정수;
typedef char 문자;
#define 출력 printf
#define 반환 return
#define 진입점 main
#define 자동 auto
#define 반복문끝 break
#define 선택지 case
#define 변함없는 const
#define 진행 continue
#define 기본 default
#define 더블 double
#define 아니면 else
#define 열거형 enum
#define 타파일전역변수 extern
#define 실수형 float
#define 위해 for
#define 이동 goto
#define 만일 if
#define 인라인 inline
typedef long 긴;
#define 등록 register
#define 제한 restrict
#define 돌아가 return
#define 짧다 short
#define 서명 signed
#define 크기 sizeof
#define 고정 static
#define 구조물 struct
#define 스위치 switch
#define 형식정의 typedef
#define 연합 union
#define 서명안함 unsigned
#define 공허 void
#define 변덕 volatile
#define 동안 while
#define 입력받기 scanf 

정수 진입점 ()
{
        정수 com, user;
        정수 cnt=0;
        정수 play=1;

        srand (time(NULL));
        com=rand()%100+1; //1에서 100사이의 난수 생성

        동안 (play==1)
        {
                출력 ("<<1~100사이의 수를 입력해 주세요>>\n");
                입력받기 ("%d",&user);


                동안 (user>100 || user<1)
                {
                        출력 ("\n잘못된 입력입니다.\n<<<다시 입력 해주세요>>>\n");
                        입력받기 ("%d",&user);
                } //조건에 맞지않는 입력일 경우 다시 입력하게 함
                만일 (user<100&&user>1)
                {
                        만일 (user>com)
                        {
                                출력 ("down!!\n\n");
                                cnt++; //시도 횟수 카운트
                        }
                        아니면 만일 (user<com)
                        {
                                출력 ("up!!\n\n");
                                cnt++; //시도 횟수 카운트

                        }
                        아니면 만일 (com==user)
                        {
                                cnt++; //시도 횟수 카운트
                                출력 ("%정답입니다!!\n%d번째에 맞추셨습니다.",cnt);
                                play=0; //게임 종료 조건
                        }
                }
        }
}
```
