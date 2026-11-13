# Day 1

Debug.log("OOO"); <br>
게임 콘솔에 메세지를 출력

Start() <br>
게임을 실행 시 한 번 호출

Update() <br>
게임을 실행 시 초당 여러 번 호출

transform.localScale = new Vector3(length, height, length); <br>
너비(x), 높이(y), 길이(z)로 객체의 크기를 나타냄

transform.position = new Vector3(0, height, 0); <br>
x, y, z로 객체의 좌표를 나타냄

한 프레임에서 다음 프레임까지 값을 기억하려면 모든 메서드 밖에 변수를 선언(필드) <br>
ex) : update() 메서드에서 변수++; 사용시

bool open = Input.GetKey(KeyCode.Space); <br>
키가 눌러진 상태를 판단
