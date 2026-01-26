# SPRING ADVANCED


## 📌 About
이 과제는 “기능 구현”보다는 **실제 현업에서 중요한 코드 품질/구조/테스트 관점의 개선**을 목표로 합니다.

- 예외/에러 원인 분석 및 실행 환경 세팅
- ArgumentResolver 복구 및 정상 동작 처리
- 코드 개선(early return, 불필요한 if-else 제거, Validation 적용)
- JPA N+1 문제를 fetch join → EntityGraph 기반으로 개선
- 실패하는 테스트 코드를 의도에 맞게 수정

---

## 🧩 Assignment Contents (Lv.0 ~ Lv.4)

### ✅ Lv.0 프로젝트 세팅 - 에러 분석 (필수)
- 애플리케이션 실행 실패 원인 분석 및 해결
- 여러 에러가 발생할 수 있어 로그 기반으로 원인 분리

### ✅ Lv.1 ArgumentResolver (필수)
- `AuthUserArgumentResolver` 로직이 동작하지 않는 문제 해결
- 컨트롤러에서 인증 사용자(AuthUser)를 정상적으로 주입받도록 수정

### ✅ Lv.2 코드 개선 (필수)
#### 1) 코드 개선 퀴즈 - Early Return
- 실패 케이스(예: 이메일 중복)에서 **불필요한 로직(passwordEncoder.encode)** 이 먼저 실행되지 않도록
- 조건을 빠르게 처리하여 가독성/성능 개선

#### 2) 리팩토링 퀴즈 - 불필요한 if-else 피하기
- 복잡한 if-else 구조를 제거하고 guard clause 형태로 단순화

#### 3) 코드 개선 퀴즈 - Validation
- Service 내부의 요청값 검증 로직을 DTO로 이동
- `spring-boot-starter-validation` + `@Valid`를 활용하여 요청 단계에서 400으로 처리

### ✅ Lv.3 N+1 문제 (필수)
- JPQL fetch join 기반 코드가 존재
- 동일한 동작을 하도록 `@EntityGraph` 기반으로 수정하여 N+1 문제 해결

### ✅ Lv.4 테스트 코드 연습 (필수)
- 의도와 다르게 작성된 테스트 수정
- 예외 케이스/성공 케이스가 정확히 검증되도록 정리

---

## 🛠️ Tech Stack
- Java
- Spring Boot
- Spring MVC
- Spring Data JPA
- Validation
- MySQL

---

## 🚀 Getting Started

### 1) Clone
```bash
git clone https://github.com/Banhklo2/spring-advanced.git
cd spring-advanced
