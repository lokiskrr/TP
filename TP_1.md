# TP1 : Plip plap votre OS
## Sommaire

- [TP1 : Plip plap votre OS](#tp1--plip-plap-votre-os)
  - [Sommaire](#sommaire)
- [I. Ressources de l'OS](#i-ressources-de-los)
  - [1. Programme, service, processus](#1-programme-service-processus)
  - [2. Mémoire et CPU](#2-mémoire-et-cpu)
  - [3. Stockage](#3-stockage)
  - [4. Réseau](#4-réseau)
  - [5. Utilisateurs](#5-utilisateurs)
  - [6. Random](#6-random)
  - [7. Ptit amusement](#7-ptit-amusement)
  

# I. Ressources de l'OS
## 1. Programme, service, processus

🌞 **Lister tous les processus en cours d'exécution sur votre machine**
```powershell
PS C:\Users\fatma> Get-Process

Handles  NPM(K)    PM(K)      WS(K)     CPU(s)     Id  SI Pr
                                                          oc
                                                          es
                                                          sN
                                                          am
                                                          e
-------  ------    -----      -----     ------     --  -- --
    169       9     2308       8524              3568   0 Ad
    232      15     3524      15872             16144   0 ae
    188      12     5064      12000              7056   0 Ag
    228      15    23120      18864       0.56  14304   1 ai
    222      16    48820      20664       1.66  15592   1 ai
    222      16    60440      48196      12.63  17056   1 ai
    405      23    14356      35116       0.39  14156   1 Ap
    314      33    18016       1596       0.14   1568   1 ba
    689      26   100024     110300     102.16   2600   1 ch
    210      13     9868      19956       0.33   3428   1 ch
   1694      54   110964     192772      70.70   7228   1 ch
    276      25   136412     169572       6.41   8960   1 ch
    416      30    99840     165836     134.58  10828   1 ch
    456      35   111328     156020     100.59  11120   1 ch
    235      19    13336      29616       0.19  13140   1 ch
    383      24    24356      49108       6.23  13236   1 ch
    190      10     6620       8296       0.06  15984   1 ch
    557      25     2204       6156               812   0 cs
    527      23     2736       6180               944   1 cs
    569      22     7936      29040      12.95  11044   1 ct
    336      18    26764      27256              3720   0 Cx
    283      10     2120       8804              3956   0 Cx
    171      10     1392       7696              4104   0 Cx
    272      11     3932      11356              4112   0 DA
    213      10     2348       9728              7088   1 DA
    764      29   265168     271236      43.73  12356   1 Di
    373      21    16616      53432       2.63  12396   1 Di
   1307     110   448180     355920     598.81  12756   1 Di
    280      16    12348      76568       0.13  13048   1 Di
   1114      47   103156     101948      14.36  13124   1 Di
    207      12    11456      32256       0.00  13208   1 Di
    421      25     7000      15968       0.80  10384   1 dl
    144       9     1804       9112       0.02  14840   1 dl
   1283      68   152732     116692              2176   1 dw
    123       8     1628       5872              4128   0 es
   5726     152   194784     290152     142.50   8568   1 ex
    464      23     9644      33164       0.41  13416   1 Fi
     42       6     1608       2884              1052   0 fo
     42       8     4056       5704              1492   1 fo
      0       0       60          8                 0   0 Id
    180      10     2092       8592              2828   0 ig
    974      22     6316      24388       1.56   8712   1 ig
    373      25    26992      19944              4272   0 In
    173       9     1560       7992              3712   0 In
    150       8     1404       7316              5504   0 In
    172      10     1500       7924              4484   0 jh
    243      17     5500      15656       0.20  10168   1 la
   1041      50    35428      47708              4176   0 Le
    224      12     3096       9992              4472   0 LM
    133       8     1512       6472              4396   0 LN
   1844      28     9612      25420              1016   0 ls
    989      66   132968      58416              4424   0 mc
    348      23     8116      22088       0.92   7760   1 mc
    280      19    11552      17404              7748   0 mc
      0       0     1452     335388              2760   0 Me
    512      29    27444       6556       0.67  10264   1 Mi
    348      20    16372      34384             14820   0 Mo
    456      16    12796      18304              4444   0 Mp
    216      17    14636      22428       0.13   9712   1 ms
    171      10     7460      15360       0.03  11164   1 ms
    280      21   136020      66904       8.03  11520   1 ms
   1359      44    57044     102964       2.84  11936   1 ms
    160       9     2072       7372       0.02  12004   1 ms
    377      18    26564      34640       0.08  12208   1 ms
    347      18    11500      31380       0.38  12220   1 ms
    700      28    79608      44392       3.34   1736   1 ms
    269      22    40636      12828       0.94   2536   1 ms
    175      10     9220       6500       0.27   6028   1 ms
    349      19    11632      19584       1.75  13556   1 ms
    498      59   448804     261012      61.22  14064   1 ms
   1379      49    53768      50160      11.78  14296   1 ms
    180       9     2072       7508       0.03  14332   1 ms
    274      23    55320      14116       0.91  14940   1 ms
    542      22    12640       6496       0.50  14968   1 ms
    230      14     7388       4328       0.45  15180   1 ms
    813     211   303912     180448              4644   0 Ms
   1243      47    63460      20868       2.17    500   1 ms
   1035      47    32340      29952       9.58  12796   1 ms
    228      12     4536      11636              9320   0 Ni
    706      26    36768      34344              4152   0 Of
    925      53    54176      95004       1.31  11348   1 On
    170      11     2364       9980       0.20   9384   1 Op
   1053     105    50136     135000       2.47  13016   1 Ph
    985      38   152452     169432       7.03  10144   1 po
    247      28    24748      18124              7864   0 Pr
    132       8     1384       5984              4500   0 Qc
      0      14     8388      35324               148   0 Re
    161       9     1584       7236              4536   0 Rs
    317      17     5600      21064       0.14   2592   1 Ru
    384      22     7188      28532       2.44   9892   1 Ru
    776      36    14412      49712       3.48   9992   1 Ru
    139       9     1992       9060       0.02  14104   1 Ru
    154      10     2148      10628       0.00  14288   1 Ru
    154      11     1360       7244              4568   0 SA
   1633     172   256448     119668      28.03   9756   1 Se
    753      19    16200      18296             10664   0 Se
    450      19     7400      18012              8256   0 Se
    188      10     1896       9860       0.05  10644   1 Se
    554      37    17944      30516              4432   0 se
    799      13     5656       9412               992   0 se
    828      36    22308      42416       1.08  16356   1 Sh
    654      21     6552      32640       6.16   7528   1 si
     58       4     1116       1116               608   0 sm
    451      24     5688      14172              3764   0 sp
    725      38    51612      81776       7.13   9780   1 St
   1299      24    11636      31564               680   0 sv
    340      19     4748      20592               748   0 sv
   1434      21     8580      16016              1128   0 sv
    325      12     2760       9856              1184   0 sv
    189      14     1976       7936              1572   0 sv
    193      13     2716      11148              1580   0 sv
    298      24     3252      12404              1588   0 sv
    193      10     2324       9884              1712   0 sv
    252      13     3004       9948              1720   0 sv
    269      10     1976       9468              1728   0 sv
    377      11     2760       9228              1816   0 sv
    283      11     3120      14980              1824   0 sv
    158      32     6276       7164              1900   0 sv
   1110      21     6284      15816              1992   0 sv
    174       9     1608       6728              2056   0 sv
    298      15     3884       8672              2132   0 sv
    386      21    28768      28876              2160   0 sv
    217      11     3072      11748              2304   0 sv
    416      14     3404      13856              2368   0 sv
    434      19     6936      15900              2448   0 sv
    194       7     1704       6052              2524   0 sv
    490      15    20820      16284              2584   0 sv
    231       8     1216       5796              2660   0 sv
    237      13     2496      11864              2668   0 sv
    183       9     1904       7268              2676   0 sv
    187      12     1912       7996              2804   0 sv
    208      10     1896       8420              2852   0 sv
    179      11     1952       8496              2864   0 sv
    166       9     1448       6956              2932   0 sv
    122       8     1320       6416              2964   0 sv
    338      15     3408      14920              3092   0 sv
    312      10    13944      18444              3164   0 sv
    238      11     2364       7616              3284   0 sv
    217      11     2276       9844              3292   0 sv
    465      13     2676       9604              3300   0 sv
    193      10     1864       7876              3440   0 sv
    558      26     6936      21136              3536   0 sv
    193      12     2228      10852              3560   0 sv
    295      26     4364      15724              3692   0 sv
    633      27    17488      33868              3704   0 sv
    304      18     6308      14096              3812   0 sv
    445      33    11380      15528              3824   0 sv
    571      22     8532      32976       3.08   3928   1 sv
    185      10     1792       7872              4040   0 sv
    270      14     2700       7876              4240   0 sv
    372      21     2800      10360              4248   0 sv
    251      12     2476       8908              4440   0 sv
    189      11     1996       8588              4592   0 sv
    136       8     1256       5776              4632   0 sv
    376      18     8008      18096              4660   0 sv
    410      19     4484      18640              4668   0 sv
    235      13     3064      12972              4788   0 sv
    283      14     2740      11660              4860   0 sv
    208      12     2256       9428              5228   0 sv
    135       9     1488       7632              5476   0 sv
    201      12     2188      10116              6068   0 sv
    318      15     4408      12852              6252   0 sv
    443      37    38940      34904              6668   0 sv
    149      10     2104       8984       0.52   7516   1 sv
    111       8     1328       6272       0.00   7636   1 sv
    213      15     1928       7176              7672   0 sv
    481      19    11372      26344       2.92   7880   1 sv
    159      42     1716       7024              7932   0 sv
    285      15     4424      19848              8316   0 sv
    244      12     2288      11940              8612   0 sv
    123       8     1224       5852              8744   0 sv
    419      23     5180      19676              8768   0 sv
    398      24     3516      12856              8992   0 sv
    301      15     4028      19664       0.41   9456   1 sv
    245      14     3356      13656              9936   0 sv
    254      15     3288      16660       0.25  10056   1 sv
    172       9     1676       7644             13232   0 sv
    590      17     7500      21836             14264   0 sv
    146       9     1704       9420       0.05  14272   1 sv
    274      15     3080      13508       0.08  14536   1 sv
    325      14     3500      14608             14744   0 sv
    440      20     6488      18532             15004   0 sv
    234      14     3496      10928             15400   0 sv
    202      11     2660      11660             15716   0 sv
    271      14     2960      15752       0.31  16052   1 sv
   4574       0       60       3004                 4   0 Sy
   1453      74   134140      13336       4.41   5192   1 Sy
    504      26     7536      27908       0.84  16816   1 Sy
    328      37     8084      19112       0.50   8228   1 ta
    556      27     8900      29852       0.56  15332   1 ta
    448      26    11432      22696       5.47   7632   1 ui
    141      10     1932       9776       0.03  17372   1 Us
    619      27     8008      35112       0.33   9824   1 Wi
    298      17     4688      19000       0.38   8904   1 Wi
    817      35    28212      85036      22.03   9488   1 Wi
    142      11     1432       6636               920   0 wi
    284      13     2680      11324              1440   1 wi
   1560      66   149360     254080      74.16   4548   1 WI
    343      15     5776      16320              1176   0 WU
    356      15     6400      10552              1272   0 WU
    226       8     1532       5456              1364   0 WU
```


🌞 **Trouver les 3 processus qui ont le plus petit identifiant**
```powershell
PS C:\Users\fatma> Get-Process | Sort-Object Id | Select-Object -First 3

Handles  NPM(K)    PM(K)      WS(K)     CPU(s)     Id  SI ProcessName
-------  ------    -----      -----     ------     --  -- -----------
      0       0       60          8                 0   0 Idle
   4573       0       60       3004                 4   0 System
      0      14     8392      35328               148   0 Registry
```

🌞 **Lister tous les services de la machine...**
```powershell
PS C:\Users\fatma> Get-Service | Where-Object { $_.Status -eq 'Running' }

Status   Name               DisplayName
------   ----               -----------
Running  AESMService        Intel® SGX AESM
Running  Appinfo            Informations d’application
Running  AppXSvc            Service de déploiement AppX (AppXSVC)
Running  AtherosSvc         AtherosSvc
Running  AudioEndpointBu... Générateur de points de terminaison...
Running  Audiosrv           Audio Windows
Running  BFE                Moteur de filtrage de base
Running  BluetoothUserSe... Service de support des utilisateurs...
Running  BrokerInfrastru... Service d’infrastructure des tâches...
Running  BTAGService        Service de passerelle audio Bluetooth
Running  BthAvctpSvc        Service AVCTP
Running  bthserv            Service de prise en charge Bluetooth
Running  camsvc             Service Gestionnaire d’accès aux fo...
Running  cbdhsvc_85b04      Service utilisateur du Presse-papie...
Running  CDPSvc             Service de plateforme des appareils...
Running  CDPUserSvc_85b04   Service pour utilisateur de platefo...
Running  ClickToRunSvc      Service Microsoft Office « Démarrer...
Running  CoreMessagingRe... CoreMessaging
Running  cphs               Intel(R) Content Protection HECI Se...
Running  cplspcon           Intel(R) Content Protection HDCP Se...
Running  CryptSvc           Services de chiffrement
Running  CxAudioSvc         CxAudioSvc Service
Running  CxAudMsg           CxAudMsg Service
Running  CxUtilSvc          CxUtilSvc
Running  DcomLaunch         Lanceur de processus serveur DCOM
Running  DeviceAssociati... Service d’association de périphérique
Running  DevicesFlowUser... Flux d’appareils_85b04
Running  Dhcp               Client DHCP
Running  DiagTrack          Expériences des utilisateurs connec...
Running  DispBrokerDeskt... Service de stratégie d'affichage
Running  DisplayEnhancem... Service d'amélioration de l'affichage
Running  Dnscache           Client DNS
Running  DolbyDAXAPI        Dolby DAX API Service
Running  DoSvc              Optimisation de livraison
Running  DPS                Service de stratégie de diagnostic
Running  DusmSvc            Consommation des données
Running  EapHost            Protocole EAP (Extensible Authentic...
Running  esifsvc            Intel(R) Dynamic Platform and Therm...
Running  EventLog           Journal d’événements Windows
Running  EventSystem        Système d’événement COM+
Running  FontCache          Service de cache de police Windows
Running  FontCache3.0.0.0   Cache de police de Windows Presenta...
Running  gpsvc              Client de stratégie de groupe
Running  igfxCUIService2... Intel(R) HD Graphics Control Panel ...
Running  IKEEXT             Modules de génération de clés IKE e...
Running  ImControllerSer... System Interface Foundation Service
Running  InstallService     Installation du service Microsoft S...
Running  IntelAudioService  Intel(R) Audio Service
Running  InventorySvc       Service d’Appraisal inventaire et c...
Running  iphlpsvc           Assistance IP
Running  jhi_service        Intel(R) Dynamic Application Loader...
Running  KeyIso             Isolation de clé CNG
Running  LanmanServer       Serveur
Running  LanmanWorkstation  Station de travail
Running  lfsvc              Service de géolocalisation
Running  LicenseManager     Serveur Gestionnaire de licences Wi...
Running  LITSSVC            Lenovo Notebook ITS Service
Running  lmhosts            Assistance NetBIOS sur TCP/IP
Running  LMS                Intel(R) Management and Security Ap...
Running  LSM                Gestionnaire de session locale
Running  McAfee WebAdvisor  McAfee WebAdvisor
Running  mc-fw-host         McAfee Framework Host
Running  MDCoreSvc          Microsoft Defender Service de base
Running  mpssvc             Pare-feu Windows Defender
Running  NcbService         Service Broker pour les connexions ...
Running  netprofm           Service Liste des réseaux
Running  NgcCtnrSvc         Conteneur Microsoft Passport
Running  NgcSvc             Microsoft Passport
Running  NPSMSvc_85b04      NPSMSvc_85b04
Running  nsi                Service Interface du magasin réseau
Running  OneSyncSvc_85b04   Hôte de synchronisation_85b04
Running  PcaSvc             Service de l’Assistant Compatibilit...
Running  PlugPlay           Plug-and-Play
Running  Power              Alimentation
Running  ProfSvc            Service de profil utilisateur
Running  QcomWlanSrv        Qualcomm Atheros WLAN Driver Service
Running  RasMan             Gestionnaire des connexions d’accès...
Running  RmSvc              Service de gestion radio
Running  RpcEptMapper       Mappeur de point de terminaison RPC
Running  RpcSs              Appel de procédure distante (RPC)
Running  RstMwService       Intel(R) Storage Middleware Service
Running  SamSs              Gestionnaire de comptes de sécurité
Running  SAService          Conexant SmartAudio service
Running  Schedule           Planificateur de tâches
Running  SecurityHealthS... Service Sécurité Windows
Running  SENS               Service de notification d’événement...
Running  ShellHWDetection   Détection matériel noyau
Running  Spooler            Spouleur d’impression
Running  SSDPSRV            Découverte SSDP
Running  SstpSvc            Service SSTP (Secure Socket Tunneli...
Running  StateRepository    Service State Repository (StateRepo...
Running  StiSvc             Acquisition d’image Windows (WIA)
Running  StorSvc            Service de stockage
Running  SysMain            SysMain
Running  SystemEventsBroker Service Broker des événements système
Running  TextInputManage... Service de gestion des entrées de t...
Running  Themes             Thèmes
Running  TimeBrokerSvc      Service Broker pour les événements ...
Running  TokenBroker        Gestionnaire de comptes web
Running  TrkWks             Client de suivi de lien distribué
Running  UdkUserSvc_85b04   Service utilisateur du kit de dével...
Running  UserManager        Gestionnaire des utilisateurs
Running  UsoSvc             Service Orchestrator pour les mises...
Running  VaultSvc           Gestionnaire d’informations d’ident...
Running  WbioSrvc           Service de biométrie Windows
Running  Wcmsvc             Gestionnaire des connexions Windows
Running  WdNisSvc           Service d’inspection réseau de l’an...
Running  webthreatdefuse... Service d’utilisateur Web Threat De...
Running  WinDefend          Service antivirus Microsoft Defender
Running  WinHttpAutoProx... Service de découverte automatique d...
Running  Winmgmt            Infrastructure de gestion Windows
Running  WlanSvc            Service de configuration automatiqu...
Running  wlidsvc            Assistant Connexion avec un compte ...
Running  WpnService         Service du système de notifications...
Running  WpnUserService_... Service utilisateur de notification...
Running  wscsvc             Centre de sécurité
Running  WSearch            Windows Search


PS C:\Users\fatma> Get-Service | Where-Object {$_.Status -eq 'Stopped'}

Status   Name               DisplayName
------   ----               -----------
Stopped  AarSvc_85b04       Agent Activation Runtime_85b04
Stopped  AJRouter           Service de routeur AllJoyn
Stopped  ALG                Service de la passerelle de la couc...
Stopped  AppIDSvc           Identité de l’application
Stopped  AppReadiness       Préparation des applications
Stopped  autotimesvc        Heure cellulaire
Stopped  AxInstSV           Programme d’installation ActiveX (A...
Stopped  BcastDVRUserSer... Service utilisateur de diffusion et...
Stopped  BDESVC             Service de chiffrement de lecteur B...
Stopped  BITS               Service de transfert intelligent en...
Stopped  CaptureService_... CaptureService_85b04
Stopped  CertPropSvc        Propagation du certificat
Stopped  ClipSVC            Service de licences de client (Clip...
Stopped  CloudBackupRest... Service de restauration et de sauve...
Stopped  COMSysApp          Application système COM+
Stopped  ConsentUxUserSv... Service utilisateur ConsentUX_85b04
Stopped  CredentialEnrol... CredentialEnrollmentManagerUserSvc_...
Stopped  CxUIUSvc           CxUIUSvc Service
Stopped  dcsvc              Service de configuration (DC) déclaré
Stopped  defragsvc          Optimiser les lecteurs
Stopped  DeviceAssociati... DeviceAssociationBroker_85b04
Stopped  DeviceInstall      Service d’installation de périphérique
Stopped  DevicePickerUse... DevicePicker_85b04
Stopped  DevQueryBroker     Service Broker de découverte en arr...
Stopped  diagnosticshub.... Service Collecteur standard du conc...
Stopped  diagsvc            Diagnostic Execution Service
Stopped  DmEnrollmentSvc    Service d'inscription de la gestion...
Stopped  dmwappushservice   Service de routage de messages Push...
Stopped  dot3svc            Configuration automatique de réseau...
Stopped  DsmSvc             Gestionnaire d’installation de péri...
Stopped  DsSvc              Service de partage des données
Stopped  edgeupdate         Microsoft Edge Update Service (edge...
Stopped  edgeupdatem        Microsoft Edge Update Service (edge...
Stopped  EFS                Système de fichiers EFS (Encrypting...
Stopped  embeddedmode       Mode incorporé
Stopped  EntAppSvc          Service de gestion des applications...
Stopped  Fax                Télécopie
Stopped  fdPHost            Hôte du fournisseur de découverte d...
Stopped  FDResPub           Publication des ressources de décou...
Stopped  fhsvc              Service d’historique des fichiers
Stopped  FileSyncHelper     FileSyncHelper
Stopped  FrameServer        Serveur de trame de la Caméra Windows
Stopped  FrameServerMonitor Moniteur de serveur de trame Caméra...
Stopped  GameInputSvc       GameInput Service
Stopped  GoogleChromeEle... Google Chrome Elevation Service (Go...
Stopped  GoogleUpdaterIn... Service interne de mise à jour Goog...
Stopped  GoogleUpdaterSe... Service de mise à jour Google (Goog...
Stopped  GraphicsPerfSvc    GraphicsPerfSvc
Stopped  HfcDisableService  Intel(R) RST HFC Disable Service
Stopped  hidserv            Service du périphérique d’interface...
Stopped  HvHost             Service d'hôte HV
Stopped  iaStorAfsService   Intel(R) Optane(TM) Memory Service
Stopped  icssvc             Service Point d'accès sans fil mobi...
Stopped  Intel(R) TPM Pr... Intel(R) TPM Provisioning Service
Stopped  IpxlatCfgSvc       Service de configuration de convers...
Stopped  KtmRm              Service KtmRm pour Distributed Tran...
Stopped  lltdsvc            Mappage de découverte de topologie ...
Stopped  LxpSvc             Service d'expérience linguistique
Stopped  MapsBroker         Gestionnaire des cartes téléchargées
Stopped  McpManagementSe... McpManagementService
Stopped  mc-wps-update      McAfee Software Update
Stopped  MessagingServic... MessagingService_85b04
Stopped  MicrosoftEdgeEl... Microsoft Edge Elevation Service (M...
Stopped  MixedRealityOpe... Service Windows Mixed Reality OpenXR
Stopped  MSDTC              Coordinateur de transactions distri...
Stopped  MSiSCSI            Service Initiateur iSCSI de Microsoft
Stopped  msiserver          Windows Installer
Stopped  NaturalAuthenti... Authentification naturelle
Stopped  NcaSvc             Assistant Connectivité réseau
Stopped  NcdAutoSetup       Configuration automatique des périp...
Stopped  Netlogon           Netlogon
Stopped  Netman             Connexions réseau
Stopped  NetSetupSvc        Service Configuration du réseau
Stopped  NetTcpPortSharing  Service de partage de ports Net.Tcp
Stopped  NlaSvc             Connaissance des emplacements réseau
Stopped  OneDrive Update... OneDrive Updater Service
Stopped  ose64              Office 64 Source Engine
Stopped  p2pimsvc           Identity Manager réseau homologue
Stopped  p2psvc             Groupement de mise en réseau de pairs
Stopped  P9RdrService_85b04 P9RdrService_85b04
Stopped  PenService_85b04   PenService_85b04
Stopped  perceptionsimul... Service de simulation de perception...
Stopped  PerfHost           Hôte de DLL de compteur de performance
Stopped  PhoneSvc           Service téléphonique
Stopped  PimIndexMainten... Données de contacts_85b04
Stopped  pla                Journaux & alertes de performance
Stopped  PNRPAutoReg        Service de publication des noms d’o...
Stopped  PNRPsvc            Protocole PNRP
Stopped  PolicyAgent        Agent de stratégie IPsec
Stopped  PrintNotify        Extensions et notifications d’impri...
Stopped  PrintWorkflowUs... PrintWorkflow_85b04
Stopped  PushToInstall      Service PushToInstall de Windows
Stopped  QWAVE              Expérience audio-vidéo haute qualit...
Stopped  RasAuto            Gestionnaire des connexions automat...
Stopped  RemoteAccess       Routage et accès distant
Stopped  RemoteRegistry     Registre à distance
Stopped  RetailDemo         Service de démo du magasin
Stopped  RpcLocator         Localisateur d’appels de procédure ...
Stopped  SCardSvr           Carte à puce
Stopped  ScDeviceEnum       Service d’énumération de périphériq...
Stopped  SCPolicySvc        Stratégie de retrait de la carte à ...
Stopped  SDRSVC             Sauvegarde Windows
Stopped  seclogon           Ouverture de session secondaire
Stopped  SEMgrSvc           Gestionnaires des paiements et des ...
Stopped  SensorDataService  Service Données de capteur
Stopped  SensorService      Service de capteur
Stopped  SensrSvc           Service de surveillance des capteurs
Stopped  SessionEnv         Configuration des services Bureau à...
Stopped  SgrmBroker         Service Broker du moniteur d'exécut...
Stopped  SharedAccess       Partage de connexion Internet (ICS)
Stopped  SharedRealitySvc   Service de données spatiales
Stopped  shpamsvc           Shared PC Account Manager
Stopped  smphost            SMP de l’Espace de stockages Microsoft
Stopped  SmsRouter          Service Routeur SMS Microsoft Windows.
Stopped  SNMPTrap           Interruption SNMP
Stopped  spectrum           Service de perception Windows
Stopped  sppsvc             Protection logicielle
Stopped  ssh-agent          OpenSSH Authentication Agent
Stopped  svsvc              Vérificateur de points
Stopped  swprv              Fournisseur de cliché instantané de...
Stopped  TapiSrv            Téléphonie
Stopped  TermService        Services Bureau à distance
Stopped  TieringEngineSe... Gestion des niveaux de stockage
Stopped  TroubleshootingSvc Service de résolution des problèmes...
Stopped  TrustedInstaller   Programme d’installation pour les m...
Stopped  tzautoupdate       Programme de mise à jour automatiqu...
Stopped  uhssvc             Microsoft Update Health Service
Stopped  UmRdpService       Redirecteur de port du mode utilisa...
Stopped  UnistoreSvc_85b04  Stockage des données utilisateur_85b04
Stopped  upnphost           Hôte de périphérique UPnP
Stopped  UserDataSvc_85b04  Accès aux données utilisateur_85b04
Stopped  VacSvc             Service de composition audio volumé...
Stopped  vds                Disque virtuel
Stopped  vgc                vgc
Stopped  vmicguestinterface Interface de services d’invité Hyper-V
Stopped  vmicheartbeat      Service Pulsation Microsoft Hyper-V
Stopped  vmickvpexchange    Service Échange de données Microsof...
Stopped  vmicrdv            Service de virtualisation Bureau à ...
Stopped  vmicshutdown       Service Arrêt de l’invité Microsoft...
Stopped  vmictimesync       Service Synchronisation date/heure ...
Stopped  vmicvmsession      Service Hyper-V PowerShell Direct
Stopped  vmicvss            Requête du service VSS Hyper-V
Stopped  VSS                Cliché instantané des volumes
Stopped  W32Time            Temps Windows
Stopped  WaaSMedicSvc       WaaSMedicSvc
Stopped  WalletService      WalletService
Stopped  WarpJITSvc         Warp JIT Service
Stopped  wbengine           Service de moteur de sauvegarde en ...
Stopped  wcncsvc            Windows Connect Now - Registre de c...
Stopped  WdiServiceHost     Service hôte WDIServiceHost
Stopped  WdiSystemHost      Hôte système de diagnostics
Stopped  WebClient          WebClient
Stopped  webthreatdefsvc    Service Web Threat Defense
Stopped  Wecsvc             Collecteur d’événements de Windows
Stopped  WEPHOSTSVC         Service hôte du fournisseur de chif...
Stopped  wercplsupport      Prise en charge du Panneau de confi...
Stopped  WerSvc             Service de rapport d’erreurs Windows
Stopped  WFDSConMgrSvc      Service Wi-Fi Direct Service de ges...
Stopped  WiaRpc             Événements d’acquisition d’images f...
Stopped  WinRM              Gestion à distance de Windows (Gest...
Stopped  wisvc              Service Windows Insider
Stopped  wlpasvc            Service de l’Assistant de profil local
Stopped  WManSvc            Service de gestion de Windows
Stopped  wmiApSrv           Carte de performance WMI
Stopped  WMPNetworkSvc      Service de partage réseau du Lecteu...
Stopped  workfolderssvc     Dossiers de travail
Stopped  WpcMonSvc          Contrôle parental
Stopped  WPDBusEnum         Service Énumérateur d’appareil mobile
Stopped  wuauserv           Windows Update
Stopped  WwanSvc            Service de configuration automatiqu...
Stopped  XblAuthManager     Gestionnaire d'authentification Xbo...
Stopped  XblGameSave        Jeu sauvegardé sur Xbox Live
Stopped  XboxGipSvc         Xbox Accessory Management Service
Stopped  XboxNetApiSvc      Service de mise en réseau Xbox Live
```

## 2. Mémoire et CPU

🌞 **RAM**
```powershell
PS C:\Users\fatma> Get-ComputerInfo | Select-Object TotalPhysicalMemory/1Gb
TotalPhysicalMemory/1Gb
-----------------------


PS C:\Users\fatma> Get-WmiObject Win32_OperatingSystem | Select-Object FreePhysicalMemory

FreePhysicalMemory
------------------
           2098080
```

🌞 **CPU**
```powershell
i dont know :)
```

## 3. Stockage

🌞 **Périphériques**
```powershell
PS C:\Users\fatma> Get-Disk | Select-Object -Property Model, Size | Format-Table -AutoSize

Model                                  Size
-----                                  ----
WDC PC SN520 SDAPMUW-512G-1101 512110190592
```

🌞 **Partitions**
```powershell
PS C:\Users\fatma> Get-Partition

   DiskPath : \\?\scsi#disk&ven_nvme&prod_wdc_pc_sn520_sda#4&117e77d0&0&020000#{53f56307-b6bf-11d0-94f2-00a0c91efb8b}

PartitionNumber  DriveLetter Offset                                               Size Type
---------------  ----------- ------                                               ---- ----
1                           1048576                                            260 MB System
2                           273678336                                           16 MB Reserved
3                C           290455552                                       475.69 GB Basic
4                           511061262336                                      1000 MB Recovery
```

🌞 **Espace disque**
```powershell
PS C:\Users\fatma> Get-PSDrive C | Select-Object Used, Free, @{Name='Total';Expression={[math]::round($_.Used + $_.Free, 2)}}

        Used         Free        Total
        ----         ----        -----
113601404928 397169397760 510770802688
```

## 4. Réseau

🌞 **Cartes réseau**
```powershell
PS C:\Users\fatma> Get-NetAdapter | Select-Object Name, Status, @{Name='IPAddress';Expression={(Get-NetIPAddress -InterfaceAlias $_.Name).IPAddress}}

Name                       Status       IPAddress
----                       ------       ---------
Connexion réseau Bluetooth Disconnected {fe80::8dd1:5fa2:62ac:eca2%9, 169.254.188.183}
Wi-Fi                      Up           {fe80::7060:92c1:74ec:7a53%6, 10.3.220.124}
```

🌞 **Connexions réseau**
```powershell
PS C:\Users\fatma> Get-NetTCPConnection | Where-Object { $_.State -eq 'Established' } | Select-Object RemoteAddress, @{Name='ProcessId';Expression={($_.OwningProcess)}}, @{Name='ProcessName';Expression={(Get-Process -Id $_.OwningProcess).Name}}

RemoteAddress   ProcessId ProcessName
-------------   --------- -----------
96.17.207.17         9824 Widgets
13.89.179.14        13416 FileCoAuth
20.189.173.13        4548 WINWORD
3.233.158.24        13236 chrome
20.223.35.26         5192 SystemSettings
40.126.32.138       16512 svchost
40.126.32.138       16512 svchost
108.177.104.94      13236 chrome
52.20.21.250        13236 chrome
151.101.130.167     13236 chrome
151.101.130.214     13236 chrome
151.101.194.214     13236 chrome
35.186.247.156      13236 chrome
151.101.65.140      13236 chrome
151.101.129.140     13236 chrome
151.101.193.140     13236 chrome
151.101.193.140     13236 chrome
151.101.130.133     13236 chrome
151.101.129.229     13236 chrome
35.186.249.72       13236 chrome
34.96.102.137       13236 chrome
172.64.155.209      13236 chrome
104.18.32.47        13236 chrome
127.0.0.1            3812 svchost
142.250.110.188     13236 chrome
35.186.224.45       12396 Discord
20.238.236.234      12220 msedge
20.199.120.151       4668 svchost
52.112.120.226      13556 msedgewebview2
52.123.134.243        500 ms-teams
162.159.134.234     12396 Discord
13.107.6.158         9756 SearchHost
52.111.231.21        4548 WINWORD
127.0.0.1            1272 WUDFHost
```
## 5. Utilisateurs

🌞 **Lister les *utilisateurs* de la machine**
```powershell
PS C:\Users\fatma> whoami
fatma\fatma

PS C:\Users\fatma> Get-LocalGroupMember -Group "Administrateurs" | Select-Object Name

Name
----
Fatma\Administrateur
FATMA\fatma
```

🌞 **Heure de login**
```powershell
PS C:\Users\fatma> Get-CimInstance -ClassName ‘Win32_LogonSession’ | Where {$_.LogonType -eq ‘2’}

LogonId Name LogonType StartTime            Status AuthenticationPackage
------- ---- --------- ---------            ------ ---------------------
511010       2         11/4/2024 2:13:34 PM        CloudAP
510957       2         11/4/2024 2:13:34 PM        CloudAP
```

🌞 **Lister les *processus* en cours d'exécution**
```powershell
PS C:\Users\fatma> Get-Process | Select-Object Id, ProcessName, @{Name='UserName'; Expression={(Get-WmiObject Win32_Process -Filter "ProcessId=$($_.Id)").GetOwner().User}}

   Id ProcessName    UserName
   -- -----------    --------
 3568 AdminService
16144 aesm_service
 7056 AggregatorHost
14304 ai             fatma
15592 ai             fatma
17056 ai             fatma
14156 Application... fatma
 1568 backgroundT... fatma
 2600 chrome         fatma
 3428 chrome         fatma
 7228 chrome         fatma
 7824 chrome         fatma
10828 chrome         fatma
11120 chrome         fatma
13140 chrome         fatma
13236 chrome         fatma
15984 chrome         fatma
  812 csrss
  944 csrss
11044 ctfmon         fatma
 3720 CxAudioSvc
 3956 CxAudMsg64
 4104 CxUtilSvc
 4112 DAX3API
 7088 DAX3API
12356 Discord        fatma
12396 Discord        fatma
12756 Discord        fatma
13048 Discord        fatma
13124 Discord        fatma
13208 Discord        fatma
10384 dllhost        fatma
14840 dllhost        fatma
 2176 dwm
 4128 esif_uf
 8568 explorer       fatma
13416 FileCoAuth     fatma
 1052 fontdrvhost
 1492 fontdrvhost
    0 Idle
 2828 igfxCUIService
 8712 igfxEM         fatma
 4272 IntelAudioS...
 3712 IntelCpHDCPSvc
 5504 IntelCpHeciSvc
 4484 jhi_service
10168 laragon        fatma
 4176 Lenovo.Mode...
 4472 LMS
 4396 LNBITSSvc
 1016 lsass
 4424 mc-fw-host
 7760 mc-fw-host     fatma
 7748 mc-neo-host
 2760 Memory Comp...
10264 Microsoft.S... fatma
14820 MoUsoCoreWo...
 4444 MpDefenderC...
 9712 msedge         fatma
11164 msedge         fatma
11520 msedge         fatma
11936 msedge         fatma
12004 msedge         fatma
12208 msedge         fatma
12220 msedge         fatma
 1736 msedgewebview2 fatma
 2536 msedgewebview2 fatma
 6028 msedgewebview2 fatma
13556 msedgewebview2 fatma
14064 msedgewebview2 fatma
14296 msedgewebview2 fatma
14332 msedgewebview2 fatma
14940 msedgewebview2 fatma
14968 msedgewebview2 fatma
15180 msedgewebview2 fatma
 4644 MsMpEng
  500 ms-teams       fatma
12796 ms-teams       fatma
 9320 NisSrv
 4152 OfficeClick...
11348 OneDrive       fatma
 9384 OpenConsole    fatma
13016 PhoneExperi... fatma
10144 powershell     fatma
 7864 Presentatio...
 4500 QcomWlanSrvx64
  148 Registry
 4536 RstMwService
 2592 RuntimeBroker  fatma
 9892 RuntimeBroker  fatma
 9992 RuntimeBroker  fatma
14104 RuntimeBroker  fatma
14288 RuntimeBroker  fatma
 4568 SASrv
 9756 SearchHost     fatma
10664 SearchIndexer
 8256 SecurityHea...
10644 SecurityHea... fatma
 4432 servicehost
  992 services
16356 ShellExperi... fatma
 7528 sihost         fatma
  608 smss
 3764 spoolsv
 9780 StartMenuEx... fatma
  680 svchost
  748 svchost
 1128 svchost
 1184 svchost
 1572 svchost
 1580 svchost
 1588 svchost
 1712 svchost
 1720 svchost
 1728 svchost
 1816 svchost
 1824 svchost
 1900 svchost
 1992 svchost
 2056 svchost
 2132 svchost
 2160 svchost
 2304 svchost
 2368 svchost
 2448 svchost
 2524 svchost
 2584 svchost
 2660 svchost
 2668 svchost
 2676 svchost
 2804 svchost
 2852 svchost
 2864 svchost
 2932 svchost
 2964 svchost
 3092 svchost
 3164 svchost
 3284 svchost
 3292 svchost
 3300 svchost
 3440 svchost
 3536 svchost
 3560 svchost
 3692 svchost
 3704 svchost
 3812 svchost
 3824 svchost
 3928 svchost        fatma
 4040 svchost
 4240 svchost
 4248 svchost
 4440 svchost
 4592 svchost
 4632 svchost
 4660 svchost
 4668 svchost
 4788 svchost
 4860 svchost
 5228 svchost
 5476 svchost
 6068 svchost
 6252 svchost
 6668 svchost
 7516 svchost        fatma
 7636 svchost        fatma
 7672 svchost
 7880 svchost        fatma
 7932 svchost
 8316 svchost
 8612 svchost
 8744 svchost
 8768 svchost
 8992 svchost
 9456 svchost        fatma
 9936 svchost
10056 svchost        fatma
14264 svchost
14272 svchost        fatma
14536 svchost        fatma
14744 svchost
15004 svchost
15400 svchost
15716 svchost
16052 svchost        fatma
    4 System
 5192 SystemSettings fatma
16816 SystemSetti... fatma
 8228 taskhostw      fatma
15332 taskhostw      fatma
 7632 uihost         fatma
17372 UserOOBEBroker fatma
 9824 Widgets        fatma
 8904 WidgetService  fatma
 9488 WindowsTerm... fatma
  920 wininit
 1440 winlogon
 4548 WINWORD        fatma
 1916 WmiPrvSE
 1176 WUDFHost
 1272 WUDFHost
 1364 WUDFHost
```

🌞 **Sur un fichier random qui se trouve dans votre dossier**
```powershell
`Téléchargements/`**
PS C:\Users\fatma> $path = "$env:USERPROFILE\Downloads\DiscordSetup.exe"
PS C:\Users\fatma> Get-Acl $path | Select-Object Owner

Owner
-----
FATMA\fatma
```

## 6. Random

🌞 **Uptime**
```powershell
PS C:\Users\fatma> (Get-CimInstance -ClassName Win32_OperatingSystem).LastBootUpTime

Monday, November 4, 2024 2:13:01 PM
```

🌞 **Device**
```powershell
PS C:\Users\fatma> Get-CimInstance -ClassName Win32_Processor | Select-Object -Property Name

Name
----
Intel(R) Core(TM) i5-8265U CPU @ 1.60GHz

# Version 
PS C:\Users\fatma> Get-CimInstance -ClassName Win32_OperatingSystem | Select-Object -Property Caption, Version

Caption                      Version
-------                      -------
Microsoft Windows 11 Famille 10.0.22631
```

🌞 **Version**
```powershell
PS C:\Users\fatma> Get-CimInstance -ClassName Win32_OperatingSystem | Select-Object -Property Caption, Version

Caption                      Version
-------                      -------
Microsoft Windows 11 Famille 10.0.22631
```

🌞 **Mise à jour**
```powershell
PS C:\Users\fatma> Get-HotFix | Select-Object -Property InstalledOn | Sort-Object InstalledOn -Descending | Select-Object -First 1

InstalledOn
-----------
10/9/2024 12:00:00 AM
```

## 7. Ptit amusement

🌞 **Lister les *connexions active*s**
```powershell

```

🌞 **En apprendre + sur le *processus* en cours d'exécution**
```powershell

```

🌞 **En apprendre + sur le *programme***
```powershell

```

🌞 **En apprendre + sur l'adresse IP**
```powershell

```

🌞 **Délai**
```powershell

```





