---
description: Représente l’état configuré d’un port de Fibre Channel synthétique ou d’un port de commutateur Fibre Channel.
ms.assetid: 680badc4-8dba-47e8-859a-0ed472a15eda
title: Classe Msvm_FcPortAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcPortAllocationSettingData
- Msvm_FcPortAllocationSettingData.InstanceID
- Msvm_FcPortAllocationSettingData.Caption
- Msvm_FcPortAllocationSettingData.Description
- Msvm_FcPortAllocationSettingData.ElementName
- Msvm_FcPortAllocationSettingData.ResourceType
- Msvm_FcPortAllocationSettingData.OtherResourceType
- Msvm_FcPortAllocationSettingData.ResourceSubType
- Msvm_FcPortAllocationSettingData.PoolID
- Msvm_FcPortAllocationSettingData.ConsumerVisibility
- Msvm_FcPortAllocationSettingData.HostResource
- Msvm_FcPortAllocationSettingData.AllocationUnits
- Msvm_FcPortAllocationSettingData.VirtualQuantity
- Msvm_FcPortAllocationSettingData.Reservation
- Msvm_FcPortAllocationSettingData.Limit
- Msvm_FcPortAllocationSettingData.Weight
- Msvm_FcPortAllocationSettingData.AutomaticAllocation
- Msvm_FcPortAllocationSettingData.AutomaticDeallocation
- Msvm_FcPortAllocationSettingData.Parent
- Msvm_FcPortAllocationSettingData.Connection
- Msvm_FcPortAllocationSettingData.Address
- Msvm_FcPortAllocationSettingData.MappingBehavior
- Msvm_FcPortAllocationSettingData.AddressOnParent
- Msvm_FcPortAllocationSettingData.VirtualQuantityUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cae27c18aa83878152ac006bf57911258d8d8980befd72becff19c7e2343e797
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681359"
---
# <a name="msvm_fcportallocationsettingdata-class"></a>MSVM \_ FcPortAllocationSettingData, classe

Représente l’état configuré d’un port de Fibre Channel synthétique ou d’un port de commutateur Fibre Channel.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcPortAllocationSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Virtual Fibre Channel VDev Default Settings";
  string  Description = "The default settings for the virtual Fibre Channel connection pool.";
  string  ElementName;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ FcPortAllocationSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ FcPortAllocationSettingData** possède les propriétés suivantes.

<dl> <dt>

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

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **MaxLen** (64)
</dt> </dl>

Brève description de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

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

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’objet. Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)). La modification de cette propriété modifie le nom d’élément du dérivé de l’appareil logique associé.

Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**HostResource**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Une seule ressource hôte peut être affectée à chaque périphérique de l’ordinateur virtuel, de sorte que seul le premier élément de ce tableau peut être défini. Pour les appareils qui prennent en charge cette fonctionnalité, définissez le premier élément du tableau **HostResource** pour qu’il contienne une référence à la ressource hôte sous-jacente à assigner. Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

Il s’agit d’une propriété en lecture seule, mais si la propriété **resourceType** est 22 (Disk) et que la propriété **ResourceSubType** est « lecteur de disque physique Microsoft », elle peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**\_ VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md) .

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

**Limite**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Quantité maximale de ressources qui seront accordées pour cette allocation. L’unité de mesure de cette propriété est spécifiée par la propriété **VirtualQuantityUnits** . Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**MappingBehavior**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie comment cette ressource est mappée aux ressources sous-jacentes. Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

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

**PoolID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur du pool de ressources à partir duquel cette ressource a été allouée. Pour les instances associées à une machine virtuelle, il s’agit de « Microsoft :*GUID* \\ *Device-Specific Data*». Pour les instances qui définissent les paramètres potentiels d’une machine virtuelle, il s’agit de « Microsoft : définition \\ *GUID* \\ *type*», où *type* peut être « maximum », « minimum », « default » ou « Increment ». Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**Réservation**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Quantité de ressources dont la disponibilité est garantie pour cette allocation. L’unité de mesure de cette propriété est spécifiée par la propriété **VirtualQuantityUnits** . Ces ressources sont garanties d’être disponibles pour la consommation par l’ordinateur virtuel. Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

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

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Lecteur de disquette** (14)
</dt> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Lecteur de CD** (15)
</dt> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Lecteur de DVD** (16)
</dt> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Port série** (17)
</dt> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Port parallèle** (18)
</dt> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Contrôleur USB** (19)
</dt> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Contrôleur Graphics** (20)
</dt> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**étendue du Stockage** (21)
</dt> <dt>

<span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disque** (22)
</dt> <dt>

<span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Bande** (23)
</dt> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Autre dispositif de stockage** (24)
</dt> <dt>

<span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Contrôleur FireWire** (25)
</dt> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unité partitionnée** (26)
</dt> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unité partitionnée de base** (27)
</dt> <dt>

<span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Alimentation (28** )
</dt> <dt>

<span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Appareil de refroidissement** (29)
</dt> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (30 32767)
</dt> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32768 65535)
</dt> </dl>

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie la quantité de ressources présentées au consommateur. L’unité de mesure de cette propriété est spécifiée par la propriété **VirtualQuantityUnits** . Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**VirtualQuantityUnits**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie l’unité de mesure pour cette allocation de ressources. La valeur de cette propriété doit être une valeur légale du qualificateur d’unités de programmation, tel que défini dans l’annexe C. 1 de DSP0004 V 2.5 ou version ultérieure. Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**Poids**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Entier qui définit la pondération relative pour chaque processeur d’ordinateur virtuel. Une fois toutes les réserves remplies, la capacité du processeur physique restant de la plateforme d’hébergement sera allouée aux ordinateurs virtuels en fonction de leurs pondérations relatives. Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

Plage : 0 1000

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

