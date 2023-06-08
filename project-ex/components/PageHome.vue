<template>
    <div>
      <div class="board">
        <table>
            <thead>
            <tr>
                <th>제목</th>
                <th>작성자</th>
                <th>날짜</th>
            </tr>
        </thead>
            <tbody>
                <tr><td>오늘자 경기</td><td>배진호</td><td>2023.06.08</td></tr>
                <tr><td>오늘자 경기</td><td>배진호</td><td>2023.06.08</td></tr>
                <tr><td>오늘자 경기</td><td>배진호</td><td>2023.06.08</td></tr>
                <tr><td>오늘자 경기</td><td>배진호</td><td>2023.06.08</td></tr>
                <tr><td>오늘자 경기</td><td>배진호</td><td>2023.06.08</td></tr>
                <tr><td>오늘자 경기</td><td>배진호</td><td>2023.06.08</td></tr>
                <tr><td>오늘자 경기</td><td>배진호</td><td>2023.06.08</td></tr>
                <tr><td>오늘자 경기</td><td>배진호</td><td>2023.06.08</td></tr>
            </tbody>
        </table>
        <br>
        <div class="number">
            <button>1</button>
            <button>2</button>
            <button>3</button>
            <button>4</button>
            <button>5</button>
        </div>
        <div class="button-container">
          <button class="list-button">목록</button>
          <button class="write-button">글쓰기</button>
        </div>
      </div>
    </div>
  </template>
<script>
export default {}
</script>
<style>
.board{
    height: 700px;
    width: 700px;
    margin: 0 auto;
    overflow: auto;
}
.button-container {
  display: flex;
  justify-content: flex-end; /* 버튼을 오른쪽에 정렬 */
  margin-top: 10px; /* 버튼과 테이블 사이 간격 조정 */
}
button {
    right: 10px;
    background-color: #004d98;
    color: #fff;
    border: none;
    padding: 8px 16px;
    font-size: 12px;
    text-align: right;
}
table{
    border-collapse: collapse;
    table-layout: fixed;
    width: 100%;
}
th,td{
    padding: 10px;
    text-align: left;
    border-bottom: 1px solid #A50044;
}
.number {
  display: flex;
  justify-content: center; /* 숫자 가운데 정렬 */
  margin-top: 10px; /* 숫자와 테이블 사이 간격 조정 */
}
.number button {
  margin-right: 5px;
}
</style>
