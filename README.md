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

transform.Rotate(x, y, z);  
speed * Time.deltaTime을 변수에 넣어서 화면 주사율에 상관없이 일정(1초마다) 회전

[SerializeField] private float size = 1.5f;  
"[SerializeField] private" 을 자료형 변수에 선행하여 작성 함으로서 다른 곳에서 참조하지 못하는 변수 생성(인스펙트에는 보임)

Mathf.Sin, Mathf.Abs, Mathf.Sqrt, Mathf.PI 등으로 실수형 c# Math사용 가능  
