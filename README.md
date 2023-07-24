<!DOCTYPE html>
<html>
<head>
    <title>로그인</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 20px;
        }
        h1 {
            text-align: center;
        }
        form {
            max-width: 300px;
            margin: 0 auto;
        }
        input[type="text"],
        input[type="password"],
        input[type="submit"] {
            display: block;
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
        }
        input[type="submit"] {
            display: inline-block;
            width: auto; /* 수정된 부분 */
            background-color: #4CAF50;
            color: white;
            border: none;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <h1>로그인</h1>
    <form id="login-form">
        <input type="text" id="username" placeholder="아이디">
        <input type="password" id="password" placeholder="비밀번호">
        <input type="submit" value="로그인">
    </form>

    <script>
        // 마스터 계정 정보
        var masterUsername = '12345';
        var masterPassword = '12345';

        // 로그인 폼 제출 이벤트 처리
        document.getElementById('login-form').addEventListener('submit', function(event) {
            event.preventDefault(); // 폼 제출 기본 동작 방지

            // 입력된 아이디와 비밀번호 가져오기
            var username = document.getElementById('username').value;
            var password = document.getElementById('password').value;

            // 마스터 계정 확인
            if (username === masterUsername && password === masterPassword) {
                // 로그인 성공 시 사이트로 이동
                window.location.href = 'http://127.0.0.1:5500/indexpostt.html';
            } else {
                alert('아이디나 비밀번호가 잘못되었습니다.');
            }
        });
    </script>
</body>
</html>
