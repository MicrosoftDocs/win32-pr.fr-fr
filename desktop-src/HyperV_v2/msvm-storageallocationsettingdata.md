---
description: Représente des paramètres spécifiquement liés à l’allocation de stockage virtuel.
ms.assetid: de6787c0-9998-4f1d-9715-f0dfa0ff70c6
title: Classe Msvm_StorageAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageAllocationSettingData
- Msvm_StorageAllocationSettingData.InstanceID
- Msvm_StorageAllocationSettingData.Caption
- Msvm_StorageAllocationSettingData.Description
- Msvm_StorageAllocationSettingData.ElementName
- Msvm_StorageAllocationSettingData.ResourceType
- Msvm_StorageAllocationSettingData.OtherResourceType
- Msvm_StorageAllocationSettingData.ResourceSubType
- Msvm_StorageAllocationSettingData.PoolID
- Msvm_StorageAllocationSettingData.ConsumerVisibility
- Msvm_StorageAllocationSettingData.HostResource
- Msvm_StorageAllocationSettingData.AllocationUnits
- Msvm_StorageAllocationSettingData.VirtualQuantity
- Msvm_StorageAllocationSettingData.Limit
- Msvm_StorageAllocationSettingData.Weight
- Msvm_StorageAllocationSettingData.StorageQoSPolicyID
- Msvm_StorageAllocationSettingData.AutomaticAllocation
- Msvm_StorageAllocationSettingData.AutomaticDeallocation
- Msvm_StorageAllocationSettingData.Parent
- Msvm_StorageAllocationSettingData.Connection
- Msvm_StorageAllocationSettingData.Address
- Msvm_StorageAllocationSettingData.MappingBehavior
- Msvm_StorageAllocationSettingData.AddressOnParent
- Msvm_StorageAllocationSettingData.VirtualResourceBlockSize
- Msvm_StorageAllocationSettingData.VirtualQuantityUnits
- Msvm_StorageAllocationSettingData.Access
- Msvm_StorageAllocationSettingData.HostResourceBlockSize
- Msvm_StorageAllocationSettingData.Reservation
- Msvm_StorageAllocationSettingData.HostExtentStartingAddress
- Msvm_StorageAllocationSettingData.HostExtentName
- Msvm_StorageAllocationSettingData.HostExtentNameFormat
- Msvm_StorageAllocationSettingData.OtherHostExtentNameFormat
- Msvm_StorageAllocationSettingData.HostExtentNameNamespace
- Msvm_StorageAllocationSettingData.OtherHostExtentNameNamespace
- Msvm_StorageAllocationSettingData.IOPSLimit
- Msvm_StorageAllocationSettingData.IOPSReservation
- Msvm_StorageAllocationSettingData.IOPSAllocationUnits
- Msvm_StorageAllocationSettingData.PersistentReservationsSupported
- Msvm_StorageAllocationSettingData.CachingMode
- Msvm_StorageAllocationSettingData.SnapshotId
- Msvm_StorageAllocationSettingData.IgnoreFlushes
- Msvm_StorageAllocationSettingData.WriteHardeningMethod
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9ba95ef5f4eb0afd20b80ab97db1ab7fc9a37b11e45638188c31459f8003cbda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950218"
---
# <a name="msvm_storageallocationsettingdata-class"></a>MSVM \_ StorageAllocationSettingData, classe

Représente des paramètres spécifiquement liés à l’allocation de stockage virtuel.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageAllocationSettingData : CIM_StorageAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Hard Disk Image Default Settings";
  string  Description = "Describes the default settings for the hard disk image resources";
  string  ElementName;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Limit = 1;
  uint32  Weight;
  string  StorageQoSPolicyID;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  uint64  VirtualResourceBlockSize;
  string  VirtualQuantityUnits = "count(fixed size block)";
  uint16  Access;
  uint64  HostResourceBlockSize;
  uint64  Reservation;
  uint64  HostExtentStartingAddress;
  string  HostExtentName;
  uint16  HostExtentNameFormat;
  string  OtherHostExtentNameFormat;
  uint16  HostExtentNameNamespace;
  string  OtherHostExtentNameNamespace;
  uint64  IOPSLimit;
  uint64  IOPSReservation;
  string  IOPSAllocationUnits;
  boolean PersistentReservationsSupported;
  uint16  CachingMode;
  string  SnapshotId = "";
  boolean IgnoreFlushes;
  uint16  WriteHardeningMethod;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ StorageAllocationSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ StorageAllocationSettingData** possède les propriétés suivantes.

<dl> <dt>

**y accéder**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie l’accès au stockage. Cette propriété est héritée de la **\_ StorageAllocationSettingData CIM**.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)
</dt> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Lecture** (1)
</dt> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Accessible en écriture** (2)
</dt> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Lecture/écriture prise en charge** (3)
</dt> </dl>

</dd> <dt>

**Adresse**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Adresse de la ressource. Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**AddressOnParent**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Décrit l’adresse de cette ressource dans le contexte du parent. Les propriétés **parent** et **AddressOnParent** sont utilisées pour décrire la relation du contrôleur, ainsi que l’ordre des appareils sur un contrôleur. Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**AllocationUnits**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Unités d’allocation utilisées par la **réservation** et les propriétés de la **limite** . Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**AutomaticAllocation**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la ressource sera automatiquement allouée. Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**AutomaticDeallocation**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la ressource sera automatiquement désallouée. Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**CachingMode**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si et comment la mise en cache des fichiers en mémoire doit être utilisée pour ce disque dur virtuel. La stratégie par défaut est définie dans le champ **DefaultVirtualHardDiskCachingMode** de la classe [**MSVM \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) .

> [!Note]  
> Ajouté dans Windows 10.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**Par défaut** (2)


</dt> <dd></dd> <dt>

<span id="No_Caching"></span><span id="no_caching"></span><span id="NO_CACHING"></span>

**Aucune mise en cache** (3)


</dt> <dd></dd> <dt>

<span id="Cache_Sharable_Parents"></span><span id="cache_sharable_parents"></span><span id="CACHE_SHARABLE_PARENTS"></span>

Mettre **en cache les parents partageables** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **MaxLen** (64)
</dt> </dl>

Brève description de l’objet. cette propriété est héritée de la [**\_ propriété managedelement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « Image de disque dur par défaut Paramètres ».

</dd> <dt>

**Connection**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Appareil auquel cette ressource est connectée. Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**ConsumerVisibility**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Visibilité du consommateur sur la ressource allouée. Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)
</dt> <dt>

<span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span>**Passe-à-** (2)
</dt> <dt>

<span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span>**Virtualisé** (3)
</dt> <dt>

<span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span>**Non représenté** (4)
</dt> </dl>

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et elle est toujours définie sur « décrit les paramètres par défaut pour les ressources de l’image de disque dur ».

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’objet. Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**HostExtentName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur unique pour l’étendue de l’hôte. L’étendue de l’hôte identifiée est utilisée pour l’allocation des ressources de stockage. Cette propriété est héritée de la **\_ StorageAllocationSettingData CIM**.

</dd> <dt>

**HostExtentNameFormat**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identifie le format utilisé pour la propriété **HostExtentName** . Cette propriété est héritée de la **\_ StorageAllocationSettingData CIM**.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)
</dt> <dt>

<span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)
</dt> <dt>

<span id="NAA"></span><span id="naa"></span>**NAA** (9)
</dt> <dt>

<span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)
</dt> <dt>

<span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)
</dt> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**Nom du périphérique du système d’exploitation** (12)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF réservé** (.. )
</dt> </dl>

</dd> <dt>

**HostExtentNameNamespace**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si l’étendue de l’hôte est un volume SCSI, la source par défaut pour les noms de volume SCSI est la page SCSI VPD 83 réponses. Cette propriété est héritée de la **\_ StorageAllocationSettingData CIM**.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)
</dt> <dt>

<span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>**VPD83Type3** (2)
</dt> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>**VPD83Type2** (3)
</dt> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>**VPD83Type1** (4)
</dt> <dt>

<span id="VPD80"></span><span id="vpd80"></span>**VPD80** (5)
</dt> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>**NodeWWN** (6)
</dt> <dt>

<span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)
</dt> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>**Espace de noms du périphérique du système d’exploitation** (8)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF réservé** (.. )
</dt> </dl>

</dd> <dt>

**HostExtentStartingAddress**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identifie l’adresse de départ sur l’extension de stockage hôte, identifiée par la propriété **HostExtentName** , qui est utilisée pour l’allocation de l’extension de stockage virtuel. Une valeur **null** indique qu’il n’existe pas de mappage direct de l’étendue de stockage virtuel à l’extension de stockage hôte référencée. Cette propriété est héritée de la **\_ StorageAllocationSettingData CIM**.

</dd> <dt>

**HostResource**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Une seule ressource hôte peut être affectée à chaque périphérique de l’ordinateur virtuel, de sorte que seul le premier élément de ce tableau peut être défini. Pour les appareils qui prennent en charge cette fonctionnalité, définissez le premier élément du tableau **HostResource** pour qu’il contienne une référence à la ressource hôte sous-jacente à assigner. Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

Il s’agit d’une propriété en lecture seule. Toutefois, si la propriété **resourceType** est 31 (disque logique) et que la propriété **ResourceSubType** est « Microsoft : Hyper-v : disque dur virtuel », « Microsoft : Hyper-v : CD/DVD virtuel » ou « Microsoft : Hyper-v : disquette virtuelle », la propriété **HostResource** peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**HostResourceBlockSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Taille, en octets, des blocs qui sont alloués sur l’hôte à la suite de cette demande d’allocation de ressources de stockage ou d’allocation de ressources de stockage. Si la taille de bloc est variable, la taille de bloc maximale, en octets, sera spécifiée. Si la taille de bloc est inconnue ou si aucun concept de bloc ne s’applique, la valeur 1 est utilisée. Cette propriété est héritée de la **\_ StorageAllocationSettingData CIM**.

</dd> <dt>

**IgnoreFlushes**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la valeur est true, Hyper-V ignore le vidage de l’écriture différée pour cet ordinateur virtuel particulier. Si la valeur est false, Hyper-V continue à réécrire sur le disque à chaque vidage. False est le paramètre par défaut.

**Windows 10 :** Cette valeur n’est pas prise en charge tant que Windows 10.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Identifie de façon unique une instance de cette classe. Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**IOPSAllocationUnits**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie les unités d’allocation utilisées par les propriétés **IOPSLimit** et **IOPSReservation** . Cette propriété a toujours la valeur :

« nombre (e/s normalisées)/seconde »

Le débit est mesuré en opérations d’e/s normalisées par seconde (IOPS) au lieu d’IOPS brutes. Lorsque vous utilisez des e/s par seconde normalisées, chaque demande d’e/s est comptabilisée comme 1 e/s normalisée si la taille de la demande est inférieure ou égale à une taille de base prédéfinie (8 Ko). Les requêtes qui sont plus volumineuses que la taille de base sont comptabilisées comme des opérations d’e/s, où N est la valeur arrondie de la taille de la demande divisée par la taille de base. Par exemple, si la taille de base est de 8 Ko, une requête de 16 Ko est comptée comme 2 opérations d’e/s normalisées, une demande de 32 Ko comme 4 opérations d’e/s normalisées, et ainsi de suite.

**Windows 8.1 :** cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.

</dd> <dt>

**IOPSLimit**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1 milliard)
</dt> </dl>

Nombre maximal d’opérations d’e/s par seconde (IOPS) qui seront servies pour cette extension de stockage virtuel. Si la valeur n’est pas définie ou est égale à zéro, il n’y a aucune limite au nombre d’e/s par seconde que l’appareil peut émettre.

> [!Note]  
> Vous pouvez utiliser la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la [**classe \_ VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md) pour modifier la valeur de cette propriété. Cette propriété est significative uniquement pour les instances **MSVM \_ StorageAllocationSettingData** qui demandent des allocations de ressources pour les ordinateurs virtuels. Elle est ignorée lors de l’allocation de ressources à un pool enfant.

 

**Windows 8.1 :** cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.

</dd> <dt>

**IOPSReservation**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1 milliard)
</dt> </dl>

Nombre minimal d’opérations d’e/s par seconde (IOPS) qui seront servies pour cette extension de stockage virtuel.

Si **IOPSLimit** et **IOPSReservation** sont tous les deux définis, la valeur de **IOPSLimit** doit être supérieure ou égale à la valeur de **IOPSReservation**.

> [!Note]  
> Vous pouvez utiliser la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la [**classe \_ VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md) pour modifier la valeur de cette propriété. Cette propriété est significative uniquement pour les instances **MSVM \_ StorageAllocationSettingData** qui demandent des allocations de ressources pour les ordinateurs virtuels. Elle est ignorée lors de l’allocation de ressources à un pool enfant.

 

**Windows 8.1 :** cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.

</dd> <dt>

**Limite**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre maximal de blocs qui seront accordés pour cette allocation de ressources de stockage au niveau de l’hôte. La taille de bloc est spécifiée par la propriété **HostResourceBlockSize** . En règle générale, la valeur de cette propriété reflète une taille maximale pour l’étendue de l’hôte alloué qui correspond à la taille de l’étendue de stockage virtuel présentée au consommateur. Une valeur inférieure à celle-ci indique une situation dans laquelle une extension de stockage virtuel peu peuplé est attendue, où le taux de remplissage est limité par la valeur de la propriété Limit. Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**MappingBehavior**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie comment cette ressource est mappée aux ressources sous-jacentes. Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**OtherHostExtentNameFormat**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne qui décrit le format de la propriété **HostExtentName** si la propriété **HostExtentNameFormat** a la valeur 1 (autre). Cette propriété est héritée de la **\_ StorageAllocationSettingData CIM**.

</dd> <dt>

**OtherHostExtentNameNamespace**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne qui décrit l’espace de noms de la propriété **HostExtentName** si la propriété **HostExtentNameNamespace** contient 1 (autre). Cette propriété est héritée de la **\_ StorageAllocationSettingData CIM**.

</dd> <dt>

**OtherResourceType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne qui décrit le type de ressource lorsqu’une valeur bien définie n’est pas disponible et que [**resourceType**](msvm-processorsettingdata.md) a la valeur 1 (autre). Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**Parent**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Parent de la ressource. Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**PersistentReservationsSupported**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si le disque dur virtuel prend en charge les réservations persistantes SCSI-3.

**Windows 8.1 :** cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.

</dd> <dt>

**PoolID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur du pool de ressources à partir duquel cette ressource a été allouée. Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**Réservation**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **override** ("reservation"), **ModelCorrespondence** ("CIM \_ StorageAllocationSettingData. HostResourceBlockSize")
</dt> </dl>

Nombre de blocs dont la disponibilité est garantie pour cette allocation de ressources de stockage au niveau de l’hôte. La taille de bloc est spécifiée par la propriété **HostResourceBlockSize** . Cette propriété est héritée de la **\_ StorageAllocationSettingData CIM**.

</dd> <dt>

**ResourceSubType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne qui décrit un sous-type spécifique à l’implémentation pour cette ressource. Par exemple, cela peut être utilisé pour distinguer différents modèles du même type de ressource. Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type de ressource représenté par ce paramètre d’allocation. Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)
</dt> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Système informatique** (2)
</dt> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processeur** (3)
</dt> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Mémoire** (4)
</dt> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Contrôleur IDE** (5)
</dt> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI parallèle** (6)
</dt> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>**HBA FC** (7)
</dt> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)
</dt> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)
</dt> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Carte Ethernet** (10)
</dt> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Autre carte réseau** (11)
</dt> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Emplacement d’e/s** (12)
</dt> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Périphérique d’e/s** (13)
</dt> <dt>

<span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Lecteur de disquette** (14)
</dt> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Lecteur de CD** (15)
</dt> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Lecteur de DVD** (16)
</dt> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Lecteur de disque** (17)
</dt> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Lecteur de bande** (18)
</dt> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**étendue du Stockage** (19)
</dt> <dt>

<span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**autre appareil de Stockage** (20)
</dt> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Port série** (21)
</dt> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Port parallèle** (22)
</dt> <dt>

<span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Contrôleur USB** (23)
</dt> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Contrôleur Graphics** (24)
</dt> <dt>

<span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**Contrôleur IEEE 1394** (25)
</dt> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unité partitionnée** (26)
</dt> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unité partitionnée de base** (27)
</dt> <dt>

<span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Alimentation (28** )
</dt> <dt>

<span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Appareil de refroidissement** (29)
</dt> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Port commuté Ethernet** (30)
</dt> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Disque logique** (31)
</dt> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Volume de Stockage** (32)
</dt> <dt>

<span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Connexion Ethernet** (33)
</dt> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (30 32767)
</dt> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32768 65535)
</dt> </dl>

</dd> <dt>

**SnapshotId**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

GUID représentant la capture instantanée dans le fichier de définition de disque dur virtuel à attacher.

> [!Note]  
> Ajouté dans Windows 10.

 

</dd> <dt>

**StorageQoSPolicyID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

spécifie l’identificateur unique de la stratégie de QoS Stockage à appliquer à cette extension de stockage virtuel.

> [!Note]  
> Ajouté dans Windows 10.

 

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de blocs présentés au consommateur. La taille de bloc est spécifiée par la propriété **VirtualResourceBlockSize** . Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**VirtualQuantityUnits**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie les unités utilisées par la propriété **VirtualQuantity** . Cette propriété est héritée de la **\_ StorageAllocationSettingData CIM**.



| Valeur                                                                                                | Signification                                                                                    |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <dt>"Count (bloc de taille fixe)"</dt> </dl> | La taille de bloc fixe est contenue dans la propriété **VirtualResourceBlockSize** .<br/> |
| <dl> <dt>poids</dt> </dl>                    | La propriété **VirtualQuantity** est mesurée en octets.<br/>                          |



 

</dd> <dt>

**VirtualResourceBlockSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Taille, en octets, des blocs qui sont présentés au consommateur à la suite de cette demande d’allocation de ressources de stockage ou d’allocation de ressources de stockage. Si la taille de bloc est variable, la taille de bloc maximale, en octets, sera spécifiée. Si la taille de bloc est inconnue ou si aucun concept de bloc ne s’applique, la valeur 1 est utilisée. Cette propriété est héritée de la **\_ StorageAllocationSettingData CIM**.

</dd> <dt>

**Poids**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Weight"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (10000)
</dt> </dl>

Spécifie une priorité relative pour cette allocation par rapport à d’autres allocations à partir du même pool de ressources. Cette propriété n’a aucune unité de mesure et est uniquement pertinente par rapport à d’autres allocations vying pour les mêmes ressources hôte. Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

Plage : 1 10000

</dd> <dt>

**WriteHardeningMethod**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique quelle méthode de sécurisation renforcée d’écriture est prise en charge par le disque.

> [!Note]  
> cette propriété a été ajoutée dans Windows 10, version 1703.

 

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**Valeur par défaut** (0)


</dt> <dd></dd> <dt>

<span id="WriteCacheEnabled"></span><span id="writecacheenabled"></span><span id="WRITECACHEENABLED"></span>

**WriteCacheEnabled** (1)


</dt> <dd></dd> <dt>

<span id="WriteCacheandFUAEnabled"></span><span id="writecacheandfuaenabled"></span><span id="WRITECACHEANDFUAENABLED"></span>

**WriteCacheandFUAEnabled** (2)


</dt> <dd></dd> <dt>

<span id="WriteCacheDisabled"></span><span id="writecachedisabled"></span><span id="WRITECACHEDISABLED"></span>

**WriteCacheDisabled** (3)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

