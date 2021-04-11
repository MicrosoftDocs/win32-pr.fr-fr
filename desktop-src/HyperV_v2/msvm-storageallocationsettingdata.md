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
ms.openlocfilehash: d889c262eee9d827a02547ddbfdff2cb121cb337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203599"
---
# <a name="msvm_storageallocationsettingdata-class"></a><span data-ttu-id="80144-103">MSVM \_ StorageAllocationSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="80144-103">Msvm\_StorageAllocationSettingData class</span></span>

<span data-ttu-id="80144-104">Représente des paramètres spécifiquement liés à l’allocation de stockage virtuel.</span><span class="sxs-lookup"><span data-stu-id="80144-104">Represents settings specifically related to the allocation of virtual storage.</span></span>

<span data-ttu-id="80144-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="80144-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="80144-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80144-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="80144-107">Membres</span><span class="sxs-lookup"><span data-stu-id="80144-107">Members</span></span>

<span data-ttu-id="80144-108">La classe **MSVM \_ StorageAllocationSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="80144-108">The **Msvm\_StorageAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="80144-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="80144-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="80144-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="80144-110">Properties</span></span>

<span data-ttu-id="80144-111">La classe **MSVM \_ StorageAllocationSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="80144-111">The **Msvm\_StorageAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="80144-112">**y accéder**</span><span class="sxs-lookup"><span data-stu-id="80144-112">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-113">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="80144-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="80144-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-115">Spécifie l’accès au stockage.</span><span class="sxs-lookup"><span data-stu-id="80144-115">Specifies the storage access.</span></span> <span data-ttu-id="80144-116">Cette propriété est héritée de la **\_ StorageAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="80144-116">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

<dl> <dt>

<span data-ttu-id="80144-117"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="80144-117"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="80144-118"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Lecture** (1)</span><span class="sxs-lookup"><span data-stu-id="80144-118"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>
</dt> <dt>

<span data-ttu-id="80144-119"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Accessible en écriture** (2)</span><span class="sxs-lookup"><span data-stu-id="80144-119"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>
</dt> <dt>

<span data-ttu-id="80144-120"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Lecture/écriture prise en charge** (3)</span><span class="sxs-lookup"><span data-stu-id="80144-120"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="80144-121">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="80144-121">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80144-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80144-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-124">Adresse de la ressource.</span><span class="sxs-lookup"><span data-stu-id="80144-124">The address of the resource.</span></span> <span data-ttu-id="80144-125">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="80144-125">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="80144-126">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="80144-126">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80144-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80144-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-129">Décrit l’adresse de cette ressource dans le contexte du parent.</span><span class="sxs-lookup"><span data-stu-id="80144-129">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="80144-130">Les propriétés **parent** et **AddressOnParent** sont utilisées pour décrire la relation du contrôleur, ainsi que l’ordre des appareils sur un contrôleur.</span><span class="sxs-lookup"><span data-stu-id="80144-130">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="80144-131">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="80144-131">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="80144-132">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="80144-132">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80144-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80144-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-135">Unités d’allocation utilisées par la **réservation** et les propriétés de la **limite** .</span><span class="sxs-lookup"><span data-stu-id="80144-135">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="80144-136">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="80144-136">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="80144-137">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="80144-137">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-138">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="80144-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80144-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-140">Indique si la ressource sera automatiquement allouée.</span><span class="sxs-lookup"><span data-stu-id="80144-140">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="80144-141">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="80144-141">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="80144-142">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="80144-142">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-143">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="80144-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80144-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-145">Indique si la ressource sera automatiquement désallouée.</span><span class="sxs-lookup"><span data-stu-id="80144-145">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="80144-146">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="80144-146">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="80144-147">**CachingMode**</span><span class="sxs-lookup"><span data-stu-id="80144-147">**CachingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-148">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="80144-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="80144-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-150">Indique si et comment la mise en cache des fichiers en mémoire doit être utilisée pour ce disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="80144-150">Indicates whether and how in-memory file caching should be used for this VHD.</span></span> <span data-ttu-id="80144-151">La stratégie par défaut est définie dans le champ **DefaultVirtualHardDiskCachingMode** de la classe [**MSVM \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="80144-151">The default policy is set in the **DefaultVirtualHardDiskCachingMode** field of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="80144-152">Ajouté dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="80144-152">Added in Windows 10.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="80144-153">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="80144-153">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="80144-154">**Par défaut** (2)</span><span class="sxs-lookup"><span data-stu-id="80144-154">**Default** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Caching"></span><span id="no_caching"></span><span id="NO_CACHING"></span>

<span data-ttu-id="80144-155">**Aucune mise en cache** (3)</span><span class="sxs-lookup"><span data-stu-id="80144-155">**No Caching** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_Sharable_Parents"></span><span id="cache_sharable_parents"></span><span id="CACHE_SHARABLE_PARENTS"></span>

<span data-ttu-id="80144-156">Mettre **en cache les parents partageables** (4)</span><span class="sxs-lookup"><span data-stu-id="80144-156">**Cache Sharable Parents** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="80144-157">**Caption**</span><span class="sxs-lookup"><span data-stu-id="80144-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80144-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80144-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80144-160">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="80144-160">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="80144-161">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="80144-161">A short description of the object.</span></span> <span data-ttu-id="80144-162">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « paramètres par défaut de l’image de disque dur ».</span><span class="sxs-lookup"><span data-stu-id="80144-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hard Disk Image Default Settings".</span></span>

</dd> <dt>

<span data-ttu-id="80144-163">**Connection**</span><span class="sxs-lookup"><span data-stu-id="80144-163">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-164">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="80144-164">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="80144-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-166">Appareil auquel cette ressource est connectée.</span><span class="sxs-lookup"><span data-stu-id="80144-166">The device to which this resource is connected.</span></span> <span data-ttu-id="80144-167">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="80144-167">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="80144-168">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="80144-168">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-169">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="80144-169">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="80144-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-171">Visibilité du consommateur sur la ressource allouée.</span><span class="sxs-lookup"><span data-stu-id="80144-171">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="80144-172">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="80144-172">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="80144-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="80144-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="80144-174"><span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span>**Passe-à-** (2)</span><span class="sxs-lookup"><span data-stu-id="80144-174"><span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span>**Passed-Through** (2)</span></span>
</dt> <dt>

<span data-ttu-id="80144-175"><span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span>**Virtualisé** (3)</span><span class="sxs-lookup"><span data-stu-id="80144-175"><span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span>**Virtualized** (3)</span></span>
</dt> <dt>

<span data-ttu-id="80144-176"><span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span>**Non représenté** (4)</span><span class="sxs-lookup"><span data-stu-id="80144-176"><span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span>**Not represented** (4)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="80144-177">**Description**</span><span class="sxs-lookup"><span data-stu-id="80144-177">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-178">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80144-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80144-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-180">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="80144-180">A description of the object.</span></span> <span data-ttu-id="80144-181">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et elle est toujours définie sur « décrit les paramètres par défaut pour les ressources de l’image de disque dur ».</span><span class="sxs-lookup"><span data-stu-id="80144-181">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Describes the default settings for the hard disk image resources".</span></span>

</dd> <dt>

<span data-ttu-id="80144-182">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="80144-182">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-183">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80144-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80144-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-185">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="80144-185">A display name for the object.</span></span> <span data-ttu-id="80144-186">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="80144-186">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="80144-187">**HostExtentName**</span><span class="sxs-lookup"><span data-stu-id="80144-187">**HostExtentName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-188">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80144-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80144-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-190">Identificateur unique pour l’étendue de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="80144-190">A unique identifier for the host extent.</span></span> <span data-ttu-id="80144-191">L’étendue de l’hôte identifiée est utilisée pour l’allocation des ressources de stockage.</span><span class="sxs-lookup"><span data-stu-id="80144-191">The identified host extent is used for the storage resource allocation.</span></span> <span data-ttu-id="80144-192">Cette propriété est héritée de la **\_ StorageAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="80144-192">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="80144-193">**HostExtentNameFormat**</span><span class="sxs-lookup"><span data-stu-id="80144-193">**HostExtentNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-194">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="80144-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="80144-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-196">Identifie le format utilisé pour la propriété **HostExtentName** .</span><span class="sxs-lookup"><span data-stu-id="80144-196">Identifies the format that is used for the **HostExtentName** property.</span></span> <span data-ttu-id="80144-197">Cette propriété est héritée de la **\_ StorageAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="80144-197">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

<dl> <dt>

<span data-ttu-id="80144-198"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="80144-198"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="80144-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="80144-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="80144-200"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span><span class="sxs-lookup"><span data-stu-id="80144-200"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span></span>
</dt> <dt>

<span data-ttu-id="80144-201"><span id="NAA"></span><span id="naa"></span>**NAA** (9)</span><span class="sxs-lookup"><span data-stu-id="80144-201"><span id="NAA"></span><span id="naa"></span>**NAA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="80144-202"><span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)</span><span class="sxs-lookup"><span data-stu-id="80144-202"><span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)</span></span>
</dt> <dt>

<span data-ttu-id="80144-203"><span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)</span><span class="sxs-lookup"><span data-stu-id="80144-203"><span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)</span></span>
</dt> <dt>

<span data-ttu-id="80144-204"><span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**Nom du périphérique du système d’exploitation** (12)</span><span class="sxs-lookup"><span data-stu-id="80144-204"><span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**OS Device Name** (12)</span></span>
</dt> <dt>

<span data-ttu-id="80144-205"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF réservé** (..</span><span class="sxs-lookup"><span data-stu-id="80144-205"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="80144-206">)</span><span class="sxs-lookup"><span data-stu-id="80144-206">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="80144-207">**HostExtentNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="80144-207">**HostExtentNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-208">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="80144-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="80144-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-210">Si l’étendue de l’hôte est un volume SCSI, la source par défaut pour les noms de volume SCSI est la page SCSI VPD 83 réponses.</span><span class="sxs-lookup"><span data-stu-id="80144-210">If the host extent is a SCSI volume, then the preferred source for SCSI volume names is SCSI VPD Page 83 responses.</span></span> <span data-ttu-id="80144-211">Cette propriété est héritée de la **\_ StorageAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="80144-211">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

<dl> <dt>

<span data-ttu-id="80144-212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="80144-212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="80144-213"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="80144-213"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="80144-214"><span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>**VPD83Type3** (2)</span><span class="sxs-lookup"><span data-stu-id="80144-214"><span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>**VPD83Type3** (2)</span></span>
</dt> <dt>

<span data-ttu-id="80144-215"><span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>**VPD83Type2** (3)</span><span class="sxs-lookup"><span data-stu-id="80144-215"><span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>**VPD83Type2** (3)</span></span>
</dt> <dt>

<span data-ttu-id="80144-216"><span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>**VPD83Type1** (4)</span><span class="sxs-lookup"><span data-stu-id="80144-216"><span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>**VPD83Type1** (4)</span></span>
</dt> <dt>

<span data-ttu-id="80144-217"><span id="VPD80"></span><span id="vpd80"></span>**VPD80** (5)</span><span class="sxs-lookup"><span data-stu-id="80144-217"><span id="VPD80"></span><span id="vpd80"></span>**VPD80** (5)</span></span>
</dt> <dt>

<span data-ttu-id="80144-218"><span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>**NodeWWN** (6)</span><span class="sxs-lookup"><span data-stu-id="80144-218"><span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>**NodeWWN** (6)</span></span>
</dt> <dt>

<span data-ttu-id="80144-219"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span><span class="sxs-lookup"><span data-stu-id="80144-219"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span></span>
</dt> <dt>

<span data-ttu-id="80144-220"><span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>**Espace de noms du périphérique du système d’exploitation** (8)</span><span class="sxs-lookup"><span data-stu-id="80144-220"><span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>**OS Device Namespace** (8)</span></span>
</dt> <dt>

<span data-ttu-id="80144-221"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF réservé** (..</span><span class="sxs-lookup"><span data-stu-id="80144-221"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="80144-222">)</span><span class="sxs-lookup"><span data-stu-id="80144-222">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="80144-223">**HostExtentStartingAddress**</span><span class="sxs-lookup"><span data-stu-id="80144-223">**HostExtentStartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-224">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="80144-224">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="80144-225">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-226">Identifie l’adresse de départ sur l’extension de stockage hôte, identifiée par la propriété **HostExtentName** , qui est utilisée pour l’allocation de l’extension de stockage virtuel.</span><span class="sxs-lookup"><span data-stu-id="80144-226">Identifies the starting address on the host storage extent, identified by the **HostExtentName** property, that is used for the allocation of the virtual storage extent.</span></span> <span data-ttu-id="80144-227">Une valeur **null** indique qu’il n’existe pas de mappage direct de l’étendue de stockage virtuel à l’extension de stockage hôte référencée.</span><span class="sxs-lookup"><span data-stu-id="80144-227">A **Null** value indicates that there is no direct mapping of the virtual storage extent to the referenced host storage extent.</span></span> <span data-ttu-id="80144-228">Cette propriété est héritée de la **\_ StorageAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="80144-228">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="80144-229">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="80144-229">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-230">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="80144-230">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="80144-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-232">Une seule ressource hôte peut être affectée à chaque périphérique de l’ordinateur virtuel, de sorte que seul le premier élément de ce tableau peut être défini.</span><span class="sxs-lookup"><span data-stu-id="80144-232">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="80144-233">Pour les appareils qui prennent en charge cette fonctionnalité, définissez le premier élément du tableau **HostResource** pour qu’il contienne une référence à la ressource hôte sous-jacente à assigner.</span><span class="sxs-lookup"><span data-stu-id="80144-233">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="80144-234">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="80144-234">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="80144-235">Il s’agit d’une propriété en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="80144-235">This is a read-only property.</span></span> <span data-ttu-id="80144-236">Toutefois, si la propriété **resourceType** est 31 (disque logique) et que la propriété **ResourceSubType** est « Microsoft : Hyper-v : disque dur virtuel », « Microsoft : Hyper-v : CD/DVD virtuel » ou « Microsoft : Hyper-v : disquette virtuelle », la propriété **HostResource** peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="80144-236">But if the **ResourceType** property is 31 (Logical Disk) and the **ResourceSubType** property is "Microsoft:Hyper-V:Virtual Hard Disk", "Microsoft:Hyper-V:Virtual CD/DVD Disk", or "Microsoft:Hyper-V:Virtual Floppy Disk", the **HostResource** property can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="80144-237">**HostResourceBlockSize**</span><span class="sxs-lookup"><span data-stu-id="80144-237">**HostResourceBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-238">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="80144-238">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="80144-239">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-240">Taille, en octets, des blocs qui sont alloués sur l’hôte à la suite de cette demande d’allocation de ressources de stockage ou d’allocation de ressources de stockage.</span><span class="sxs-lookup"><span data-stu-id="80144-240">The size, in bytes, of the blocks that are allocated at the host as the result of this storage resource allocation or storage resource allocation request.</span></span> <span data-ttu-id="80144-241">Si la taille de bloc est variable, la taille de bloc maximale, en octets, sera spécifiée.</span><span class="sxs-lookup"><span data-stu-id="80144-241">If the block size is variable, then the maximum block size, in bytes, will be specified.</span></span> <span data-ttu-id="80144-242">Si la taille de bloc est inconnue ou si aucun concept de bloc ne s’applique, la valeur 1 est utilisée.</span><span class="sxs-lookup"><span data-stu-id="80144-242">If the block size is unknown or if a block concept does not apply, then the value 1 will be used.</span></span> <span data-ttu-id="80144-243">Cette propriété est héritée de la **\_ StorageAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="80144-243">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="80144-244">**IgnoreFlushes**</span><span class="sxs-lookup"><span data-stu-id="80144-244">**IgnoreFlushes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-245">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="80144-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80144-246">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-247">Si la valeur est true, Hyper-V ignore le vidage de l’écriture différée pour cet ordinateur virtuel particulier.</span><span class="sxs-lookup"><span data-stu-id="80144-247">If set to true, Hyper-V will ignore write back flushing for that particular virtual machine.</span></span> <span data-ttu-id="80144-248">Si la valeur est false, Hyper-V continue à réécrire sur le disque à chaque vidage.</span><span class="sxs-lookup"><span data-stu-id="80144-248">If set to false, Hyper-V will continue to write back to the disk on every flush.</span></span> <span data-ttu-id="80144-249">False est le paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="80144-249">The default setting is false.</span></span>

<span data-ttu-id="80144-250">**Windows 10 :** Cette valeur n’est pas prise en charge avant Windows 10.</span><span class="sxs-lookup"><span data-stu-id="80144-250">**Windows 10:** This value is not supported until Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="80144-251">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="80144-251">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-252">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80144-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80144-253">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-253">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80144-254">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="80144-254">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="80144-255">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="80144-255">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="80144-256">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="80144-256">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="80144-257">**IOPSAllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="80144-257">**IOPSAllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-258">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80144-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80144-259">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-260">Spécifie les unités d’allocation utilisées par les propriétés **IOPSLimit** et **IOPSReservation** .</span><span class="sxs-lookup"><span data-stu-id="80144-260">Specifies the allocation units used by the **IOPSLimit** and **IOPSReservation** properties.</span></span> <span data-ttu-id="80144-261">Cette propriété a toujours la valeur :</span><span class="sxs-lookup"><span data-stu-id="80144-261">This property always has the value:</span></span>

<span data-ttu-id="80144-262">« nombre (e/s normalisées)/seconde »</span><span class="sxs-lookup"><span data-stu-id="80144-262">"count(normalized I/O) / second"</span></span>

<span data-ttu-id="80144-263">Le débit est mesuré en opérations d’e/s normalisées par seconde (IOPS) au lieu d’IOPS brutes.</span><span class="sxs-lookup"><span data-stu-id="80144-263">Throughput is measured in normalized I/O operations per second (IOPS) instead of raw IOPS.</span></span> <span data-ttu-id="80144-264">Lorsque vous utilisez des e/s par seconde normalisées, chaque demande d’e/s est comptabilisée comme 1 e/s normalisée si la taille de la demande est inférieure ou égale à une taille de base prédéfinie (8 Ko).</span><span class="sxs-lookup"><span data-stu-id="80144-264">When using normalized IOPS, each I/O request is accounted for as 1 normalized I/O if the size of the request is less than or equal to a predefined base size (8 KB).</span></span> <span data-ttu-id="80144-265">Les requêtes qui sont plus volumineuses que la taille de base sont comptabilisées comme des opérations d’e/s, où N est la valeur arrondie de la taille de la demande divisée par la taille de base.</span><span class="sxs-lookup"><span data-stu-id="80144-265">Requests that are larger than the base size are accounted for as N I/O operations, where N is the rounded-up value of the request size divided by the base size.</span></span> <span data-ttu-id="80144-266">Par exemple, si la taille de base est de 8 Ko, une requête de 16 Ko est comptée comme 2 opérations d’e/s normalisées, une demande de 32 Ko comme 4 opérations d’e/s normalisées, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="80144-266">For example, if the base size is 8 KB, a 16-KB request is counted as 2 normalized I/O operations, a 32-KB request as 4 normalized I/O operations, and so on.</span></span>

<span data-ttu-id="80144-267">**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="80144-267">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="80144-268">**IOPSLimit**</span><span class="sxs-lookup"><span data-stu-id="80144-268">**IOPSLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-269">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="80144-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="80144-270">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80144-271">Qualificateurs : [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1 milliard)</span><span class="sxs-lookup"><span data-stu-id="80144-271">Qualifiers: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1000000000)</span></span>
</dt> </dl>

<span data-ttu-id="80144-272">Nombre maximal d’opérations d’e/s par seconde (IOPS) qui seront servies pour cette extension de stockage virtuel.</span><span class="sxs-lookup"><span data-stu-id="80144-272">The maximum number of I/O operations per second (IOPS) that will be serviced for this virtual storage extent.</span></span> <span data-ttu-id="80144-273">Si la valeur n’est pas définie ou est égale à zéro, il n’y a aucune limite au nombre d’e/s par seconde que l’appareil peut émettre.</span><span class="sxs-lookup"><span data-stu-id="80144-273">If the value isn't defined or is zero, there is no limit to the number of IOPS that the device can issue.</span></span>

> [!Note]  
> <span data-ttu-id="80144-274">Vous pouvez utiliser la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la [**classe \_ VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md) pour modifier la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="80144-274">You can use the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to modify the value of this property.</span></span> <span data-ttu-id="80144-275">Cette propriété est significative uniquement pour les instances **MSVM \_ StorageAllocationSettingData** qui demandent des allocations de ressources pour les ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="80144-275">This property is meaningful only for **Msvm\_StorageAllocationSettingData** instances that request resource allocations for virtual machines.</span></span> <span data-ttu-id="80144-276">Elle est ignorée lors de l’allocation de ressources à un pool enfant.</span><span class="sxs-lookup"><span data-stu-id="80144-276">It's ignored when allocating resources to a child pool.</span></span>

 

<span data-ttu-id="80144-277">**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="80144-277">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="80144-278">**IOPSReservation**</span><span class="sxs-lookup"><span data-stu-id="80144-278">**IOPSReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-279">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="80144-279">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="80144-280">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80144-281">Qualificateurs : [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1 milliard)</span><span class="sxs-lookup"><span data-stu-id="80144-281">Qualifiers: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1000000000)</span></span>
</dt> </dl>

<span data-ttu-id="80144-282">Nombre minimal d’opérations d’e/s par seconde (IOPS) qui seront servies pour cette extension de stockage virtuel.</span><span class="sxs-lookup"><span data-stu-id="80144-282">The minimum number of I/O operations per second (IOPS) that will be serviced for this virtual storage extent.</span></span>

<span data-ttu-id="80144-283">Si **IOPSLimit** et **IOPSReservation** sont tous les deux définis, la valeur de **IOPSLimit** doit être supérieure ou égale à la valeur de **IOPSReservation**.</span><span class="sxs-lookup"><span data-stu-id="80144-283">If both **IOPSLimit** and **IOPSReservation** are defined, the value of **IOPSLimit** must be greater than or equal to the value of **IOPSReservation**.</span></span>

> [!Note]  
> <span data-ttu-id="80144-284">Vous pouvez utiliser la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la [**classe \_ VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md) pour modifier la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="80144-284">You can use the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to modify the value of this property.</span></span> <span data-ttu-id="80144-285">Cette propriété est significative uniquement pour les instances **MSVM \_ StorageAllocationSettingData** qui demandent des allocations de ressources pour les ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="80144-285">This property is meaningful only for **Msvm\_StorageAllocationSettingData** instances that request resource allocations for virtual machines.</span></span> <span data-ttu-id="80144-286">Elle est ignorée lors de l’allocation de ressources à un pool enfant.</span><span class="sxs-lookup"><span data-stu-id="80144-286">It's ignored when allocating resources to a child pool.</span></span>

 

<span data-ttu-id="80144-287">**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="80144-287">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="80144-288">**Limite**</span><span class="sxs-lookup"><span data-stu-id="80144-288">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-289">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="80144-289">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="80144-290">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-291">Nombre maximal de blocs qui seront accordés pour cette allocation de ressources de stockage au niveau de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="80144-291">The maximum number of blocks that will be granted for this storage resource allocation at the host.</span></span> <span data-ttu-id="80144-292">La taille de bloc est spécifiée par la propriété **HostResourceBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="80144-292">The block size is specified by the **HostResourceBlockSize** property.</span></span> <span data-ttu-id="80144-293">En règle générale, la valeur de cette propriété reflète une taille maximale pour l’étendue de l’hôte alloué qui correspond à la taille de l’étendue de stockage virtuel présentée au consommateur.</span><span class="sxs-lookup"><span data-stu-id="80144-293">Usually the value of this property would reflect a maximum size for the allocated host extent that matches the size of the virtual storage extent presented to the consumer.</span></span> <span data-ttu-id="80144-294">Une valeur inférieure à celle-ci indique une situation dans laquelle une extension de stockage virtuel peu peuplé est attendue, où le taux de remplissage est limité par la valeur de la propriété Limit.</span><span class="sxs-lookup"><span data-stu-id="80144-294">A value less than that would indicate a situation where a sparsely populated virtual storage extent is expected, where the fill rate is limited by the value of the Limit property.</span></span> <span data-ttu-id="80144-295">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="80144-295">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="80144-296">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="80144-296">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-297">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="80144-297">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="80144-298">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-299">Spécifie comment cette ressource est mappée aux ressources sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="80144-299">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="80144-300">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="80144-300">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="80144-301">**OtherHostExtentNameFormat**</span><span class="sxs-lookup"><span data-stu-id="80144-301">**OtherHostExtentNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-302">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80144-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80144-303">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-304">Chaîne qui décrit le format de la propriété **HostExtentName** si la propriété **HostExtentNameFormat** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="80144-304">A string that describes the format of the **HostExtentName** property if the **HostExtentNameFormat** property is 1 (Other).</span></span> <span data-ttu-id="80144-305">Cette propriété est héritée de la **\_ StorageAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="80144-305">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="80144-306">**OtherHostExtentNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="80144-306">**OtherHostExtentNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-307">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80144-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80144-308">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-309">Chaîne qui décrit l’espace de noms de la propriété **HostExtentName** si la propriété **HostExtentNameNamespace** contient 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="80144-309">A string that describes the namespace of the **HostExtentName** property if the **HostExtentNameNamespace** property contains 1 (Other).</span></span> <span data-ttu-id="80144-310">Cette propriété est héritée de la **\_ StorageAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="80144-310">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="80144-311">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="80144-311">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-312">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80144-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80144-313">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-314">Chaîne qui décrit le type de ressource lorsqu’une valeur bien définie n’est pas disponible et que [**resourceType**](msvm-processorsettingdata.md) a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="80144-314">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="80144-315">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="80144-315">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="80144-316">**Parent**</span><span class="sxs-lookup"><span data-stu-id="80144-316">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-317">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80144-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80144-318">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-319">Parent de la ressource.</span><span class="sxs-lookup"><span data-stu-id="80144-319">The parent of the resource.</span></span> <span data-ttu-id="80144-320">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="80144-320">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="80144-321">**PersistentReservationsSupported**</span><span class="sxs-lookup"><span data-stu-id="80144-321">**PersistentReservationsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-322">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="80144-322">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80144-323">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-324">Indique si le disque dur virtuel prend en charge les réservations persistantes SCSI-3.</span><span class="sxs-lookup"><span data-stu-id="80144-324">Indicates whether the virtual hard disk supports SCSI-3 persistent reservations.</span></span>

<span data-ttu-id="80144-325">**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="80144-325">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="80144-326">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="80144-326">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-327">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80144-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80144-328">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-329">Identificateur du pool de ressources à partir duquel cette ressource a été allouée.</span><span class="sxs-lookup"><span data-stu-id="80144-329">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="80144-330">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="80144-330">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="80144-331">**Réservation**</span><span class="sxs-lookup"><span data-stu-id="80144-331">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-332">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="80144-332">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="80144-333">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80144-334">Qualificateurs : **override** ("reservation"), **ModelCorrespondence** ("CIM \_ StorageAllocationSettingData. HostResourceBlockSize")</span><span class="sxs-lookup"><span data-stu-id="80144-334">Qualifiers: **Override** ("Reservation"), **ModelCorrespondence** ("CIM\_StorageAllocationSettingData.HostResourceBlockSize")</span></span>
</dt> </dl>

<span data-ttu-id="80144-335">Nombre de blocs dont la disponibilité est garantie pour cette allocation de ressources de stockage au niveau de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="80144-335">The number of blocks that are guaranteed to be available for this storage resource allocation at the host.</span></span> <span data-ttu-id="80144-336">La taille de bloc est spécifiée par la propriété **HostResourceBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="80144-336">The block size is specified by the **HostResourceBlockSize** property.</span></span> <span data-ttu-id="80144-337">Cette propriété est héritée de la **\_ StorageAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="80144-337">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="80144-338">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="80144-338">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-339">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80144-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80144-340">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-341">Chaîne qui décrit un sous-type spécifique à l’implémentation pour cette ressource.</span><span class="sxs-lookup"><span data-stu-id="80144-341">A string that describes an implementation-specific subtype for this resource.</span></span> <span data-ttu-id="80144-342">Par exemple, cela peut être utilisé pour distinguer différents modèles du même type de ressource.</span><span class="sxs-lookup"><span data-stu-id="80144-342">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="80144-343">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="80144-343">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="80144-344">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="80144-344">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-345">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="80144-345">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="80144-346">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-347">Type de ressource représenté par ce paramètre d’allocation.</span><span class="sxs-lookup"><span data-stu-id="80144-347">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="80144-348">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="80144-348">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="80144-349"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="80144-349"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="80144-350"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Système informatique** (2)</span><span class="sxs-lookup"><span data-stu-id="80144-350"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="80144-351"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processeur** (3)</span><span class="sxs-lookup"><span data-stu-id="80144-351"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="80144-352"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Mémoire** (4)</span><span class="sxs-lookup"><span data-stu-id="80144-352"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="80144-353"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Contrôleur IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="80144-353"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="80144-354"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI parallèle** (6)</span><span class="sxs-lookup"><span data-stu-id="80144-354"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="80144-355"><span id="FC_HBA"></span><span id="fc_hba"></span>**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="80144-355"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="80144-356"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="80144-356"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="80144-357"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="80144-357"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="80144-358"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Carte Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="80144-358"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="80144-359"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Autre carte réseau** (11)</span><span class="sxs-lookup"><span data-stu-id="80144-359"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="80144-360"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Emplacement d’e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="80144-360"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="80144-361"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Périphérique d’e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="80144-361"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="80144-362"><span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Lecteur de disquette** (14)</span><span class="sxs-lookup"><span data-stu-id="80144-362"><span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Diskette Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="80144-363"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Lecteur de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="80144-363"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="80144-364"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Lecteur de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="80144-364"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="80144-365"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Lecteur de disque** (17)</span><span class="sxs-lookup"><span data-stu-id="80144-365"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Disk Drive** (17)</span></span>
</dt> <dt>

<span data-ttu-id="80144-366"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Lecteur de bande** (18)</span><span class="sxs-lookup"><span data-stu-id="80144-366"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Tape Drive** (18)</span></span>
</dt> <dt>

<span data-ttu-id="80144-367"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extension de stockage** (19)</span><span class="sxs-lookup"><span data-stu-id="80144-367"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (19)</span></span>
</dt> <dt>

<span data-ttu-id="80144-368"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Autre dispositif de stockage** (20)</span><span class="sxs-lookup"><span data-stu-id="80144-368"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other Storage Device** (20)</span></span>
</dt> <dt>

<span data-ttu-id="80144-369"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Port série** (21)</span><span class="sxs-lookup"><span data-stu-id="80144-369"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (21)</span></span>
</dt> <dt>

<span data-ttu-id="80144-370"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Port parallèle** (22)</span><span class="sxs-lookup"><span data-stu-id="80144-370"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (22)</span></span>
</dt> <dt>

<span data-ttu-id="80144-371"><span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Contrôleur USB** (23)</span><span class="sxs-lookup"><span data-stu-id="80144-371"><span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB controller** (23)</span></span>
</dt> <dt>

<span data-ttu-id="80144-372"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Contrôleur Graphics** (24)</span><span class="sxs-lookup"><span data-stu-id="80144-372"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (24)</span></span>
</dt> <dt>

<span data-ttu-id="80144-373"><span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**Contrôleur IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="80144-373"><span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="80144-374"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unité partitionnée** (26)</span><span class="sxs-lookup"><span data-stu-id="80144-374"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="80144-375"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unité partitionnée de base** (27)</span><span class="sxs-lookup"><span data-stu-id="80144-375"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="80144-376"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Alimentation (28** )</span><span class="sxs-lookup"><span data-stu-id="80144-376"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="80144-377"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Appareil de refroidissement** (29)</span><span class="sxs-lookup"><span data-stu-id="80144-377"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="80144-378"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Port commuté Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="80144-378"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet Switch Port** (30)</span></span>
</dt> <dt>

<span data-ttu-id="80144-379"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Disque logique** (31)</span><span class="sxs-lookup"><span data-stu-id="80144-379"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logical Disk** (31)</span></span>
</dt> <dt>

<span data-ttu-id="80144-380"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Volume de stockage** (32)</span><span class="sxs-lookup"><span data-stu-id="80144-380"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)</span></span>
</dt> <dt>

<span data-ttu-id="80144-381"><span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Connexion Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="80144-381"><span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet connection** (33)</span></span>
</dt> <dt>

<span data-ttu-id="80144-382"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (30 32767)</span><span class="sxs-lookup"><span data-stu-id="80144-382"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (30 32767)</span></span>
</dt> <dt>

<span data-ttu-id="80144-383"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="80144-383"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="80144-384">**SnapshotId**</span><span class="sxs-lookup"><span data-stu-id="80144-384">**SnapshotId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-385">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80144-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80144-386">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-386">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-387">GUID représentant la capture instantanée dans le fichier de définition de disque dur virtuel à attacher.</span><span class="sxs-lookup"><span data-stu-id="80144-387">A GUID representing which snapshot within the VHD Set file is to be attached.</span></span>

> [!Note]  
> <span data-ttu-id="80144-388">Ajouté dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="80144-388">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="80144-389">**StorageQoSPolicyID**</span><span class="sxs-lookup"><span data-stu-id="80144-389">**StorageQoSPolicyID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-390">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80144-390">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80144-391">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-392">Spécifie l’identificateur unique de la stratégie de qualité de service de stockage à appliquer à cette extension de stockage virtuel.</span><span class="sxs-lookup"><span data-stu-id="80144-392">Specifies the unique identifier of the Storage QoS Policy to be applied to this virtual storage extent.</span></span>

> [!Note]  
> <span data-ttu-id="80144-393">Ajouté dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="80144-393">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="80144-394">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="80144-394">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-395">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="80144-395">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="80144-396">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-397">Nombre de blocs présentés au consommateur.</span><span class="sxs-lookup"><span data-stu-id="80144-397">The number of blocks that are presented to the consumer.</span></span> <span data-ttu-id="80144-398">La taille de bloc est spécifiée par la propriété **VirtualResourceBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="80144-398">The block size is specified by the **VirtualResourceBlockSize** property.</span></span> <span data-ttu-id="80144-399">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="80144-399">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="80144-400">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="80144-400">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-401">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80144-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80144-402">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-403">Spécifie les unités utilisées par la propriété **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="80144-403">Specifies the units used by the **VirtualQuantity** property.</span></span> <span data-ttu-id="80144-404">Cette propriété est héritée de la **\_ StorageAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="80144-404">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>



| <span data-ttu-id="80144-405">Valeur</span><span class="sxs-lookup"><span data-stu-id="80144-405">Value</span></span>                                                                                                | <span data-ttu-id="80144-406">Signification</span><span class="sxs-lookup"><span data-stu-id="80144-406">Meaning</span></span>                                                                                    |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="80144-407"><dt>"Count (bloc de taille fixe)"</dt></span><span class="sxs-lookup"><span data-stu-id="80144-407"><dt>"count(fixed size block)"</dt></span></span> </dl> | <span data-ttu-id="80144-408">La taille de bloc fixe est contenue dans la propriété **VirtualResourceBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="80144-408">The fixed block size is contained in the **VirtualResourceBlockSize** property.</span></span><br/> |
| <dl> <span data-ttu-id="80144-409"><dt>poids</dt></span><span class="sxs-lookup"><span data-stu-id="80144-409"><dt>"byte"</dt></span></span> </dl>                    | <span data-ttu-id="80144-410">La propriété **VirtualQuantity** est mesurée en octets.</span><span class="sxs-lookup"><span data-stu-id="80144-410">The **VirtualQuantity** property is measured in bytes.</span></span><br/>                          |



 

</dd> <dt>

<span data-ttu-id="80144-411">**VirtualResourceBlockSize**</span><span class="sxs-lookup"><span data-stu-id="80144-411">**VirtualResourceBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-412">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="80144-412">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="80144-413">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-414">Taille, en octets, des blocs qui sont présentés au consommateur à la suite de cette demande d’allocation de ressources de stockage ou d’allocation de ressources de stockage.</span><span class="sxs-lookup"><span data-stu-id="80144-414">The size, in bytes, of the blocks that are presented to the consumer as the result of this storage resource allocation or storage resource allocation request.</span></span> <span data-ttu-id="80144-415">Si la taille de bloc est variable, la taille de bloc maximale, en octets, sera spécifiée.</span><span class="sxs-lookup"><span data-stu-id="80144-415">If the block size is variable, then the maximum block size, in bytes, will be specified.</span></span> <span data-ttu-id="80144-416">Si la taille de bloc est inconnue ou si aucun concept de bloc ne s’applique, la valeur 1 est utilisée.</span><span class="sxs-lookup"><span data-stu-id="80144-416">If the block size is unknown or if a block concept does not apply, then the value 1 will be used.</span></span> <span data-ttu-id="80144-417">Cette propriété est héritée de la **\_ StorageAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="80144-417">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="80144-418">**Poids**</span><span class="sxs-lookup"><span data-stu-id="80144-418">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-419">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="80144-419">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="80144-420">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-420">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80144-421">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Weight"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (10000)</span><span class="sxs-lookup"><span data-stu-id="80144-421">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Weight"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (10000)</span></span>
</dt> </dl>

<span data-ttu-id="80144-422">Spécifie une priorité relative pour cette allocation par rapport à d’autres allocations à partir du même pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="80144-422">Specifies a relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="80144-423">Cette propriété n’a aucune unité de mesure et est uniquement pertinente par rapport à d’autres allocations vying pour les mêmes ressources hôte.</span><span class="sxs-lookup"><span data-stu-id="80144-423">This property has no unit of measure and is only relevant when compared to other allocations vying for the same host resources.</span></span> <span data-ttu-id="80144-424">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="80144-424">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="80144-425">Plage : 1 10000</span><span class="sxs-lookup"><span data-stu-id="80144-425">Range: 1 10000</span></span>

</dd> <dt>

<span data-ttu-id="80144-426">**WriteHardeningMethod**</span><span class="sxs-lookup"><span data-stu-id="80144-426">**WriteHardeningMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80144-427">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="80144-427">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="80144-428">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80144-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80144-429">Indique quelle méthode de sécurisation renforcée d’écriture est prise en charge par le disque.</span><span class="sxs-lookup"><span data-stu-id="80144-429">Indicates what write hardening method is supported by the disk.</span></span>

> [!Note]  
> <span data-ttu-id="80144-430">Cette propriété a été ajoutée dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="80144-430">This property was added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="80144-431">**Valeur par défaut** (0)</span><span class="sxs-lookup"><span data-stu-id="80144-431">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="WriteCacheEnabled"></span><span id="writecacheenabled"></span><span id="WRITECACHEENABLED"></span>

<span data-ttu-id="80144-432">**WriteCacheEnabled** (1)</span><span class="sxs-lookup"><span data-stu-id="80144-432">**WriteCacheEnabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WriteCacheandFUAEnabled"></span><span id="writecacheandfuaenabled"></span><span id="WRITECACHEANDFUAENABLED"></span>

<span data-ttu-id="80144-433">**WriteCacheandFUAEnabled** (2)</span><span class="sxs-lookup"><span data-stu-id="80144-433">**WriteCacheandFUAEnabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WriteCacheDisabled"></span><span id="writecachedisabled"></span><span id="WRITECACHEDISABLED"></span>

<span data-ttu-id="80144-434">**WriteCacheDisabled** (3)</span><span class="sxs-lookup"><span data-stu-id="80144-434">**WriteCacheDisabled** (3)</span></span>


<span data-ttu-id="80144-435"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="80144-435"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="80144-436">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80144-436">Requirements</span></span>



| <span data-ttu-id="80144-437">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80144-437">Requirement</span></span> | <span data-ttu-id="80144-438">Valeur</span><span class="sxs-lookup"><span data-stu-id="80144-438">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80144-439">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80144-439">Minimum supported client</span></span><br/> | <span data-ttu-id="80144-440">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80144-440">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="80144-441">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80144-441">Minimum supported server</span></span><br/> | <span data-ttu-id="80144-442">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80144-442">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="80144-443">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="80144-443">Namespace</span></span><br/>                | <span data-ttu-id="80144-444">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="80144-444">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="80144-445">MOF</span><span class="sxs-lookup"><span data-stu-id="80144-445">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80144-446"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="80144-446"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="80144-447">DLL</span><span class="sxs-lookup"><span data-stu-id="80144-447">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80144-448"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="80144-448"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

