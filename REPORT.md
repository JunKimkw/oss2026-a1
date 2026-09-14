# A1 리포트

- 이름: 김준영
- 학번: 2023202012 
- GitHub ID: JunKimkw

## 어디를 둘러봤는지

awesome-nodejs에서 Weird와 Mad science 카테고리를 찾아봤다. 그리고 터미널에서는 npm search "cli table", npm search "ascii art" 같은 검색어를 시도해봤다. npmjs.com에서 몇몇 패키지의 Keywords 링크를 눌러 비슷한 패키지들도 같이 살펴봤다.

---

## 선정한 패키지

### 1. `cows`

**선정 이유:**
선정 이유: awesome-nodejs의 "Weird" 카테고리에서 봤는데, "400개가 넘는 ASCII 소 그림"이라는 설명이 재밌어서 골랐다.

**이것으로 무엇을 할 수 있을지:**
CLI 도구에 랜덤 마스코트를 붙이는데 쓸 수 있을 것 같다. 예를 들어 빌드나 테스트가 끝났을 때 소 그림을 출력해주는 장난스러운 스크립트를 만들어볼 수 있을 것 같다.

**확인 결과:**

```
$ npm view cows version time.modified license dependencies
version = '3.0.1'
time.modified = '2024-07-26T23:52:34.584Z'
license = 'MIT'

$ npm view cows deprecated

```

**출력을 보고 알게 된 것:**
time.modified가 배포일이 아니라고 해서 npm view cows time --json으로 실제 배포일을 따로 확인해보니 최신 버전(3.0.1)이 2024-07-26에 발행된 것으로 나왔다. time.modified와 실제 배포일이 거의 같았다. 라이선스도 MIT로 명확하고 deprecated 표시도 없어서 최근까지 관리되고 있는 패키지라고 봐도 될 것 같다.

---

### 2. `stegcloak`

**선정 이유:**
겉보기엔 평범한 문자열인데 그 안에 암호화된 메시지를 숨길 수 있다는 설명이 신기해서 골랐다. 문자를 숨길 수 있다는 점이 뭔가 이용할 수 있는 부분이 많아 보이기도 했다.

**이것으로 무엇을 할 수 있을지:**
친구에게 보내는 메시지 안에 눈에 안 보이는 힌트를 숨겨서 보내는 간단한 방탈출 게임 같은 걸 만들어볼 수 있을 것 같다. 실제로 안전한 암호화인지는 모르겠지만 개념 자체가 재밌다.

**확인 결과:**

```
$ npm view stegcloak version time.modified license dependencies
version = '1.1.1'
time.modified = '2022-05-18T17:20:59.112Z'
license = 'MIT'
dependencies = {
  'browserify-cipher': '^1.0.1',
  chalk: '^4.0.0',
  clipboardy: '^2.3.0',
  commander: '^5.1.0',
  'create-hmac': '^1.1.7',
  'crypto-browserify': '^3.12.0',
  inquirer: '^7.1.0',
  jsonfile: '^6.0.1',
  lzutf8: '^0.5.5',
  ora: '^4.0.4',
  pbkdf2: '^3.0.17',
  ramda: '^0.27.0',
  randombytes: '^2.1.0',
  'safe-buffer': '^5.2.0',
  'timing-safe-equal': '^1.0.0'
}

$ npm view stegcloak deprecated

```

**출력을 보고 알게 된 것:**
time.modified는 2022년으로 나오지만, time --json으로 확인한 결과 실제 마지막 배포일은 2020-06-20이었다. 마지막 배포가 오래전이라 지금도 관리되는 패키지는 아닌 것 같다. 그래도 deprecated는 아니고 MIT 라이선스라서 기능이 어느 정도 완성돼서 업데이트를 안 하는 경우일 수도 있다고 생각했다. 다만 의존성이 15개나 되고 그중 다수가 오래된 버전에 고정돼 있어서 실제로 설치하면 보안 경고가 뜰 가능성이 있어 보인다.

---

### 3. `nerds`

**선정 이유:**
해리포터, 스타워즈, 포켓몬 같은 "nerd"와 관련된 데이터를 준다는 설명이 특이하고 평소에 좋아하는 소재라서 골랐다. 특히 포켓몬 관련 데이터가 있다는 점이 마음에 들었다.

**이것으로 무엇을 할 수 있을지:**
퀴즈 앱이나 랜덤 캐릭터 뽑기 같은 프로젝트에서 활용할 수 있을 것 같다. 예를 들어 포켓몬이나 스타워즈 같은 데이터를 랜덤으로 하나씩 뽑아서 사용자에게 보여주는 프로그램을 만들거나 캐릭터 이름을 이용해서 간단한 퀴즈를 만드는 데 사용할 수 있을 것 같다.

**확인 결과:**

```
$ npm view nerds version time.modified license dependencies
version = '1.3.6'
time.modified = '2022-06-21T00:24:26.825Z'
license = 'MIT'
dependencies = { lodash: '4.13.1' }

$ npm view nerds deprecated

```

**출력을 보고 알게 된 것:**
time.modified만 보면 2022년이라 비교적 최근처럼 보이지만, time --json으로 확인한 실제 마지막 배포는 2016-07-26이었다. README에서 경고했던 "메타데이터만 갱신되어도 time.modified가 바뀐다"는 게 정확히 이 경우였다. lodash도 4.13.1이라는 옛날 버전 하나에 고정돼 있어서 9년째 방치된 패키지로 보인다. deprecated 표시는 없었지만 실제로 쓰려면 GitHub 저장소 상태를 한 번 더 확인해봐야 할 것 같다.

---

## 설치해본 패키지

```
$ npm install cows

$ node try.js
*_                     *_     ( oo             *_
  \      (__)            \    /\/                \  (__)
   \.----( oo____         \.-/----._____          \.( oo___\____
    ||____\/____ \         ||__________ \          |_\/________ \
    OO          `OO        OO          `OO         OO          `OO

                    Cow-vette Cow-vertible  (of cowrse)
```

---

## 막혔던 부분 (채점하지 않음)

처음에는 설치하고 바로 try.js를 실행했는데 아무것도 출력되지 않아서 패키지가 제대로 설치되지 않은 줄 알았다. 나중에 README를 다시 확인해보니 import만 하는 것이 아니라 함수를 호출해야 실제로 ASCII 소 그림이 출력된다는 것을 알게 되었다.

---

## AI 사용

Claude에게 다음과 같이 명령함: "npm에 어떤 패키지들이 있는지 둘러보고, 눈에 띈 것 10개를 골라줘 그리고 마지막으로 아직 관리가 되고있는 패키지인지 확인해줘."

AI의 설명과 실제 출력은 크게 다르지 않았지만, time.modified와 실제 배포일이 다를 수 있다는 점은 AI가 먼저 짚어주지 않았다면 지나쳤을 것 같다.
---

## 제출 전 확인

- [o] 저장소 이름이 `oss2026-a1`, 공개 범위가 Public
- [o] `git status` 결과가 `nothing to commit, working tree clean`
- [o] `node_modules` 폴더를 지우고 `npm install` → `node try.js` 를 다시 해도 실행됨
- [o] 마지막 커밋을 push함
