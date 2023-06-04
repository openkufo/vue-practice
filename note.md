## 데이터 바인딩
### 사용 이유
- vue 실시간 자동 렌더링
- 데이터 변수 저장

### 바닐라 js 데이터 바인딩
```js
document.getElementById().innerHTML = 'insert';
```

### vue 데이터 바인딩
```js
<template>
    {{ data1 }}
</template>

<script>
    ...
    data(){
        return {
            data1 : 10,
            data2 : 20,
        }
    },
    ...
</script>
```

### HTML 태그도 바인딩 가능 ( 콜론 사용)
```js
<template>
    <h4 class="red" :style="스타일">XX 원룸</h4>
</template>

<script>
    ...
    data(){
        return {
            스타일 : 'color : blue',
        }
    },
    ...
</script>
```

### 반복문
```js
menus : ['Home', 'Shop', 'About'],

<a v-for="menu in menus" :key="menu"> {{ menu }} </a>
```