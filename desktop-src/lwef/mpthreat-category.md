---
title: Énumération MPTHREAT_CATEGORY (MpClient. h)
description: Catégories de menaces possibles.
ms.assetid: 478ED59E-5D3C-43B3-A89D-44A649EDD086
keywords:
- MPTHREAT_CATEGORY énumération des fonctionnalités d’environnement Windows héritées
- PMPTHREAT_CATEGORY des fonctionnalités d’environnement Windows héritées d’un pointeur d’énumération
topic_type:
- apiref
api_name:
- MPTHREAT_CATEGORY
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a149ef6ce6ebadacbac6f0dd35247d793ca7000
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513591"
---
# <a name="mpthreat_category-enumeration"></a>\_Énumération de la catégorie MPTHREAT

Catégories de menaces possibles.

## <a name="syntax"></a>Syntaxe

```C++
typedef enum tagMPTHREAT_CATEGORY {
  MP_THREAT_CATEGORY_INVALID                    = 0,
  MP_THREAT_CATEGORY_ADWARE                     = 1,
  MP_THREAT_CATEGORY_SPYWARE                    = 2,
  MP_THREAT_CATEGORY_PASSWORDSTEALER            = 3,
  MP_THREAT_CATEGORY_TROJANDOWNLOADER           = 4,
  MP_THREAT_CATEGORY_WORM                       = 5,
  MP_THREAT_CATEGORY_BACKDOOR                   = 6,
  MP_THREAT_CATEGORY_REMOTEACCESSTROJAN         = 7,
  MP_THREAT_CATEGORY_TROJAN                     = 8,
  MP_THREAT_CATEGORY_EMAILFLOODER               = 9,
  MP_THREAT_CATEGORY_KEYLOGGER                  = 10,
  MP_THREAT_CATEGORY_DIALER                     = 11,
  MP_THREAT_CATEGORY_MONITORINGSOFTWARE         = 12,
  MP_THREAT_CATEGORY_BROWSERMODIFIER            = 13,
  MP_THREAT_CATEGORY_COOKIE                     = 14,
  MP_THREAT_CATEGORY_BROWSERPLUGIN              = 15,
  MP_THREAT_CATEGORY_AOLEXPLOIT                 = 16,
  MP_THREAT_CATEGORY_NUKER                      = 17,
  MP_THREAT_CATEGORY_SECURITYDISABLER           = 18,
  MP_THREAT_CATEGORY_JOKEPROGRAM                = 19,
  MP_THREAT_CATEGORY_HOSTILEACTIVEXCONTROL      = 20,
  MP_THREAT_CATEGORY_SOFTWAREBUNDLER            = 21,
  MP_THREAT_CATEGORY_STEALTHNOTIFIER            = 22,
  MP_THREAT_CATEGORY_SETTINGSMODIFIER           = 23,
  MP_THREAT_CATEGORY_TOOLBAR                    = 24,
  MP_THREAT_CATEGORY_REMOTECONTROLSOFTWARE      = 25,
  MP_THREAT_CATEGORY_TROJANFTP                  = 26,
  MP_THREAT_CATEGORY_POTENTIALUNWANTEDSOFTWARE  = 27,
  MP_THREAT_CATEGORY_ICQEXPLOIT                 = 28,
  MP_THREAT_CATEGORY_TROJANTELNET               = 29,
  MP_THREAT_CATEGORY_EXPLOIT                    = 30,
  MP_THREAT_CATEGORY_FILESHARINGPROGRAM         = 31,
  MP_THREAT_CATEGORY_MALWARE_CREATION_TOOL      = 32,
  MP_THREAT_CATEGORY_REMOTE_CONTROL_SOFTWARE    = 33,
  MP_THREAT_CATEGORY_TOOL                       = 34,
  MP_THREAT_CATEGORY_TROJAN_DENIALOFSERVICE     = 36,
  MP_THREAT_CATEGORY_TROJAN_DROPPER             = 37,
  MP_THREAT_CATEGORY_TROJAN_MASSMAILER          = 38,
  MP_THREAT_CATEGORY_TROJAN_MONITORINGSOFTWARE  = 39,
  MP_THREAT_CATEGORY_TROJAN_PROXYSERVER         = 40,
  MP_THREAT_CATEGORY_VIRUS                      = 42,
  MP_THREAT_CATEGORY_KNOWN                      = 43,
  MP_THREAT_CATEGORY_UNKNOWN                    = 44,
  MP_THREAT_CATEGORY_SPP                        = 45,
  MP_THREAT_CATEGORY_BEHAVIOR                   = 46,
  MP_THREAT_CATEGORY_VULNERABILTIY              = 47,
  MP_THREAT_CATEGORY_POLICY                     = 48
} MPTHREAT_CATEGORY, *PMPTHREAT_CATEGORY;
```

## <a name="constants"></a>Constantes

Catégorie de menace | Description
-|-
<span id="MP_THREAT_CATEGORY_INVALID"></span><span id="mp_threat_category_invalid"></span>Pack d’e **\_ catégorie de menace \_ \_ non valide** | La catégorie de menace n’existe pas ou a été mal orthographiée.
<span id="MP_THREAT_CATEGORY_ADWARE"></span><span id="mp_threat_category_adware"></span>Pack d’e **\_ \_ \_ logiciel publicitaire de catégorie de menaces** | Application potentiellement indésirable qui affiche des publications.
<span id="MP_THREAT_CATEGORY_SPYWARE"></span><span id="mp_threat_category_spyware"></span>Pack d’e **\_ \_ \_ logiciel espion de catégorie de menace** | Programme malveillant qui transmet des informations sur l’appareil ou l’utilisateur, sans le consentement ou la connaissance de l’utilisateur.
<span id="MP_THREAT_CATEGORY_PASSWORDSTEALER"></span><span id="mp_threat_category_passwordstealer"></span>Pack d’e **\_ catégorie de menace \_ \_ PASSWORDSTEALER** | Application qui collecte et/ou transmet un mot de passe à une personne malveillante.
<span id="MP_THREAT_CATEGORY_TROJANDOWNLOADER"></span><span id="mp_threat_category_trojandownloader"></span>**\_ \_ TROJANDOWNLOADER catégorie de menace MP \_** | Un cheval de Troie qui télécharge des applications malveillantes ou potentiellement indésirables sur un appareil infecté.
<span id="MP_THREAT_CATEGORY_WORM"></span><span id="mp_threat_category_worm"></span>Pack d’e **\_ \_ \_ ver de catégorie de menace** | Logiciel malveillant auto-propagé qui peut se distribuer automatiquement via des connexions réseau.
<span id="MP_THREAT_CATEGORY_BACKDOOR"></span><span id="mp_threat_category_backdoor"></span>**\_catégorie de menace MP \_ \_ Backdoor** | Programme malveillant qui fournit un moyen de contourner les protocoles de sécurité et d’authentification normaux sur un appareil.
<span id="MP_THREAT_CATEGORY_REMOTEACCESSTROJAN"></span><span id="mp_threat_category_remoteaccesstrojan"></span>Pack d’e **\_ catégorie de menace \_ \_ REMOTEACCESSTROJAN** | Cheval de Troie qui fournit l’accès à distance à un ordinateur.
<span id="MP_THREAT_CATEGORY_TROJAN"></span><span id="mp_threat_category_trojan"></span>**\_cheval de \_ Troie catégorie de menaces MP \_** | Logiciel malveillant qui se présente comme un logiciel légitime.
<span id="MP_THREAT_CATEGORY_EMAILFLOODER"></span><span id="mp_threat_category_emailflooder"></span>Pack d’e **\_ catégorie de menace \_ \_ EMAILFLOODER** | Le programme malveillant envoie un volume important de courrier électronique à une cible.
<span id="MP_THREAT_CATEGORY_KEYLOGGER"></span><span id="mp_threat_category_keylogger"></span>Pack d’e **\_ \_ \_ enregistreur de catégorie de menace** | Programme malveillant qui enregistre les séquences de touches de l’utilisateur, en volant potentiellement les mots de passe et autres données sensibles.
<span id="MP_THREAT_CATEGORY_DIALER"></span><span id="mp_threat_category_dialer"></span>Pack d’e **\_ \_ \_ numéroteur de catégorie de menace** | Programme malveillant qui effectue des appels téléphoniques non autorisés, souvent aux tarifs Premium.
<span id="MP_THREAT_CATEGORY_MONITORINGSOFTWARE"></span><span id="mp_threat_category_monitoringsoftware"></span>Pack d’e **\_ catégorie de menace \_ \_ MONITORINGSOFTWARE** | Application potentiellement indésirable qui surveille l’activité des utilisateurs, telle que ce que l’utilisateur tape sur le clavier ou les vues sur son écran.
<span id="MP_THREAT_CATEGORY_BROWSERMODIFIER"></span><span id="mp_threat_category_browsermodifier"></span>Pack d’e **\_ catégorie de menace \_ \_ BROWSERMODIFIER** | Application potentiellement indésirable qui modifie les paramètres du navigateur Web sans le consentement de l’utilisateur.
<span id="MP_THREAT_CATEGORY_COOKIE"></span><span id="mp_threat_category_cookie"></span>Pack d’e **\_ \_ \_ cookie de catégorie de menace** | Données qu’un serveur Web envoie à un navigateur, ce qui lui permet d’enregistrer des informations sur l’utilisateur, telles que les paramètres d’application Web, lors de visites répétées.
<span id="MP_THREAT_CATEGORY_BROWSERPLUGIN"></span><span id="mp_threat_category_browserplugin"></span>Pack d’e **\_ catégorie de menace \_ \_ BROWSERPLUGIN** | Logiciel qui permet à un navigateur Web standard d’afficher et d’exécuter des types spécifiques de contenu, tels que des fichiers multimédias, des images animées et des formulaires interactifs.
<span id="MP_THREAT_CATEGORY_AOLEXPLOIT"></span><span id="mp_threat_category_aolexploit"></span>Pack d’e **\_ catégorie de menace \_ \_ AOLEXPLOIT** | Logiciel malveillant qui attaque les utilisateurs du service Internet AOL, souvent en récupérant des mots de passe ou en modifiant des paramètres.
<span id="MP_THREAT_CATEGORY_NUKER"></span><span id="mp_threat_category_nuker"></span>Pack d’e **\_ catégorie de menace \_ \_ NUKER** | Programme malveillant conçu pour bloquer un appareil ou le rendre moins stable.
<span id="MP_THREAT_CATEGORY_SECURITYDISABLER"></span><span id="mp_threat_category_securitydisabler"></span>Pack d’e **\_ catégorie de menace \_ \_ SECURITYDISABLER** | Programme malveillant qui désactive les paramètres de sécurité ou les produits.
<span id="MP_THREAT_CATEGORY_JOKEPROGRAM"></span><span id="mp_threat_category_jokeprogram"></span>Pack d’e **\_ catégorie de menace \_ \_ JOKEPROGRAM** | Application conçue pour amuser ou effrayer un utilisateur, sans endommager réellement l’appareil.
<span id="MP_THREAT_CATEGORY_HOSTILEACTIVEXCONTROL"></span><span id="mp_threat_category_hostileactivexcontrol"></span>Pack d’e **\_ catégorie de menace \_ \_ HOSTILEACTIVEXCONTROL** | Contrôle ActiveX conçu par une personne malveillante pour endommager un appareil. Un contrôle ActiveX est un type de module complémentaire de navigateur propre à Internet Explorer.
<span id="MP_THREAT_CATEGORY_SOFTWAREBUNDLER"></span><span id="mp_threat_category_softwarebundler"></span>Pack d’e **\_ catégorie de menace \_ \_ SOFTWAREBUNDLER** | Logiciel qui installe d’autres applications potentiellement indésirables, telles que des logiciels publicitaires ou des logiciels espions. Le contrat de licence du logiciel de regroupement peut nécessiter ces autres composants pour fonctionner.
<span id="MP_THREAT_CATEGORY_STEALTHNOTIFIER"></span><span id="mp_threat_category_stealthnotifier"></span>Pack d’e **\_ catégorie de menace \_ \_ STEALTHNOTIFIER** | Programme malveillant qui se connecte à un serveur distant via une connexion furtive pour notifier une personne malveillante que le logiciel malveillant a été installé.
<span id="MP_THREAT_CATEGORY_SETTINGSMODIFIER"></span><span id="mp_threat_category_settingsmodifier"></span>Pack d’e **\_ catégorie de menace \_ \_ SETTINGSMODIFIER** | Application potentiellement indésirable qui modifie les paramètres d’un utilisateur sans la connaissance ou le consentement de l’utilisateur.
<span id="MP_THREAT_CATEGORY_TOOLBAR"></span><span id="mp_threat_category_toolbar"></span>Pack d’e **\_ \_ \_ barre d’outils catégorie de menace** | Une application potentiellement indésirable (PUA) qui installe une barre d’outils sur le navigateur Web de l’utilisateur ; souvent fournis avec des PUA supplémentaires, tels que des logiciels publicitaires.
<span id="MP_THREAT_CATEGORY_REMOTECONTROLSOFTWARE"></span><span id="mp_threat_category_remotecontrolsoftware"></span>Pack d’e **\_ catégorie de menace \_ \_ REMOTECONTROLSOFTWARE** | Application potentiellement indésirable qui fournit l’accès à distance à un appareil.
<span id="MP_THREAT_CATEGORY_TROJANFTP"></span><span id="mp_threat_category_trojanftp"></span>Pack d’e **\_ catégorie de menace \_ \_ TROJANFTP** | Cheval de Troie qui utilise un serveur FTP pour permettre à une personne malveillante de charger ou de télécharger des fichiers à partir d’un appareil.
<span id="MP_THREAT_CATEGORY_POTENTIALUNWANTEDSOFTWARE"></span><span id="mp_threat_category_potentialunwantedsoftware"></span>Pack d’e **\_ catégorie de menace \_ \_ POTENTIALUNWANTEDSOFTWARE** | Également appelée *application potentiellement indésirable* ou *PUA*; logiciel qui peut se comporter de façon excessivement intrusive, que l’utilisateur n’a peut-être pas prévue ou entièrement consenti.
<span id="MP_THREAT_CATEGORY_ICQEXPLOIT"></span><span id="mp_threat_category_icqexploit"></span>Pack d’e **\_ catégorie de menace \_ \_ ICQEXPLOIT** | Un cheval de Troie qui attaque le service de messagerie ICQ, souvent en récupérant les mots de passe ou en falsifiant les paramètres.
<span id="MP_THREAT_CATEGORY_TROJANTELNET"></span><span id="mp_threat_category_trojantelnet"></span>Pack d’e **\_ catégorie de menace \_ \_ TROJANTELNET** | Cheval de Troie qui installe un serveur Telnet sur l’ordinateur d’un utilisateur sans la connaissance ou le consentement de l’utilisateur.
<span id="MP_THREAT_CATEGORY_EXPLOIT"></span><span id="mp_threat_category_exploit"></span>Pack d’e **\_ \_ \_ exploitation de la catégorie menace** | Code malveillant tirant parti d’une vulnérabilité sur un appareil ou un système.
<span id="MP_THREAT_CATEGORY_FILESHARINGPROGRAM"></span><span id="mp_threat_category_filesharingprogram"></span>Pack d’e **\_ catégorie de menace \_ \_ FILESHARINGPROGRAM** | Application potentiellement indésirable qui ouvre un appareil au partage d’égal à égal des fichiers de l’appareil.
<span id="MP_THREAT_CATEGORY_MALWARE_CREATION_TOOL"></span><span id="mp_threat_category_malware_creation_tool"></span>Pack d’e **\_ \_outil de \_ \_ création de \_ logiciels malveillants de catégorie de menace** | Application capable de générer automatiquement des fichiers malveillants.
<span id="MP_THREAT_CATEGORY_REMOTE_CONTROL_SOFTWARE"></span><span id="mp_threat_category_remote_control_software"></span>Pack d’e **\_ \_logiciel de \_ \_ contrôle \_ à distance de catégorie de menace** | Application potentiellement indésirable qui autorise l’accès à distance à un appareil.
<span id="MP_THREAT_CATEGORY_TOOL"></span><span id="mp_threat_category_tool"></span>Pack d’e **\_ \_ \_ outil catégorie de menace** | Utilitaire qui permet à une personne malveillante d’exécuter des actions malveillantes sur un appareil.
<span id="MP_THREAT_CATEGORY_TROJAN_DENIALOFSERVICE"></span><span id="mp_threat_category_trojan_denialofservice"></span>Pack d’e **\_ THREAT \_ Category \_ cheval de Troie \_ DENIALOFSERVICE** | Cheval de Troie conçu pour envoyer un grand nombre de requêtes réseau à une cible dans le cadre d’une attaque par déni de service (DoS).
<span id="MP_THREAT_CATEGORY_TROJAN_DROPPER"></span><span id="mp_threat_category_trojan_dropper"></span>Pack d’e **\_ \_élimination des \_ chevaux \_ de Troie de catégorie de menace** | Un cheval de Troie qui télécharge et installe des programmes malveillants ou des applications potentiellement indésirables sur une cible.
<span id="MP_THREAT_CATEGORY_TROJAN_MASSMAILER"></span><span id="mp_threat_category_trojan_massmailer"></span>Pack d’e **\_ THREAT \_ Category \_ cheval de Troie \_ MASSMAILER** | Cheval de Troie qui envoie un volume important d’e-mails à une cible, destiné à saturer la boîte de réception de la cible.
<span id="MP_THREAT_CATEGORY_TROJAN_MONITORINGSOFTWARE"></span><span id="mp_threat_category_trojan_monitoringsoftware"></span>Pack d’e **\_ THREAT \_ Category \_ cheval de Troie \_ MONITORINGSOFTWARE** | Un cheval de Troie qui surveille l’activité des utilisateurs, tels que les éléments que l’utilisateur tape sur le clavier ou les vues sur leur écran.
<span id="MP_THREAT_CATEGORY_TROJAN_PROXYSERVER"></span><span id="mp_threat_category_trojan_proxyserver"></span>Pack d’e **\_ THREAT \_ Category \_ cheval de Troie \_ PROXYSERVER** | Serveur proxy installé par un cheval de Troie, indiquant qu’il s’agit d’une connexion Internet ininterrompue tout en autorisant l’accès non autorisé à l’appareil infecté.
<span id="MP_THREAT_CATEGORY_VIRUS"></span><span id="mp_threat_category_virus"></span>Pack d’e **\_ \_ \_ virus de catégorie de menace** | Programme malveillant qui réplique, en général, en infectant d’autres fichiers dans le système, ce qui permet l’exécution du code de programme malveillant et sa propagation lorsque ces fichiers sont activés.
<span id="MP_THREAT_CATEGORY_KNOWN"></span><span id="mp_threat_category_known"></span>Pack d’e **\_ catégorie de menace \_ \_ connue** | Une menace malveillante non spécifiée.
<span id="MP_THREAT_CATEGORY_UNKNOWN"></span><span id="mp_threat_category_unknown"></span>Pack d’e **\_ catégorie de menace \_ \_ inconnue** | Une menace malveillante non spécifiée n’a pas encore été définie.
<span id="MP_THREAT_CATEGORY_SPP"></span><span id="mp_threat_category_spp"></span>Pack d’e **\_ catégorie de menace \_ \_ spp** | Technologie anti-piratage qui requiert l’activation de chaque installation d’un produit Windows auprès de Microsoft.
<span id="MP_THREAT_CATEGORY_BEHAVIOR"></span><span id="mp_threat_category_behavior"></span>Pack d’e **\_ \_ \_ comportement de catégorie de menace** | Type de détection basée sur les actions de fichier qui sont souvent associées à une activité malveillante.
<span id="MP_THREAT_CATEGORY_VULNERABILTIY"></span><span id="mp_threat_category_vulnerabiltiy"></span>Pack d’e **\_ catégorie de menace \_ \_ VULNERABILTIY** | Toute faiblesse, tout processus administratif ou toute activité qui rend un appareil vulnérable à une attaque par une menace.
<span id="MP_THREAT_CATEGORY_POLICY"></span><span id="mp_threat_category_policy"></span>Pack d’e **\_ \_ \_ stratégie de catégorie de menace** | Ensemble de règles définies par un administrateur, qui contrôlent les fonctionnalités sur les appareils de bureau et mobiles, tels que les mises à jour logicielles.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| Client minimal pris en charge | Windows 8 (applications de bureau uniquement) |
| Serveur minimal pris en charge | Windows Server 2012 (applications de bureau uniquement) |
| En-tête | MpClient. h |
