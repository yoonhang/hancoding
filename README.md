스프링부트 무작정 따라하기 -> vscode version up..

hancoding

https://www.youtube.com/watch?v=LJKVX20YeLU&list=PLZzruF3-_clsWF2aULPsUPomgolJ-idGJ&index=10

https://github.com/HanCoding/board_exam_project

개발환경
 
IDE(통합개발환경) : vscode

개발 언어 : Java 1.8.0

프레임워크 : Spring Boot 3.3.1

빌드 : Gradle

DB(데이터베이스) : MariaDB 10.3.30

DB 접근 기술 : JPA

View 템플릿 : Thymeleaf

===========
test db insert....

DELIMITER $$

CREATE PROCEDURE testDataInsert()
BEGIN
    DECLARE i INT DEFAULT 1;

    WHILE i <= 120 DO
        INSERT INTO board(title, content)
          VALUES(concat('제목',i), concat('내용',i));
        SET i = i + 1;
    END WHILE;
END$$
DELIMITER $$
