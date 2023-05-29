# EmuELEC 사용자를 위한 ScummVM 한글화 패치

각 폴더 안의 README.md 파일을 확인해 주세요</br>
게임롬은 제공되지 않습니다</br>
EmuELEC에서 ScummVM의 게임 설치는 [EmuELEC Wiki](https://github.com/british-choi/EmuELEC/wiki/ScummVM-%EA%B2%8C%EC%9E%84-%EC%84%A4%EC%B9%98)를 참조하세요

|게임명|발매일|폴더|
|--|--|--|
|매니악 맨션|1988|[Maniac Mansion (DOS)](https://github.com/british-choi/ScummVM-Kor-Trs/tree/master/Maniac%20Mansion%20(DOS))|
|작의 모험 Enhanced|1988|[Zak McKracken Enhanced Version (DOS)](https://github.com/british-choi/ScummVM-Kor-Trs/tree/master/Zak%20McKracken%20Enhanced%20Version%20(DOS))|
|매니악 맨션 Enhanced|1989|[Maniac Mansion Enhanced Version (DOS)](https://github.com/british-choi/ScummVM-Kor-Trs/tree/master/Maniac%20Mansion%20Enhanced%20Version%20(DOS))|
|인디아나 존스 3 최후의 성전|1989|[Indiana Jones and the Last Crusade (FLOPPY/VGA/DOS)](https://github.com/british-choi/ScummVM-Kor-Trs/tree/master/Indiana%20Jones%20and%20the%20Last%20Crusade%20(Floppy%20DOS%20VGA))|
|룸|1990|[Loom (CD DOS VGA)](https://github.com/british-choi/ScummVM-Kor-Trs/tree/master/Loom%20(CD%20DOS%20VGA))|
|작의 모험|1991|[Zak McKracken (FM-TOWNS)](https://github.com/british-choi/ScummVM-Kor-Trs/tree/master/Zak%20McKracken%20(FM-Town))|
|룸|1991|[Loom (CD FM-TOWNS)](https://github.com/british-choi/ScummVM-Kor-Trs/tree/master/Loom%20(CD%20FM-TOWNS))|
|인디아나 존스 4 - 아틀란티스의 운명|1992|[Indiana Jones and the Fate of Atlantis (CD DOS)](Indiana%20Jones%20and%20the%20Fate%20of%20Atlantis%20(CD%20DOS))|
|샘 & 맥스 히트 더 로드|1993|[Sam & Max Hit the Road (CD DOS)](https://github.com/british-choi/ScummVM-Kor-Trs/tree/master/Sam%20%26%20Max%20Hit%20the%20Road%20(CD%20DOS))|
|풀 쓰로틀|1995|[Full Throttle (DOS)](https://github.com/british-choi/ScummVM-Kor-Trs/tree/master/Full%20Throttle%20(DOS))|
|원숭이섬의 비밀 Ultimate Talkie Edition|2009|[The Secret Of Monkey Island (Ultimate Talkie Edition DOS)](https://github.com/british-choi/ScummVM-Kor-Trs/tree/master/The%20Secret%20Of%20Monkey%20Island%20(Ultimate%20Talkie%20Edition%20DOS))|
|원숭이섬2 Ultimate Talkie Edition|2010|[Monkey Island 2 (Ultimate Talkie Edition/DOS)](https://github.com/british-choi/ScummVM-Kor-Trs/tree/master/Monkey%20Island%202%20(Ultimate%20Talkie%20Edition%20DOS))|

<br>

## 한글판 EmuELEC 개발자가 ScummVM 한글화 패치를 만들게 된 이유

개발자는 ScummVM이 뭐하는 것인지도 모르고 있었을 때가 있었습니다. 당연히 어떻게 실행하는지 관심도 없었고 (시간이 없어서 게임을 거의 안해요) 그러다 한글 패치 ScummVM 게임에 대한 문의가 와서 어떤 게임들이 있고, 어떤 방식으로 rom을 넣는 지 찾아보기 시작했습니다.<br>
한글 패치에는 V1 방식 V2 방식 이런 것이 있었고, V1 방식으로된 패치는 EmuELEC에서 구동이 불가능하다는 사실을 알았습니다. ScummVM용 한글 패치 게임이 V1 전용으로만 나온 것이 있고, V1 / V2 모두 제공되는 방식이 있었기 때문에 V1 전용 게임을 EmuELEC에서 구동하기 위해서는 ScummVM-Kor 을 core로 사용해야 한다는 제한이 있었습니다. ScummVM-Kor은 이미 개발이 중단되어 더이상 Update가 되고 있지 않고 있었습니다. 그리고 V1 게임을 ScummVM Official 에서 구동시키기 위해서 분석하던 중 korean.trs 파일을 사용해서 Fan translation 을 작성할 수 있다는 것을 알아내었고, 관련 코드를 작성하신 분이 한국인이라는 것을 확인했습니다. 추적끝에 해당 코드를 작성하신 원스타님께 메일을 보내서 어떻게 사용하는지 문의하였고, 몇몇 번역은 이미 번역 파일을 만들었지만, 공개하지 않아서 사용되고 있지 않아서 아무도 모르는 상태였던 것입니다.<br>
결국은 EmuELEC에서 V1 전용 한글패치를 사용할 수 있도록 하기 위한 프로젝트 였습니다. 현재는 작의 모험을 제외(30% 정도 번역한 것이 있는 것으로 아는데, 입수하지 못했습니다)한 거의 대부분의 V1 전용 한글 패치는 korean.trs 파일로 변환해서 Upload 하였습니다.<br>
많은 분들의 노력으로 인해 국내 게임 유저들이 즐겁게 게임을 할 수 있습니다.<br>
자료를 공개해 주신 많은 분들께 감사드립니다.<br>
<br>
## 한글화 FM-TOWN 구동을 위한 Windows용 ScummVM 
ScummVM에서 FM-TOWN은 일본어만 지원되도록 구현되어 있습니다. 그래서 EmuELEC이 아닌 다른 Platform에서 FM-TOWN용 한글화 패치 적용시 정상적인 구동이 되지 않았습니다. 간혹 Windows에서 ScummVM으로 게임을 하시는 분들이 FM-TOWN용 한글화 패치를 사용할 수 없어서 아쉬워 하던 부분을 해결하기 위해 Windows용으로도 Build 하였습니다. 이제 Windows에서도 한글화된 FM-TOWN용 게임을 즐기시길 바랍니다.<br>
[scummvm-2.7.0-win32-x86_64.zip](https://github.com/british-choi/ScummVM-Kor-Trs/blob/master/scummvm-2.7.0-win32-x86_64.zip)
