1. 테스트 코드의 중요성 
   - 버그를 사전에 차단 가능
   - 가능 추가 및 리팩토링 가능 
   - 요구사항 적용을 빠르게 가능
   - 빠른 시간 내 개발 가능
   
2. Kotlin 을 사용할 수 있는 환경 구축 
   - plugin 설정 및 의존성 설정 하기 (build.gradle)
   - 사용하고 있는 JDK 버전 일치 
   
   ```
   id 'org.jetbrains.kotlin.jvm' version '1.6.21'
   implementation 'org.jetbrains.kotlin:kotlin-stdlib-jdk8'
   ```
  
   ```
   compileKotlin {
      kotlinOptions {
         jvmTarget = "11"
      }
   }
   ```
   ```
   compileTestKotlin {
     kotlinOptions {
        jvmTarget = "11"
     }
   }
   ```
   
3. Kotlin 패키지 생성 (기 java 와 동일하게 셋팅)
   - Kotlin 용 디렉토리 생성 시, Mark Directory As 설정 이 안되어 있다면, 별도 설정 가능
