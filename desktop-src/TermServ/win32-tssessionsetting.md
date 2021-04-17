---
title: Classe Win32_TSSessionSetting
description: Définit des paramètres de configuration pour la \_ classe de terminal Win32, tels que les limites de temps, les actions de déconnexion et de reconnexion.
ms.assetid: e115f370-270c-404f-b6c6-7781c1ff376f
ms.tgt_platform: multiple
keywords:
- Win32_TSSessionSetting de la classe Services Bureau à distance
- Win32_TSSessionSetting de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting
- Win32_TSSessionSetting.Caption
- Win32_TSSessionSetting.Description
- Win32_TSSessionSetting.InstallDate
- Win32_TSSessionSetting.Name
- Win32_TSSessionSetting.Status
- Win32_TSSessionSetting.TerminalName
- Win32_TSSessionSetting.ActiveSessionLimit
- Win32_TSSessionSetting.BrokenConnectionAction
- Win32_TSSessionSetting.BrokenConnectionPolicy
- Win32_TSSessionSetting.DisconnectedSessionLimit
- Win32_TSSessionSetting.IdleSessionLimit
- Win32_TSSessionSetting.PolicySourceActiveSessionLimit
- Win32_TSSessionSetting.PolicySourceBrokenConnectionAction
- Win32_TSSessionSetting.PolicySourceDisconnectedSessionLimit
- Win32_TSSessionSetting.PolicySourceIdleSessionLimit
- Win32_TSSessionSetting.PolicySourceReconnectionPolicy
- Win32_TSSessionSetting.ReconnectionPolicy
- Win32_TSSessionSetting.TimeLimitPolicy
- Win32_TSSessionSetting.EnableTimeoutWarning
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e780cdedee0fe447499bed5013dadc2ba9b448b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509374"
---
# <a name="win32_tssessionsetting-class"></a>\_Classe TSSessionSetting Win32

La classe WMI **Win32 \_ TSSessionSetting** définit des paramètres de configuration pour la classe de [**\_ Terminal Win32**](win32-terminal.md) , tels que les limites de temps, les actions de déconnexion et de reconnexion.

La syntaxe suivante est simplifiée à partir du code MOF et comprend toutes les propriétés définies et héritées, par ordre alphabétique. Pour obtenir des informations de référence sur les méthodes, consultez le tableau des méthodes plus loin dans cette rubrique.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("Win32_WIN32_TSSESSIONSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSSessionSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ActiveSessionLimit;
  uint32   BrokenConnectionAction;
  uint32   BrokenConnectionPolicy;
  uint32   DisconnectedSessionLimit;
  uint32   IdleSessionLimit;
  uint32   PolicySourceActiveSessionLimit;
  uint32   PolicySourceBrokenConnectionAction;
  uint32   PolicySourceDisconnectedSessionLimit;
  uint32   PolicySourceIdleSessionLimit;
  uint32   PolicySourceReconnectionPolicy;
  uint32   ReconnectionPolicy;
  uint32   TimeLimitPolicy;
  uint32   EnableTimeoutWarning;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ TSSessionSetting** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ TSSessionSetting** possède ces méthodes.



| Méthode                                                              | Description                                                              |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**BrokenConnection**](win32-tssessionsetting-brokenconnection.md) | Définit les propriétés de connexion rompues incluses dans cette classe.<br/> |
| [**TimeLimit**](win32-tssessionsetting-timelimit.md)               | Définit les propriétés de limite de temps incluses dans cette classe.<br/>        |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ TSSessionSetting** a ces propriétés.

<dl> <dt>

**ActiveSessionLimit**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Durée maximale, en millisecondes, allouée à une session active. La valeur 0 spécifie une durée infinie.

</dd> <dt>

**BrokenConnectionAction**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Action que le serveur effectue sur la session lorsqu’une connexion a été interrompue en raison d’une perte de réseau ou de délais.

<dt>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Déconnecter** (0)


</dt> <dd>

L’utilisateur est déconnecté de la session.

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (1)


</dt> <dd>

La session est définitivement supprimée du serveur.

</dd> </dl>

</dd> <dt>

**BrokenConnectionPolicy**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

La stratégie utilisée par le serveur pour déterminer quand arrêter une connexion en raison d’une perte de réseau ou de délais.

<dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Serveur-override** (1)


</dt> <dd>

Les paramètres de stratégie de déconnexion de l’utilisateur sont remplacés par le serveur.

</dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Par utilisateur** (0)


</dt> <dd>

Les paramètres de stratégie de déconnexion de l’utilisateur sont activés.

</dd> </dl>

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

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**DisconnectedSessionLimit**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Intervalle de temps, en millisecondes, après lequel une session déconnectée est arrêtée. La valeur 0 spécifie une durée infinie.

</dd> <dt>

**EnableTimeoutWarning**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Active l’avertissement d’expiration du délai d’attente.

**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** Cette propriété n’est pas disponible.

</dd> <dt>

**IdleSessionLimit**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Intervalle de temps, en millisecondes, après lequel une session inactive est terminée. La valeur 0 spécifie une durée infinie.

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

**PolicySourceActiveSessionLimit**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **ActiveSessionLimit** est configurée par le serveur, la stratégie de groupe ou par défaut.

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

**PolicySourceBrokenConnectionAction**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **BrokenConnectionAction** est configurée par le serveur, la stratégie de groupe ou par défaut.

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

**PolicySourceDisconnectedSessionLimit**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **DisconnectedSessionLimit** est configurée par le serveur, la stratégie de groupe ou par défaut.

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

**PolicySourceIdleSessionLimit**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **IdleSessionLimit** est configurée par le serveur, la stratégie de groupe ou par défaut.

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

**PolicySourceReconnectionPolicy**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **ReconnectPolicy** est configurée par le serveur, la stratégie de groupe ou par défaut.

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

**ReconnectionPolicy**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie si un utilisateur doit utiliser le client précédent pour se reconnecter à une session déconnectée.

<dt>

<span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>

<span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>**N’importe quel client** (0)


</dt> <dd>

N’importe quel client sera utilisé pour se reconnecter.

</dd> <dt>

<span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>

<span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>**Client précédent** (1)


</dt> <dd>

Le client précédent utilisé dans une connexion sera utilisé pour se reconnecter.

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

**TimeLimitPolicy**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

La stratégie utilisée par le serveur pour déterminer les limites de temps pour les sessions utilisateur.

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Par utilisateur** (0)


</dt> <dd>

Les paramètres de stratégie de limites horaires de l’utilisateur sont activés.

</dd> <dt>

<span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>

<span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>**Remplacement de serveur** (1)


</dt> <dd>

Les paramètres de stratégie de limites horaires de l’utilisateur sont remplacés par le serveur.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Notes

Sachez que les winstations associés à la session de console ne peuvent pas accéder aux méthodes et aux propriétés de cette classe. Si vous tentez de le faire en spécifiant « console » comme valeur de la propriété TerminalName, les méthodes de cet objet retournent **WBEM \_ E \_ non \_ pris en charge**. Ce code d’erreur est également renvoyé si une station Windows tente d’appeler des méthodes de cet objet dans le but d’ajouter ou de modifier les propriétés de sécurité des comptes LocalSystem, LocalService ou NetworkService.

Pour se connecter à l’espace de noms « root \\ cimv2 \\ licences TS », le niveau d’authentification doit inclure la confidentialité du paquet. Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**. Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de 6. L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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
</dt> <dt>

[**\_Paramètre CIM**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

