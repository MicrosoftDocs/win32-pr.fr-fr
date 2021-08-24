---
title: Classe Win32_TSEnvironmentSetting
description: Définit les paramètres de configuration pour la \_ classe de terminal Win32, y compris la stratégie de programme initiale.
ms.assetid: 2d310a1e-a1bd-4ccb-965e-8389aaa2e4c1
ms.tgt_platform: multiple
keywords:
- Win32_TSEnvironmentSetting de la classe Services Bureau à distance
- Win32_TSEnvironmentSetting de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting
- Win32_TSEnvironmentSetting.Caption
- Win32_TSEnvironmentSetting.Description
- Win32_TSEnvironmentSetting.InstallDate
- Win32_TSEnvironmentSetting.Name
- Win32_TSEnvironmentSetting.Status
- Win32_TSEnvironmentSetting.TerminalName
- Win32_TSEnvironmentSetting.ClientWallPaper
- Win32_TSEnvironmentSetting.InitialProgramPath
- Win32_TSEnvironmentSetting.InitialProgramPolicy
- Win32_TSEnvironmentSetting.PolicySourceClientWallPaper
- Win32_TSEnvironmentSetting.PolicySourceInitialProgramPath
- Win32_TSEnvironmentSetting.PolicySourceStartIn
- Win32_TSEnvironmentSetting.Startin
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ede3347581267d9fcec00a82c016c273c239c9673b536843753e6b59ec2341
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119514319"
---
# <a name="win32_tsenvironmentsetting-class"></a>\_Classe TSEnvironmentSetting Win32

La classe WMI **Win32 \_ TSEnvironmentSetting** définit les paramètres de configuration pour la classe de [**\_ Terminal Win32**](win32-terminal.md) , y compris la stratégie de programme initiale.

La syntaxe suivante est simplifiée à partir du code MOF et comprend toutes les propriétés définies et héritées, par ordre alphabétique. Pour obtenir des informations de référence sur les méthodes, consultez le tableau des méthodes plus loin dans cette rubrique.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("Win32_WIN32_TSENVIRONMENTSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSEnvironmentSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ClientWallPaper;
  string   InitialProgramPath;
  uint32   InitialProgramPolicy;
  uint32   PolicySourceClientWallPaper;
  uint32   PolicySourceInitialProgramPath;
  uint32   PolicySourceStartIn;
  string   Startin;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ TSEnvironmentSetting** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ TSEnvironmentSetting** possède ces méthodes.



| Méthode                                                                      | Description                                                            |
|:----------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**InitialProgram**](win32-tsenvironmentsetting-initialprogram.md)         | Définit les propriétés du programme de démarrage incluses dans cette classe.<br/> |
| [**SetClientWallPaper**](win32-tsenvironmentsetting-setclientwallpaper.md) | Définit la propriété **ClientWallPaper** .<br/>                      |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ TSEnvironmentSetting** a ces propriétés.

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

**ClientWallPaper**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie si l’image de papier peint est affichée sur le client. Si vous n’affichez pas l’image de papier peint, vous pouvez économiser des ressources système en diminuant le temps nécessaire pour redessiner l’écran.

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)


</dt> <dd>

L’image de papier peint n’est pas affichée sur le client.

</dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)


</dt> <dd>

L’image de papier peint est affichée sur le client.

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

**InitialProgramPath**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Le nom et le chemin d’accès du programme que l’utilisateur exécutera immédiatement après l’ouverture de session sur le serveur hôte de session Bureau à distance.

</dd> <dt>

**InitialProgramPolicy**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

La stratégie utilisée par le serveur pour déterminer le chemin d’accès et le nom de fichier du programme de démarrage, ainsi que le nom du dossier dans lequel il se trouve.

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Par utilisateur** (0)


</dt> <dd>

Les paramètres du programme de démarrage de l’utilisateur sont activés.

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Serveur-override** (1)


</dt> <dd>

Les paramètres du programme de démarrage de l’utilisateur sont remplacés par le serveur.

</dd> <dt>

<span id="Single-App_Mode"></span><span id="single-app_mode"></span><span id="SINGLE-APP_MODE"></span>

<span id="Single-App_Mode"></span><span id="single-app_mode"></span><span id="SINGLE-APP_MODE"></span>**Mode mono-application** (2)


</dt> <dd>

Une seule application est exécutée dans cette session. Les informations du programme de démarrage sont ignorées.

</dd> </dl>

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

**PolicySourceClientWallPaper**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **ClientWallPaper** est configurée par le serveur, la stratégie de groupe ou par défaut.

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

Par défaut

</dd> </dl>

</dd> <dt>

**PolicySourceInitialProgramPath**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **InitialProgramPath** est configurée par le serveur, la stratégie de groupe ou par défaut.

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

Par défaut

</dd> </dl>

</dd> <dt>

**PolicySourceStartIn**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **Started** est configurée par le serveur, la stratégie de groupe ou par défaut.

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

Par défaut

</dd> </dl>

</dd> <dt>

**Startin**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès du répertoire de travail du programme que l’utilisateur exécutera immédiatement après l’ouverture de session sur le serveur hôte de session Bureau à distance.

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

</dd> </dl>

## <a name="remarks"></a>Remarques

Sachez que les winstations qui sont associés à la session de console ne peuvent pas accéder aux méthodes et aux propriétés de cette classe. Si vous tentez de le faire en spécifiant « console » comme valeur de la propriété **TerminalName** , les méthodes de cet objet retournent **WBEM \_ E \_ non \_ pris en charge**. Ce code d’erreur est également retourné si une station Windows tente d’appeler des méthodes de cet objet pour ajouter ou modifier les propriétés de sécurité des comptes LocalSystem, LocalService ou NetworkService.

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

 

