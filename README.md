# 👻 Modire ya Ghost yo Kurinda Umutekano
**Igikoresho cya PowerShell cyo Gukomerezaho Umutekano wa Windows na Azure**

> **Gukomerezaho umutekano mu buryo bwo gukingira kuri Windows endpoints na Azure.** Ghost itanga imikorere ya PowerShell yo gukomerezaho umutekano ishobora gufasha kugabanya inzira zisanzwe zo gutera hakoreshejwe guhagarika serivisi n'imigendekere itakenewe.

## ⚠️ Ibyitonderwa Ngenderwaho

**IKIZAMINI NI NGOMBWA**: Buri gihe gera Ghost mu buryo butari ubwo mukora mbere. Guhagarika serivisi birashobora kugira ingaruka ku mirimo yemewe y'ubucuruzi.

**NTA GARANTI**: Nubwo Ghost yibanda ku nzira zisanzwe zo gutera, nta gikoresho cy'umutekano gishobora kubuza ibitero byose. Iyi ni kimwe mu bigize ingamba zuzuye zo kurinda umutekano.

**INGARUKA KU MIKORERE**: Imwe mu mikorere irashobora kugira ingaruka ku mikorere ya sisitemu. Subiragamo buri gahunda mbere yo gutangiza.

**ISUZUMA RY'ABAHANGA**: Ku buryo bwo gukora, ganira n'inzobere mu mutekano kugira ngo wemeze ko amabwiriza ahuye n'ibikenewe n'umuryango wawe.

## 📊 Ibijyanye n'Umutekano

Ibyangijwe na Ransomware byageze kuri **miliyari 57 za amadolari muri 2025**, ubushakashatsi bwerekana ko ibitero byinshi byatsinze bikoresha serivisi zisanzwe za Windows hamwe no gutandukanya amabwiriza. Inzira zisanzwe zo gutera zirimo:

- **90% by'ibintu bya ransomware** birimo gukoresha nabi RDP
- **Intege nke za SMBv1** zatumye habaho ibitero nka WannaCry na NotPetya
- **Macro z'inyandiko** zikomeje kuba uburyo nyamukuru bwo gutanga malware
- **Ibitero bishingiye kuri USB** bikomeje kugisha imbaraga kuri air-gapped networks
- **Gukoresha nabi PowerShell** byiyongereye cyane mu myaka yashize

## 🛡️ Imikorere ya Ghost yo Kurinda Umutekano

Ghost itanga **imikorere 16 yo gukomerezaho Windows** hamwe no **guhuza umutekano wa Azure**:

### Gukomerezaho Windows Endpoint

| Imikorere | Intego | Ibyitonderwa |
|----------|---------|----------------|
| `Set-RDP` | Igenzura kwinjira kuri Remote Desktop | Bishobora kugira ingaruka ku micungire kure |
| `Set-SMBv1` | Igenzura protocol ya SMB ya kera | Bikenewe kuri sisitemu zishaje cyane |
| `Set-AutoRun` | Igenzura AutoPlay/AutoRun | Bishobora kugira ingaruka ku bukoreshwa bworoshye |
| `Set-USBStorage` | Ibuza ibikoresho byo kubika USB | Bishobora kugira ingaruka ku gukoresha USB byemewe |
| `Set-Macros` | Igenzura gukora macro muri Office | Bishobora kugira ingaruka ku nyandiko zifite macro |
| `Set-PSRemoting` | Igenzura PowerShell remoting | Bishobora kugira ingaruka ku micungire kure |
| `Set-WinRM` | Igenzura Windows Remote Management | Bishobora kugira ingaruka ku micungire kure |
| `Set-LLMNR` | Igenzura protocol yo gukemura amazina | Muri rusange ni byiza kuyihagarika |
| `Set-NetBIOS` | Igenzura NetBIOS hejuru ya TCP/IP | Bishobora kugira ingaruka kuri porogaramu za kera |
| `Set-AdminShares` | Igenzura shares z'ubuyobozi | Bishobora kugira ingaruka ku kwinjira kuri dosiye kure |
| `Set-Telemetry` | Igenzura gukusanya amakuru | Bishobora kugira ingaruka ku bushobozi bwo gusuzuma |
| `Set-GuestAccount` | Igenzura konti y'abashyitsi | Muri rusange ni byiza kuyihagarika |
| `Set-ICMP` | Igenzura ibisubizo bya ping | Bishobora kugira ingaruka ku isuzuma rya network |
| `Set-RemoteAssistance` | Igenzura Remote Assistance | Bishobora kugira ingaruka ku mikorere ya help desk |
| `Set-NetworkDiscovery` | Igenzura kubona network | Bishobora kugira ingaruka ku kureberera network |
| `Set-Firewall` | Igenzura Windows Firewall | Ni ngombwa ku mutekano wa network |

### Umutekano wa Azure Cloud

| Imikorere | Intego | Ibisabwa |
|----------|---------|--------------|
| `Set-AzureSecurityDefaults` | Ikora umutekano wa Azure AD wa shingiro | Uruhushya rwa Microsoft Graph |
| `Set-AzureConditionalAccess` | Itegura politiki yo kwinjira | Uruhushya rwa Azure AD P1/P2 |
| `Set-AzurePrivilegedUsers` | Isuzuma konti zifite uburenganzira bwihariye | Uruhushya rwa Global Admin |

### Amahitamo yo Gutangiza mu Bikorwa Binini

| Uburyo | Ikoreshwa | Ibisabwa |
|--------|----------|--------------|
| **Gukora Gutya** | Ikizamini, ibidukikije bito | Uburenganzira bwa admin bwaho |
| **Group Policy** | Ibidukikije bya domain | Admin wa domain, gucunga GP |
| **Microsoft Intune** | Ibikoresho byacungwa na cloud | Uruhushya rwa Intune, Graph API |

## 🚀 Gutangira Vuba

### Isuzuma ry'Umutekano
```powershell
# Kiriza modire ya Ghost
IEX(Invoke-WebRequest 'https://raw.githubusercontent.com/jimrtyler/Ghost/main/Ghost.ps1')

# Suzuma imiterere y'umutekano y'ubu
Get-Ghost
```

### Gukomerezaho kw'Ibanze (Gera Mbere)
```powershell
# Gukomerezaho ngombwa - mbere gera mu bidukikije bya laboratwari
Set-Ghost -SMBv1 -AutoRun -Macros

# Subiramo impinduka
Get-Ghost
```

### Gutangiza mu Bikorwa Binini
```powershell
# Gutangiza Group Policy (ibidukikije bya domain)
Set-Ghost -SMBv1 -AutoRun -GroupPolicy

# Gutangiza Intune (ibikoresho byacungwa na cloud)
Set-Ghost -SMBv1 -RDP -USBStorage -Intune
```

## 📋 Uburyo bwo Gushyiraho

### Ihitamo 1: Gupakurura Gutya (Ikizamini)
```powershell
IEX(Invoke-WebRequest 'https://raw.githubusercontent.com/jimrtyler/Ghost/main/Ghost.ps1')
```

### Ihitamo 2: Gushyiraho Modire
```powershell
# Shyiraho kuva kuri PowerShell Gallery (iyo iboneka)
Install-Module Ghost -Scope CurrentUser
Import-Module Ghost
```

### Ihitamo 3: Gutangiza mu Bikorwa Binini
```powershell
# Koporora ahantu ha network kugira ngo utangize Group Policy
# Shiraho scripts za PowerShell za Intune kugira ngo utangize cloud
```

## 💼 Ingero z'Ibikoreshwa

### Ubucuruzi Buto
```powershell
# Uburinda bw'ibanze hamwe n'ingaruka nke
Set-Ghost -SMBv1 -AutoRun -Macros -ICMP
```

### Ibidukikije by'Ubuzima
```powershell
# Gukomerezaho kwibanda kuri HIPAA
Set-Ghost -SMBv1 -RDP -USBStorage -AdminShares -Telemetry
```

### Serivisi z'Imari
```powershell
# Imiterere y'umutekano wa hejuru
Set-Ghost -RDP -SMBv1 -AutoRun -USBStorage -Macros -PSRemoting -AdminShares
```

### Umuryango Wibanda kuri Cloud
```powershell
# Gutangiza kuri Intune
Connect-IntuneGhost -Interactive
Set-Ghost -SMBv1 -RDP -AutoRun -Macros -Intune
```

## 🔍 Ibisobanuro by'Imikorere

### Imikorere y'Ibanze yo Gukomerezaho

#### Serivisi za Network
- **RDP**: Ibuza kwinjira kuri remote desktop cyangwa ikora port itunguranye
- **SMBv1**: Ihagarika protocol ya kera yo gusangira dosiye
- **ICMP**: Ibuza ibisubizo bya ping ku makuru yo gukusanya amakuru
- **LLMNR/NetBIOS**: Ibuza protocol za kera zo gukemura amazina

#### Umutekano wa Porogaramu
- **Macros**: Ihagarika gukora macro muri porogaramu za Office
- **AutoRun**: Ibuza gukora mu buryo bwikora kuva kuri media ishobora gukurwaho

#### Icungamutungo kure
- **PSRemoting**: Ihagarika ibiganiro bya PowerShell kure
- **WinRM**: Ihagarika Windows Remote Management
- **Remote Assistance**: Ibuza guhuza Remote Assistance

#### Kugenzura Kwinjira
- **Admin Shares**: Ihagarika shares za C$, ADMIN$
- **Guest Account**: Ihagarika kwinjira kuri konti y'abashyitsi
- **USB Storage**: Ibuza gukoresha ibikoresho bya USB

### Guhuza Azure
```powershell
# Huza na tenant ya Azure
Connect-AzureGhost -Interactive

# Kora umutekano wa mburabuzi
Set-AzureSecurityDefaults -Enable

# Shiraho kwinjira bisabwa
Set-AzureConditionalAccess -BlockLegacyAuth -RequireMFA

# Suzuma abakoresha bafite uburenganzira bwihariye
Set-AzurePrivilegedUsers -AuditOnly
```

### Guhuza Intune (Gishya muri v2)
```powershell
# Huza na Intune
Connect-IntuneGhost -Interactive

# Tangiza ukoresheje politiki za Intune
Set-IntuneGhost -Settings @{
    RDP = $true
    SMBv1 = $true
    USBStorage = $true
    Macros = $true
}
```

## ⚠️ Ibyitonderwa by'Akamaro

### Ibisabwa by'Ikizamini
- **Ibidukikije bya Laboratwari**: Mbere gera amabwiriza yose mu bidukikije bitandukanyije
- **Gutangiza Icyiciro** | Tangiza buhoro buhoro kugira ngo umenye ibibazo
- **Gahunda yo Gusubira Inyuma**: Emeza ko ushobora gusubiza inyuma impinduka iyo bikenewe
- **Inyandiko**: Andika amabwiriza akora mu bidukikije byawe

### Ingaruka Zishobora Kubaho
- **Umusaruro w'Abakoresha**: Amabwiriza amwe ashobora kugira ingaruka ku mirimo ya buri munsi
- **Porogaramu za Kera**: Sisitemu zishaje zirashobora gukeneye protocol runaka
- **Kwinjira kure**: Tekereza ku ngaruka ku micungire yemewe kure
- **Ibikorwa by'Ubucuruzi**: Emeza ko amabwiriza atagira nabi ibikorwa ngenderwaho

### Imipaka y'Umutekano
- **Kurinda mu Bujyakuzimu**: Ghost ni urwego rumwe rw'umutekano, ntabwo ari igisubizo cyuzuye
- **Imicungire Ikomeje**: Umutekano ukeneye gukurikiranwa no kuvugururwa buri gihe
- **Imyitozo y'Abakoresha**: Igenzura rya tekiniki rigomba guhuza no kumenyekana umutekano
- **Ubwitonzi bw'Iterabwoba**: Uburyo bushya bwo gutera bushobora kurenza kurinda kwa none

## 🎯 Ingero z'Ibintu by'Igitero

Nubwo Ghost yibanda ku nzira zisanzwe zo gutera, kubungabunga ukomeye biterwa n'ishyirwa mu bikorwa neza no kugerageza:

### Ibitero bya WannaCry
- **Gukemura**: `Set-Ghost -SMBv1` ihagarika protocol ifite intege nke
- **Ibyitonderwa**: Emeza ko nta sisitemu ya kera ikeneye SMBv1

### Ransomware ishingiye kuri RDP
- **Gukemura**: `Set-Ghost -RDP` ibuza kwinjira kuri remote desktop
- **Ibyitonderwa**: Birashobora gukeneye uburyo bubandi bwo kwinjira kure

### Malware ishingiye ku Nyandiko
- **Gukemura**: `Set-Ghost -Macros` ihagarika gukora macro
- **Ibyitonderwa**: Birashobora kugira ingaruka ku nyandiko zifite macro zemewe

### Iterabwoba ritangwa na USB
- **Gukemura**: `Set-Ghost -USBStorage -AutoRun` ibuza imikorere ya USB
- **Ibyitonderwa**: Birashobora kugira ingaruka ku gukoresha ibikoresho bya USB byemewe

## 🏢 Ibintu by'Ibikorwa Binini

### Inkunga ya Group Policy
```powershell
# Koresha amabwiriza ukoresheje registeri ya Group Policy
Set-Ghost -SMBv1 -RDP -AutoRun -GroupPolicy

# Amabwiriza akoreshwa muri domain yose nyuma yo kuvugurura GP
gpupdate /force
```

### Guhuza Microsoft Intune
```powershell
# Kora politiki za Intune ku mabwiriza ya Ghost
Set-IntuneGhost -Settings $GhostSettings -Interactive

# Politiki zitangizwa mu buryo bwikora ku bikoresho byacungwa
```

### Raporo y'Ubwubahirize
```powershell
# Kora raporo y'isuzuma ry'umutekano
Get-Ghost | Export-Csv -Path "SecurityAudit-$(Get-Date -Format 'yyyy-MM-dd').csv"

# Raporo y'imiterere y'umutekano wa Azure
Get-AzureGhost | Out-File "AzureSecurityReport.txt"
```

## 📚 Ibyiza byiza

### Mbere yo Gutangiza
1. **Andika Imiterere y'Ubu**: Koresha `Get-Ghost` mbere y'impinduka
2. **Gerageza Neza**: Emeza mu bidukikije bitari ubwo mukora
3. **Tegura Gahunda yo Gusubira Inyuma**: Menya uburyo wo gusubiza inyuma buri gahunda
4. **Isuzuma ry'Ababifitemo Inyungu**: Emeza ko ibice by'ubucuruzi byemera impinduka

### Mu gihe cyo Gutangiza
1. **Uburyo bw'Ibice**: Mbere tangiza mu matsinda ya pilot
2. **Kurikirana Ingaruka**: Reba ibibazo by'abakoresha cyangwa ibibazo bya sisitemu
3. **Andika Ibibazo**: Andika ikibazo icyo ari cyo cyose kugira ngo bitumenyekane
4. **Menyesha Impinduka**: Menyesha abakoresha iterambere ry'umutekano

### Nyuma yo Gutangiza
1. **Isuzuma Rihoraho**: Koresha `Get-Ghost` buri gihe kugira ngo wemeze amabwiriza
2. **Vugurura Inyandiko**: Komeza imiterere y'umutekano ivuguruye
3. **Subiramo Imikorere**: Kurikirana ibintu bya umutekano
4. **Iterambere Rihoraho**: Hindura amabwiriza ukurikije iterabwoba

## 🔧 Gukemura Ibibazo

### Ibibazo Bisanzwe
- **Amakosa y'Uruhushya**: Emeza ko ufite ibiganiro bya PowerShell byashizweho
- **Iterana rya Serivisi**: Serivisi zimwe zishobora kuba zifitanye isano
- **Guhuza Porogaramu**: Gerageza hamwe na porogaramu z'ubucuruzi
- **Guhuza Network**: Emeza ko kwinjira kure gikomeje gukora

### Amahitamo yo Kugaruka
```powershell
# Ongera ukore serivisi runaka iyo bikenewe
Set-RDP -Enable
Set-SMBv1 -Enable
Set-AutoRun -Enable
Set-Macros -Enable
```

## 👨‍💻 Kuri Umwanditsi

**Jim Tyler** - Microsoft MVP kuri PowerShell
- **YouTube**: [@PowerShellEngineer](https://youtube.com/@PowerShellEngineer) (10,000+ abiyandikishije)
- **Newsletter**: [PowerShell.News](https://powershell.news) - Amakuru y'umutekano ya buri cyumweru
- **Umwanditsi**: "PowerShell for Systems Engineers"
- **Uburambe**: Imyaka myinshi ya automation ya PowerShell n'umutekano wa Windows

## 📄 Uruhushya n'Ibyangombwa

### Uruhushya rwa MIT
Ghost itangwa munsi y'uruhushya rwa MIT ku gukoresha ubuntu, guhindura, no gukwirakwiza.

### Ibyangombwa ku Mutekano
- **Nta Garanti**: Ghost itangwa "nk'uko iri" nta garanti yo mu bwoko ubwo ari bwo bwose
- **Ikizamini Ni Ngombwa**: Buri gihe gera mbere mu bidukikije bitari ubwo mukora
- **Ubuyobozi bw'Inzobere**: Ku gutangiza mu bikorwa, ganira n'inzobere mu mutekano
- **Ingaruka ku Mikorere**: Abanditsi ntibazabazwa ku mikorere yose ihagaritswe
- **Umutekano w'Ibanze**: Ghost ni igice cy'ingamba zuzuye z'umutekano

### Inkunga
- **Ibibazo bya GitHub**: [Menyesha bugs cyangwa usabe ibikorwa](https://github.com/jimrtyler/Ghost/issues)
- **Inyandiko**: Koresha `Get-Help <function> -Full` ku bufasha burambuye
- **Umuryango**: Amahuriro ya PowerShell n'umutekano

---

**🔒 Komeza imiterere y'umutekano wawe ukoresheje Ghost - ariko buri gihe gera mbere.**

```powershell
# Tangira n'isuzuma, ntabwo ari ibitekerezo
Get-Ghost
```

**⭐ Niba Ghost yafashije mu gutezimbere imiterere y'umutekano wawe, tanga iki repository inyenyeri!**