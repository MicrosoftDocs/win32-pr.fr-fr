---
description: Représente un adaptateur Ethernet émulé.
ms.assetid: 8E990C76-7D48-42B0-BB4D-C4C07B1C482A
title: Msvm_EmulatedEthernetPort, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EmulatedEthernetPort
- Msvm_EmulatedEthernetPort.SetPowerState
- Msvm_EmulatedEthernetPort.EnableDevice
- Msvm_EmulatedEthernetPort.OnlineDevice
- Msvm_EmulatedEthernetPort.QuiesceDevice
- Msvm_EmulatedEthernetPort.SaveProperties
- Msvm_EmulatedEthernetPort.RestoreProperties
- Msvm_EmulatedEthernetPort.InstanceID
- Msvm_EmulatedEthernetPort.Caption
- Msvm_EmulatedEthernetPort.Description
- Msvm_EmulatedEthernetPort.ElementName
- Msvm_EmulatedEthernetPort.InstallDate
- Msvm_EmulatedEthernetPort.Name
- Msvm_EmulatedEthernetPort.OperationalStatus
- Msvm_EmulatedEthernetPort.StatusDescriptions
- Msvm_EmulatedEthernetPort.Status
- Msvm_EmulatedEthernetPort.HealthState
- Msvm_EmulatedEthernetPort.CommunicationStatus
- Msvm_EmulatedEthernetPort.DetailedStatus
- Msvm_EmulatedEthernetPort.OperatingStatus
- Msvm_EmulatedEthernetPort.PrimaryStatus
- Msvm_EmulatedEthernetPort.EnabledState
- Msvm_EmulatedEthernetPort.OtherEnabledState
- Msvm_EmulatedEthernetPort.RequestedState
- Msvm_EmulatedEthernetPort.EnabledDefault
- Msvm_EmulatedEthernetPort.TimeOfLastStateChange
- Msvm_EmulatedEthernetPort.AvailableRequestedStates
- Msvm_EmulatedEthernetPort.TransitioningToState
- Msvm_EmulatedEthernetPort.SystemCreationClassName
- Msvm_EmulatedEthernetPort.SystemName
- Msvm_EmulatedEthernetPort.CreationClassName
- Msvm_EmulatedEthernetPort.DeviceID
- Msvm_EmulatedEthernetPort.PowerManagementSupported
- Msvm_EmulatedEthernetPort.PowerManagementCapabilities
- Msvm_EmulatedEthernetPort.Availability
- Msvm_EmulatedEthernetPort.StatusInfo
- Msvm_EmulatedEthernetPort.LastErrorCode
- Msvm_EmulatedEthernetPort.ErrorDescription
- Msvm_EmulatedEthernetPort.ErrorCleared
- Msvm_EmulatedEthernetPort.OtherIdentifyingInfo
- Msvm_EmulatedEthernetPort.PowerOnHours
- Msvm_EmulatedEthernetPort.TotalPowerOnHours
- Msvm_EmulatedEthernetPort.IdentifyingDescriptions
- Msvm_EmulatedEthernetPort.AdditionalAvailability
- Msvm_EmulatedEthernetPort.MaxQuiesceTime
- Msvm_EmulatedEthernetPort.Speed
- Msvm_EmulatedEthernetPort.MaxSpeed
- Msvm_EmulatedEthernetPort.RequestedSpeed
- Msvm_EmulatedEthernetPort.UsageRestriction
- Msvm_EmulatedEthernetPort.PortType
- Msvm_EmulatedEthernetPort.OtherPortType
- Msvm_EmulatedEthernetPort.OtherNetworkPortType
- Msvm_EmulatedEthernetPort.PortNumber
- Msvm_EmulatedEthernetPort.LinkTechnology
- Msvm_EmulatedEthernetPort.OtherLinkTechnology
- Msvm_EmulatedEthernetPort.PermanentAddress
- Msvm_EmulatedEthernetPort.NetworkAddresses
- Msvm_EmulatedEthernetPort.FullDuplex
- Msvm_EmulatedEthernetPort.AutoSense
- Msvm_EmulatedEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_EmulatedEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_EmulatedEthernetPort.MaxDataSize
- Msvm_EmulatedEthernetPort.Capabilities
- Msvm_EmulatedEthernetPort.CapabilityDescriptions
- Msvm_EmulatedEthernetPort.EnabledCapabilities
- Msvm_EmulatedEthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1ec13ae369f6d5e3d884f74c96d7df27c2f5fa97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520458"
---
# <a name="msvm_emulatedethernetport-class"></a>MSVM \_ EmulatedEthernetPort, classe

Représente un adaptateur Ethernet émulé. Cet adaptateur est utilisé lorsqu’un ordinateur virtuel ne peut pas exécuter le port Ethernet synthétique quand aucun circuit intégré n’est installé dans l’invité.

> [!Note]  
> Cette classe n’est pas disponible pour les ordinateurs virtuels de génération 2.

 

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EmulatedEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Port";
  string   Description = "Microsoft Emulated Ethernet Port";
  string   ElementName = "Legacy Network Adapter";
  datetime InstallDate;
  string   Name = "Ethernet Port";
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_EmulatedEthernetPort";
  string   DeviceID = "Microsoft:GUID\device-specific data";
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint16   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  uint64   Speed = 1000000000;
  uint64   MaxSpeed = 1000000000;
  uint64   RequestedSpeed = 1000000000;
  uint16   UsageRestriction = 4;
  uint16   PortType = 1;
  string   OtherPortType = "Virtual Ethernet";
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology = 2;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  string   NetworkAddresses[];
  boolean  FullDuplex = True;
  boolean  AutoSense = True;
  string   SupportedMaximumTransmissionUnit = 1500;
  uint64   ActiveMaximumTransmissionUnit = 1500;
  uint32   MaxDataSize = 1500;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  uint16   EnabledCapabilities[];
  string   OtherEnabledCapabilities[];
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ EmulatedEthernetPort** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MSVM \_ EmulatedEthernetPort** possède ces méthodes.



| Méthode                                                                     | Description                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| **EnableDevice**                                                           | Cette méthode n'est pas prise en charge.<br/> |
| **OnlineDevice**                                                           | Cette méthode n'est pas prise en charge.<br/> |
| **QuiesceDevice**                                                          | Cette méthode n'est pas prise en charge.<br/> |
| [**RequestStateChange**](msvm-emulatedethernetport-requeststatechange.md) | Demande un changement d’État.<br/>      |
| [**Réinitialiser**](msvm-emulatedethernetport-reset.md)                           | Réinitialise l’appareil émulé.<br/>   |
| **RestoreProperties**                                                      | Cette méthode n'est pas prise en charge.<br/> |
| **SaveProperties**                                                         | Cette méthode n'est pas prise en charge.<br/> |
| **SetPowerState**                                                          | Cette méthode n'est pas prise en charge.<br/> |



 

### <a name="properties"></a>Propriétés

La classe **MSVM \_ EmulatedEthernetPort** possède les propriétés suivantes.

<dl> <dt>

**ActiveMaximumTransmissionUnit**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Unité de transmission maximale (MTU) active ou négociée qui peut être prise en charge. Cette propriété est héritée de [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)et est toujours définie sur 1500.

</dd> <dt>

**AdditionalAvailability**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Disponibilité et état supplémentaires de l’appareil, au-delà de celui spécifié dans la propriété **Availability** . Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur 6 (« non applicable »).

</dd> <dt>

**Détection automatique**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si le port réseau peut déterminer automatiquement la vitesse ou d’autres caractéristiques de communication du support réseau attaché. Cette propriété est héritée de [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)et est toujours définie sur **true**.

</dd> <dt>

**Disponibilité**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Disponibilité et état principaux de l’appareil. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur **null**.

</dd> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) utilisée pour initier un changement d’État. Les valeurs répertoriées sont un sous-ensemble des valeurs contenues dans la propriété **RequestedStatesSupported** de l’instance associée de la **\_ EnabledLogicalElementCapabilities CIM**, où les valeurs sélectionnées sont une fonction de l’état actuel du [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)). Cette propriété peut être non **null** si une implémentation est en mesure de publier l’ensemble de valeurs possibles en tant que fonction de l’état actuel. Cette propriété a la **valeur null** si une implémentation ne peut pas déterminer le jeu de valeurs possibles en tant que fonction de l’état actuel.

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

**Capabilities**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Fonctionnalités du port Ethernet. Cette propriété est héritée de [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) et n’est pas utilisée.

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau de chaînes de forme libre qui fournit des explications plus détaillées sur les fonctionnalités de port Ethernet indiquées dans le tableau de **fonctionnalités** . Notez que chaque entrée de ce tableau est liée à l’entrée dans le tableau de **fonctionnalités** qui se trouve dans le même index. Cette propriété est héritée de [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) et n’est pas utilisée.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Brève description de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « port Ethernet ».

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

Nom de la classe ou de la sous-classe utilisée lors de la création d’une instance. Quand elle est utilisée avec les autres propriétés de clé de cette classe, cette propriété autorise l’identification unique de toutes les instances de cette classe et de ses sous-classes. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur « MSVM \_ EmulatedEthernetPort ».

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « port Ethernet émulé Microsoft ».

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires. Une valeur **null** indique que cette propriété n’est pas implémentée. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Une adresse ou d’autres informations d’identification utilisées pour nommer de façon unique l’unité logique. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur « Microsoft :*GUID* \\ *Device-Specific Data*».

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « carte réseau héritée ».

</dd> <dt>

**EnabledCapabilities**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Les fonctionnalités qui sont activées dans la liste de tous les éléments pris en charge, qui sont définis dans le tableau de **fonctionnalités** . Cette propriété est héritée de [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), mais elle n’est pas utilisée.

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément. Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) et est toujours définie sur 2 (« activé »).

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

États activés et désactivés d’un élément. Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 5 (« non applicable »).

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si l’erreur signalée dans **LastErrorCode** est maintenant désactivée. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne qui fournit des informations supplémentaires sur l’erreur enregistrée dans **LastErrorCode**, ainsi que des informations sur toutes les actions correctives qui peuvent être effectuées. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.

</dd> <dt>

**FullDuplex**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si le port fonctionne en mode duplex intégral. Cette propriété est héritée de [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)et est toujours définie sur **true**.

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Intégrité actuelle de l’élément. Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5 (« OK »).

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau **OtherIdentifyingInfo** . Chaque entrée de ce tableau est liée à l’entrée dans **OtherIdentifyingInfo** qui se trouve dans le même index. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Valeur **DateTime** qui indique le moment où l’objet a été installé. L’absence de valeur n’indique pas que l’objet n’est pas installé. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

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

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Dernier code d’erreur signalé par l’unité logique. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.

</dd> <dt>

**LinkTechnology**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Types de liens. Si la valeur 1 (« other ») est définie, la propriété associée **OtherLinkTechnology** contient une description de chaîne du type de lien. Cette propriété est héritée de [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) et a toujours la valeur 2 (« Ethernet »).

</dd> <dt>

**MaxDataSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Taille maximale du champ INFO (non-MAC) qui sera reçu ou transmis. Cette propriété est héritée de [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)et est toujours définie sur 1500.

</dd> <dt>

**MaxQuiesceTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.

</dd> <dt>

**MaxSpeed**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Bande passante maximale du port, en bits par seconde. Cette propriété est héritée de [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))et est toujours définie sur 1 milliard.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Étiquette par laquelle l’objet est connu. Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur « port Ethernet ».

</dd> <dt>

**NetworkAddresses**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Les adresses MAC Ethernet/802.3, au format 12 chiffres hexadécimaux (par exemple, « 010203040506 »), chaque paire représentant l’un des six octets de l’adresse MAC dans l’ordre des bits canoniques (le bit d’adresse de groupe se trouve dans le bit de poids faible du premier caractère de la chaîne). Cette propriété est héritée de [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) et n’est pas utilisée.

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

États actuels de l’élément. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 2 (« OK »).

</dd> <dt>

**OtherEnabledCapabilities**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau de chaînes de forme libre qui fournit des explications plus détaillées sur les fonctionnalités activées spécifiées comme « other ». Cette propriété est héritée de [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) et n’est pas utilisée.

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (« other »). Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1. Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) et n’est pas utilisée.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Toutes les données, en plus des informations d’ID de l’appareil, qui peuvent être utilisées pour identifier un périphérique logique. Par exemple, vous pouvez utiliser cette propriété pour stocker le nom complet du système d’exploitation de l’appareil. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.

</dd> <dt>

**OtherLinkTechnology**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Valeur de chaîne qui décrit **LinkTechnology** lorsqu’il a la valeur 1 (« other »). Cette propriété est héritée de [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), mais elle n’est pas utilisée.

</dd> <dt>

**OtherNetworkPortType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Cette propriété est héritée de [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) et a la valeur **null**.

</dd> <dt>

**OtherPortType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type de module, lorsque **portType** a la valeur 1 (« other »). Cette propriété est héritée de [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)) et est toujours définie sur « Ethernet virtuel ».

</dd> <dt>

**PermanentAddress**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Adresse réseau qui est codée en dur dans un port. Cette adresse peut être modifiée à l’aide d’une mise à niveau du microprogramme ou d’une configuration logicielle. Lorsque cette modification est apportée, le champ doit être mis à jour en même temps. Elle doit être laissée vide si aucune adresse codée en dur n’existe pour la carte réseau. Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**Numéroport**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Les ports réseau sont souvent numérotés par rapport à un module logique ou à un élément réseau. Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).



| Valeur                                                                        | Signification                             |
|------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>0</dt> </dl> | La carte d’interface réseau n’est pas émulée.<br/> |
| <dl> <dt>1</dt> </dl> | La carte d’interface réseau est émulée.<br/>     |



 

</dd> <dt>

**PortType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Mode spécifique actuellement activé pour le port. Si la valeur 1 (« other ») est définie, la propriété associée **OtherPortType** contient une description de chaîne du type de port. Cette propriété est héritée de [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)et est toujours définie sur 1 (« other »).

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Les fonctionnalités de gestion de l’alimentation de l’appareil. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si l’appareil peut être géré par l’alimentation. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.

</dd> <dt>

**PowerOnHours**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre d’heures consécutives pendant lesquelles ce périphérique a été alimenté depuis son dernier cycle d’alimentation. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Fournit des informations d’état de haut niveau. Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir des informations d’état d’intégrité de haut niveau et détaillées pour l’élément et ses sous-composants. Une valeur **null** indique que cette propriété n’est pas implémentée. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**RequestedSpeed**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Bande passante demandée du port, en bits par seconde. La bande passante réelle est indiquée dans LogicalPort. Speed. Cette propriété est héritée de [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))et est toujours définie sur 1 milliard.

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Dernier État demandé ou souhaité pour le service de gestion. Quand **EnabledState** a la valeur 5 (« non applicable »), cette propriété n’a aucune signification. Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 12 (« non applicable »).

</dd> <dt>

**Vitesse**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Bande passante actuelle du port, en bits par seconde. Pour les ports qui varient en bande passante ou pour ceux pour lesquels aucune estimation précise ne peut être effectuée, cette propriété doit contenir la bande passante nominale. Cette propriété est héritée de [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)et est toujours définie sur 1 milliard.

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
</dt> </dl>

Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** . Les entrées de ce tableau sont corrélées avec celles situées au même index de tableau dans **OperationalStatus**. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur « OK ».

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

État de l’unité logique. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.

</dd> <dt>

**SupportedMaximumTransmissionUnit**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **Units** ("bytes")
</dt> </dl>

Unité de transmission maximale (MTU) qui peut être prise en charge, en octets. Cette propriété est héritée de [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)et est toujours définie sur 1500.

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de la classe de création du système d’étendue. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur « MSVM \_ ComputerSystem ».

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

ID de machine virtuelle sous forme de **GUID** . Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date ou heure de la dernière modification de l' **EnabledState** de l’élément. Si l’état de l’élément n’a pas été modifié et que cette propriété est remplie, elle doit être définie sur une valeur d’intervalle 0. Si une modification d’État a été demandée, mais rejetée ou n’a pas encore été traitée, la propriété ne doit pas être mise à jour. Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) et n’est pas utilisée.

</dd> <dt>

**TotalPowerOnHours**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre total d’heures d’alimentation de cet appareil. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique l’État cible de la transition de l’instance. Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.

</dd> <dt>

**UsageRestriction**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Dans certains cas, un port logique peut être identifiable comme un port frontal ou back end. S’il n’existe aucune restriction sur l’utilisation du port, la valeur doit être définie sur 4 (« non restreint »). Cette propriété est héritée de [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)) et a toujours la valeur 4 (« non restreint »).

</dd> </dl>

## <a name="remarks"></a>Notes

L’accès à la classe **MSVM \_ EmulatedEthernetPort** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_ETHERNETPORT CIM**](cim-ethernetport.md)
</dt> <dt>

[**\_ETHERNETPORT CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

