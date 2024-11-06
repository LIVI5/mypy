# SWE_2021_41_2024_2_week_6
---
### 👋 Hi, I’m @LIVI5, I'm learning about **Open Source Software** and trying to use _Markdown_! 
#### 🌱 I will explain my assignment from week4 and week5!
<br>

## Week 4
### Link
---
> **[Repository](https://github.com/LIVI5/SWE_2021_41_2024_2_week_4 "LIVI5/week4")**
> - It's link of my repository


### Code
---
```python
def isHappy(n):
  input_num = n
  val=0
  str_num = str(n)  # str으로 변환하여 각 자리수에 접근
  len_num = len(str_num)

  for x in range(len_num) : # 각 자리의 수의 제곱을 더해줌
    val += (int(str_num[x])) ** 2
```
> - <del> 이제부터 한국어로 쓰겠습니다... </del>
> - 이 과제는 HappyNumber를 찾는 함수 *isHappy()* 를 구현하는 것이었습니다.
>> **HappyNumber?** 각 자리수의 제곱을 더하는 시행을 계속 반복할 때, 1이 나올 수 있는 수를 말합니다.
> - 각 자리수에 접근하기 위해 str으로 변환하고 val 변수에 제곱을 더해주는 반복을 했습니다.
<br>

```python
  print(val)
  if val >= 10 :
    return isHappy(val)
  else :
    if val == 1 :
      return True
    else :
      return False
```
> val의 계산이 끝난 후, 위와 같은 코드로 함수를 재귀적으로 시행했을 때 다음과 같이 결과가 출력되는 것을 확인했습니다.
<br>
<img src="https://github.com/user-attachments/assets/b98792df-c4ff-4ac1-be5a-9411719bf667" width="100px" height="200px" title="example1"/>
<img src="https://github.com/user-attachments/assets/9ce8d2bf-1127-409f-aab5-26020ce6b9a0" width="100px" height="200px" title="example1"/>
<br>

> 위 결과를 바탕으로 다음과 같은 특징을 발견하였습니다.
> - 위 코드로 임의의 값 n을 넣었을 때 val가 4가 되는 순간부터 반복이 멈추고 False가 나왔다.
> - n에 4를 넣으면 (4, 16, ... ,20, 4, 16, ... ,20) 과 같이 일정 배열이 반복된다.

<br>

> 이를 바탕으로 다음과 같이 코드를 수정하였습니다.
> - happy number가 아니라면 val가 4가 나오는 순간부터 일정 배열이 반복되며 loop에서 빠져나오지 못한다.
> - val==4 가 되는 순간이 나온다면 'un'happy number이어서 False를 반환하고
> - 그렇지 않다면 happy number이므로 loop를 빠져나와 True를 반환한다.

```python

  if val == 4 :
    return False
  elif val == 1 :
    return True
  else :
    return isHappy(val)
```
<br>
<br>

## Week 5
### Submission
---
![week5](https://github.com/user-attachments/assets/f6737bbc-f744-4e2b-bada-89236ef0e3b8)

### Code
---

> ```bash
>docker exec <ossp_container> cat /etc/os-release
>```
> - <ossp_container> 내에서 운영 체제 정보를 출력합니다.
<br>

> ```bash
>docker exec <ossp_container> git --version
>docker exec <ossp_container> python3 --version
>```
> - <ossp_container> 에 있는 git과 python3의 버전을 출력합니다.
<br>

> ```bash
>docker inspect --format="{{ .HostConfig.Binds }}" <ossp_container>
>```
> - 호스트 파일 시스템과 컨테이너 간의 바인드 마운트를 출력 포멧에 따라 출력합니다.
<br>

---
<br>

### 감사합니다. :)
