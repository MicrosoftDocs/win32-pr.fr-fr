---
title: Classe Win32_TSSessionDirectory
description: Définit les paramètres de configuration du Service Broker pour les connexions Bureau à distance Connexion Bureau à distance pour la \_ classe Win32 TSSessionDirectorySetting.
ms.assetid: ef9042c2-4a35-49e9-b195-fb37c0919068
ms.tgt_platform: multiple
keywords:
- Win32_TSSessionDirectory de la classe Services Bureau à distance
- Win32_TSSessionDirectory de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory
- Win32_TSSessionDirectory.Caption
- Win32_TSSessionDirectory.Description
- Win32_TSSessionDirectory.InstallDate
- Win32_TSSessionDirectory.Name
- Win32_TSSessionDirectory.Status
- Win32_TSSessionDirectory.SessionDirectoryLocation
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryLocation
- Win32_TSSessionDirectory.SessionDirectoryActive
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryActive
- Win32_TSSessionDirectory.SessionDirectoryExposeServerIP
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryExposeServerIP
- Win32_TSSessionDirectory.SessionDirectoryClusterName
- Win32_TSSessionDirectory.PolicySourceLoadBalancing
- Win32_TSSessionDirectory.GetLoadBalancingState
- Win32_TSSessionDirectory.GetServerWeight
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryClusterName
- Win32_TSSessionDirectory.SessionDirectoryIPAddress
- Win32_TSSessionDirectory.GetTSRedirectorMode
- Win32_TSSessionDirectory.PolicySourceTSRedirectorMode
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb50ed77b99f415ae551dfcf69655af5c1d77501
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193372"
---
# <a name="win32_tssessiondirectory-class"></a>\_Classe TSSessionDirectory Win32

Définit les paramètres de configuration du Service Broker pour les connexions Bureau à distance Connexion Bureau à distance pour la classe [**Win32 \_ TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) .

> [!Note]  
> dans Windows Server 2008 R2, le nom de session broker TS (session broker TS) a été modifié en service broker pour les connexions bureau à distance. Ces propriétés s’appliquent à tous les systèmes d’exploitation pris en charge, sauf indication contraire.

 

La syntaxe suivante est simplifiée à partir du code MOF et comprend toutes les propriétés définies et héritées, par ordre alphabétique. Pour obtenir des informations de référence sur les méthodes, consultez le tableau des méthodes plus loin dans cette rubrique.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("Win32_WIN32_TSSESSIONDIRECTORY_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TSSessionDirectory : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   SessionDirectoryLocation;
  uint32   PolicySourceSessionDirectoryLocation;
  uint32   SessionDirectoryActive;
  uint32   PolicySourceSessionDirectoryActive;
  uint32   SessionDirectoryExposeServerIP;
  uint32   PolicySourceSessionDirectoryExposeServerIP;
  string   SessionDirectoryClusterName;
  uint32   PolicySourceLoadBalancing;
  uint32   GetLoadBalancingState;
  uint32   GetServerWeight;
  uint32   PolicySourceSessionDirectoryClusterName;
  string   SessionDirectoryIPAddress;
  uint32   GetTSRedirectorMode;
  uint32   PolicySourceTSRedirectorMode;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ TSSessionDirectory** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ TSSessionDirectory** possède ces méthodes.



| Méthode                                                                                                  | Description                                                                                                  |
|:--------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| [**CreateUserDiskTemplate**](createuserdisktemplate-win32-tssessiondirectory.md)                       | Crée un modèle de disque utilisateur.<br/>                                                                     |
| [**DisableUserVhd**](disableuservhd-win32-tssessiondirectory.md)                                       | Désactive un disque dur virtuel de profil utilisateur.<br/>                                                                      |
| [**EnableUserVhd**](enableuservhd-win32-tssessiondirectory.md)                                         | Active un disque dur virtuel de profil utilisateur sur un serveur hôte hôte.<br/>                                                     |
| [**GetCurrentRedirectableAddresses**](getcurrentredirectableaddresses-win32-tssessiondirectory.md)     | Obtient la liste configurée actuellement des adresses DNS éligibles et le type de redirection.<br/>        |
| [**GetRedirectableAddresses**](getredirectableaddresses-win32-tssessiondirectory.md)                   | Obtient la liste complète des adresses DNS éligibles.<br/>                                                |
| [**PingSessionDirectory**](pingsessiondirectory-win32-tssessiondirectory.md)                           | Vérifie si le serveur du Service Broker pour les connexions Bureau à distance est disponible.<br/>                                      |
| [**SetCurrentRedirectableAddresses**](setcurrentredirectableaddresses-win32-tssessiondirectory.md)     | Définit la liste configurée des adresses DNS éligibles et le type de redirection.<br/>                     |
| [**SetLoadBalancingState**](setloadbalancingstate-win32-tssessiondirectory.md)                         | Définit la valeur pour indiquer si le serveur doit participer à l’équilibrage de charge du Service Broker pour les connexions Bureau à distance.<br/> |
| [**SetServerWeight**](setserverweight-win32-tssessiondirectory.md)                                     | Définit la valeur du poids du serveur pour l’équilibrage de charge du Service Broker pour les connexions Bureau à distance.<br/>                             |
| [**SetSessionDirectoryActive**](win32-tssessiondirectory-setsessiondirectoryactive.md)                 | Désactive et active le Service Broker pour les connexions Bureau à distance.<br/>                                                    |
| [**SetSessionDirectoryExposeServerIP**](win32-tssessiondirectory-setsessiondirectoryexposeserverip.md) | Définit la propriété **SessionDirectoryExposeServerIP** .<br/>                                             |
| [**SetSessionDirectoryProperty**](win32-tssessiondirectory-setsessiondirectoryproperty.md)             | Définit la propriété **SessionDirectoryLocation** ou la propriété **SessionDirectoryClusterName** .<br/>   |
| [**SetTSRedirectorMode**](settsredirectormode-win32-tssessiondirectory.md)                             | Cette méthode n’est pas disponible.<br/>                                                                     |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ TSSessionDirectory** a ces propriétés.

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

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**GetLoadBalancingState**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si le serveur est configuré pour participer à l’équilibrage de charge du Service Broker pour les connexions Bureau à distance.

<dt>

0
</dt> <dd>

Le serveur n’est pas configuré pour participer à l’équilibrage de charge du Service Broker pour les connexions Bureau à distance.

</dd> <dt>

1
</dt> <dd>

Le serveur est configuré pour participer à l’équilibrage de charge du Service Broker pour les connexions Bureau à distance.

</dd> </dl>

</dd> <dt>

**GetServerWeight**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Récupère la valeur de poids du serveur qui est utilisée dans l’équilibrage de charge du Service Broker pour les connexions Bureau à distance.

</dd> <dt>

**GetTSRedirectorMode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si le serveur est configuré pour agir en tant que redirecteur de Services Bureau à distance.

<dt>

0
</dt> <dd>

Le serveur est configuré pour agir en tant que redirecteur de Services Bureau à distance.

</dd> <dt>

1
</dt> <dd>

Le serveur n’est pas configuré pour agir en tant que redirecteur de Services Bureau à distance.

</dd> </dl>

**Windows Server 2008 :** Cette propriété n’est pas disponible.

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

**PolicySourceLoadBalancing**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **GetLoadBalancingState** est configurée par le serveur ou par la stratégie de groupe.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> </dl>

</dd> <dt>

**PolicySourceSessionDirectoryActive**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **SessionDirectoryActive** est configurée par le serveur ou par la stratégie de groupe.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> </dl>

</dd> <dt>

**PolicySourceSessionDirectoryClusterName**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **SessionDirectoryClusterName** est configurée par le serveur ou par la stratégie de groupe.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> </dl>

</dd> <dt>

**PolicySourceSessionDirectoryExposeServerIP**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **SessionDirectoryExposeServerIP** est configurée par le serveur ou par la stratégie de groupe.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> </dl>

</dd> <dt>

**PolicySourceSessionDirectoryLocation**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **SessionDirectoryLocation** est configurée par le serveur ou par la stratégie de groupe.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> </dl>

</dd> <dt>

**PolicySourceTSRedirectorMode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Cette propriété n’est pas disponible.

**Windows Server 2008 R2 :** Indique si la propriété **GetTSRedirectorMode** est configurée par le serveur ou par la stratégie de groupe.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> </dl>

</dd> <dt>

**SessionDirectoryActive**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Spécifie si Services Bureau à distance fait partie du Service Broker pour les connexions Bureau à distance.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Services Bureau à distance la participation au service Broker pour les connexions Bureau à distance est désactivée.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Services Bureau à distance la participation au service Broker pour les connexions Bureau à distance est activée.

</dd> </dl>

</dd> <dt>

**SessionDirectoryClusterName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Adresse IP virtuelle du cluster auquel appartient le serveur hôte de session Bureau à distance.

</dd> <dt>

**SessionDirectoryExposeServerIP**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie si la récupération de l’adresse IP du Service Broker pour les connexions Bureau à distance est autorisée.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

La récupération est refusée.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

La récupération est autorisée.

</dd> </dl>

</dd> <dt>

**SessionDirectoryIPAddress**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Adresse IP de la carte réseau utilisée par l’annuaire de sessions.

</dd> <dt>

**SessionDirectoryLocation**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom DNS réseau ou adresse IP du serveur sur lequel le service du Service Broker pour les connexions Bureau à distance est en cours d’exécution.

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

</dd> </dl>

## <a name="remarks"></a>Notes

Pour se connecter à l' \\ \\ \\ espace de \\ noms licences TS cimv2 racine, le niveau d’authentification doit inclure la confidentialité du paquet. Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**. pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « pktPrivacy », avec une valeur de six.

l’exemple VBScript (Visual Basic scripting Edition) suivant montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



dans Windows Server 2008, le nom de la fonctionnalité annuaire de sessions des services terminal server a été remplacé par session Broker des services terminal server.

dans Windows Server 2008 R2, le nom de la fonctionnalité Session broker des Services Terminal server a été remplacé par Connexion Bureau à distance broker.

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Paramètre CIM**](cim-setting.md)
</dt> <dt>

[**\_TSSessionDirectorySetting Win32**](win32-tssessiondirectorysetting.md)
</dt> </dl>

 

