---
title: Classe Win32_TSGeneralSetting
description: Représente les paramètres généraux du terminal, tels que le niveau de chiffrement et le protocole de transport.
ms.assetid: a31d68c0-e446-4d78-85e0-5173e7870255
ms.tgt_platform: multiple
keywords:
- Win32_TSGeneralSetting de la classe Services Bureau à distance
- Win32_TSGeneralSetting de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting
- Win32_TSGeneralSetting.Caption
- Win32_TSGeneralSetting.Description
- Win32_TSGeneralSetting.InstallDate
- Win32_TSGeneralSetting.Name
- Win32_TSGeneralSetting.Status
- Win32_TSGeneralSetting.TerminalName
- Win32_TSGeneralSetting.CertificateName
- Win32_TSGeneralSetting.Certificates
- Win32_TSGeneralSetting.Comment
- Win32_TSGeneralSetting.MinEncryptionLevel
- Win32_TSGeneralSetting.PolicySourceMinEncryptionLevel
- Win32_TSGeneralSetting.PolicySourceSecurityLayer
- Win32_TSGeneralSetting.PolicySourceUserAuthenticationRequired
- Win32_TSGeneralSetting.SecurityLayer
- Win32_TSGeneralSetting.SSLCertificateSHA1Hash
- Win32_TSGeneralSetting.SSLCertificateSHA1HashType
- Win32_TSGeneralSetting.TerminalProtocol
- Win32_TSGeneralSetting.Transport
- Win32_TSGeneralSetting.UserAuthenticationRequired
- Win32_TSGeneralSetting.WindowsAuthentication
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de2cc2e7ede46b503e0d33f65c5735d5e0cc653a75184384be2d706bfc8ac9cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999809"
---
# <a name="win32_tsgeneralsetting-class"></a>\_Classe TSGeneralSetting Win32

La classe WMI **\_ TSGeneralSetting** WMI représente les paramètres généraux du terminal, tels que le niveau de chiffrement et le protocole de transport.

La syntaxe suivante est simplifiée à partir du code MOF et comprend toutes les propriétés définies et héritées, par ordre alphabétique. Pour obtenir des informations de référence sur les méthodes, consultez le tableau des méthodes plus loin dans cette rubrique.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("Win32_WIN32_TSGENERALSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSGeneralSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   CertificateName;
  uint8    Certificates[];
  string   Comment;
  uint32   MinEncryptionLevel;
  uint32   PolicySourceMinEncryptionLevel;
  uint32   PolicySourceSecurityLayer;
  uint32   PolicySourceUserAuthenticationRequired;
  uint32   SecurityLayer;
  string   SSLCertificateSHA1Hash;
  uint32   SSLCertificateSHA1HashType;
  string   TerminalProtocol;
  string   Transport;
  uint32   UserAuthenticationRequired;
  uint32   WindowsAuthentication;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ TSGeneralSetting** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ TSGeneralSetting** possède ces méthodes.



| Méthode                                                                                        | Description                                                                                                                                                             |
|:----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetEncryptionLevel**](win32-tsgeneralsetting-setencryptionlevel.md)                       | Définit le niveau de chiffrement.<br/>                                                                                                                                   |
| [**SetSecurityLayer**](win32-tsgeneralsetting-setsecuritylayer.md)                           | Définit la couche de sécurité sur l’une des « couches de sécurité RDP » (0), « Negotiate » (1) ou « SSL » (2).<br/>                                                                   |
| [**SetUserAuthenticationRequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) | Active ou désactive l’exigence selon laquelle les utilisateurs doivent être authentifiés au moment de la connexion en définissant la valeur de la propriété **UserAuthenticationRequired** .<br/> |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ TSGeneralSetting** a ces propriétés.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Brève description (chaîne d’une ligne) de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**CertificateName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom d’affichage du nom d’objet du certificat personnel de l’ordinateur local.

</dd> <dt>

**Certificats**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Contient un magasin de certificats sérialisés qui contient tous les certificats du magasin de **comptes My User** sur l’ordinateur qui sont des certificats de serveur valides pour une utilisation avec SSL (Secure Sockets Layer).

</dd> <dt>

**Commentaire**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Nom descriptif de la combinaison couche de session et protocole de transport.

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")
</dt> </dl>

Date à laquelle l’objet a été installé. L’absence d’une valeur n’indique pas que l’objet n’est pas installé.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**MinEncryptionLevel**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **faible** («seules les données envoyées du client au serveur sont protégées par un chiffrement basé sur la puissance de clé standard du serveur. Les données envoyées du serveur au client ne sont pas protégées.»), **moyenne** (« toutes les données envoyées entre le serveur et le client sont protégées par un chiffrement basé sur la puissance de clé standard du serveur »), **élevé** (« toutes les données envoyées entre le serveur et le client sont protégées par le niveau de clé maximal de onserver basé sur le chiffrement. »)
</dt> </dl>

Niveau de chiffrement minimal.

<dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>**Faible** (1)


</dt> <dd>

Niveau de chiffrement faible. Seules les données envoyées du client au serveur sont chiffrées à l’aide du chiffrement 56 bits. Sachez que les données envoyées du serveur au client ne sont pas chiffrées.

</dd> <dt>

<span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>

<span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>**Compatible moyenne/client** (2)


</dt> <dd>

Niveau de chiffrement compatible avec le client. Toutes les données envoyées du client au serveur et du serveur au client sont chiffrées au niveau de clé maximal pris en charge par le client.

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>**Élevé** (3)


</dt> <dd>

Niveau élevé de chiffrement. Toutes les données envoyées du client au serveur et du serveur au client sont chiffrées à l’aide d’un chiffrement 128 bits puissant. Les clients qui ne prennent pas en charge ce niveau de chiffrement ne peuvent pas se connecter.

</dd> <dt>

<span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>

<span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>**Compatible FIPS** (4)


</dt> <dd>

Chiffrement compatible FIPS. Toutes les données envoyées du client au serveur et du serveur au client sont chiffrées et déchiffrées avec les algorithmes de chiffrement normes FIPS (Federal Information Processing Standard) (FIPS) à l’aide des modules de chiffrement Microsoft. FIPS est une norme intitulée « exigences de sécurité pour les modules cryptographiques ». FIPS 140-1 (1994) et FIPS 140-2 (2001) décrivent les exigences gouvernementales pour les modules de chiffrement matériels et logiciels utilisés au sein du gouvernement des États-Unis.

</dd> </dl>

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de l'objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**PolicySourceMinEncryptionLevel**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **MinEncryptionLevel** est configurée par le serveur, par la stratégie de groupe ou par défaut.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> <dt>

2 (0X2)
</dt> <dd>

Default

</dd> </dl>

</dd> <dt>

**PolicySourceSecurityLayer**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **securitylayer** est configurée par le serveur, par la stratégie de groupe ou par défaut.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> <dt>

2 (0X2)
</dt> <dd>

Default

</dd> </dl>

</dd> <dt>

**PolicySourceUserAuthenticationRequired**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **UserAuthenticationRequired** est configurée par le serveur, par la stratégie de groupe ou par défaut.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> <dt>

2 (0X2)
</dt> <dd>

Default

</dd> </dl>

</dd> <dt>

**SecurityLayer**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **RDPSecurityLayer** (« couche de sécurité RDP : communication entre le serverand le client utilise le chiffrement RDP natif. »), **Negotiate** («la couche la plus sécurisée prise en charge par le client sera utilisée. S’il est pris en charge, TLS 1,0 sera utilisé.»), **SSL** («SSL (TLS 1,0) sera utilisé pour l’authentification du serveur et forencrypting toutes les données transférées entre le serveur et le client. Ce paramètre requiert que le serveur dispose d’un certificat compatible SSL.»), **NEWTBD** (« une nouvelle couche de sécurité dans LONGHORN ».)
</dt> </dl>

Spécifie la couche de sécurité utilisée entre le client et le serveur.

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**Couche de sécurité RDP** (1)


</dt> <dd>

La communication entre le serveur et le client utilise le chiffrement RDP natif.

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Négocier** (2)


</dt> <dd>

La couche la plus sécurisée prise en charge par le client est utilisée. S’il est pris en charge, SSL (TLS 1,0) est utilisé.

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span id="SSL"></span><span id="ssl"></span>**SSL** (3)


</dt> <dd>

SSL (TLS 1,0) est utilisé pour l’authentification du serveur et pour le chiffrement de toutes les données transférées entre le serveur et le client. Ce paramètre requiert que le serveur dispose d’un certificat compatible SSL. Ce paramètre n’est pas compatible avec une valeur **MinEncryptionLevel** de 1.

</dd> <dt>

<span id="NEWTBD"></span><span id="newtbd"></span>

<span id="NEWTBD"></span><span id="newtbd"></span>**NEWTBD** (4)


</dt> <dd>

Nouvelle couche de sécurité.

</dd> </dl>

</dd> <dt>

**SSLCertificateSHA1Hash**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie le hachage SHA1 au format hexadécimal du certificat SSL à utiliser par le serveur cible.

L’empreinte numérique d’un certificat peut être trouvée à l’aide du composant logiciel enfichable Certificats de la console MMC sous l’onglet Détails de la page Propriétés du certificat.

</dd> <dt>

**SSLCertificateSHA1HashType**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique l’état de la propriété **SSLCertificateSHA1Hash** .

<dt>

0 (0x0)
</dt> <dd>

Non valide

</dd> <dt>

1 (0x1)
</dt> <dd>

Auto-signé par défaut

</dd> <dt>

2 (0X2)
</dt> <dd>

Stratégie de groupe par défaut appliquée

</dd> <dt>

3 (0x3)
</dt> <dd>

Custom

</dd> </dl>

</dd> <dt>

**État**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

État actuel de l’objet. Divers États opérationnels et inopérationnels peuvent être définis. Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche). Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ». Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives. Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

<dt>



 (« OK »)


</dt> <dd></dd> <dt>



 (« Erreur »)


</dt> <dd></dd> <dt>



 (« Détérioré »)


</dt> <dd></dd> <dt>



 ("Inconnu")


</dt> <dd></dd> <dt>



 (« Échec prédit »)


</dt> <dd></dd> <dt>



 (« Démarrage »)


</dt> <dd></dd> <dt>



 (« Arrêt »)


</dt> <dd></dd> <dt>



 (« Service »)


</dt> <dd></dd> </dl>

</dd> <dt>

**TerminalName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom du terminal.

Cette propriété est héritée de [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).

</dd> <dt>

**TerminalProtocol**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom du protocole de couche session ; par exemple, Microsoft RDP 5,0.

</dd> <dt>

**Transport**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type de transport utilisé dans la connexion ; par exemple, TCP, NetBIOS ou IPX/SPX.

</dd> <dt>

**UserAuthenticationRequired**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie le type d’authentification utilisateur utilisé pour les connexions à distance. Si la valeur est 1, ce qui signifie qu’elle est activée, **UserAuthenticationRequired** nécessite l’authentification de l’utilisateur au moment de la connexion pour augmenter la protection du serveur contre les attaques réseau. Seuls les clients [protocole RDP (Remote Desktop Protocol)](remote-desktop-protocol.md) (RDP) qui prennent en charge le protocole rdp version 6,0 ou une version ultérieure sont en mesure de se connecter. Pour éviter les interruptions pour les utilisateurs distants, il est recommandé de déployer les clients RDP qui prennent en charge la version de protocole appropriée avant d’activer la propriété.

Utilisez la méthode [**SetUserAuthenticationRequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) pour activer ou désactiver cette propriété.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

L’authentification de l’utilisateur au niveau de la connexion est désactivée.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

L’authentification utilisateur à la connexion est activée.

</dd> </dl>

</dd> <dt>

**WindowsAuthentication**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

spécifie si la connexion est définie par défaut sur le processus d’authentification Windows standard ou sur un autre package d’authentification qui a été installé sur le système.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

n’utilise pas par défaut le processus d’authentification Windows standard.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

la valeur par défaut est le processus d’authentification Windows standard.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Remarques

Sachez que les stations Windows qui ne sont pas associées à la session de console ne peuvent pas accéder aux méthodes et aux propriétés de cette classe. Si vous tentez de le faire en spécifiant « console » comme valeur de la propriété TerminalName, les méthodes de cet objet retournent **WBEM \_ E \_ non \_ pris en charge**. Ce code d’erreur est également renvoyé si une station Windows tente d’appeler des méthodes de cet objet dans le but d’ajouter ou de modifier les propriétés de sécurité des comptes LocalSystem, LocalService ou NetworkService.

Pour se connecter à \\ l' \\ \\ espace de noms licences TS cimv2 racine, le niveau d’authentification doit inclure la confidentialité du paquet. Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**. pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « pktPrivacy », avec une valeur de 6. l’exemple VBScript (Visual Basic scripting Edition) suivant montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TerminalSetting Win32**](win32-terminalsetting.md)
</dt> </dl>

 

