---
title: Classe Win32_TSDeploymentSettings
description: Définit les paramètres par défaut utilisés par la Gestionnaire RemoteApp lors de la création de fichiers protocole RDP (Remote Desktop Protocol) (RDP).
ms.assetid: b3eeef86-e6cb-40ea-99f8-200c5993f31e
ms.tgt_platform: multiple
keywords:
- Win32_TSDeploymentSettings de la classe Services Bureau à distance
- Win32_TSDeploymentSettings de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSDeploymentSettings
- Win32_TSDeploymentSettings.Caption
- Win32_TSDeploymentSettings.Description
- Win32_TSDeploymentSettings.InstallDate
- Win32_TSDeploymentSettings.Name
- Win32_TSDeploymentSettings.Status
- Win32_TSDeploymentSettings.Port
- Win32_TSDeploymentSettings.FarmName
- Win32_TSDeploymentSettings.GatewayUsage
- Win32_TSDeploymentSettings.GatewayName
- Win32_TSDeploymentSettings.GatewayAuthMode
- Win32_TSDeploymentSettings.GatewayUseCachedCreds
- Win32_TSDeploymentSettings.RequireServerAuth
- Win32_TSDeploymentSettings.ColorBitDepth
- Win32_TSDeploymentSettings.AllowFontSmoothing
- Win32_TSDeploymentSettings.UseMultimon
- Win32_TSDeploymentSettings.RedirectionOptions
- Win32_TSDeploymentSettings.HasCertificate
- Win32_TSDeploymentSettings.CertificateHash
- Win32_TSDeploymentSettings.CertificateIssuedTo
- Win32_TSDeploymentSettings.CertificateIssuedBy
- Win32_TSDeploymentSettings.CertificateExpiresOn
- Win32_TSDeploymentSettings.CustomRDPSettings
- Win32_TSDeploymentSettings.DeploymentRDPSettings
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f254363968099ab73c5f3f14f1f15ab8554f62a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465091"
---
# <a name="win32_tsdeploymentsettings-class"></a>\_Classe TSDeploymentSettings Win32

Définit les paramètres par défaut utilisés par la Gestionnaire RemoteApp lors de la création de fichiers protocole RDP (Remote Desktop Protocol) (RDP). Ces paramètres n’affectent pas les applications ou les ordinateurs de bureau publiés.

## <a name="syntax"></a>Syntaxe

``` syntax
class Win32_TSDeploymentSettings : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  sint32   Port;
  string   FarmName;
  sint32   GatewayUsage;
  string   GatewayName;
  sint32   GatewayAuthMode;
  boolean  GatewayUseCachedCreds;
  boolean  RequireServerAuth;
  sint32   ColorBitDepth;
  boolean  AllowFontSmoothing;
  boolean  UseMultimon;
  sint32   RedirectionOptions;
  boolean  HasCertificate;
  uint8    CertificateHash[];
  string   CertificateIssuedTo;
  string   CertificateIssuedBy;
  string   CertificateExpiresOn;
  string   CustomRDPSettings;
  string   DeploymentRDPSettings;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ TSDeploymentSettings** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ TSDeploymentSettings** a ces propriétés.

<dl> <dt>

**AllowFontSmoothing**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique s’il faut autoriser le lissage des polices.

</dd> <dt>

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

**CertificateExpiresOn**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Date d’expiration du certificat. Cette valeur est stockée sous la forme d’un format [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) 64 bits.

</dd> <dt>

**CertificateHash**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Empreinte numérique du certificat utilisé pour signer les fichiers RDP.

</dd> <dt>

**CertificateIssuedBy**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie à qui le certificat est émis.

</dd> <dt>

**CertificateIssuedTo**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie à qui le certificat est émis.

</dd> <dt>

**ColorBitDepth**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Profondeur de bit de couleur de l’affichage. Les valeurs possibles sont 4, 8, 15, 16, 24 et 32.

</dd> <dt>

**CustomRDPSettings**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Contenu du fichier RDP qui correspond aux paramètres RDP personnalisés dans Gestionnaire RemoteApp.

</dd> <dt>

**DeploymentRDPSettings**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Contenu du fichier RDP qui correspond aux paramètres de déploiement dans Gestionnaire RemoteApp. Si cette valeur est définie, les paramètres de déploiement RDP remplacent les paramètres par défaut de cette classe. Par exemple, si vous définissez la propriété **GatewayAuthMode** dans cette classe et que vous définissez la propriété **DeploymentRDPSettings** , la propriété **GatewayAuthMode** de cette classe sera ignorée et la valeur **GatewayAuthMode** de la **DeploymentRDPSettings** sera utilisée.

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

**FarmName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Nom du serveur hôte de session Bureau à distance ou nom de domaine complet (FQDN) de la batterie de serveurs hôte de session Bureau à distance.

</dd> <dt>

**GatewayAuthMode**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Méthode d’authentification de la passerelle des services Bureau à distance. Les valeurs suivantes sont possibles.

<dt>

0
</dt> <dd>

Mot de passe

</dd> <dt>

1
</dt> <dd>

Carte à puce

</dd> <dt>

4
</dt> <dd>

Autoriser l’utilisateur à effectuer une sélection pendant la connexion.

</dd> </dl>

</dd> <dt>

**GatewayName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Nom du serveur de passerelle Bureau à distance à utiliser.

</dd> <dt>

**GatewayUsage**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique s’il faut utiliser un serveur de passerelle Bureau à distance pour se connecter au serveur hôte de session Bureau à distance cible à travers un pare-feu. Les valeurs suivantes sont possibles.

<dt>

0
</dt> <dd>

N’utilisez pas de serveur de passerelle Bureau à distance.

</dd> <dt>

1
</dt> <dd>

Utilisez un serveur de passerelle Bureau à distance. Contournez le serveur de passerelle Bureau à distance pour les adresses locales.

</dd> <dt>

2
</dt> <dd>

Utilisez un serveur de passerelle Bureau à distance.

</dd> <dt>

3
</dt> <dd>

Détecter automatiquement les paramètres du serveur de passerelle Bureau à distance.

</dd> </dl>

</dd> <dt>

**GatewayUseCachedCreds**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Dans la mesure du possible, utilisez les mêmes informations d’identification de l’utilisateur pour le serveur de passerelle Bureau à distance et le serveur hôte de session Bureau à distance.

</dd> <dt>

**HasCertificate**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique s’il faut utiliser un certificat pour signer les fichiers RDP.

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

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de l'objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Port**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Port RDP à utiliser.

</dd> <dt>

**RedirectionOptions**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie les options de redirection des appareils et des ressources pour les connexions RemoteApp. Les indicateurs pour **RedirectionOptions** peuvent être combinés. Les valeurs suivantes sont possibles.

<dt>

0
</dt> <dd>

Aucune redirection de l’appareil ou de la ressource.

</dd> <dt>

1
</dt> <dd>

Rediriger les lecteurs de disque.

</dd> <dt>

2
</dt> <dd>

Rediriger les imprimantes.

</dd> <dt>

4
</dt> <dd>

Redirigez le presse-papiers.

</dd> <dt>

8
</dt> <dd>

Redirigez les appareils Plug-and-Play pris en charge.

</dd> <dt>

16
</dt> <dd>

Rediriger les cartes à puce.

</dd> <dt>

32
</dt> <dd>

Rediriger l’audio.

</dd> <dt>

64
</dt> <dd>

Rediriger les ports série.

</dd> </dl>

</dd> <dt>

**RequireServerAuth**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique s’il faut exiger l’authentification du serveur.

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

**UseMultimon**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si plusieurs analyses sont activées pour le bureau.

</dd> </dl>

## <a name="remarks"></a>Notes

Vous devez être membre du groupe administrateurs pour définir des propriétés à l’aide de cette classe.

Si **RequireServerAuth** a la valeur **true**, tenez compte des points suivants :

-   Si le programme RemoteApp est destiné à une utilisation intranet et que tous les ordinateurs clients exécutent Windows Server 2008 ou Windows Vista, vous n’avez pas besoin de configurer le serveur hôte de session Bureau à distance pour utiliser un certificat SSL. Dans ce cas, Authentification au niveau du réseau est utilisé.
-   Vous devez spécifier le nom de domaine complet du serveur ou de la batterie de serveurs pour la valeur de la propriété **FarmName** .

Pour se connecter à l’espace de noms « CIMV2 \\ licences TS », le niveau d’authentification doit inclure la confidentialité du paquet. Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**, qui peut être défini à l’aide de la fonction com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) . Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de 6. L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Ils sont installés sur l’ordinateur lorsque vous ajoutez le rôle associé. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tsallow. mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



 

