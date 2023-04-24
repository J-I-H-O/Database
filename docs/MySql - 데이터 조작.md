# (부록) MySql - 데이터 조작

### insert - 데이터 삽입

- 문법

```sql
insert into 테이블명 (필드명1, 필드명2, ...) values (필드값1, 필드값2, ...);
```

- 예제

```sql
insert into friend (name, tel, address) values ('송예진', '031-123-4567', '경기도 용인');
```

### select - 데이터 검색

- 문법

```sql
select 필드명, 필드명2, ... from 테이블명 where 조건식
```

- 예제

```sql
select name, tel, address from member where age>=50 and gender='M';
```

### like - 특정 문자열이 포함된 레코드 검색

- 문법

```sql
select 필드명, 필드명2, ... from 테이블명 where 검색 필드 like 문자열_수식;
```

- 예제

```sql
select name, tel from member where name like '박%';
```

### order by - 레코드 정렬

- 문법

```sql
select 필드명, 필드명2, ... from 테이블명 order by 필드명;
```

- 예제

```sql
select name, age, address, tel, gender from member order by age;
```

- order 구에 desc 사용 시 내림차순 정렬

### update - 레코드 수정

- 문법

```sql
update 테이블명 set 필드명=필드값 where 조건식;
```

- 예제

```sql
update member set tel='123-4567' where name='고재진';
```

### delete - 레코드 삭제

- 문법

```sql
delete from 테이블명 where 조건식;
```

- 예제

```sql
delete from member where name='김수련';
```