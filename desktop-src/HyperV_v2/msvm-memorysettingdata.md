---
description: Représente l’état configuré de la mémoire pour un ordinateur virtuel.
ms.assetid: 4B6FEE50-1C5F-4F41-B14A-E10B40400A1B
title: Classe Msvm_MemorySettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MemorySettingData
- Msvm_MemorySettingData.InstanceID
- Msvm_MemorySettingData.Caption
- Msvm_MemorySettingData.Description
- Msvm_MemorySettingData.ElementName
- Msvm_MemorySettingData.ResourceType
- Msvm_MemorySettingData.OtherResourceType
- Msvm_MemorySettingData.ResourceSubType
- Msvm_MemorySettingData.PoolID
- Msvm_MemorySettingData.ConsumerVisibility
- Msvm_MemorySettingData.HostResource
- Msvm_MemorySettingData.HugePagesEnabled
- Msvm_MemorySettingData.AllocationUnits
- Msvm_MemorySettingData.VirtualQuantity
- Msvm_MemorySettingData.Reservation
- Msvm_MemorySettingData.Limit
- Msvm_MemorySettingData.Weight
- Msvm_MemorySettingData.AutomaticAllocation
- Msvm_MemorySettingData.AutomaticDeallocation
- Msvm_MemorySettingData.Parent
- Msvm_MemorySettingData.Connection
- Msvm_MemorySettingData.Address
- Msvm_MemorySettingData.MappingBehavior
- Msvm_MemorySettingData.AddressOnParent
- Msvm_MemorySettingData.VirtualQuantityUnits
- Msvm_MemorySettingData.DynamicMemoryEnabled
- Msvm_MemorySettingData.TargetMemoryBuffer
- Msvm_MemorySettingData.IsVirtualized
- Msvm_MemorySettingData.SwapFilesInUse
- Msvm_MemorySettingData.MaxMemoryBlocksPerNumaNode
- Msvm_MemorySettingData.SgxSize
- Msvm_MemorySettingData.SgxEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 47309fead7ee45936f34e1e4286ee94437823df7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951924"
---
# <a name="msvm_memorysettingdata-class"></a><span data-ttu-id="de6f0-103">MSVM \_ MemorySettingData, classe</span><span class="sxs-lookup"><span data-stu-id="de6f0-103">Msvm\_MemorySettingData class</span></span>

<span data-ttu-id="de6f0-104">Représente l’état configuré de la mémoire pour un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="de6f0-104">Represents the configured state of the memory for a virtual machine.</span></span>

<span data-ttu-id="de6f0-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="de6f0-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="de6f0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de6f0-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MemorySettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Memory Default Settings";
  string  Description = "Describes the default settings for the memory resources.";
  string  ElementName;
  uint16  ResourceType = 4;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Memory";
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  boolean HugePagesEnabled;
  string  AllocationUnits = "byte * 2^20";
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "byte * 2^20";
  boolean DynamicMemoryEnabled;
  uint32  TargetMemoryBuffer;
  boolean IsVirtualized = True;
  boolean SwapFilesInUse;
  uint64  MaxMemoryBlocksPerNumaNode;
  uint64  SgxSize;
  boolean SgxEnabled;
};
```

## <a name="members"></a><span data-ttu-id="de6f0-107">Membres</span><span class="sxs-lookup"><span data-stu-id="de6f0-107">Members</span></span>

<span data-ttu-id="de6f0-108">La classe **MSVM \_ MemorySettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="de6f0-108">The **Msvm\_MemorySettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="de6f0-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="de6f0-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="de6f0-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="de6f0-110">Properties</span></span>

<span data-ttu-id="de6f0-111">La classe **MSVM \_ MemorySettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="de6f0-111">The **Msvm\_MemorySettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="de6f0-112">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="de6f0-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="de6f0-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-115">Adresse de la ressource.</span><span class="sxs-lookup"><span data-stu-id="de6f0-115">The address of the resource.</span></span> <span data-ttu-id="de6f0-116">Par exemple, l’adresse MAC d’un port Ethernet.</span><span class="sxs-lookup"><span data-stu-id="de6f0-116">For example, the MAC address of an Ethernet port.</span></span> <span data-ttu-id="de6f0-117">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="de6f0-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="de6f0-118">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="de6f0-118">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="de6f0-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-121">Décrit l’adresse de cette ressource dans le contexte du parent.</span><span class="sxs-lookup"><span data-stu-id="de6f0-121">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="de6f0-122">Les propriétés **parent** et **AddressOnParent** sont utilisées pour décrire la relation du contrôleur, ainsi que l’ordre des appareils sur un contrôleur.</span><span class="sxs-lookup"><span data-stu-id="de6f0-122">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="de6f0-123">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="de6f0-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="de6f0-124">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="de6f0-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="de6f0-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-127">Unités d’allocation utilisées par la **réservation** et les propriétés de la **limite** .</span><span class="sxs-lookup"><span data-stu-id="de6f0-127">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="de6f0-128">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="de6f0-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="de6f0-129">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="de6f0-129">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-130">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="de6f0-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-132">Indique si la ressource sera automatiquement allouée.</span><span class="sxs-lookup"><span data-stu-id="de6f0-132">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="de6f0-133">Par exemple, lorsque cette propriété a la valeur **true** et que la machine virtuelle consommatrice est sous tension, cette ressource sera allouée.</span><span class="sxs-lookup"><span data-stu-id="de6f0-133">For example, when this property is set to **True** and the consuming virtual machine is powered on, this resource would be allocated.</span></span> <span data-ttu-id="de6f0-134">La valeur **false** indique que la ressource doit être allouée de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="de6f0-134">A value of **False** indicates the resource must be explicitly allocated.</span></span> <span data-ttu-id="de6f0-135">Par exemple, le paramètre peut représenter un support amovible (tel qu’un CD-ROM ou une disquette) où le média n’est pas présent au démarrage.</span><span class="sxs-lookup"><span data-stu-id="de6f0-135">For example, the setting may represent removable media (such as a CD-ROM or a floppy disk) where at startup, the media is not present.</span></span> <span data-ttu-id="de6f0-136">Une opération explicite est requise pour allouer la ressource.</span><span class="sxs-lookup"><span data-stu-id="de6f0-136">An explicit operation is required to allocate the resource.</span></span> <span data-ttu-id="de6f0-137">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="de6f0-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="de6f0-138">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="de6f0-138">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-139">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="de6f0-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-141">Indique si la ressource sera automatiquement allouée.</span><span class="sxs-lookup"><span data-stu-id="de6f0-141">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="de6f0-142">Par exemple, lorsque cette propriété a la valeur **true** et que la machine virtuelle consommatrice est sous tension, cette ressource sera allouée.</span><span class="sxs-lookup"><span data-stu-id="de6f0-142">For example when this property is set to **True** and the consuming virtual machine is powered on, this resource would be allocated.</span></span> <span data-ttu-id="de6f0-143">Lorsque cette propriété a la **valeur false**, la ressource doit être allouée explicitement.</span><span class="sxs-lookup"><span data-stu-id="de6f0-143">When this property is **False**, the resource must be explicitly allocated.</span></span> <span data-ttu-id="de6f0-144">Par exemple, le paramètre peut représenter un support amovible (tel qu’un CD-ROM ou une disquette) où le média n’est pas présent au démarrage.</span><span class="sxs-lookup"><span data-stu-id="de6f0-144">For example, the setting may represent removable media (such as a CD-ROM or a floppy disk) where at startup, the media is not present.</span></span> <span data-ttu-id="de6f0-145">Une opération explicite est requise pour allouer la ressource.</span><span class="sxs-lookup"><span data-stu-id="de6f0-145">An explicit operation is required to allocate the resource.</span></span> <span data-ttu-id="de6f0-146">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="de6f0-146">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="de6f0-147">**Caption**</span><span class="sxs-lookup"><span data-stu-id="de6f0-147">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-148">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="de6f0-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-150">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="de6f0-150">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-151">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="de6f0-151">A short description of the object.</span></span> <span data-ttu-id="de6f0-152">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="de6f0-152">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="de6f0-153">**Connection**</span><span class="sxs-lookup"><span data-stu-id="de6f0-153">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-154">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="de6f0-154">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-156">Appareil auquel cette ressource est connectée.</span><span class="sxs-lookup"><span data-stu-id="de6f0-156">The device to which this resource is connected.</span></span> <span data-ttu-id="de6f0-157">Par exemple, un réseau nommé ou un port commuté.</span><span class="sxs-lookup"><span data-stu-id="de6f0-157">For example, a named network or switch port.</span></span> <span data-ttu-id="de6f0-158">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="de6f0-158">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="de6f0-159">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="de6f0-159">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-160">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="de6f0-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-162">Décrit la visibilité des consommateurs sur la ressource allouée.</span><span class="sxs-lookup"><span data-stu-id="de6f0-162">Describes the consumers visibility to the allocated resource.</span></span> <span data-ttu-id="de6f0-163">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="de6f0-163">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="de6f0-164">**Description**</span><span class="sxs-lookup"><span data-stu-id="de6f0-164">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-165">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="de6f0-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-167">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="de6f0-167">A description of the object.</span></span> <span data-ttu-id="de6f0-168">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="de6f0-168">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="de6f0-169">**DynamicMemoryEnabled**</span><span class="sxs-lookup"><span data-stu-id="de6f0-169">**DynamicMemoryEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-170">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="de6f0-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-172">Indique si la mémoire dynamique est activée pour l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="de6f0-172">Indicates whether dynamic memory is enabled for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="de6f0-173">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="de6f0-173">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="de6f0-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-176">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="de6f0-176">A display name for the object.</span></span> <span data-ttu-id="de6f0-177">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="de6f0-177">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="de6f0-178">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="de6f0-178">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-179">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="de6f0-179">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-181">Le premier élément de ce tableau contient une référence à la ressource hôte sous-jacente à assigner.</span><span class="sxs-lookup"><span data-stu-id="de6f0-181">The first element of this array contains a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="de6f0-182">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="de6f0-182">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), but it is not used.</span></span>

</dd> <dt>
  
<span data-ttu-id="de6f0-183">**HugePagesEnabled**</span><span class="sxs-lookup"><span data-stu-id="de6f0-183">**HugePagesEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-184">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="de6f0-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-186">Indique si la mémoire est sauvegardée par 1 Go de pages ou non.</span><span class="sxs-lookup"><span data-stu-id="de6f0-186">Whether the memory is backed by 1GB pages or not.</span></span>

</dd> <dt>

<span data-ttu-id="de6f0-187">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="de6f0-187">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-188">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="de6f0-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-190">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="de6f0-190">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-191">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="de6f0-191">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="de6f0-192">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="de6f0-192">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="de6f0-193">**IsVirtualized**</span><span class="sxs-lookup"><span data-stu-id="de6f0-193">**IsVirtualized**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-194">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="de6f0-194">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-196">Indique si cet appareil est virtualisé ou transmis.</span><span class="sxs-lookup"><span data-stu-id="de6f0-196">Indicates whether this device is virtualized or passed through.</span></span> <span data-ttu-id="de6f0-197">Quand la valeur est **false**, la ressource hôte ou sous-jacente est utilisée.</span><span class="sxs-lookup"><span data-stu-id="de6f0-197">When set to **False**, the underlying or host resource is used.</span></span> <span data-ttu-id="de6f0-198">Au moins un élément doit être présent dans la propriété **DeviceID** .</span><span class="sxs-lookup"><span data-stu-id="de6f0-198">At least one item should be present in the **DeviceID** property.</span></span> <span data-ttu-id="de6f0-199">Quand la valeur est **true**, la ressource est virtualisée et peut ne pas être mappée directement à une ressource hôte/sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="de6f0-199">When set to **True**, the resource is virtualized and may not map directly to an underlying/host resource.</span></span> <span data-ttu-id="de6f0-200">Certaines implémentations peuvent prendre en charge une attribution spécifique pour les ressources virtualisées, auquel cas les ressources hôtes sont exposées à l’aide de la propriété **DeviceID** .</span><span class="sxs-lookup"><span data-stu-id="de6f0-200">Some implementations may support specific assignment for virtualized resources, in which case the host resources are exposed by using the **DeviceID** property.</span></span> <span data-ttu-id="de6f0-201">Cette propriété a toujours la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="de6f0-201">This property is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="de6f0-202">**Limite**</span><span class="sxs-lookup"><span data-stu-id="de6f0-202">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-203">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="de6f0-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-205">Quantité maximale de mémoire qui peut être consommée par l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="de6f0-205">The maximum amount of memory that may be consumed by the virtual machine.</span></span> <span data-ttu-id="de6f0-206">Pour un ordinateur virtuel pour lequel la mémoire dynamique est activée, il s’agit du paramètre de mémoire maximale.</span><span class="sxs-lookup"><span data-stu-id="de6f0-206">For a virtual machine with dynamic memory enabled, this represents the maximum memory setting.</span></span> <span data-ttu-id="de6f0-207">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="de6f0-207">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="de6f0-208">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="de6f0-208">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-209">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="de6f0-209">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-210">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-211">Spécifie comment cette ressource est mappée aux ressources sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="de6f0-211">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="de6f0-212">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="de6f0-212">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="de6f0-213">**MaxMemoryBlocksPerNumaNode**</span><span class="sxs-lookup"><span data-stu-id="de6f0-213">**MaxMemoryBlocksPerNumaNode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-214">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="de6f0-214">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-216">Quantité maximale de mémoire qui peut être observée dans l’ordinateur virtuel comme appartenant à un seul nœud NUMA.</span><span class="sxs-lookup"><span data-stu-id="de6f0-216">The maximum amount of memory that can be observed within the virtual machine as belonging to a single NUMA node.</span></span>

</dd> <dt>

<span data-ttu-id="de6f0-217">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="de6f0-217">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-218">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="de6f0-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-219">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-220">Chaîne qui décrit le type de ressource lorsqu’une valeur bien définie n’est pas disponible et que **resourceType** a la valeur « other ».</span><span class="sxs-lookup"><span data-stu-id="de6f0-220">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value "Other".</span></span> <span data-ttu-id="de6f0-221">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="de6f0-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="de6f0-222">**Parent**</span><span class="sxs-lookup"><span data-stu-id="de6f0-222">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-223">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="de6f0-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-225">Parent de la ressource.</span><span class="sxs-lookup"><span data-stu-id="de6f0-225">The parent of the resource.</span></span> <span data-ttu-id="de6f0-226">Par exemple, un contrôleur pour l’allocation actuelle.</span><span class="sxs-lookup"><span data-stu-id="de6f0-226">For example, a controller for the current allocation.</span></span> <span data-ttu-id="de6f0-227">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="de6f0-227">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="de6f0-228">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="de6f0-228">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-229">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="de6f0-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-230">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-231">Identificateur du pool de ressources à partir duquel cette ressource a été allouée.</span><span class="sxs-lookup"><span data-stu-id="de6f0-231">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="de6f0-232">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="de6f0-232">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="de6f0-233">**Réservation**</span><span class="sxs-lookup"><span data-stu-id="de6f0-233">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-234">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="de6f0-234">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-235">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-236">Spécifie la quantité de mémoire dont la disponibilité est garantie pour cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="de6f0-236">Specifies the amount of memory guaranteed to be available for this virtual machine.</span></span> <span data-ttu-id="de6f0-237">Pour un ordinateur virtuel pour lequel la mémoire dynamique est activée, il s’agit du paramètre de mémoire minimal.</span><span class="sxs-lookup"><span data-stu-id="de6f0-237">For a virtual machine with dynamic memory enabled, this represents the minimum memory setting.</span></span> <span data-ttu-id="de6f0-238">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="de6f0-238">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="de6f0-239">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="de6f0-239">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-240">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="de6f0-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-241">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-242">Chaîne qui décrit un sous-type spécifique à l’implémentation pour cette ressource.</span><span class="sxs-lookup"><span data-stu-id="de6f0-242">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="de6f0-243">Par exemple, cela peut être utilisé pour distinguer différents modèles du même type de ressource.</span><span class="sxs-lookup"><span data-stu-id="de6f0-243">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="de6f0-244">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="de6f0-244">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="de6f0-245">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="de6f0-245">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-246">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="de6f0-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-247">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-248">Type de ressource représenté par ce paramètre d’allocation.</span><span class="sxs-lookup"><span data-stu-id="de6f0-248">The type of resource that this allocation setting represents.</span></span> <span data-ttu-id="de6f0-249">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)et est toujours définie sur 4 (mémoire).</span><span class="sxs-lookup"><span data-stu-id="de6f0-249">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 4 (Memory).</span></span>

</dd> <dt>

<span data-ttu-id="de6f0-250">**SgxEnabled**</span><span class="sxs-lookup"><span data-stu-id="de6f0-250">**SgxEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-251">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="de6f0-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-252">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-253">Indique si la messagerie SGX est activée.</span><span class="sxs-lookup"><span data-stu-id="de6f0-253">Indicates if SGX is enabled.</span></span>

> [!Note]  
> <span data-ttu-id="de6f0-254">Cette propriété a été ajoutée dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="de6f0-254">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="de6f0-255">**SgxSize**</span><span class="sxs-lookup"><span data-stu-id="de6f0-255">**SgxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-256">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="de6f0-256">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-257">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-258">Quantité de mémoire SGX à allouer pour la machine virtuelle, en Mo.</span><span class="sxs-lookup"><span data-stu-id="de6f0-258">The amount of SGX memory to allocate for the VM, in MB.</span></span>

> [!Note]  
> <span data-ttu-id="de6f0-259">Cette propriété a été ajoutée dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="de6f0-259">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="de6f0-260">**SwapFilesInUse**</span><span class="sxs-lookup"><span data-stu-id="de6f0-260">**SwapFilesInUse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-261">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="de6f0-261">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-262">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-263">**True** si la pagination de second niveau est active ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="de6f0-263">**True** if second level paging is active; otherwise, **False**.</span></span>

</dd> <dt>

<span data-ttu-id="de6f0-264">**TargetMemoryBuffer**</span><span class="sxs-lookup"><span data-stu-id="de6f0-264">**TargetMemoryBuffer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-265">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="de6f0-265">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-266">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-267">Définit la quantité de mémoire supplémentaire qui doit être réservée pour un ordinateur virtuel au moment de l’exécution, sous la forme d’un pourcentage de la mémoire totale dont l’ordinateur virtuel a besoin.</span><span class="sxs-lookup"><span data-stu-id="de6f0-267">Defines the amount of extra memory that should be reserved for a virtual machine at runtime, as a percentage of the total memory that the virtual machine is thought to need.</span></span> <span data-ttu-id="de6f0-268">Cela s’applique uniquement aux machines virtuelles pour lesquelles la mémoire dynamique est activée.</span><span class="sxs-lookup"><span data-stu-id="de6f0-268">This only applies to virtual machines with dynamic memory enabled.</span></span>

<span data-ttu-id="de6f0-269">Cette propriété peut être comprise entre 5 et 2000.</span><span class="sxs-lookup"><span data-stu-id="de6f0-269">This property can be in the range of 5 to 2000.</span></span>

</dd> <dt>

<span data-ttu-id="de6f0-270">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="de6f0-270">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-271">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="de6f0-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-272">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-273">Quantité totale de mémoire vive (RAM) de l’ordinateur virtuel, comme indiqué par le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="de6f0-273">The total amount of RAM in the virtual machine, as seen by the guest operating system.</span></span> <span data-ttu-id="de6f0-274">Pour un ordinateur virtuel pour lequel la mémoire dynamique est activée, il s’agit de la mémoire initiale disponible au démarrage.</span><span class="sxs-lookup"><span data-stu-id="de6f0-274">For a virtual machine with dynamic memory enabled, this represents the initial memory available at startup.</span></span> <span data-ttu-id="de6f0-275">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="de6f0-275">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="de6f0-276">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="de6f0-276">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-277">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="de6f0-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-278">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-279">Spécifie l’unité de mesure pour cette allocation de ressources.</span><span class="sxs-lookup"><span data-stu-id="de6f0-279">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="de6f0-280">La valeur de cette propriété doit être une valeur légale du qualificateur d’unités de programmation, tel que défini dans l’annexe C. 1 de DSP0004 V 2.5 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="de6f0-280">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="de6f0-281">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="de6f0-281">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="de6f0-282">**Poids**</span><span class="sxs-lookup"><span data-stu-id="de6f0-282">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6f0-283">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="de6f0-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="de6f0-284">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6f0-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6f0-285">Définit la valeur de pondération de l’allocation de mémoire pour chaque ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="de6f0-285">Defines the memory allocation weighting value for each virtual machine.</span></span> <span data-ttu-id="de6f0-286">Une fois toutes les réserves remplies, la mémoire restante de la plateforme d’hébergement sera allouée aux ordinateurs virtuels en fonction de leurs pondérations relatives (sans dépasser la valeur spécifiée par la propriété **Limit** ).</span><span class="sxs-lookup"><span data-stu-id="de6f0-286">After all reserves have been met, the remaining memory of the hosting platform will be allocated to virtual machines based on their relative weights (not to exceed the value specified by the **Limit** property).</span></span> <span data-ttu-id="de6f0-287">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="de6f0-287">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de6f0-288">Notes</span><span class="sxs-lookup"><span data-stu-id="de6f0-288">Remarks</span></span>

<span data-ttu-id="de6f0-289">L’accès à la classe **MSVM \_ MemorySettingData** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="de6f0-289">Access to the **Msvm\_MemorySettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="de6f0-290">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="de6f0-290">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="de6f0-291">Exemples</span><span class="sxs-lookup"><span data-stu-id="de6f0-291">Examples</span></span>

```powershell
function WaitForResult
{
  param($result)
  if ($result.ReturnValue -eq 4096)
  {
    while($true)
    {
      $result.Job
      if ($result.Job -ne $null)
      {
        if ($result.Job.JobState -gt 4)
        {
          return $result.Job.ErrorCode
        }
      }
      start-sleep 1
    }
  }
  else
  {
    return $result.ReturnValue
  }
}

if ($($args.count) -ne 2)
{
  Write-Host "EnableHugePages.ps1 VMName SizeInMB"
  return
}

$vmName = $args[0]
$sizeInMB = $args[1]
 
$namespace = "root\virtualization\v2"
$vm = Get-WmiObject -class MSVM_ComputerSystem -filter "ElementName='$vmName'" -namespace $namespace
$settings = Get-WmiObject -query "Associators of {$vm} where ResultClass = Msvm_VirtualSystemSettingData" -namespace $namespace
$vmSettings = $settings | ? VirtualSystemType -eq "Microsoft:Hyper-V:System:Realized"
$memorySettings = Get-WmiObject -query "Associators of {$vmSettings} where ResultClass = Msvm_MemorySettingData" -namespace $namespace

$memorySettings.MaxMemoryBlocksPerNumaNode = $sizeInMB
$memorySettings.Reservation = $sizeInMB
$memorySettings.Limit = $sizeInMB
$memorySettings.VirtualQuantity = $sizeInMB
$memorySettings.HugePagesEnabled = $True

$vmSvc = Get-WmiObject -class Msvm_VirtualSystemManagementService -namespace $namespace
$res = $vmSvc.ModifyResourceSettings($memorySettings.GetText(2))
if (WaitForResult($res) -ne 0)
{
  Write-Host "Failed."
}
```

## <a name="requirements"></a><span data-ttu-id="de6f0-292">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de6f0-292">Requirements</span></span>



| <span data-ttu-id="de6f0-293">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de6f0-293">Requirement</span></span> | <span data-ttu-id="de6f0-294">Valeur</span><span class="sxs-lookup"><span data-stu-id="de6f0-294">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de6f0-295">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de6f0-295">Minimum supported client</span></span><br/> | <span data-ttu-id="de6f0-296">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="de6f0-296">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="de6f0-297">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de6f0-297">Minimum supported server</span></span><br/> | <span data-ttu-id="de6f0-298">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="de6f0-298">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="de6f0-299">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="de6f0-299">Namespace</span></span><br/>                | <span data-ttu-id="de6f0-300">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="de6f0-300">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="de6f0-301">MOF</span><span class="sxs-lookup"><span data-stu-id="de6f0-301">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de6f0-302"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="de6f0-302"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="de6f0-303">DLL</span><span class="sxs-lookup"><span data-stu-id="de6f0-303">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de6f0-304"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="de6f0-304"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="de6f0-305">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de6f0-305">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de6f0-306">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="de6f0-306">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="de6f0-307">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="de6f0-307">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="de6f0-308">Classes de mémoire</span><span class="sxs-lookup"><span data-stu-id="de6f0-308">Memory Classes</span></span>](memory-classes.md)
</dt> </dl>

 

