[MAheui](../) / [CLI](./README.md/)

# MAheui CLI

마희 CLI에 대한 명세입니다. (알파희/아희++ 와의 호환성을 고려합니다.)

## Sub Commands

 * --aheui-compat -A<br>
   아희 호환 모드로 가동합니다.
 * --help         -h<br>
   해당 구현체에 대한 도움말을 띄웁니다.
 * --version      -v<br>
   현재 구현체의 버전 및 마희 버전을 띄웁니다.
 * --optimize     -O<br>
   최적화 수치를 설정합니다.<br>
   0: 최적화 없음.<br>
   1: 간단한 스택크기 추정으로 빠르게 쓰이지 않는 코드를 제거하고 상수 연산을 병합합니다.<br>
   2: 스택크기 추정으로 완벽하게 쓰이지 않는 코드를 제거하고, 코드 조각을 직렬화해 재배치하고, 상수 연산을 병합합니다.<br>
   사용법: --optimize=0, -O1 or -O 2
 * --source       -S<br>
   소스 코드 종류를 설정합니다. 기본 값은 auto입니다.
   auto: 소스 유형을 추측합니다. 파일이름이 .aheuic이거나 바이트코드 종료 패턴이 담겨 있으면 bytecode로 추측합니다. 파일이름이 .aheuis이면 asm으로 추측합니다. 파일이름이 .aheui이면 text로 추정합니다. 추정할 수 없으면 text로 추정합니다.<br>
   bytecode: 마희 바이트코드. (마셈블리의 바이트코드 표현형)<br>
   asm: 맣셈블리 참고<br>
   사용법: --source=asm, -Sbytecode or -S text
 * --target       -T<br>
   결과물 유형. 기본값은 run입니다. run, bytecode, asm 가운데 하나를 쓸 수 있습니다.<br>
   run: 주어진 코드를 실행합니다.<br>
   bytecode: 마희 바이트코드. (맣셈블리의 바이트코드 표현형)<br>
   asm: 맣셈블리 참고<br>
   usage: --target=asm, -Tbytecode or -T run
 * --output       -o<br>
   결과물 파일. 기본값은 아래와 같습니다. 각 결과물 유형에 따라 자세한 내용을 확인하세요.<br>
   `-` 이면 표준 출력입니다.<br>
   `run` 이 옵션은 무시됩니다.<br>
   `bytecode` 기본 값은 .aheuic 파일입니다.<br>
   `asm` 기본 값은 .aheuis 파일입니다.<br>
   --target=asm+comment: asm에 주석이 추가됩니다.
 * --cmd          -c<br>
   코드를 파일 대신 문자열로 받아 넘겨줍니다.
 * --strict       -s<br>
   코드를 엄격하게 실행합니다.<br>
   표준에서 예외 처리하는 모든 것은 실제로 오류를 던집니다.
 * --repl         -R<br>
   마희 REPL을 실행합니다.
