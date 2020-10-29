[0] Wins
[1] Losses
[2] Kills
[3] Deaths
[4] TimePlayed (in seconds)

```
Operator ID: 5:5
Operator: Bandit
Type: Defender

Operator ID: 2:7
Operator: Blackbeard
Type: Attacker

Operator ID: 2:5
Operator: Blitz
Type: Attacker

Operator ID: 2:6
Operator: Buck
Type: Attacker

Operator ID: 2:8
Operator: Capitao
Type: Attacker

Operator ID: 2:2
Operator: Castle
Type: Defender

Operator ID: 3:8
Operator: Caveira
Type: Defender

Operator ID: 3:10
Operator: Clash
Type: Defender

Operator ID: 2:3
Operator: Doc
Type: Defender

Operator ID: 2:D
Operator: Dokkaebi
Type: Attacker

Operator ID: 3:9
Operator: Echo
Type: Defender

Operator ID: 2:C
Operator: Ela
Type: Defender

Operator ID: 4:E
Operator: Finka
Type: Attacker

Operator ID: 5:2
Operator: Thermite
Type: Attacker

Operator ID: 3:4
Operator: Fuze
Type: Attacker

Operator ID: 2:4
Operator: Glaz
Type: Attacker

Operator ID: 2:15
Operator: Goyo
Type: Defender

Operator ID: 3:12
Operator: Gridlock
Type: Attacker

Operator ID: 2:9
Operator: Hibana
Type: Attacker

Operator ID: 3:5
Operator: Iq
Type: Attacker

Operator ID: 2:A
Operator: Jackal
Type: Attacker

Operator ID: 4:5
Operator: Jager
Type: Defender

Operator ID: 3:11
Operator: Kaid
Type: Defender

Operator ID: 3:6
Operator: Frost
Type: Defender

Operator ID: 3:1
Operator: Mute
Type: Defender

Operator ID: 3:7
Operator: Valkyrie
Type: Defender

Operator ID: 3:C
Operator: Zofia
Type: Attacker

Operator ID: 2:B
Operator: Ying
Type: Attacker

Operator ID: 2:14
Operator: Warden
Type: Defender

Operator ID: 3:D
Operator: Vigil
Type: Defender

Operator ID: 4:3
Operator: Twitch
Type: Attacker

Operator ID: 5:1
Operator: Thatcher
Type: Attacker

Operator ID: 5:4
Operator: Tachanka
Type: Defender

Operator ID: 2:1
Operator: Smoke
Type: Defender

Operator ID: 4:1
Operator: Sledge
Type: Attacker

Operator ID: 3:3
Operator: Rook
Type: Defender

Operator ID: 4:2
Operator: Pulse
Type: Defender

Operator ID: 2:13
Operator: Nokk
Type: Attacker

Operator ID: 2:11
Operator: Nomad
Type: Attacker

Operator ID: 2:12
Operator: Mozzie
Type: Defender

Operator ID: 5:3
Operator: Montagne
Type: Attacker

Operator ID: 3:A
Operator: Mira
Type: Defender

Operator ID: 2:10
Operator: Maverick
Type: Attacker

Operator ID: 2:F
Operator: Maestro
Type: Defender

Operator ID: 3:E
Operator: Lion
Type: Attacker

Operator ID: 3:B
Operator: Lesion
Type: Defender

Operator ID: 2:1A
Operator: Melusi
Type: Defender

Operator ID: 4:17
Operator: Ace
Type: Attacker

Operator ID: 1:1B
Operator: Zero
Type: Attacker

Operator ID: 4:4
Operator: Kapkan
Type: Defender

Operator ID: 2:19
Operator: Iana
Type: Attacker

Operator ID: 2:18
Operator: Oryx
Type: Defender

Operator ID: 2:17
Operator: Kali
Type: Attacker

Operator ID: 3:17
Operator: Wamai
Type: Defender

Operator ID: 3:F
Operator: Alibi
Type: Defender

Operator ID: 2:16
Operator: Amaru
Type: Attacker

Operator ID: 3:2
Operator: Ash
Type: Attacker
```

Script:
```js
const jsonResp = {...}
let response = ""
Object.keys(jsonResp.operators).forEach(op => {
    const opObject = jsonResp.operators[op]
    response += `Operator ID: ${opObject.id}\nOperator: ${op}\nType: ${opObject.type == "atk" ? "Attacker" : "Defender"}\n\n`
})
console.log(response)
```
