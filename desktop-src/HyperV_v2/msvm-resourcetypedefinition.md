---
description: Définit un mappage d’un type de ressource à ses classes d’implémentation.
ms.assetid: 0911454D-2494-49D5-8480-212E9ADD1B45
title: Classe Msvm_ResourceTypeDefinition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceTypeDefinition
- Msvm_ResourceTypeDefinition.ResourceType
- Msvm_ResourceTypeDefinition.OtherResourceType
- Msvm_ResourceTypeDefinition.ResourceSubType
- Msvm_ResourceTypeDefinition.LogicalDeviceClassName
- Msvm_ResourceTypeDefinition.SettingDataClassName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: edfbf2ec9772fa710df5fc0d024abfcad6d826d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529309"
---
# <a name="msvm_resourcetypedefinition-class"></a><span data-ttu-id="bba7f-103">MSVM \_ ResourceTypeDefinition, classe</span><span class="sxs-lookup"><span data-stu-id="bba7f-103">Msvm\_ResourceTypeDefinition class</span></span>

<span data-ttu-id="bba7f-104">Définit un mappage d’un type de ressource à ses classes d’implémentation.</span><span class="sxs-lookup"><span data-stu-id="bba7f-104">Defines a mapping of a resource type to its implementation classes.</span></span>

<span data-ttu-id="bba7f-105">La syntaxe suivante est simplifiée format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="bba7f-105">The following syntax is simplified Managed Object Format (MOF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="bba7f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bba7f-106">Syntax</span></span>

``` syntax
class Msvm_ResourceTypeDefinition
{
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  string LogicalDeviceClassName;
  string SettingDataClassName;
};
```

## <a name="members"></a><span data-ttu-id="bba7f-107">Membres</span><span class="sxs-lookup"><span data-stu-id="bba7f-107">Members</span></span>

<span data-ttu-id="bba7f-108">La classe **MSVM \_ ResourceTypeDefinition** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="bba7f-108">The **Msvm\_ResourceTypeDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="bba7f-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bba7f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bba7f-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bba7f-110">Properties</span></span>

<span data-ttu-id="bba7f-111">La classe **MSVM \_ ResourceTypeDefinition** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="bba7f-111">The **Msvm\_ResourceTypeDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bba7f-112">**LogicalDeviceClassName**</span><span class="sxs-lookup"><span data-stu-id="bba7f-112">**LogicalDeviceClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba7f-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bba7f-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bba7f-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bba7f-115">Nom de la classe dérivée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) qui implémente l’unité logique pour ce type de ressource.</span><span class="sxs-lookup"><span data-stu-id="bba7f-115">The name of the class derived from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) that implements the logical device for this resource type.</span></span>

</dd> <dt>

<span data-ttu-id="bba7f-116">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="bba7f-116">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba7f-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bba7f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bba7f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-119">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="bba7f-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="bba7f-120">Chaîne qui décrit le type de ressource lorsqu’une valeur bien définie n’est pas disponible et que **resourceType** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="bba7f-120">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="bba7f-121">Il existe une correspondance avec la propriété **OtherResourceType** de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="bba7f-121">There is a correspondence with the **OtherResourceType** property of [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="bba7f-122">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="bba7f-122">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba7f-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bba7f-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bba7f-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-125">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="bba7f-125">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="bba7f-126">Chaîne qui décrit un sous-type spécifique à l’implémentation pour cette ressource.</span><span class="sxs-lookup"><span data-stu-id="bba7f-126">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="bba7f-127">Par exemple, cela peut être utilisé pour distinguer différents modèles du même type de ressource.</span><span class="sxs-lookup"><span data-stu-id="bba7f-127">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="bba7f-128">Il existe une correspondance avec la propriété **ResourceSubType** de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="bba7f-128">There is a correspondence with the **ResourceSubType** property of [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="bba7f-129">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="bba7f-129">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba7f-130">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bba7f-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bba7f-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-132">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="bba7f-132">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="bba7f-133">Type de ressource représenté par ce paramètre d’allocation.</span><span class="sxs-lookup"><span data-stu-id="bba7f-133">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="bba7f-134">Il existe une correspondance avec la propriété **resourceType** de [**la \_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="bba7f-134">There is a correspondence with the **ResourceType** property of [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="bba7f-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="bba7f-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-136"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Système informatique** (2)</span><span class="sxs-lookup"><span data-stu-id="bba7f-136"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-137"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processeur** (3)</span><span class="sxs-lookup"><span data-stu-id="bba7f-137"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-138"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Mémoire** (4)</span><span class="sxs-lookup"><span data-stu-id="bba7f-138"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-139"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Contrôleur IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="bba7f-139"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-140"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI parallèle** (6)</span><span class="sxs-lookup"><span data-stu-id="bba7f-140"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-141"><span id="FC_HBA"></span><span id="fc_hba"></span>**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="bba7f-141"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-142"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="bba7f-142"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-143"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="bba7f-143"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-144"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Carte Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="bba7f-144"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-145"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Autre carte réseau** (11)</span><span class="sxs-lookup"><span data-stu-id="bba7f-145"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-146"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Emplacement d’e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="bba7f-146"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-147"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Périphérique d’e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="bba7f-147"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-148"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Lecteur de disquette** (14)</span><span class="sxs-lookup"><span data-stu-id="bba7f-148"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-149"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Lecteur de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="bba7f-149"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-150"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Lecteur de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="bba7f-150"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-151"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Port série** (17)</span><span class="sxs-lookup"><span data-stu-id="bba7f-151"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (17)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-152"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Port parallèle** (18)</span><span class="sxs-lookup"><span data-stu-id="bba7f-152"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (18)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-153"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Contrôleur USB** (19)</span><span class="sxs-lookup"><span data-stu-id="bba7f-153"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (19)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-154"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Contrôleur Graphics** (20)</span><span class="sxs-lookup"><span data-stu-id="bba7f-154"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (20)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-155"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extension de stockage** (21)</span><span class="sxs-lookup"><span data-stu-id="bba7f-155"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (21)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-156"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disque** (22)</span><span class="sxs-lookup"><span data-stu-id="bba7f-156"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disk** (22)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-157"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Bande** (23)</span><span class="sxs-lookup"><span data-stu-id="bba7f-157"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Tape** (23)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-158"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Autre dispositif de stockage** (24)</span><span class="sxs-lookup"><span data-stu-id="bba7f-158"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other storage device** (24)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-159"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Contrôleur FireWire** (25)</span><span class="sxs-lookup"><span data-stu-id="bba7f-159"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-160"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unité partitionnée** (26)</span><span class="sxs-lookup"><span data-stu-id="bba7f-160"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-161"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unité partitionnée de base** (27)</span><span class="sxs-lookup"><span data-stu-id="bba7f-161"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-162"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Alimentation (28** )</span><span class="sxs-lookup"><span data-stu-id="bba7f-162"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-163"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Appareil de refroidissement** (29)</span><span class="sxs-lookup"><span data-stu-id="bba7f-163"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-164"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (30 32767)</span><span class="sxs-lookup"><span data-stu-id="bba7f-164"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (30 32767)</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-165"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="bba7f-165"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bba7f-166">**SettingDataClassName**</span><span class="sxs-lookup"><span data-stu-id="bba7f-166">**SettingDataClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba7f-167">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bba7f-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba7f-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bba7f-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bba7f-169">Nom de la classe dérivée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) qui implémente les paramètres pour ce type de ressource.</span><span class="sxs-lookup"><span data-stu-id="bba7f-169">The name of the class derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) that implements the settings for this resource type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bba7f-170">Notes</span><span class="sxs-lookup"><span data-stu-id="bba7f-170">Remarks</span></span>

<span data-ttu-id="bba7f-171">L’accès à la classe **MSVM \_ ResourceTypeDefinition** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="bba7f-171">Access to the **Msvm\_ResourceTypeDefinition** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="bba7f-172">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="bba7f-172">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="bba7f-173">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bba7f-173">Requirements</span></span>



| <span data-ttu-id="bba7f-174">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bba7f-174">Requirement</span></span> | <span data-ttu-id="bba7f-175">Valeur</span><span class="sxs-lookup"><span data-stu-id="bba7f-175">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bba7f-176">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bba7f-176">Minimum supported client</span></span><br/> | <span data-ttu-id="bba7f-177">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bba7f-177">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bba7f-178">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bba7f-178">Minimum supported server</span></span><br/> | <span data-ttu-id="bba7f-179">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bba7f-179">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bba7f-180">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="bba7f-180">End of client support</span></span><br/>    | <span data-ttu-id="bba7f-181">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="bba7f-181">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="bba7f-182">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="bba7f-182">End of server support</span></span><br/>    | <span data-ttu-id="bba7f-183">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="bba7f-183">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="bba7f-184">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bba7f-184">Namespace</span></span><br/>                | <span data-ttu-id="bba7f-185">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="bba7f-185">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bba7f-186">MOF</span><span class="sxs-lookup"><span data-stu-id="bba7f-186">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bba7f-187"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bba7f-187"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bba7f-188">DLL</span><span class="sxs-lookup"><span data-stu-id="bba7f-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bba7f-189"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bba7f-189"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

