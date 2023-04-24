# (부록) MySql - 테이블

### 테이블 생성

- 문법

```sql
create table 테이블명 (
	필드명1, 데이터형,
	필드명2, 데이터형,
	필드명3, 데이터형,
	...
	primary key(필드명)
);
```

- 예제

```sql
create table mem (
	num int not null auto_increment,
	id char(20) not null,
	pass char(20) not null,
	name char(20) not null,
	age int,
	primary key(num)
);
```

- `not null`: null 값을 허용하지 않음
- `auto_increment`: 레코드에 데이터를 입력할 때 필드 값이 자동으로 증가함
레코드에 데이터를 입력할 때 num 필드에 값을 입력하지 않아도 0부터 1씩 값이 자동으로 증가하고, 그 값이 num 필드에 저장됨
- `primary key(주 키)`: 테이블의 필드 중 중복되면 안되는 필드, 즉 레코드를 식별하는데 사용되는 필드

### 테이블 구조 확인

- 문법

```sql
desc 테이블명;
```

- 예제

```sql
desc mem;
```

### 테이블에 새로운 필드 추가

- 문법

```sql
alter table 테이블명 add 새로운_필드명 필드_데이터형;
```

- 예제

```sql
alter table mem add email char(30);
```

### 테이블에서 필드 삭제하기

- 문법

```sql
alter table 테이블명 drop 삭제할_필드명1, 삭제할_필드명2...;
```

- 예제

```sql
alter table mem drop email;
```

### 테이블에서 필드 수정하기

- 문법

```sql
alter table 테이블명 change 변경할_필드명 새로운_필드명 필드_데이터형;
```

- 예제

```sql
alter table mem change age phone char(20);
```

### 테이블에서 필드 데이터형 수정하기

- 문법

```sql
alter table 테이블명 modify 필드명 수정할_데이터형;
```

- 예제

```sql
alter table mem modify phone int;
```

### 테이블 이름 변경하기

- 문법

```sql
alter table 테이블명 rename 새로운_테이블명;
```

- 예제

```sql
alter table mem rename mem2;
```

### 테이블 삭제하기

- 문법

```sql
drop table 테이블명;
```

- 예제

```sql
drop table mem2;
```