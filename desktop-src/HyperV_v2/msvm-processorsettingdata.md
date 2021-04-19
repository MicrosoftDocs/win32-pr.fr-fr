---
description: Représente les paramètres de processeur virtuel pour un ordinateur virtuel.
ms.assetid: 2B299793-E1CD-49D4-898C-AE60B49F44F5
title: Classe Msvm_ProcessorSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProcessorSettingData
- Msvm_ProcessorSettingData.InstanceID
- Msvm_ProcessorSettingData.Caption
- Msvm_ProcessorSettingData.Description
- Msvm_ProcessorSettingData.ElementName
- Msvm_ProcessorSettingData.ResourceType
- Msvm_ProcessorSettingData.OtherResourceType
- Msvm_ProcessorSettingData.ResourceSubType
- Msvm_ProcessorSettingData.PoolID
- Msvm_ProcessorSettingData.ConsumerVisibility
- Msvm_ProcessorSettingData.HostResource
- Msvm_ProcessorSettingData.AllocationUnits
- Msvm_ProcessorSettingData.VirtualQuantity
- Msvm_ProcessorSettingData.Reservation
- Msvm_ProcessorSettingData.Limit
- Msvm_ProcessorSettingData.Weight
- Msvm_ProcessorSettingData.AutomaticAllocation
- Msvm_ProcessorSettingData.AutomaticDeallocation
- Msvm_ProcessorSettingData.Parent
- Msvm_ProcessorSettingData.Connection
- Msvm_ProcessorSettingData.Address
- Msvm_ProcessorSettingData.MappingBehavior
- Msvm_ProcessorSettingData.AddressOnParent
- Msvm_ProcessorSettingData.VirtualQuantityUnits
- Msvm_ProcessorSettingData.LimitCPUID
- Msvm_ProcessorSettingData.HwThreadsPerCore
- Msvm_ProcessorSettingData.LimitProcessorFeatures
- Msvm_ProcessorSettingData.MaxProcessorsPerNumaNode
- Msvm_ProcessorSettingData.MaxNumaNodesPerSocket
- Msvm_ProcessorSettingData.EnableHostResourceProtection
- Msvm_ProcessorSettingData.CpuGroupId
- Msvm_ProcessorSettingData.HideHypervisorPresent
- Msvm_ProcessorSettingData.ExposeVirtualizationExtensions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5154105c4deab13f93bb65078a5c9527283620e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544892"
---
# <a name="msvm_processorsettingdata-class"></a><span data-ttu-id="557d4-103">MSVM \_ ProcessorSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="557d4-103">Msvm\_ProcessorSettingData class</span></span>

<span data-ttu-id="557d4-104">Représente les paramètres de processeur virtuel pour un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="557d4-104">Represents the virtual processor settings for a virtual machine.</span></span>

<span data-ttu-id="557d4-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="557d4-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="557d4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="557d4-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ProcessorSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Processor";
  string  Description = "A logical processor of the hypervisor running on the host computer system.";
  string  ElementName;
  uint16  ResourceType = 3;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Processor";
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits = "percent / 1000";
  uint64  VirtualQuantity = "count";
  uint64  Reservation = 0;
  uint64  Limit = 100000;
  uint32  Weight = 100;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  boolean LimitCPUID;
  uint64  HwThreadsPerCore;
  boolean LimitProcessorFeatures;
  uint64  MaxProcessorsPerNumaNode;
  uint64  MaxNumaNodesPerSocket;
  boolean EnableHostResourceProtection;
  string  CpuGroupId;
  boolean HideHypervisorPresent;
  boolean ExposeVirtualizationExtensions;
};
```

## <a name="members"></a><span data-ttu-id="557d4-107">Membres</span><span class="sxs-lookup"><span data-stu-id="557d4-107">Members</span></span>

<span data-ttu-id="557d4-108">La classe **MSVM \_ ProcessorSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="557d4-108">The **Msvm\_ProcessorSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="557d4-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="557d4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="557d4-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="557d4-110">Properties</span></span>

<span data-ttu-id="557d4-111">La classe **MSVM \_ ProcessorSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="557d4-111">The **Msvm\_ProcessorSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="557d4-112">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="557d4-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="557d4-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-115">Adresse de la ressource.</span><span class="sxs-lookup"><span data-stu-id="557d4-115">The address of the resource.</span></span> <span data-ttu-id="557d4-116">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="557d4-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="557d4-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="557d4-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="557d4-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-120">Décrit l’adresse de cette ressource dans le contexte du parent.</span><span class="sxs-lookup"><span data-stu-id="557d4-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="557d4-121">Les propriétés **parent** et **AddressOnParent** sont utilisées pour décrire la relation du contrôleur, ainsi que l’ordre des appareils sur un contrôleur.</span><span class="sxs-lookup"><span data-stu-id="557d4-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="557d4-122">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="557d4-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="557d4-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="557d4-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="557d4-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-126">Unités d’allocation utilisées par la **réservation** et les propriétés de la **limite** .</span><span class="sxs-lookup"><span data-stu-id="557d4-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="557d4-127">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="557d4-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="557d4-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="557d4-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-129">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="557d4-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-131">Indique si la ressource sera automatiquement allouée.</span><span class="sxs-lookup"><span data-stu-id="557d4-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="557d4-132">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="557d4-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="557d4-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="557d4-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-134">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="557d4-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-136">Indique si la ressource sera automatiquement désallouée.</span><span class="sxs-lookup"><span data-stu-id="557d4-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="557d4-137">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="557d4-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="557d4-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="557d4-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="557d4-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="557d4-141">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="557d4-141">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="557d4-142">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="557d4-142">A short description of the object.</span></span> <span data-ttu-id="557d4-143">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="557d4-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="557d4-144">**Connection**</span><span class="sxs-lookup"><span data-stu-id="557d4-144">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-145">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="557d4-145">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="557d4-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-147">Appareil auquel cette ressource est connectée.</span><span class="sxs-lookup"><span data-stu-id="557d4-147">The device to which this resource is connected.</span></span> <span data-ttu-id="557d4-148">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="557d4-148">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="557d4-149">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="557d4-149">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-150">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="557d4-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-152">Décrit la visibilité du consommateur sur la ressource allouée.</span><span class="sxs-lookup"><span data-stu-id="557d4-152">Describes the consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="557d4-153">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="557d4-153">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="557d4-154">**CpuGroupId**</span><span class="sxs-lookup"><span data-stu-id="557d4-154">**CpuGroupId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="557d4-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-157">ID du groupe de processeurs auquel cette machine virtuelle est liée.</span><span class="sxs-lookup"><span data-stu-id="557d4-157">The Cpu Group Id this VM is bound to.</span></span> <span data-ttu-id="557d4-158">Lorsque la valeur est 0, cela signifie qu’elle n’est pas liée à un groupe de PROCESSEURs spécifique.</span><span class="sxs-lookup"><span data-stu-id="557d4-158">When value is 0 it means is not bound to a specific CPU group.</span></span>

> [!Note]  
> <span data-ttu-id="557d4-159">Cette propriété a été ajoutée dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="557d4-159">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="557d4-160">**Description**</span><span class="sxs-lookup"><span data-stu-id="557d4-160">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="557d4-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-163">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="557d4-163">A description of the object.</span></span> <span data-ttu-id="557d4-164">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="557d4-164">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="557d4-165">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="557d4-165">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-166">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="557d4-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-168">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="557d4-168">A display name for the object.</span></span> <span data-ttu-id="557d4-169">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="557d4-169">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="557d4-170">La modification de cette propriété modifie le **ElementName** du dérivé de l’appareil logique associé.</span><span class="sxs-lookup"><span data-stu-id="557d4-170">Changing this property will change the **ElementName** of the associated logical device derivative.</span></span>

</dd> <dt>

<span data-ttu-id="557d4-171">**EnableHostResourceProtection**</span><span class="sxs-lookup"><span data-stu-id="557d4-171">**EnableHostResourceProtection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-172">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="557d4-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-174">Indique si la machine virtuelle doit activer les fonctionnalités qui augmentent la protection des ressources de l’hôte de la charge de travail en cours d’exécution dans la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="557d4-174">Indicates whether the VM should enable features that increase the protection of host resources from workload running in the VM.</span></span>

> [!Note]  
> <span data-ttu-id="557d4-175">Ajouté dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="557d4-175">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="557d4-176">**ExposeVirtualizationExtensions**</span><span class="sxs-lookup"><span data-stu-id="557d4-176">**ExposeVirtualizationExtensions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-177">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="557d4-177">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-179">Indique si Hyper-V doit exposer les extensions de virtualisation de matériel virtualisées à la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="557d4-179">Indicates whether Hyper-V should expose virtualized hardware virtualization extensions to the VM.</span></span>

> [!Note]  
> <span data-ttu-id="557d4-180">Cette propriété a été ajoutée dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="557d4-180">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="557d4-181">**HideHypervisorPresent**</span><span class="sxs-lookup"><span data-stu-id="557d4-181">**HideHypervisorPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-182">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="557d4-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-184">Indique si Hyper-V doit signaler qu’un hyperviseur est présent à l’invité imbriqué.</span><span class="sxs-lookup"><span data-stu-id="557d4-184">Indicates whether Hyper-V should report that a hypervisor is present to the nested guest.</span></span>

> [!Note]  
> <span data-ttu-id="557d4-185">Cette propriété a été ajoutée dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="557d4-185">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="557d4-186">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="557d4-186">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-187">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="557d4-187">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="557d4-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-189">Expose une attribution spécifique à l’hôte ou aux ressources sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="557d4-189">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="557d4-190">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="557d4-190">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="557d4-191">**HwThreadsPerCore**</span><span class="sxs-lookup"><span data-stu-id="557d4-191">**HwThreadsPerCore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-192">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="557d4-192">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-194">Indique le nombre de threads SMT par cœur signalés à l’invité.</span><span class="sxs-lookup"><span data-stu-id="557d4-194">Indicates the number of SMT threads per core reported to the guest.</span></span> <span data-ttu-id="557d4-195">Ce rapport est indépendant du fait que le matériel pour SMT est présent.</span><span class="sxs-lookup"><span data-stu-id="557d4-195">This reporting is independent of whether the hardware for SMT is present.</span></span>

> [!Note]  
> <span data-ttu-id="557d4-196">Cette propriété a été ajoutée dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="557d4-196">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="557d4-197">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="557d4-197">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-198">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="557d4-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="557d4-200">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="557d4-200">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="557d4-201">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="557d4-201">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="557d4-202">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="557d4-202">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="557d4-203">**Limite**</span><span class="sxs-lookup"><span data-stu-id="557d4-203">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-204">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="557d4-204">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-205">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-206">Quantité maximale de ressources processeur qui peuvent être consommées par l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="557d4-206">The maximum amount of CPU resources that may be consumed by the virtual machine.</span></span> <span data-ttu-id="557d4-207">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="557d4-207">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="557d4-208">100000</span><span class="sxs-lookup"><span data-stu-id="557d4-208">100000</span></span>

<span data-ttu-id="557d4-209">Plage : 0 100000</span><span class="sxs-lookup"><span data-stu-id="557d4-209">Range: 0 100000</span></span>

</dd> <dt>

<span data-ttu-id="557d4-210">**LimitCPUID**</span><span class="sxs-lookup"><span data-stu-id="557d4-210">**LimitCPUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-211">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="557d4-211">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-212">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-213">Indique si l’ordinateur virtuel doit réduire l’identificateur de l’UC.</span><span class="sxs-lookup"><span data-stu-id="557d4-213">Indicates whether the virtual machine should lower the CPU identifier.</span></span> <span data-ttu-id="557d4-214">Certains systèmes d’exploitation plus anciens peuvent vous obliger à limiter les fonctionnalités du processeur de cette façon afin de les exécuter.</span><span class="sxs-lookup"><span data-stu-id="557d4-214">Some older operating systems may require you to limit processor functionality in this way in order to run.</span></span>

</dd> <dt>

<span data-ttu-id="557d4-215">**LimitProcessorFeatures**</span><span class="sxs-lookup"><span data-stu-id="557d4-215">**LimitProcessorFeatures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-216">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="557d4-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-217">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-218">Indique si l’ordinateur virtuel doit limiter les fonctionnalités de l’UC exposées au système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="557d4-218">Indicates whether the virtual machine should limit the CPU features exposed to the operating system.</span></span> <span data-ttu-id="557d4-219">Le fait de limiter les fonctionnalités du processeur permet à la machine virtuelle d’être migrée vers différents systèmes d’ordinateurs hôtes avec des processeurs différents.</span><span class="sxs-lookup"><span data-stu-id="557d4-219">Limiting the processor features enables the virtual machine to be migrated to different host computer systems with different processors.</span></span> <span data-ttu-id="557d4-220">La migration d’ordinateurs virtuels entre des ordinateurs équipés de processeurs de différents fournisseurs n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="557d4-220">Migrating virtual machines between computers with processors from different vendors is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="557d4-221">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="557d4-221">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-222">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="557d4-222">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-223">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-224">Spécifie comment cette ressource est mappée aux ressources sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="557d4-224">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="557d4-225">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="557d4-225">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="557d4-226">**MaxNumaNodesPerSocket**</span><span class="sxs-lookup"><span data-stu-id="557d4-226">**MaxNumaNodesPerSocket**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-227">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="557d4-227">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-229">Nombre maximal de nœuds NUMA qui peuvent être observés dans l’ordinateur virtuel comme appartenant à un seul socket de processeur.</span><span class="sxs-lookup"><span data-stu-id="557d4-229">The maximum number of NUMA nodes that can be observed within the virtual machine as belonging to a single processor socket.</span></span>

</dd> <dt>

<span data-ttu-id="557d4-230">**MaxProcessorsPerNumaNode**</span><span class="sxs-lookup"><span data-stu-id="557d4-230">**MaxProcessorsPerNumaNode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-231">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="557d4-231">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-232">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-233">Nombre maximal de processeurs virtuels qui peuvent être observés dans l’ordinateur virtuel comme appartenant à un seul nœud NUMA virtuel.</span><span class="sxs-lookup"><span data-stu-id="557d4-233">The maximum number of virtual processors that can be observed within the virtual machine as belonging to a single virtual NUMA node.</span></span>

</dd> <dt>

<span data-ttu-id="557d4-234">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="557d4-234">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-235">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="557d4-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-236">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-237">Chaîne qui décrit le type de ressource lorsqu’une valeur bien définie n’est pas disponible et que **resourceType** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="557d4-237">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="557d4-238">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="557d4-238">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="557d4-239">**Parent**</span><span class="sxs-lookup"><span data-stu-id="557d4-239">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-240">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="557d4-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-241">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-242">Parent de la ressource.</span><span class="sxs-lookup"><span data-stu-id="557d4-242">The parent of the resource.</span></span> <span data-ttu-id="557d4-243">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="557d4-243">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="557d4-244">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="557d4-244">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-245">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="557d4-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-246">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-247">Identificateur du pool de ressources à partir duquel cette ressource a été allouée.</span><span class="sxs-lookup"><span data-stu-id="557d4-247">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="557d4-248">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="557d4-248">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="557d4-249">**Réservation**</span><span class="sxs-lookup"><span data-stu-id="557d4-249">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-250">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="557d4-250">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-251">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-252">Quantité de ressources de processeur réservées pour une utilisation par l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="557d4-252">The amount of CPU resources that are reserved for use by the virtual machine.</span></span> <span data-ttu-id="557d4-253">Ces ressources sont garanties d’être disponibles pour la consommation par l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="557d4-253">These resources are guaranteed to be available for consumption by the virtual machine.</span></span> <span data-ttu-id="557d4-254">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="557d4-254">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="557d4-255">0</span><span class="sxs-lookup"><span data-stu-id="557d4-255">0</span></span>

<span data-ttu-id="557d4-256">Plage : 0 100000</span><span class="sxs-lookup"><span data-stu-id="557d4-256">Range: 0 100000</span></span>

</dd> <dt>

<span data-ttu-id="557d4-257">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="557d4-257">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-258">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="557d4-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-259">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-260">Chaîne qui décrit un sous-type spécifique à l’implémentation pour cette ressource.</span><span class="sxs-lookup"><span data-stu-id="557d4-260">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="557d4-261">Par exemple, cela peut être utilisé pour distinguer différents modèles du même type de ressource.</span><span class="sxs-lookup"><span data-stu-id="557d4-261">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="557d4-262">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="557d4-262">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="557d4-263">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="557d4-263">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-264">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="557d4-264">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-265">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-266">Type de ressource représenté par ce paramètre d’allocation.</span><span class="sxs-lookup"><span data-stu-id="557d4-266">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="557d4-267">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="557d4-267">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="557d4-268">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="557d4-268">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-269">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="557d4-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-270">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-271">Nombre total de cœurs dans l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="557d4-271">The total number of cores in the virtual machine.</span></span> <span data-ttu-id="557d4-272">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="557d4-272">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="557d4-273">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="557d4-273">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-274">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="557d4-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-275">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-276">Spécifie l’unité de mesure pour cette allocation de ressources.</span><span class="sxs-lookup"><span data-stu-id="557d4-276">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="557d4-277">La valeur de cette propriété doit être une valeur légale du qualificateur d’unités de programmation, tel que défini dans l’annexe C. 1 de DSP0004 V 2.5 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="557d4-277">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="557d4-278">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="557d4-278">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="557d4-279">**Poids**</span><span class="sxs-lookup"><span data-stu-id="557d4-279">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557d4-280">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="557d4-280">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="557d4-281">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="557d4-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="557d4-282">Poids de chaque processeur d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="557d4-282">The weight for each virtual machine processor.</span></span> <span data-ttu-id="557d4-283">Une fois toutes les réserves remplies, la capacité du processeur physique restant de la plateforme d’hébergement sera allouée aux ordinateurs virtuels en fonction de leurs pondérations relatives.</span><span class="sxs-lookup"><span data-stu-id="557d4-283">After all reserves have been met, the remaining physical processor capacity of the hosting platform will be allocated to virtual machines based on their relative weights.</span></span> <span data-ttu-id="557d4-284">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="557d4-284">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="557d4-285">100</span><span class="sxs-lookup"><span data-stu-id="557d4-285">100</span></span>

<span data-ttu-id="557d4-286">Plage : 0 10000</span><span class="sxs-lookup"><span data-stu-id="557d4-286">Range: 0 10000</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="557d4-287">Notes</span><span class="sxs-lookup"><span data-stu-id="557d4-287">Remarks</span></span>

<span data-ttu-id="557d4-288">L’accès à la classe **MSVM \_ ProcessorSettingData** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="557d4-288">Access to the **Msvm\_ProcessorSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="557d4-289">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="557d4-289">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="557d4-290">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="557d4-290">Requirements</span></span>



| <span data-ttu-id="557d4-291">Condition requise</span><span class="sxs-lookup"><span data-stu-id="557d4-291">Requirement</span></span> | <span data-ttu-id="557d4-292">Valeur</span><span class="sxs-lookup"><span data-stu-id="557d4-292">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="557d4-293">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="557d4-293">Minimum supported client</span></span><br/> | <span data-ttu-id="557d4-294">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="557d4-294">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="557d4-295">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="557d4-295">Minimum supported server</span></span><br/> | <span data-ttu-id="557d4-296">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="557d4-296">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="557d4-297">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="557d4-297">Namespace</span></span><br/>                | <span data-ttu-id="557d4-298">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="557d4-298">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="557d4-299">MOF</span><span class="sxs-lookup"><span data-stu-id="557d4-299">MOF</span></span><br/>                      | <dl> <span data-ttu-id="557d4-300"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="557d4-300"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="557d4-301">DLL</span><span class="sxs-lookup"><span data-stu-id="557d4-301">DLL</span></span><br/>                      | <dl> <span data-ttu-id="557d4-302"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="557d4-302"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="557d4-303">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="557d4-303">See also</span></span>

<dl> <dt>

[<span data-ttu-id="557d4-304">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="557d4-304">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="557d4-305">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="557d4-305">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="557d4-306">Classes de processeur</span><span class="sxs-lookup"><span data-stu-id="557d4-306">Processor Classes</span></span>](processor-classes.md)
</dt> </dl>

 

