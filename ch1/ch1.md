# Hw 1 
/tmp에 missing이라는 새로운 경로를 만들어 보세요 .
```bash
mkdir /tmp/missing # 경로 생성

ls /tmp/ | grep missing # 생성 확인
```

# Hw 2
touch라는 프로그램을 관찰해보세요. man 프로그램이 도움이 될겁니다.
```bash
man touch
```

# Hw3 
touch를 이용해서 semester라는 파일을 missing 안에 만들어 보세요.
```bash
touch /tmp/missing/semester # 파일 생성

ls /tmp/missing/ | grep se # 확인
```

# Hw4
아래 주어진 것을 그 파일에 써보세요. 단, 한번에 한줄씩
```shell
#!/bin/sh
curl --head --silent https://missing.csail.mit.edu
```
첫번째 줄을 작동시키는게 꽤 까다로울 것입니다. #으로 시작하는 것은 코멘트(comment)고, !는 큰 따옴표(")로 둘러쌓인 문자열 내에서도 특별한 의미를 가집니다. 배시(Bash)는 작은 따옴표' 문자열과 큰따옴표를 구분합니다. 이것은 매우 헷갈리는 케이스입니다. Bash 인용 관련 메뉴얼 페이지에 더 자세한 정보가 설명돼있습니다.

```bash
echo '#!/bin/sh' > /tmp/missing/semester # 한줄 쓰기
echo 'curl --head --silent https://missing.csail.mit.edu' >> /tmp/missing/semester # >>: 이어 쓰기 

# 확인
cat /tmp/missing/semester
```

comment:
따옴표(')와 쌍 따옴표(") 구분하기
bash에서 따옴표(')로 감싼 문자열은 문자열 그대로 사용됨. `${}`로 감싸서 변수 대입이 안되고 입력한 그대로 출력
반면 쌍따옴표(")로 감싼 문자열에서는 bash의 변수(`${}`)를 그대로 사용할 수 있음. 

# Hw5
파일을 실행해보세요. 예를 들어, (./semester)라는 경로를 셸에 입력해보세요. 이것이 왜 작동하지 않는지 ls를 이용해 파악해보세요. (힌트: 파일의 비트 권한을 확인해보세요.)


