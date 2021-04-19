---
description: Représente la configuration actuelle d’un commutateur Ethernet virtuel.
ms.assetid: a7c03517-332d-47ce-8e04-c2187bcb2977
title: Classe Msvm_VirtualEthernetSwitchSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchSettingData
- Msvm_VirtualEthernetSwitchSettingData.InstanceID
- Msvm_VirtualEthernetSwitchSettingData.Caption
- Msvm_VirtualEthernetSwitchSettingData.Description
- Msvm_VirtualEthernetSwitchSettingData.ElementName
- Msvm_VirtualEthernetSwitchSettingData.VirtualSystemIdentifier
- Msvm_VirtualEthernetSwitchSettingData.VirtualSystemType
- Msvm_VirtualEthernetSwitchSettingData.Notes
- Msvm_VirtualEthernetSwitchSettingData.CreationTime
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationID
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationDataRoot
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationFile
- Msvm_VirtualEthernetSwitchSettingData.SnapshotDataRoot
- Msvm_VirtualEthernetSwitchSettingData.SuspendDataRoot
- Msvm_VirtualEthernetSwitchSettingData.SwapFileDataRoot
- Msvm_VirtualEthernetSwitchSettingData.LogDataRoot
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupAction
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupActionDelay
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualEthernetSwitchSettingData.AutomaticShutdownAction
- Msvm_VirtualEthernetSwitchSettingData.AutomaticRecoveryAction
- Msvm_VirtualEthernetSwitchSettingData.RecoveryFile
- Msvm_VirtualEthernetSwitchSettingData.VLANConnection
- Msvm_VirtualEthernetSwitchSettingData.AssociatedResourcePool
- Msvm_VirtualEthernetSwitchSettingData.MaxNumMACAddress
- Msvm_VirtualEthernetSwitchSettingData.IOVPreferred
- Msvm_VirtualEthernetSwitchSettingData.ExtensionOrder
- Msvm_VirtualEthernetSwitchSettingData.BandwidthReservationMode
- Msvm_VirtualEthernetSwitchSettingData.TeamingEnabled
- Msvm_VirtualEthernetSwitchSettingData.PacketDirectEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3eccbd9dabe853f01c54c78ca651d590afc49f17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544255"
---
# <a name="msvm_virtualethernetswitchsettingdata-class"></a>MSVM \_ VirtualEthernetSwitchSettingData, classe

Représente la configuration actuelle d’un commutateur Ethernet virtuel.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchSettingData : CIM_VirtualEthernetSwitchSettingData
{
  string   InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string   Caption = "Virtual Ethernet Switch Settings";
  string   Description = "Active settings for the virtual Ethernet switch";
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
  string   VLANConnection[];
  string   AssociatedResourcePool[];
  uint32   MaxNumMACAddress;
  boolean  IOVPreferred = FALSE;
  string   ExtensionOrder[];
  uint32   BandwidthReservationMode = 0;
  boolean  TeamingEnabled = FALSE;
  boolean  PacketDirectEnabled = FALSE;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ VirtualEthernetSwitchSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ VirtualEthernetSwitchSettingData** possède les propriétés suivantes.

<dl> <dt>

**AssociatedResourcePool**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Liste des pools de ressources hôtes à associer ou actuellement associés au commutateur Ethernet dans le but d’allouer des connexions Ethernet entre un ordinateur virtuel et un commutateur Ethernet. Chaque valeur doit être conforme à l’URI WBEM de production \_ \_ UntypedInstancePath tel que défini dans DSP0207. Cette propriété est héritée de la **\_ VirtualEthernetSwitchSettingData CIM**.

</dd> <dt>

**AutomaticRecoveryAction**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Action à entreprendre pour l’ordinateur virtuel lors de l’échec du logiciel exécuté par l’ordinateur virtuel. Dans ce cas, les échecs signifient qu’il s’agit d’une défaillance pouvant être détectée par la plateforme hôte, telle qu’une condition d’état d’attente non interruptible. Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))et n’est pas utilisée.

</dd> <dt>

**AutomaticShutdownAction**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Action à entreprendre pour l’ordinateur virtuel lorsque l’ordinateur hôte est arrêté. Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))et n’est pas utilisée.

</dd> <dt>

**AutomaticStartupAction**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Action à effectuer pour l’ordinateur virtuel au démarrage de l’ordinateur hôte. Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))et n’est pas utilisée.

</dd> <dt>

**AutomaticStartupActionDelay**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Délai avant le démarrage automatique de l’ordinateur virtuel. Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))et n’est pas utilisée.

</dd> <dt>

**AutomaticStartupActionSequenceNumber**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre qui indique la séquence relative d’activation d’ordinateur virtuel lors du démarrage du système hôte. Un nombre inférieur indique une activation antérieure. Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))et n’est pas utilisée.

</dd> <dt>

**BandwidthReservationMode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Mode de réservation de bande passante.

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**Valeur par défaut** (0)


</dt> <dd></dd> <dt>

<span id="Weight"></span><span id="weight"></span><span id="WEIGHT"></span>

**Poids** (1)


</dt> <dd></dd> <dt>

<span id="Absolute"></span><span id="absolute"></span><span id="ABSOLUTE"></span>

**Absolu** (2)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Aucun** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Brève description de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « paramètres du commutateur Ethernet virtuel ».

</dd> <dt>

**ConfigurationDataRoot**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès d’un répertoire où sont stockées les informations relatives à la configuration de l’ordinateur virtuel. Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))et n’est pas utilisée.

</dd> <dt>

**Fichier ConfigurationFile**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès relatif et nom de fichier d’un fichier dans lequel sont stockées les informations relatives à la configuration de l’ordinateur virtuel. Ce chemin d’accès est relatif à la propriété **ConfigurationDataRoot** . Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))et n’est pas utilisée.

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur unique de la configuration de l’ordinateur virtuel. Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))et n’est pas utilisée.

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date et heure de création des paramètres. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « paramètres actifs pour le commutateur Ethernet virtuel ».

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’objet. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**ExtensionOrder**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Tableau d’instances incorporées de la classe [**MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md) qui représentent les extensions de commutateur liées à ce commutateur, dans l’ordre dans lequel elles sont appliquées.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Identifie de façon unique une instance de cette classe. Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)) et est toujours définie sur « Microsoft :*GUID* \\ *DeviceSpecificData*».

</dd> <dt>

**IOVPreferred**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie si la virtualisation d’e/s de racine unique (SR-IOV) est préférée ou non, si elle est disponible, sur la carte sous-jacente.

</dd> <dt>

**LogDataRoot**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès d’un répertoire dans lequel sont stockées les informations de journalisation de l’ordinateur virtuel. Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))et n’est pas utilisée.

</dd> <dt>

**MaxNumMACAddress**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie le nombre maximal d’adresses MAC uniques qui peuvent être appris par le commutateur pour prendre en charge l’apprentissage des adresses MAC, comme défini dans la norme IEEE 802,1. Cette propriété est héritée de la **\_ VirtualEthernetSwitchSettingData CIM**.

</dd> <dt>

**Remarques**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Les notes fournies par l’utilisateur sont liées à la machine virtuelle. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**PacketDirectEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie si le PacketDirect doit être utilisé, le cas échéant. La valeur par défaut est **false**.

> [!Note]  
> Cette propriété a été ajoutée dans Windows 10 et Windows Server 2016.

 

</dd> <dt>

**RecoveryFile**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès complet d’un fichier dans lequel sont stockées les informations relatives à la récupération de l’ordinateur virtuel. Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))et n’est pas utilisée.

</dd> <dt>

**SnapshotDataRoot**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès d’un répertoire où sont stockées les informations sur les captures instantanées d’ordinateur virtuel. Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))et n’est pas utilisée.

</dd> <dt>

**SuspendDataRoot**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès d’un répertoire où sont stockées les informations relatives aux informations relatives à la suspension de l’ordinateur virtuel. Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))et n’est pas utilisée.

</dd> <dt>

**SwapFileDataRoot**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès d’un répertoire où sont stockés les fichiers d’échange de l’ordinateur virtuel. Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))et n’est pas utilisée.

</dd> <dt>

**TeamingEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie si l’Association de cartes réseau doit être utilisée. La valeur par défaut est **false**.

> [!Note]  
> Cette propriété a été ajoutée à Windows 10 et Windows Server 2016.

 

</dd> <dt>

**Attribut virtualsystemidentifier**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de l’objet [**CIM \_ CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) auquel appartiennent les données de ce paramètre. Cette propriété est une substitution de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**VirtualSystemType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie le type de machine virtuelle que les données de paramètre représentent. Cette propriété est héritée de [**la \_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**VLANConnection**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Liste d’identificateurs de réseau local virtuel auxquels ce commutateur peut accéder. Cette propriété est héritée de la **\_ VirtualEthernetSwitchSettingData CIM**.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

