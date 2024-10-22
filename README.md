# JDBC 게시판 서비스
## 시작 가이드
### 1. 프로젝트 다운로드
```bash
git clone
```
### 2. DB 연결 정보 Properties 파일 생성
🚨 본인이 사용할 정보로 필수적으로 변경해주세요 !
```bash
#!/bin/bash

mkdir -p src/resources

cat <<EOL > src/resources/dbconfig.properties
# 본인 DB URL 입력
url=jdbc:mysql://127.0.0.1:3306/board
# 본인 DB 계정 입력
username=root
# 본인 DB 비밀번호 입력
password=123456
EOL
```

## 주요 기능
### 게시판 기능
- 게시글 작성
- 게시글 삭제
- 게시글 수정
- 게시글 전체 조회 (목록 조회)
- 게시글 개별 조회 (상세 조회)
- 게시글 제목으로 검색
 
### 1. 게시글 작성
![스크린샷 2024-08-05 172911](https://github.com/user-attachments/assets/107da544-28ff-497e-97aa-d2a6b626f001)
### 2. 게시글 삭제
![게시글 삭제](https://github.com/user-attachments/assets/0d597cc1-5d6d-41da-a9e3-b2b54b717033)
### 3. 게시글 수정
![게시글 수정](https://github.com/user-attachments/assets/f9048c51-4d2e-473d-8e84-b4b84f26aed2)
### 4. 게시글 전체 조회
![전체 조회 게시글 있음](https://github.com/user-attachments/assets/892dce47-e97a-4341-9f26-86dfdc9f0cfb)
### 5. 게시글 개별 조회
![개별 조회](https://github.com/user-attachments/assets/18cdbba7-0e7c-4bba-b4c0-9463a686f4cc)
### 6. 게시글 제목으로 검색
![게시글 제목으로 검색](https://github.com/user-attachments/assets/b2b18953-75ee-44d6-83cf-dc6e4ef0f4a6)

### 댓글 기능

![스크린샷 2024-08-05 오후 2 27 03](https://github.com/user-attachments/assets/fea4412c-6c00-4871-a572-e742fbd6ff8b)

### 1. 댓글 작성
![스크린샷 2024-08-05 오후 2 27 36](https://github.com/user-attachments/assets/8f797c7c-edb5-4737-8d45-eced39d0c84d)

### 2. 게시글의 댓글 전체 조회
![스크린샷 2024-08-05 오후 2 27 46](https://github.com/user-attachments/assets/a10183ea-1e66-48eb-a034-45900f26f07b)


### 3. 댓글 수정
![스크린샷 2024-08-05 오후 2 28 03](https://github.com/user-attachments/assets/951d7914-c624-4fd0-b01b-c2da5114f4ef)

### 4. 댓글 삭제
![스크린샷 2024-08-05 오후 2 28 10](https://github.com/user-attachments/assets/1f370006-2656-46f2-9559-cc3da354a48e)



### 회원 기능
### 1. 회원가입
#### 회원가입 성공
<img width="300" alt="image" src="https://github.com/user-attachments/assets/fe5daa7e-a978-4b20-90c8-94570c06f06d">

#### 입력한 이메일이 형식에 맞지 않는 경우
<img width="300" alt="image" src="https://github.com/user-attachments/assets/e074b0f2-392c-46b8-a6db-41b28c93c99a">

#### 입력한 비밀번호와 확인용 비밀번호 값이 다른 경우
<img width="300" alt="image" src="https://github.com/user-attachments/assets/2f1bc49b-0125-4b15-a006-d13e9657d760">

#### 아이디와 비밀번호를 빈값으로 전달한 경우
<img width="300" alt="image" src="https://github.com/user-attachments/assets/efb837f9-f583-47c0-b79d-40b579db4a0b">

#### 비밀번호와 비밀번호 확인값을 빈값으로 전달한 경우
<img width="300" alt="image" src="https://github.com/user-attachments/assets/30f34ca1-1c96-4d2e-9b41-e5d4e9b4c06b">


### 2. 로그인
#### 로그인 성공
<img width="300" alt="image" src="https://github.com/user-attachments/assets/711c0518-3119-438f-952b-c5e99556ecf2">

#### 로그인 실패(아이디를 틀리게 입력)
<img width="300" alt="image" src="https://github.com/user-attachments/assets/d95d9f31-9021-4305-8074-1fcacdafd4e3">

#### 로그인 실패(비밀번호를 틀리게 입력)
<img width="300" alt="image" src="https://github.com/user-attachments/assets/ba49ed05-2822-468d-b37b-13fef739d902">

#### 로그인 실패(아이디, 비밀번호를 틀리게 입력)
<img width="300" alt="image" src="https://github.com/user-attachments/assets/591cb23b-4c75-4bd2-b7b8-6e15aef30f51">

#### 회원이 다시 로그인을 시도하는 경우
<img width="300" alt="image" src="https://github.com/user-attachments/assets/5de510b9-afa2-4935-805a-d6279c650e0c">


### 3. 로그아웃
#### 로그아웃 성공
<img width="300" alt="image" src="https://github.com/user-attachments/assets/fba10a6b-7595-4375-b39c-742f2619224c">

#### 비회원이 로그아웃을 시도하는 경우
<img width="300" alt="image" src="https://github.com/user-attachments/assets/2fa2ff7e-dc4e-429c-b865-06fd61340f01">


##  ERD
![ERD](https://github.com/user-attachments/assets/35c11868-5e3a-43b2-8798-6d43fb2f480e)


###  DB 생성 쿼리
```sql
CREATE TABLE `Comment` (
	comment_id	BIGINT	    PRIMARY KEY    AUTO_INCREMENT,
	board_id	    BIGINT	    NOT NULL,
	member_id	    BIGINT	    NOT NULL,
	parent_id	    BIGINT	    NULL	COMMENT '원래 댓글 번호',
	content	    	TEXT	    NOT NULL,
	created_at		DATETIME	NOT NULL   DEFAULT NOW(),
	modified_at		DATETIME	NOT NULL,
	is_deleted    ENUM('Y', 'N')  NOT NULL DEFAULT 'N'
);

DROP TABLE IF EXISTS `Member`;

CREATE TABLE `Member` (
	member_id    BIGINT       PRIMARY KEY    AUTO_INCREMENT,
	email        VARCHAR(500) NOT NULL COMMENT '로그인 아이디',
	password     VARCHAR(500) NOT NULL,
	nickname     VARCHAR(500) NOT NULL COMMENT '회원 닉네임',
	created_at   DATETIME     NOT NULL     DEFAULT NOW(),
	is_deleted   ENUM('Y', 'N')  NOT NULL DEFAULT 'N'
);

DROP TABLE IF EXISTS `Board`;

CREATE TABLE `Board` (
	board_id	   BIGINT	    PRIMARY KEY    AUTO_INCREMENT,
	member_id	   BIGINT	    NOT NULL,
	title	       VARCHAR(50)	NOT NULL,
	content	   TEXT	        NOT NULL,
	created_at   DATETIME	    NOT NULL     DEFAULT NOW(),
	modified_at  DATETIME	    NOT NULL,
	is_deleted   ENUM('Y', 'N')  NOT NULL DEFAULT 'N'
);

ALTER TABLE Board ADD CONSTRAINT `fk_member_board` FOREIGN KEY (member_id)
	REFERENCES Member(member_id);

ALTER TABLE Comment ADD CONSTRAINT `fk_member_comment` FOREIGN KEY (member_id)
	REFERENCES Member(member_id);

ALTER TABLE Comment ADD CONSTRAINT `fk_board_comment` FOREIGN KEY (board_id)
	REFERENCES Board(board_id);

ALTER TABLE Comment ADD CONSTRAINT `fk_comment_comment` FOREIGN KEY (parent_id)
	REFERENCES Comment(comment_id);
```
