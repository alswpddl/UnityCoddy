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

# Day 3

[Header("Movement")]  
뒤따르는 필드들을 묶기 위해 필드 위에 굵은 제목을 표시

[Tooltip("Units per second")]  
마우스를 필드 이름 위에 올려놓으면 해당 텍스트를 표시

[Range(0f, 10f)]  
슬라이더를 표시하고 Inspector에서 값을 0과 10 사이로 유지(코드는 변경 됨)

[HideInInspector]  
public 필드를 Inspector에서 숨기지만, 다른 스크립트에서는 계속 사용 가능

Input.GetKeyDown(KeyCode.Space);  
키를 누를 때마다 한 프레임 동안 true

Input.GetKey(KeyCode.Space);  
키를 누르고 있는 동안 매 프레임 true

Input.GetKeyUp(KeyCode.Space);  
키에서 손을 뗄 때 한 프레임 동안 true

Horizontal : x축    
Vertical : z축

Input.GetAxis("Horizontal or Vertical");  
좌우 화살표 키(A or D)를 -1 ~ 1사이의 숫자로 변환

Input.GetAxisRaw("Horizontal or Vertical");  
좌우 화살표 키(A or D)를 -1 or 0 or 1의 즉각적인 숫자로 변환

Input.GetButtonDown("Fire1");  
GetButton은 키의 "이름"을 인식 GetKey와 같이 GetButtonDown, GetButtonUp도 마찬가지로 가능

# Day 4

Input.GetMouseButtonDown(0 or 1 or 2)  
0 : 마우스 왼쪽  
1 : 마우스 휠  
2 : 마우스 오른쪽  
Input.GetMouseButtonDown(0) = Input.GetKeyDown(KeyCode.Mouse0)

public Vector3 current = new Vector3(1, 0, 0);  
public Vector3 motor = new Vector3(0, 0, 2);  
motor += current(1, 0, 2)처럼 벡터끼리의 연산이 가능  
trans.position += motor

Vector3.right (1, 0, 0) 및 Vector3.left (-1, 0, 0)  
Vector3.up (0, 1, 0) 및 Vector3.down (0, -1, 0)  
Vector3.forward (0, 0, 1) 및 Vector3.back (0, 0, -1)  

if (Input.GetKey(KeyCode.UpArrow)) {  
  transform.position += Vector3.up * speed * Time.deltaTime;  
}  
와 같이 사용 가능

transform.forward  
transform.up 및 transform.down  
transform.left 및 transform.right  
오브젝트 자체의 방향

transform.Translate(Vector3.forward * speed * Time.deltaTime)  
벡터를 오브젝트의 방향에서 해석
