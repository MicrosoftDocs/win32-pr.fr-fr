---
description: Représente un système d’ordinateur physique ou un ordinateur virtuel.
ms.assetid: 1db9e169-1466-4898-ab95-e9d622fe43cb
title: Classe Msvm_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem
- Msvm_ComputerSystem.SetPowerState
- Msvm_ComputerSystem.InstanceID
- Msvm_ComputerSystem.Caption
- Msvm_ComputerSystem.Description
- Msvm_ComputerSystem.ElementName
- Msvm_ComputerSystem.InstallDate
- Msvm_ComputerSystem.OperationalStatus
- Msvm_ComputerSystem.StatusDescriptions
- Msvm_ComputerSystem.Status
- Msvm_ComputerSystem.HealthState
- Msvm_ComputerSystem.CommunicationStatus
- Msvm_ComputerSystem.DetailedStatus
- Msvm_ComputerSystem.OperatingStatus
- Msvm_ComputerSystem.PrimaryStatus
- Msvm_ComputerSystem.EnabledState
- Msvm_ComputerSystem.OtherEnabledState
- Msvm_ComputerSystem.RequestedState
- Msvm_ComputerSystem.EnabledDefault
- Msvm_ComputerSystem.TimeOfLastStateChange
- Msvm_ComputerSystem.AvailableRequestedStates
- Msvm_ComputerSystem.TransitioningToState
- Msvm_ComputerSystem.CreationClassName
- Msvm_ComputerSystem.Name
- Msvm_ComputerSystem.PrimaryOwnerName
- Msvm_ComputerSystem.PrimaryOwnerContact
- Msvm_ComputerSystem.Roles
- Msvm_ComputerSystem.NameFormat
- Msvm_ComputerSystem.OtherIdentifyingInfo
- Msvm_ComputerSystem.IdentifyingDescriptions
- Msvm_ComputerSystem.Dedicated
- Msvm_ComputerSystem.OtherDedicatedDescriptions
- Msvm_ComputerSystem.ResetCapability
- Msvm_ComputerSystem.PowerManagementCapabilities
- Msvm_ComputerSystem.OnTimeInMilliseconds
- Msvm_ComputerSystem.ProcessID
- Msvm_ComputerSystem.TimeOfLastConfigurationChange
- Msvm_ComputerSystem.NumberOfNumaNodes
- Msvm_ComputerSystem.ReplicationState
- Msvm_ComputerSystem.ReplicationHealth
- Msvm_ComputerSystem.ReplicationMode
- Msvm_ComputerSystem.FailedOverReplicationType
- Msvm_ComputerSystem.LastReplicationType
- Msvm_ComputerSystem.LastApplicationConsistentReplicationTime
- Msvm_ComputerSystem.LastReplicationTime
- Msvm_ComputerSystem.LastSuccessfulBackupTime
- Msvm_ComputerSystem.EnhancedSessionModeState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae36179e14b584bad4e68350e27d485cdc10c42b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551878"
---
# <a name="msvm_computersystem-class"></a>\_Classe MSVM ComputerSystem

Représente un système d’ordinateur physique ou un ordinateur virtuel.

Pour récupérer des informations pour le VMMS, utilisez la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ComputerSystem : CIM_ComputerSystem
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   CreationClassName;
  string   Name = "GUID";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   NameFormat;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability = 1;
  uint16   PowerManagementCapabilities[];
  uint64   OnTimeInMilliseconds;
  uint32   ProcessID;
  datetime TimeOfLastConfigurationChange;
  uint16   NumberOfNumaNodes;
  uint16   ReplicationState;
  uint16   ReplicationHealth;
  uint16   ReplicationMode;
  uint16   FailedOverReplicationType;
  uint16   LastReplicationType;
  DateTime LastApplicationConsistentReplicationTime;
  DateTime LastReplicationTime;
  DateTime LastSuccessfulBackupTime;
  uint16   EnhancedSessionModeState;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ ComputerSystem** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MSVM \_ ComputerSystem** possède ces méthodes.



| Méthode                                                                                         | Description                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InjectNonMaskableInterrupt**](injectnonmaskableinterrupt-msvm-computersystem.md)           | Injecte une interruption non masquable dans la machine virtuelle. Cette méthode est prise en charge uniquement pour les instances de la classe **MSVM \_ ComputerSystem** qui représentent un ordinateur virtuel.<br/> **Windows 8.1 :** Cette méthode n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.<br/>                                    |
| [**RequestReplicationStateChange**](msvm-computersystem-requestreplicationstatechange.md)     | Demande que l’état de réplication de l’ordinateur virtuel soit remplacé par la valeur spécifiée. Cette méthode est prise en charge uniquement pour les instances de la classe **MSVM \_ ComputerSystem** qui représentent un ordinateur virtuel.<br/>                                                                                                        |
| [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md) | Demande que l’état de réplication de l’ordinateur virtuel soit remplacé par la valeur spécifiée. Cette méthode est prise en charge uniquement pour les instances de la classe **MSVM \_ ComputerSystem** qui représentent un ordinateur virtuel.<br/> **Windows 8.1 :** Cette méthode n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.<br/> |
| [**RequestStateChange**](requeststatechange-msvm-computersystem.md)                           | Demande que l’état de l’ordinateur virtuel soit modifié. Cette méthode est prise en charge uniquement pour les instances de la classe **MSVM \_ ComputerSystem** qui représentent un ordinateur virtuel.<br/>                                                                                                                                           |
| **SetPowerState**                                                                              | Cette méthode n'est pas prise en charge.<br/>                                                                                                                                                                                                                                                                                            |



 

### <a name="properties"></a>Propriétés

La classe **MSVM \_ ComputerSystem** possède ces propriétés.

<dl> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) utilisée pour initier un changement d’État. Les valeurs répertoriées sont un sous-ensemble des valeurs contenues dans la propriété **RequestedStatesSupported** de l’instance associée de la **\_ EnabledLogicalElementCapabilities CIM**, où les valeurs sélectionnées sont une fonction de l’état actuel de l’objet [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) . Cette propriété peut être non **null** si une implémentation est en mesure de publier l’ensemble de valeurs possibles en tant que fonction de l’état actuel. Cette propriété a la **valeur null** si une implémentation ne peut pas déterminer le jeu de valeurs possibles en tant que fonction de l’état actuel.

Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).

<dl> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)
</dt> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arrêter** (4)
</dt> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Hors connexion** (6)
</dt> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)
</dt> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Différer** (8)
</dt> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Suspension** (9)
</dt> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Redémarrer** (10)
</dt> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Réinitialiser** (11)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF réservé** (.. )
</dt> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Brève description de l’objet. Cette propriété est héritée de la classe [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) et contient l’une des valeurs suivantes.



| Valeur                                                                                                | Signification                                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>« Ordinateur virtuel »</dt> </dl>         | L’instance représente une machine virtuelle.<br/>    |
| <dl> <dt>« Système informatique d’hébergement »</dt> </dl> | L’instance représente l’ordinateur hôte.<br/> |



 

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent. Une valeur **null** indique que cette propriété n’est pas implémentée. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de la classe ou de la sous-classe utilisée lors de la création d’une instance. Cette propriété est héritée [**du \_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system)et est toujours définie sur « MSVM \_ ComputerSystem ».

</dd> <dt>

**Dédié**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si le système informatique est un système à usage spécifique (dédié à une utilisation particulière) et s’il s’agit d’un système à usage général. Cette propriété est héritée de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)et est toujours définie sur 0 (non dédié).

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et contient l’une des valeurs suivantes.



| Valeur                                                                                                          | Signification                                                  |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>« Système d’ordinateur virtuel Microsoft »</dt> </dl> | L’instance représente une machine virtuelle.<br/>    |
| <dl> <dt>« Système informatique d’hébergement Microsoft »</dt> </dl> | L’instance représente l’ordinateur hôte.<br/> |



 

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires. Une valeur **null** indique que cette propriété n’est pas implémentée. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’objet. Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur le nom d’affichage de l’ordinateur pour un ordinateur virtuel ou le nom NetBIOS du système d’exploitation de gestion.

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément. Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) et sera l’une des valeurs suivantes.

<dl> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)
</dt> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Activé mais hors connexion** (6)
</dt> </dl>

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

États activés et désactivés d’un élément. Cette propriété peut également indiquer les transitions entre ces États demandés. Cette propriété est héritée de la classe [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) et est définie sur 2 (activé) pour un ordinateur physique ou sur l’une des valeurs suivantes pour une machine virtuelle. Pour obtenir une vue graphique de ces États, consultez la section Notes.



| Valeur                                                                                                                                                                                                                                                                       | Signification                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Inconnu**</dt> <dt>0</dt> </dl>                                                 | Impossible de déterminer l’état de l’élément.<br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Autre**</dt> <dt>1</dt> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Activé**</dt> <dt>2</dt> </dl>                                                 | L’élément est en cours d’exécution.<br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Désactivé**</dt> <dt>3</dt> </dl>                                             | L’élément est désactivé.<br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <dt>**Arrêt**</dt> de <dt>4</dt> </dl>                         | L’élément est en cours de passage à un état désactivé.<br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**Non applicable**</dt> <dt>5</dt> </dl>                     | L’élément ne prend pas en charge l’activation ou la désactivation.<br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <dt>**Activé mais hors connexion**</dt> <dt>6</dt> </dl> | L’élément peut exécuter des commandes et supprimer toutes les nouvelles demandes.<br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <dt>**Dans le test**</dt> <dt>7</dt> </dl>                                                 | L’élément est dans un état de test.<br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <dt>**Différé**</dt> <dt>8</dt> </dl>                                             | L’élément peut exécuter des commandes, mais il met en file d’attente toutes les nouvelles demandes.<br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <dt>**Suspension**</dt> <dt>9</dt> </dl>                                                 | L’élément est activé, mais en mode restreint. Le comportement de l’élément est similaire à l’état activé (2), mais ne traite qu’un ensemble restreint de commandes. Toutes les autres demandes sont mises en file d’attente.<br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> À <dt>**partir**</dt> de <dt>10</dt> </dl>                                            | L’élément est en train d’accéder à un état activé (2). Les nouvelles demandes sont mises en file d’attente.<br/>                                                                                                             |



 

</dd> <dt>

**EnhancedSessionModeState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie l’état actuel du mode de session étendu sur l’ordinateur virtuel.

Le fournisseur WMI Hyper-V déclenche un [**\_ \_ InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) chaque fois que le **EnhancedSessionModeState** de la classe **MSVM \_ ComputerSystem** change. Si une session vmconnection active reçoit un **\_ \_ InstanceModificationEvent**, elle tente de basculer en mode de session étendu si l’utilisateur a activé ce paramètre.

**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.

**EnhancedSessionModeState** peut prendre l’une des valeurs suivantes :

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>**Autorisé et disponible** (2)


</dt> <dd>

Le mode étendu est autorisé et disponible sur l’ordinateur virtuel.

</dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Non autorisé** (3)


</dt> <dd>

Le mode étendu n’est pas autorisé sur la machine virtuelle.

</dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>**Autorisé mais non disponible** (6)


</dt> <dd>

Le mode étendu est autorisé et n’est pas disponible actuellement sur la machine virtuelle.

</dd> </dl>

</dd> <dt>

**FailedOverReplicationType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**FailedOverReplicationType**")
</dt> </dl>

Type de point de données de récupération appliqué pendant l’opération de basculement.

> [!Note]  
> Cette propriété est déconseillée à partir de Windows 8.1 ; Utilisez plutôt la propriété du même nom dans la classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) pour obtenir la valeur de la relation principale ou étendue.

 

Les valeurs possibles sont les suivantes :

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Aucun** (0)


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

**Normal** (1)


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

**Cohérence des applications** (2)


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

**Planifiée** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie l’intégrité actuelle de l’élément. Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.

Lorsqu’une erreur critique se produit, consultez le journal des événements pour plus d’informations. La propriété **EnabledState** peut également contenir plus d’informations. Par exemple, lorsque l’espace disque est très faible, **HealthState** est défini sur 25, l’ordinateur virtuel s’interrompt et **EnabledState** a la valeur 32768 (suspendu).

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).



| Valeur                                                                                                                                                                                                                                                            | Signification                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**OK**</dt> <dt>5</dt> </dl>                                                                               | L’ordinateur virtuel est entièrement fonctionnel et fonctionne dans des paramètres opérationnels normaux et sans erreur.<br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <dt>**Erreur majeure**</dt> <dt>20</dt> </dl>             | L’ordinateur virtuel a subi un échec majeur. Cette valeur est utilisée lorsqu’un ou plusieurs disques contenant les disques durs virtuels de l’ordinateur virtuel manquent d’espace disque et que l’ordinateur virtuel a été suspendu.<br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <dt>**Erreur critique**</dt> <dt>25</dt> </dl> | L’élément n’est pas fonctionnel et la récupération n’est peut-être pas possible. Cela peut indiquer que le processus de travail de l’ordinateur virtuel (Vmwp.exe) ne répond pas aux demandes de contrôle ou d’informations, ou qu’un ou plusieurs disques contenant les disques durs virtuels de l’ordinateur virtuel manquent d’espace disque.<br/> |



 

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Cette propriété est héritée de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)et est toujours définie sur **null**.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date et heure de création de la configuration d’ordinateur virtuel pour un ordinateur virtuel, ou **valeur null**, pour un système d’exploitation de gestion. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Identifie de façon unique une instance de cette classe. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

Dans Windows 8, il existe une seule instance de [**ReplicationSettingData**](msvm-replicationsettingdata.md) pour chaque système informatique ou ordinateur virtuel. Par Windows 8.1, une machine virtuelle de récupération a deux instances de **ReplicationSettingData**. Ce changement différencie et associe les données de paramètres à la relation de réplication.



| Nom de la propriété  | Valeur Windows 8               | Valeur Windows 8.1                          |
|----------------|-------------------------------|--------------------------------------------|
| **InstanceID** | Microsoft : <vmguid> \\ HVR | Microsoft : <vmguid> \\ HVR \\<0/1> |



 

Dans la valeur Windows 8.1, 0 indique primaire et 1 indique la réplication étendue. Pour plus d’informations sur la réplication étendue, consultez [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).

</dd> <dt>

**LastApplicationConsistentReplicationTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastApplicationConsistentReplicationTime**")
</dt> </dl>

Heure à laquelle la dernière réplication de cohérence des applications a été reçue pour l’ordinateur virtuel.

> [!Note]  
> Cette propriété est déconseillée à partir de Windows 8.1 ; Utilisez plutôt la propriété du même nom dans la classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) pour obtenir la valeur de la relation principale ou étendue.

 

</dd> <dt>

**LastReplicationTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationTime**")
</dt> </dl>

Heure à laquelle la dernière réplication est reçue lors de la récupération de la machine virtuelle.

> [!Note]  
> Cette propriété est déconseillée à partir de Windows 8.1 ; Utilisez plutôt la propriété du même nom dans la classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) pour obtenir la valeur de la relation principale ou étendue.

 

</dd> <dt>

**LastReplicationType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationType**")
</dt> </dl>

Type de la dernière réplication qui a été reçue pour l’ordinateur virtuel.

> [!Note]  
> Cette propriété est déconseillée à partir de Windows 8.1 ; Utilisez plutôt la propriété du même nom dans la classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) pour obtenir la valeur de la relation principale ou étendue.

 

Les valeurs possibles sont les suivantes :

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Aucun** (0)


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

**Normal** (1)


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

**Cohérence des applications** (2)


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

**Planifiée** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**LastSuccessfulBackupTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Heure à laquelle la dernière sauvegarde réussie est terminée pour la machine virtuelle.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Étiquette par laquelle l’objet est connu. Cette propriété est héritée [**du \_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system)et est toujours définie sur «*GUID*».

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne qui identifie la façon dont le nom système a été généré, à l’aide de la méthode heuristique de sous-classe. Cette propriété est héritée de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)et est toujours définie sur **null**.

</dd> <dt>

**Nœuds NUMA**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de nœuds NUMA (ununiform Memory Access) du système informatique. Quand **MSVM \_ ComputerSystem** représente le système informatique d’hébergement, cette propriété contient le nombre de nœuds NUMA physiques. Quand **MSVM \_ ComputerSystem** représente un ordinateur virtuel, cette propriété contient le nombre de nœuds NUMA virtuels qui sont présentés au système d’exploitation invité par le biais de la table d’affinité des ressources système (SRAT) ACPI.

</dd> <dt>

**OnTimeInMilliseconds**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« millisecondes »)
</dt> </dl>

Pour la machine virtuelle, cette propriété indique la durée, en millisecondes, depuis la dernière activation, réinitialisation ou restauration de l’ordinateur. Cette fois, vous excluez l’heure à laquelle la machine virtuelle était à l’état suspendu. Pour le système d’exploitation de gestion, cette propriété a la valeur **null**.

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** . Une valeur **null** indique que cette propriété n’est pas implémentée. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau qui contient les États actuels de l’objet. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement). La valeur à l’index zéro (0) est l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                   | Signification                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**OK**</dt> <dt>2</dt> </dl>                                                                                      | L’ordinateur virtuel est fonctionnel et fonctionne normalement.<br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <dt>**Dégradé**</dt> <dt>3</dt> </dl>                                         | L’ordinateur virtuel ne fonctionne que partiellement. Cela indique que le stockage qui contient la configuration n’est pas accessible. Une machine virtuelle dans cet État peut uniquement être désactivée ou supprimée. <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <dt>**Échec prédictif**</dt> <dt>5</dt> </dl> | L’ordinateur virtuel est fonctionnel mais peut échouer à l’avenir. Cela indique que l’espace libre est insuffisant sur le stockage qui contient le disque dur virtuel de l’ordinateur virtuel. L’ordinateur virtuel sera mis en pause si l’espace disque disponible est insuffisant.<br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <dt></dt> <dt>10</dt> arrêtés </dl>                                            | Cette valeur n’est pas prise en charge. Si la machine virtuelle est arrêtée, la propriété **EnabledState** aura la valeur 3 (désactivé).<br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <dt>**Dans le service**</dt> <dt>11</dt> </dl>                                | L’ordinateur virtuel est en cours de traitement d’une demande.<br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <dt>**Dormant**</dt> <dt>15</dt> </dl>                                            | Cette valeur n’est pas prise en charge. Si la machine virtuelle est interrompue ou suspendue, la propriété **EnabledState** aura la valeur 32769 (suspendu) ou 32768 (suspendu).<br/>                                                                                    |



 

La valeur à l’index 1 (1) est facultative et contient des informations d’état secondaire. Un client doit utiliser l’état principal de l’index zéro (0) pour déterminer si une nouvelle demande peut être émise pour l’ordinateur virtuel. Si **OperationalStatus** \[ 0 \] est égal à 2 (OK), l’opération indiquée par **OperationalStatus** \[ 1 \] peut être interrompue.

La valeur à **OperationalStatus** \[ 1 \] est l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                                                   | Signification                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <dt>**Création de l’instantané**</dt> <dt>32768</dt> </dl>                                 | Un instantané est en cours de création pour l’ordinateur virtuel.<br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> <dt>**Application de l’instantané**</dt> <dt>32769</dt> </dl>                                 | Un instantané est en cours d’application sur la machine virtuelle.<br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <dt>**Suppression de l’instantané**</dt> <dt>32770</dt> </dl>                                 | Un instantané est en cours de suppression de l’ordinateur virtuel.<br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <dt>**En attente de démarrage de**</dt> <dt>32771</dt> </dl>                                     | L’ordinateur virtuel démarre une fois que le délai de démarrage automatique s’est écoulé.<br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <dt>**Fusion des disques**</dt> <dt>32772</dt> </dl>                                                 | Les disques durs virtuels des instantanés précédemment supprimés sont en cours de fusion.<br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <dt>**Exportation de l’ordinateur virtuel**</dt> <dt>32773</dt> </dl> | L’ordinateur virtuel est en cours d’exportation.<br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> <dt>**Migration de la machine virtuelle**</dt> <dt>32774</dt> </dl> | L’ordinateur virtuel est en cours de migration dynamique d’un ordinateur physique vers un autre.<br/>  |



 

</dd> <dt>

**OtherDedicatedDescriptions**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne qui décrit comment ou pourquoi le système est dédié lorsque le tableau **dédié** comprend la valeur 2 (autre). Cette propriété est héritée de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)et est toujours définie sur **null**.

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

État activé ou désactivé de l’ordinateur virtuel lorsque la propriété **EnabledState** a la valeur 1 (autre). Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1. Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Cette propriété est héritée de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)et est toujours définie sur **null**.

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Cette propriété est héritée de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), mais elle n’est pas utilisée.

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne qui indique comment le propriétaire du système principal peut être atteint (par exemple, un numéro de téléphone ou une adresse de messagerie). Cette propriété est héritée [**du \_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system)et est toujours définie sur **null**.

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom du propriétaire du système principal. Cette propriété est héritée [**du \_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system)et est toujours définie sur **null**.

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Fournit des informations d’état de haut niveau. Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir des informations d’état d’intégrité de haut niveau et détaillées pour l’élément et ses sous-composants. Une valeur **null** indique que cette propriété n’est pas implémentée. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**ProcessID**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur du processus sous lequel cet ordinateur virtuel est en cours d’exécution. Cette valeur peut être utilisée pour identifier de façon unique l’instance de Vmwp.exe sur le système qui exécute l’ordinateur virtuel.

</dd> <dt>

**ReplicationHealth**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationHealth**")
</dt> </dl>

Intégrité de la réplication pour la machine virtuelle.

> [!Note]  
> Cette propriété est déconseillée à partir de Windows 8.1 ; Utilisez plutôt la propriété du même nom dans la classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) pour obtenir la valeur de la relation principale ou étendue.

 

Les valeurs possibles sont les suivantes :

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Non applicable** (0)


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

**OK** (1)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Avertissement** (2)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Critique** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationMode**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie le mode de réplication pour la machine virtuelle. Il s’agit de l’une des valeurs suivantes.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Aucun** (0)


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Principal** (1)


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>**Réplica** (2)


</dt> <dd>

Récupération

</dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>**Réplica de test** (3)


</dt> <dd>

Réplica

</dd> <dt>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>**Réplica étendu** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationState**")
</dt> </dl>

État de réplication de la machine virtuelle.

> [!Note]  
> Cette propriété est déconseillée à partir de Windows 8.1 ; Utilisez plutôt la propriété du même nom dans la classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) pour obtenir la valeur de la relation principale ou étendue.

 

Les valeurs possibles sont les suivantes :

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Désactivé** (0)


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

**Prêt pour la réplication** (1)


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

**En attente de l’exécution de la réplication initiale** (2)


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

**Réplication** (3)


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

**Réplication synchronisée terminée** (4)


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

**Récupéré** (5)


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

**Validé** (6)


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

**Suspendu** (7)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Critique** (8)


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

**En attente de démarrage de la resynchronisation** (9)


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

**Resynchronisation** (10)


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

**Resynchronisation suspendue** (11)


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

**Basculement en cours** (12)


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

**Restauration automatique en cours** (13)


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

**Restauration automatique terminée** (14)


</dt> <dd></dd> </dl>

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Dernier État demandé ou souhaité pour l’ordinateur virtuel passé à la méthode [**RequestStateChange**](requeststatechange-msvm-computersystem.md) , ou 12 (non applicable) si aucun changement d’État n’est en cours. L’état réel de l’élément est représenté par **EnabledState**. Cette propriété est fournie pour comparer les derniers États activés et actuellement activés ou désactivés. Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**ResetCapability**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Cette propriété est héritée de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)et est toujours définie sur 1 (autre).

</dd> <dt>

**Rôles**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau de chaînes qui décrivent les rôles joués par le système dans l’environnement informatique. Cette propriété est héritée [**du \_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system)et est toujours définie sur **null**.

</dd> <dt>

**État**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **arrayType** ("indexé")
</dt> </dl>

Tableau qui contient des chaînes qui décrivent les valeurs de tableau **OperationalStatus** correspondantes. Par exemple, si 11 (en service) est la valeur affectée à **OperationalStatus** \[ 0 \] , **StatusDescriptions** \[ 0 \] peut contenir une explication sur la raison pour laquelle l’ordinateur virtuel traite une demande. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**TimeOfLastConfigurationChange**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date et heure de la dernière modification du fichier de configuration de l’ordinateur virtuel. Le fichier de configuration est modifié lors de certaines opérations d’ordinateur virtuel, ainsi que lors de l’ajout, de la modification ou de la suppression de l’un des paramètres de l’ordinateur virtuel ou de l’appareil.

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date et heure de la dernière modification de l’état activé de l’élément. Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique l’État cible de la transition de l’instance. Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Notes

L’illustration suivante montre les valeurs **EnabledState** .

![diagramme d’État pour les valeurs enabledState pour Windows Server 2008 R2](images/msvm-computersystem-enabledstate-win2008r2.png)

Quand une propriété de la classe **MSVM \_ ComputerSystem** change, le fournisseur WMI indique un événement [**\_ \_ InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) qui décrit les modifications. L’état précédent est contenu dans la propriété **PreviousInstance** , et le nouvel État est contenu dans la propriété **TargetInstance** . Cet événement est asynchrone ; au moment du traitement de l’événement **\_ \_ InstanceModificationEvent** , la propriété **TargetInstance** peut ne pas refléter l’état actuel.

L’accès à la classe **MSVM \_ ComputerSystem** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Exemples

Consultez [interrogation d’objets de mise en réseau](querying-networking-objects.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_ComputerSystem CIM**](cim-computersystem.md)
</dt> <dt>

[**\_\_InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent)
</dt> <dt>

[**\_ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem)
</dt> <dt>

[**MSVM \_ ComputerSystem (v1)**](/previous-versions/windows/desktop/virtual/msvm-computersystem)
</dt> <dt>

[Classes du système virtuel](virtual-system-classes.md)
</dt> </dl>

 

