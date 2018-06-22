[MAheui](../) / [맣셈블리](./README.md/)

# MAhsembly

직렬화된 마희 코드입니다. 알파희와의 호환성을 위해 일단 알파희의 앟셈블리 스펙을 그대로 사용합니다.

원시 명령

 * halt: ㅎ
 * add: ㄷ
 * mul: ㄸ
 * sub: ㅌ
 * div: ㄴ
 * mod: ㄹ
 * pop: ㅁ without ㅇ/ㅎ
 * popnum: ㅁ with ㅇ
 * popchar: ㅁ with ㅎ
 * push $v: ㅂ without ㅇ/ㅎ. Push THE VALUE $v. $v is not an index of consonants.
 * pushnum: ㅂ with ㅇ
 * pushchar: ㅂ with ㅎ
 * dup: ㅃ
 * swap: ㅍ
 * sel $v: ㅅ. $v is always an integer order of final consonants.
 * mov $v: ㅆ. $v is always an integer order of final consonants.
 * cmp: ㅈ
 * brz $v: ㅊ. If a popped value is zero, program counter is set to $v; otherwise +1.

확장 명령 (선형 코드는 위치 정보를 잃고 일부 명령이 스택 크기 점검을 하지 않으므로 추가 명령 필요)

 * brpop2 $v: If current stack doesn't have 2 values to pop, program counter is set to $v; otherwise +1.
 * brpop1 $v: If current stack doesn't have 1 values to pop, program counter is set to $v; otherwise +1.
 * jmp $v: Program counter is set to $v.
