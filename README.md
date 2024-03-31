# 개요
Flutter에서 레이아웃을 구성하는 핵심 개념인 Row 위젯과 Column 위젯을 공부하고, 두개의 조합을 통해 어떤 식의 레이아웃을 구성할 수 있는지 실습한다.

# Flex
Row와 Column 위젯은 Flex 레이아웃 모델을 따라가고 있다.   
수평으로 나열할 때는 Row, 수직으로 나열할 때는 Column을 사용한다.   
만약 CSS에 익숙하다면 `display: flex`와 동일한 모델로 이해하면 쉽다.   
   
Flex는 유연한 레이아웃 모델로, 자식 요소들을 배치할 때 부모 컨테이너 기준으로 자식을 배치시킨다.   
Flex 레이아웃 모델을 가장 잘 설명하는 그림은 아래 그림이다.

![flex_box](https://github.com/kyomin/flutter-row-and-column/assets/46395776/caaca527-3a25-4530-8145-7df9074e386e)

기본적으로 주 축(main axix)과 교차 축(cross axis)을 가지며, 주축에 따라서 방향이 전환된다.   
주축이 수평이라면 Row, 주축이 수직이라면 Column 위젯을 사용하면 된다.

# Row and Column

### MainAxisAlignment
주축 정렬이다.

- start - 시작 (디폴트)
- end - 끝
- center - 가운데
- spaceBetween - 범위의 끝과 끝까지 위젯과 위젯의 사이가 동일하게 배치된다.
- spaceEvenly - 위젯과 위젯의 사이가 동일하게 배치되지만, 끝과 끝에도 위젯이 아닌 빈 간격으로 시작한다.
- spaceAround - spaceEvenly + 끝과 끝의 간격은 1/2

### CrossAxisAlignment
반대축 정렬이다.   
즉, Column이면 Row 기준, Row면 Column 기준으로 정렬이 일어난다.

- start - 시작
- end - 끝
- center - 가운데 (디폴트)
- stretch - 반대축으로 최대한 늘린다.

### MainAxisSize
주축 크기이다.

- max - 최대
- min - 최소

### Expanded / Flexible

- Expanded - 남아있는 공간들을 Expanded가 감싸고 있는 위젯들이 나눠서 차지한다.
- Flexible - Expanded와 반대로 명시된 크기 이외의 남은 공간들은 버려서 상위 위젯에 귀속되도록 한다.
- flex - 나머지 공간을 나눠먹는 비율이며, 디폴트는 1이다.

# 실습 결과 화면
![row_and_column](https://github.com/kyomin/flutter-row-and-column/assets/46395776/bd899f62-2d98-47c3-895f-08ab3d294ea5)