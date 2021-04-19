---
description: Représente les paramètres d’allocation de ressources d’un élément managé pour un type de ressource spécifique.
ms.assetid: f27910c7-a88a-4694-80fe-7761945782e0
title: Classe CIM_AllocationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AllocationCapabilities
- CIM_AllocationCapabilities.ResourceType
- CIM_AllocationCapabilities.OtherResourceType
- CIM_AllocationCapabilities.ResourceSubType
- CIM_AllocationCapabilities.RequestTypesSupported
- CIM_AllocationCapabilities.SharingMode
- CIM_AllocationCapabilities.SupportedAddStates
- CIM_AllocationCapabilities.SupportedRemoveStates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d022023142b38905067e30a4c1be3b133e49a86f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512924"
---
# <a name="cim_allocationcapabilities-class"></a><span data-ttu-id="76ad6-103">\_Classe CIM AllocationCapabilities</span><span class="sxs-lookup"><span data-stu-id="76ad6-103">CIM\_AllocationCapabilities class</span></span>

<span data-ttu-id="76ad6-104">Représente les paramètres d’allocation de ressources d’un élément managé pour un type de ressource spécifique.</span><span class="sxs-lookup"><span data-stu-id="76ad6-104">Represents the resource allocation settings of a managed element for a specific resource type.</span></span>

## <a name="syntax"></a><span data-ttu-id="76ad6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76ad6-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_AllocationCapabilities : CIM_Capabilities
{
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  uint16 RequestTypesSupported;
  uint16 SharingMode;
  uint16 SupportedAddStates[];
  uint16 SupportedRemoveStates[];
};
```

## <a name="members"></a><span data-ttu-id="76ad6-106">Membres</span><span class="sxs-lookup"><span data-stu-id="76ad6-106">Members</span></span>

<span data-ttu-id="76ad6-107">La classe **CIM \_ AllocationCapabilities** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="76ad6-107">The **CIM\_AllocationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="76ad6-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="76ad6-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="76ad6-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="76ad6-109">Properties</span></span>

<span data-ttu-id="76ad6-110">La classe **CIM \_ AllocationCapabilities** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="76ad6-110">The **CIM\_AllocationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="76ad6-111">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="76ad6-111">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76ad6-112">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76ad6-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76ad6-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76ad6-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76ad6-114">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**ResourceType**»)</span><span class="sxs-lookup"><span data-stu-id="76ad6-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="76ad6-115">Type de ressource pour ce paramètre d’allocation lorsque la propriété **resourceType** est définie sur « 1 » (autre).</span><span class="sxs-lookup"><span data-stu-id="76ad6-115">The resource type for this allocation setting when the **ResourceType** property is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="76ad6-116">**RequestTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="76ad6-116">**RequestTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76ad6-117">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76ad6-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76ad6-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76ad6-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76ad6-119">Indique si la demande d’une ressource spécifique est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="76ad6-119">Indicates whether requesting a specific resource is supported.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="76ad6-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="76ad6-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span>

<span data-ttu-id="76ad6-121"><span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span>**Spécifique** (2)</span><span class="sxs-lookup"><span data-stu-id="76ad6-121"><span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span>**Specific** (2)</span></span>


</dt> <dd>

<span data-ttu-id="76ad6-122">La demande peut inclure une demande de ressource spécifique.</span><span class="sxs-lookup"><span data-stu-id="76ad6-122">Request can include a request for specific resource.</span></span>

</dd> <dt>

<span id="General"></span><span id="general"></span><span id="GENERAL"></span>

<span data-ttu-id="76ad6-123"><span id="General"></span><span id="general"></span><span id="GENERAL"></span>**Général** (3)</span><span class="sxs-lookup"><span data-stu-id="76ad6-123"><span id="General"></span><span id="general"></span><span id="GENERAL"></span>**General** (3)</span></span>


</dt> <dd>

<span data-ttu-id="76ad6-124">La demande n’inclut pas de ressource spécifique.</span><span class="sxs-lookup"><span data-stu-id="76ad6-124">Request does not include specific resource.</span></span>

</dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="76ad6-125"><span id="Both"></span><span id="both"></span><span id="BOTH"></span>**Les deux** (4)</span><span class="sxs-lookup"><span data-stu-id="76ad6-125"><span id="Both"></span><span id="both"></span><span id="BOTH"></span>**Both** (4)</span></span>


</dt> <dd>

<span data-ttu-id="76ad6-126">Les requêtes spécifiques et générales sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="76ad6-126">Both specific and general requests are supported.</span></span>

</dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="76ad6-127"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="76ad6-127"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="76ad6-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="76ad6-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="76ad6-129">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="76ad6-129">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76ad6-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76ad6-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76ad6-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76ad6-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76ad6-132">Description d’un sous-type spécifique à l’implémentation pour cette ressource.</span><span class="sxs-lookup"><span data-stu-id="76ad6-132">A description of an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="76ad6-133">Par exemple, cela peut être utilisé pour distinguer différents modèles du même type de ressource.</span><span class="sxs-lookup"><span data-stu-id="76ad6-133">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="76ad6-134">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="76ad6-134">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76ad6-135">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76ad6-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76ad6-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76ad6-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76ad6-137">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AllocationCapabilities**.**OtherResourceType**","[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**ResourceType**»)</span><span class="sxs-lookup"><span data-stu-id="76ad6-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AllocationCapabilities**.**OtherResourceType**", "[**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="76ad6-138">Type de ressource affecté à ce paramètre d’allocation.</span><span class="sxs-lookup"><span data-stu-id="76ad6-138">The type of resource that is assigned to this allocation setting.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="76ad6-139">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="76ad6-139">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

<span data-ttu-id="76ad6-140">**Système informatique** (2)</span><span class="sxs-lookup"><span data-stu-id="76ad6-140">**Computer System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

<span data-ttu-id="76ad6-141">**Processeur** (3)</span><span class="sxs-lookup"><span data-stu-id="76ad6-141">**Processor** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

<span data-ttu-id="76ad6-142">**Mémoire** (4)</span><span class="sxs-lookup"><span data-stu-id="76ad6-142">**Memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

<span data-ttu-id="76ad6-143">**Contrôleur IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="76ad6-143">**IDE Controller** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

<span data-ttu-id="76ad6-144">**HBA SCSI parallèle** (6)</span><span class="sxs-lookup"><span data-stu-id="76ad6-144">**Parallel SCSI HBA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

<span data-ttu-id="76ad6-145">**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="76ad6-145">**FC HBA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

<span data-ttu-id="76ad6-146">**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="76ad6-146">**iSCSI HBA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

<span data-ttu-id="76ad6-147">**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="76ad6-147">**IB HCA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

<span data-ttu-id="76ad6-148">**Carte Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="76ad6-148">**Ethernet Adapter** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

<span data-ttu-id="76ad6-149">**Autre carte réseau** (11)</span><span class="sxs-lookup"><span data-stu-id="76ad6-149">**Other Network Adapter** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

<span data-ttu-id="76ad6-150">**Emplacement d’e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="76ad6-150">**I/O Slot** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

<span data-ttu-id="76ad6-151">**Périphérique d’e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="76ad6-151">**I/O Device** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

<span data-ttu-id="76ad6-152">**Lecteur de disquette** (14)</span><span class="sxs-lookup"><span data-stu-id="76ad6-152">**Floppy Drive** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

<span data-ttu-id="76ad6-153">**Lecteur de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="76ad6-153">**CD Drive** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

<span data-ttu-id="76ad6-154">**Lecteur de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="76ad6-154">**DVD drive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="76ad6-155">**Lecteur de disque** (17)</span><span class="sxs-lookup"><span data-stu-id="76ad6-155">**Disk Drive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

<span data-ttu-id="76ad6-156">**Lecteur de bande** (18)</span><span class="sxs-lookup"><span data-stu-id="76ad6-156">**Tape Drive** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

<span data-ttu-id="76ad6-157">**Extension de stockage** (19)</span><span class="sxs-lookup"><span data-stu-id="76ad6-157">**Storage Extent** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

<span data-ttu-id="76ad6-158">**Autre dispositif de stockage** (20)</span><span class="sxs-lookup"><span data-stu-id="76ad6-158">**Other Storage Device** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

<span data-ttu-id="76ad6-159">**Port série** (21)</span><span class="sxs-lookup"><span data-stu-id="76ad6-159">**Serial port** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="76ad6-160">**Port parallèle** (22)</span><span class="sxs-lookup"><span data-stu-id="76ad6-160">**Parallel port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

<span data-ttu-id="76ad6-161">**Contrôleur USB** (23)</span><span class="sxs-lookup"><span data-stu-id="76ad6-161">**USB Controller** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

<span data-ttu-id="76ad6-162">**Contrôleur Graphics** (24)</span><span class="sxs-lookup"><span data-stu-id="76ad6-162">**Graphics controller** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

<span data-ttu-id="76ad6-163">**Contrôleur IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="76ad6-163">**IEEE 1394 Controller** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

<span data-ttu-id="76ad6-164">**Unité partitionnée** (26)</span><span class="sxs-lookup"><span data-stu-id="76ad6-164">**Partitionable Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

<span data-ttu-id="76ad6-165">**Unité partitionnée de base** (27)</span><span class="sxs-lookup"><span data-stu-id="76ad6-165">**Base Partitionable Unit** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="76ad6-166">**Puissance** (28)</span><span class="sxs-lookup"><span data-stu-id="76ad6-166">**Power** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

<span data-ttu-id="76ad6-167">**Capacité de refroidissement** (29)</span><span class="sxs-lookup"><span data-stu-id="76ad6-167">**Cooling Capacity** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

<span data-ttu-id="76ad6-168">**Port commuté Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="76ad6-168">**Ethernet Switch Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

<span data-ttu-id="76ad6-169">**Disque logique** (31)</span><span class="sxs-lookup"><span data-stu-id="76ad6-169">**Logical Disk** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

<span data-ttu-id="76ad6-170">**Volume de stockage** (32)</span><span class="sxs-lookup"><span data-stu-id="76ad6-170">**Storage Volume** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

<span data-ttu-id="76ad6-171">**Connexion Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="76ad6-171">**Ethernet Connection** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="76ad6-172">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="76ad6-172">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="76ad6-173">**Fournisseur réservé** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="76ad6-173">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="76ad6-174">**SharingMode**</span><span class="sxs-lookup"><span data-stu-id="76ad6-174">**SharingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76ad6-175">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76ad6-175">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76ad6-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76ad6-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76ad6-177">Indique comment l’accès à la ressource sous-jacente est accordé.</span><span class="sxs-lookup"><span data-stu-id="76ad6-177">Indicates how access to the underlying resource is granted.</span></span>

<span data-ttu-id="76ad6-178">La quantité réelle est contrôlée par min, taille maximale, poids, etc.</span><span class="sxs-lookup"><span data-stu-id="76ad6-178">Actual quantity is controlled by min, max size, weights, etc.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="76ad6-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="76ad6-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="76ad6-180"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dédié** (2)</span><span class="sxs-lookup"><span data-stu-id="76ad6-180"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (2)</span></span>


</dt> <dd>

<span data-ttu-id="76ad6-181">Accès exclusif à la ressource sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="76ad6-181">Exclusive access to underlying resource.</span></span>

</dd> <dt>

<span id="Shared"></span><span id="shared"></span><span id="SHARED"></span>

<span data-ttu-id="76ad6-182"><span id="Shared"></span><span id="shared"></span><span id="SHARED"></span>**Partagé** (3)</span><span class="sxs-lookup"><span data-stu-id="76ad6-182"><span id="Shared"></span><span id="shared"></span><span id="SHARED"></span>**Shared** (3)</span></span>


</dt> <dd>

<span data-ttu-id="76ad6-183">Utilisation partagée de la ressource sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="76ad6-183">Shared use of underlying resource.</span></span>

</dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="76ad6-184"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="76ad6-184"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="76ad6-185"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="76ad6-185"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="76ad6-186">**SupportedAddStates**</span><span class="sxs-lookup"><span data-stu-id="76ad6-186">**SupportedAddStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76ad6-187">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76ad6-187">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="76ad6-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76ad6-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76ad6-189">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**»)</span><span class="sxs-lookup"><span data-stu-id="76ad6-189">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="76ad6-190">États du système pris en charge lors de la création d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="76ad6-190">The system states that are supported when a new resource is created.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="76ad6-191">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="76ad6-191">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="76ad6-192">**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="76ad6-192">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="76ad6-193">**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="76ad6-193">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="76ad6-194">**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="76ad6-194">**Shutting Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="76ad6-195">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="76ad6-195">**Not Applicable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

<span data-ttu-id="76ad6-196">**Activé mais hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="76ad6-196">**Enabled but Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="76ad6-197">**Dans test** (7)</span><span class="sxs-lookup"><span data-stu-id="76ad6-197">**In Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="76ad6-198">**Différé** (8)</span><span class="sxs-lookup"><span data-stu-id="76ad6-198">**Deferred** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="76ad6-199">**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="76ad6-199">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="76ad6-200">**Démarrage** (10)</span><span class="sxs-lookup"><span data-stu-id="76ad6-200">**Starting** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="76ad6-201">En **Pause** (11)</span><span class="sxs-lookup"><span data-stu-id="76ad6-201">**Paused** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="76ad6-202">**Suspendu** (12)</span><span class="sxs-lookup"><span data-stu-id="76ad6-202">**Suspended** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="76ad6-203">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="76ad6-203">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="76ad6-204">**Fournisseur réservé** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="76ad6-204">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="76ad6-205">**SupportedRemoveStates**</span><span class="sxs-lookup"><span data-stu-id="76ad6-205">**SupportedRemoveStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76ad6-206">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76ad6-206">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="76ad6-207">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76ad6-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76ad6-208">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**»)</span><span class="sxs-lookup"><span data-stu-id="76ad6-208">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="76ad6-209">États du système pris en charge lorsqu’une ressource est supprimée.</span><span class="sxs-lookup"><span data-stu-id="76ad6-209">The system states that are supported when a resource is removed.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="76ad6-210">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="76ad6-210">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="76ad6-211">**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="76ad6-211">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="76ad6-212">**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="76ad6-212">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="76ad6-213">**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="76ad6-213">**Shutting Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="76ad6-214">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="76ad6-214">**Not Applicable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

<span data-ttu-id="76ad6-215">**Activé mais hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="76ad6-215">**Enabled but Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="76ad6-216">**Dans test** (7)</span><span class="sxs-lookup"><span data-stu-id="76ad6-216">**In Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="76ad6-217">**Différé** (8)</span><span class="sxs-lookup"><span data-stu-id="76ad6-217">**Deferred** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="76ad6-218">**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="76ad6-218">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="76ad6-219">**Démarrage** (10)</span><span class="sxs-lookup"><span data-stu-id="76ad6-219">**Starting** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="76ad6-220">En **Pause** (11)</span><span class="sxs-lookup"><span data-stu-id="76ad6-220">**Paused** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="76ad6-221">**Suspendu** (12)</span><span class="sxs-lookup"><span data-stu-id="76ad6-221">**Suspended** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="76ad6-222">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="76ad6-222">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="76ad6-223">**Fournisseur réservé** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="76ad6-223">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


<span data-ttu-id="76ad6-224"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="76ad6-224"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="76ad6-225">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76ad6-225">Requirements</span></span>



| <span data-ttu-id="76ad6-226">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76ad6-226">Requirement</span></span> | <span data-ttu-id="76ad6-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="76ad6-227">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76ad6-228">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76ad6-228">Minimum supported client</span></span><br/> | <span data-ttu-id="76ad6-229">Windows 8</span><span class="sxs-lookup"><span data-stu-id="76ad6-229">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="76ad6-230">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76ad6-230">Minimum supported server</span></span><br/> | <span data-ttu-id="76ad6-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="76ad6-231">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="76ad6-232">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="76ad6-232">Namespace</span></span><br/>                | <span data-ttu-id="76ad6-233">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="76ad6-233">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="76ad6-234">MOF</span><span class="sxs-lookup"><span data-stu-id="76ad6-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76ad6-235"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="76ad6-235"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="76ad6-236">DLL</span><span class="sxs-lookup"><span data-stu-id="76ad6-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76ad6-237"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="76ad6-237"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="76ad6-238">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76ad6-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76ad6-239">**\_Fonctionnalités CIM**</span><span class="sxs-lookup"><span data-stu-id="76ad6-239">**CIM\_Capabilities**</span></span>](cim-capabilities.md)
</dt> </dl>

 

