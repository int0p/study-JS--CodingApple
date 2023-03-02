<script>

    let alertMsg = '알림창';

    function changeMsg(msg) {
        alertMsg = msg;
    }

    function display(state) {
        document.getElementById('alert').style.display = state;
    }
</script>

<div className="alert-box" id="alert">
    <p>{alertMsg}</p>
    <button on:click={()=>{display('none')}}>닫기</button>
</div>

<!--저장된 알림메세지를 보여줌 -->
<button on:click={()=>{display('block')}}> alertMsg 보여줘</button>

<!--알림메세지 변경-->
<button on:click={()=>{changeMsg('아이디를 입력하세요')}}> 버튼1</button>
<button on:click={()=>{changeMsg('비밀번호를 입력하세요')}}> 버튼2</button>

<style>
    .alert-box {
        background-color: skyblue;
        padding: 20px;
        color: white;
        border-radius: 5px;
        display: none;
    }
</style>