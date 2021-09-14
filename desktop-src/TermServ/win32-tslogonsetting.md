---
title: Classe Win32_TSLogonSetting
description: Définit des paramètres de configuration pour la \_ classe de terminal Win32 relative à l’ouverture de session client.
ms.assetid: a2ccb419-da1a-44d1-8a7a-4d0266fc1be8
ms.tgt_platform: multiple
keywords:
- Win32_TSLogonSetting de la classe Services Bureau à distance
- Win32_TSLogonSetting de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting
- Win32_TSLogonSetting.Caption
- Win32_TSLogonSetting.Description
- Win32_TSLogonSetting.InstallDate
- Win32_TSLogonSetting.Name
- Win32_TSLogonSetting.Status
- Win32_TSLogonSetting.TerminalName
- Win32_TSLogonSetting.ClientLogonInfoPolicy
- Win32_TSLogonSetting.Domain
- Win32_TSLogonSetting.Password
- Win32_TSLogonSetting.PolicySourceDomain
- Win32_TSLogonSetting.PolicySourcePromptForPassword
- Win32_TSLogonSetting.PolicySourceUserName
- Win32_TSLogonSetting.PromptForPassword
- Win32_TSLogonSetting.UserName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e656f3913bb7320253dc9dbca6710f37e0cbdded
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193411"
---
# <a name="win32_tslogonsetting-class"></a>\_Classe TSLogonSetting Win32

La classe WMI **Win32 \_ TSLogonSetting** définit des paramètres de configuration pour la classe de [**\_ Terminal Win32**](win32-terminal.md) relative à l’ouverture de session client.

La syntaxe suivante est simplifiée à partir du code MOF et comprend toutes les propriétés définies et héritées, par ordre alphabétique. Pour obtenir des informations de référence sur les méthodes, consultez le tableau des méthodes plus loin dans cette rubrique.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("Win32_WIN32_TSLOGONSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSLogonSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ClientLogonInfoPolicy;
  string   Domain;
  string   Password;
  uint32   PolicySourceDomain;
  uint32   PolicySourcePromptForPassword;
  uint32   PolicySourceUserName;
  uint32   PromptForPassword;
  string   UserName;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ TSLogonSetting** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ TSLogonSetting** possède ces méthodes.



| Méthode                                                                    | Description                                                                    |
|:--------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**ExplicitLogon**](win32-tslogonsetting-explicitlogon.md)               | Définit les informations d’identification du nom d’utilisateur, du mot de passe et de l’authentification de domaine.<br/> |
| [**SetPromptForPassword**](win32-tslogonsetting-setpromptforpassword.md) | Définit la propriété **PromptForPassword** .<br/>                            |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ TSLogonSetting** a ces propriétés.

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

**ClientLogonInfoPolicy**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

La stratégie utilisée par le serveur pour déterminer les paramètres de connexion.

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Par utilisateur** (0)


</dt> <dd>

Les paramètres de connexion utilisateur individuels sont activés.

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Serveur-override** (1)


</dt> <dd>

Les paramètres de connexion utilisateur individuels sont remplacés par le serveur.

</dd> </dl>

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

**Domaine**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Informations d’identification d’authentification de connexion au domaine de l’utilisateur. Il s’agit du domaine dans lequel réside l’ordinateur de l’utilisateur. Cette propriété ne peut pas dépasser 17 caractères.

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

**Mot de passe**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Informations d’identification d’authentification par mot de passe de l’utilisateur. Cette propriété ne peut pas comporter plus de 14 caractères. Il est recommandé de définir le niveau de sécurité sur la confidentialité des paquets (wbemAuthenticationLevelPktPrivacy = 6) si vous interrogez cette propriété. Cela est dû au fait que le mot de passe n’est pas chiffré sur le réseau sans ce niveau de sécurité. Pour plus d’informations sur la définition des niveaux de sécurité, consultez Définition de la sécurité des processus de l' [application cliente](/windows/desktop/WmiSdk/setting-client-application-process-security) dans la documentation du SDK WMI.

</dd> <dt>

**PolicySourceDomain**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété de **domaine** est configurée par le serveur, la stratégie de groupe ou par défaut.

<dt>

0
</dt> <dd>

Serveur

</dd> <dt>

1
</dt> <dd>

Stratégie de groupe

</dd> <dt>

2
</dt> <dd>

Default

</dd> </dl>

</dd> <dt>

**PolicySourcePromptForPassword**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **PromptForPassword** est configurée par le serveur, la stratégie de groupe ou par défaut.

<dt>

0
</dt> <dd>

Serveur

</dd> <dt>

1
</dt> <dd>

Stratégie de groupe

</dd> <dt>

2
</dt> <dd>

Default

</dd> </dl>

</dd> <dt>

**PolicySourceUserName**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété de **nom d’utilisateur** est configurée par le serveur, la stratégie de groupe ou par défaut.

<dt>

0
</dt> <dd>

Serveur

</dd> <dt>

1
</dt> <dd>

Stratégie de groupe

</dd> <dt>

2
</dt> <dd>

Default

</dd> </dl>

</dd> <dt>

**PromptForPassword**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie si l’utilisateur est toujours invité à entrer un mot de passe lors de la connexion au serveur.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

L’utilisateur n’est pas invité à entrer un mot de passe.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

L'utilisateur est invité à entrer un mot de passe.

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

**UserName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Informations d’identification d’authentification par nom d’utilisateur de l’utilisateur. Cette propriété ne peut pas comporter plus de 20 caractères.

</dd> </dl>

## <a name="remarks"></a>Notes

Sachez que les winstations associés à la session de console ne peuvent pas accéder aux méthodes et aux propriétés de cette classe. Si vous tentez de le faire en spécifiant « console » comme valeur de la propriété TerminalName, les méthodes de cet objet retournent **WBEM \_ E \_ non \_ pris en charge**. Ce code d’erreur est retourné si une station Windows tente d’appeler des méthodes de cet objet pour ajouter ou modifier les propriétés de sécurité des comptes LocalSystem, LocalService ou NetworkService.

Pour se connecter à \\ l' \\ \\ espace de noms licences TS cimv2 racine, le niveau d’authentification doit inclure la confidentialité du paquet. Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**. pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « pktPrivacy », avec une valeur de 6. l’exemple VBScript (Visual Basic scripting Edition) suivant montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Terminal Win32**](win32-terminal.md)
</dt> <dt>

[**\_TerminalSetting Win32**](win32-terminalsetting.md)
</dt> </dl>

 

