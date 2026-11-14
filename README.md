# Day 1

Debug.log("OOO");  
게임 콘솔에 메세지를 출력

Start()  
게임을 실행 시 한 번 호출

Update()  
게임을 실행 시 초당 여러 번 호출

transform.localScale = new Vector3(length, height, length);  
너비(x), 높이(y), 길이(z)로 객체의 크기를 나타냄

transform.position = new Vector3(0, height, 0);  
x, y, z로 객체의 좌표를 나타냄

한 프레임에서 다음 프레임까지 값을 기억하려면 모든 메서드 밖에 변수를 선언(필드)  
ex) : update() 메서드에서 변수++; 사용시

bool open = Input.GetKey(KeyCode.Space);  
키가 눌러진 상태를 판단

# Day 2

transform.position += new Vector3(x, y, z);  
update() 메서드에 작성함으로서, 위치를 일정하게 바꿀 수 있음

transform.Rotate(x, y, z);  
각 변수에 [speed * Time.deltaTime]을 넣음으로서 모니터 주사율에 상관없이 일정하게(1초마다) 회전 가능

[SerializeField] private float size = 1.5f;  
"[SerializeField] private을 작성하면 외부에서 건들 수 없는 비공개 변수 작성이 가능(인스펙터에는 표시)

Mathf.Sin, Mathf.Abs, Mathf.Sqrt, Mathf.PI 사용 가능  

