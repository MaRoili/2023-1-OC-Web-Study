<내용정리>
# Box model
1.	블록 레벨 요소 : <div> , <p> , <h1>
	Div, p, h1 한칸씩 큰 박스 생성 
2.	인라인 레벨 요소: <span>, <strong>
	Span, strong 자신만을 감싸는 작은 박스

Content: <strong> strong </strong> 에서 strong을 content라고 한다
Padding: 컨텐츠와 border 사이의 간격 // 넓힐 수도 좁힐 수도 있다 (옷 패딩처럼 사이 공간으로 생각)
Border: 테두리 
Margin: 요소와 요소 사이의 여백 / border와 다른 요소 사이의 여백
코드- margin: 10px 30px 0px 20px; 할 때/위아래 오른쪽 왼쪽 간격 같을 시 10px 30px 처럼 2개만 적기


# Flex Box Layout 
Flexible layout
아이템이 배열될 방향인 주축을 정할 수 있다
주축과 수직한 축은 cross axis라고 한다
<div class=”flex-box”>
<div class=”box”>1</div>
<div class=”box”>2</div>
<div class=”box”>3</div>
세로로 배열되던 것이

Flex-box{
Display: flex;
Flex-direction: row;
} 하면 가로 방향으로 배열
이렇게 하면 main cross는 row, cross axis는 column이다

Display: flex;
Flex-direction: column; 하면
Main axis는 column이고 cross axis는 row이다

- 예시 정리
Justify-content: center; -> 윗줄에서 센터
Justify-content: space-around; -> 윗줄에서 간격 존재
Justify-content: flex-end; -> 윗줄에서 끝에
Align-item: end / center -> 맨 아랫줄에 / 가운데 쪽에

Justify-content: main axis
Align-item: cross axis / 저주-콘서트(justi main) , 크로스-라인(얼라인)
- 숙제
Flex-direction: row-reverse; – 요소들을 정렬 할 방향 지정


<과제>
6주차 과제 flexbox froggy 
1.	justify-content: flex-end;
2.	justify-content: flex-end;
3.	justify-content: space-around;
4.	justify-content: space-between;
5.	align-items: flex-end;
6.	align-items: center;
justify-content: center;
7.	justify-content: space-around;
align-items: end;
8.	flex-direction: row-reverse;
9.	flex-direction: column;
10.	flex-direction: row-reverse;
justify-content: flex-end;
11.	flex-direction: column;
justify-content: end;
12.	flex-direction: column-reverse;
justify-content: space-between;
13.	flex-direction: row-reverse;
    align-items: end;
    justify-content: center;
18. flex-wrap: wrap;
19. flex-direction: column;
flex-wrap: wrap;
20. flex-flow: column wrap;
