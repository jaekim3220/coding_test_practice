# 프로그래머스 코딩테스트 연습(힌트가 있을 뿐 답 없음)
------------------------------------------------------------------------------------------
## - 이름이 없는 동물의 아이디(SQL)
select 문의 구조 이해, where 조건, order by 정렬

## - 최댓값 구하기(SQL)
max 또는 

## - 가장 비싼 상품 구하기(SQL)
select 문의 구조 이해, 최대값 추출 명령어, 이름 변경 명령어 as

## - 흉부외과 또는 일반외과 의사 목록 출력하기(SQL)
where 조건(특정 과만 출력), datetime을 date로 변형(구글 검색으로 방법조회)해서 사용(문제오류:테이블은 DATE 형식인데 동작은 DATETIME로 실행되서 통과가 안됨), order by 정렬

## - 과일로 만든 아이스크림 고르기(SQL)
상반기 아이스크림 총주문량이 3,000보다 높으면서 아이스크림의 주 성분이 과일인(where문, and) 아이스크림의 맛을 총주문량이 큰 순서대로 조회하는(order by desc) SQL 문을 작성
->select문 and, where 조건, order by desc
(SELECT FLAVOR from FIRST_HALF where TOTAL_ORDER > 3000 and FLAVOR in (select FLAVOR from ICECREAM_INFO where INGREDIENT_TYPE = 'fruit_based') order by TOTAL_ORDER desc;) - select in은 특정 '값' 추출, select from은 '테이블' 추출

## - 조건에 맞는 도서와 저자 리스트 출력하기(SQL)
date_format(dt,”%Y-%m-%d”)로 datetime을 date로 변형
inner join문
select b.BOOK_ID, a.AUTHOR_NAME, date_format(b.PUBLISHED_DATE, '%Y-%m-%d') as PUBLISHED_DATE from AUTHOR a inner join BOOK b ON a.author_id = b.author_id
where b.CATEGORY = '경제' order by PUBLISHED_DATE;

## - 성분으로 구분한 아이스크림 총 주문량(SQL)
group by, 
- ------------------------------------------------------------------------------------------------------
# 여기는 Python 문제

## - 더 크게 합치기
int, str, min, max

## - 꼬리 문자열
list 초기 값, append, list to string(.join)

## - A 강조하기
쉽게는 lower, replace // .upper, .lower, and("A"가 아닌 모든 대문자 알파벳)

## - 개미 군단

## - 접미사인지 확인하기

## - 피자 나눠 먹기 (3)

- 짝수의 합

- 배열의 평균값

- 양꼬치

- 편지

- 정수 찾기

- 문자열의 앞의 n글자

- n의 배수

- 문자열을 정수로 변환하기

- 조건에 맞게 수열 변환하기 3

- 부분 문자열인지 확인하기

- 공백으로 구분하기 1

- 짝수 홀수 개수

- 문자열 정수의 합

- 접두사인지 확인하기

- 모음 제거

- 카운트 업

- 카운트 다운

- 길이에 따른 연산

- 원소들의 곱과 합

- 배열 원소의 길이
len, a for a in list

- 피자 나눠 먹기 (1)
나머지, 몫

- 중앙값 구하기\
변수 설정, 순서 나열, 홀/짝수 구분, 배열/함수 구분

- 순서쌍의 개수\
리스트 컴프리헨션

- 삼각형의 완성조건 (1)\
변수 생성, 오름차순, if문

- 문자 리스트를 문자열로 변환하기\
.join()문

- 특정 문자 제거하기\
.replace(,)

- 첫 번째로 나오는 음수\
변수, range, if

- 뒤에서 5등까지\
순서 정렬

- 머쓱이보다 키 큰 사람\
변수 증가, for, if

- 중복된 숫자 개수\
- 변수 증가, for, if (단순히 중복된 숫자를 count)

- 문자 반복 출력하기\
join, for, .append, .extend, .insert

- 배열의 유사도\
count용 변수, for, if

- 짝수는 싫어요\
append, 홀/짝 구분, for

- 자릿수 더하기\
정수, 문자열

- 원소들의 곱과 합\
변수, for문 덧셈/곱셈

- 숨어있는 숫자의 덧셈 (1)\
append, .isdigit()

- 특정한 문자를 대문자로 바꾸기\
upper, replace

- 홀짝 구분하기\
f-string

- 원하는 문자열 찾기\
if in, lower/upper

- 조건에 맞게 수열 변환하기 1\
for, if, append

- 배열의 원소만큼 추가하기\
extend, append 차이점 확인, 배열의 괄호 확인

- 글자 이어 붙여 문자열 만들기\
for문, index_list의 숫자를 확인 후 해당 숫자 자릿수의 글자를 새로운 list에 더하여 list를 완성

- 배열에서 문자열 대소문자 변환하기\
for문, upper, lower, append, 몫

- 주사위 게임 1\
if문, 제곱 pow, 절대값 abs

- 문자열 바꿔서 찾기\
(list와 문자열-string 구분) -> (append, extend는 list문임을 기억)

- 배열 만들기 1\
range

- 369 게임\
count는 list, 문자열에만 인식됨

- 이어 붙인 수\
홀/짝 구분 , str/int 구분

- 제곱수 판별하기\
import math, sqrt 또는 (n**(1/x))

- 행렬의 덧셈\
2중 배열,
print(len(lista))
print(len(lista[0]))

- 세균 증식\
pow

- 대문자와 소문자\
문자열 더하기, upper, lower

- 홀수 vs 짝수\
sum함수, 리스트 형식의 홀/짝 유도, return을 배제할 경우 max를 사용할 수 있음

- 배열 비교하기\
len, 대소비교, sum, 변수 생성

- 배열의 길이에 따라 다른 연산하기\
len, range, 

- 공백으로 구분하기 2\
split

- 암호 해독\
list화 문자열의 차이를 이해, range(0,a,b)/range(b-1,a,b)의 차이를 이해

- 홀짝에 따라 다른 값 반환하기\
제곱 개념, range 개념 : n까지 계산하려면 범위는 마지막 범위는 n+1로 지정해야함
