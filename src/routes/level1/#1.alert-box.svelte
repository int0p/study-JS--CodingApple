<script>

    function show(msg){
        document.getElementById('alert').style.display = 'block';
        document.getElementsByClassName('title')[0].innerHTML=msg;
    }
    function close(){
        document.getElementById('alert').style.display = 'none';
    }

    function look(state){
        document.getElementById('alert').style.display = state;
    }
</script>


<div class="alert-box" id="alert">
    <p class="title">알림창</p>
    <button on:click={close}>닫기</button>
</div>
<button on:click={()=>{look('block')}}> 보여줘</button>

<button on:click={()=>{show('아이디를 입력하세요')}}> 버튼1 </button>
<button on:click={()=>{show('비밀번호를 입력하세요')}}> 버튼2 </button>

<style>
    .alert-box {
        background-color: skyblue;
        padding: 20px;
        color: white;
        border-radius: 5px;
        display: none;
    }
</style>