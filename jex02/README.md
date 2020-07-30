# 오라클 스키마

``` sql
> 테이블 생성 및 더미 데이터

---테이블생성---
CREATE SEQUENCE SEQ_BOARD;

CREATE TABLE TBL_BOARD(
    BNO NUMBER(10,0),
    TITLE VARCHAR2(200) NOT NULL,
    CONTENT VARCHAR2(2000) NOT NULL,
    WRITER VARCHAR2(50) NOT NULL,
    REGDATE DATE DEFAULT SYSDATE,
    UPDATEDATE DATE DEFAULT SYSDATE
);

ALTER TABLE TBL_BOARD ADD CONSTRAINT PK_BOARD
PRIMARY KEY(BNO);