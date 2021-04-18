---
description: Représente l’état configuré du service Service VSS (VSS).
ms.assetid: FAE8E8F7-525A-4E5A-91B3-B73343337352
title: Classe Msvm_VssComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssComponentSettingData
- Msvm_VssComponentSettingData.InstanceID
- Msvm_VssComponentSettingData.Caption
- Msvm_VssComponentSettingData.Description
- Msvm_VssComponentSettingData.ElementName
- Msvm_VssComponentSettingData.ResourceType
- Msvm_VssComponentSettingData.OtherResourceType
- Msvm_VssComponentSettingData.ResourceSubType
- Msvm_VssComponentSettingData.PoolID
- Msvm_VssComponentSettingData.ConsumerVisibility
- Msvm_VssComponentSettingData.HostResource
- Msvm_VssComponentSettingData.AllocationUnits
- Msvm_VssComponentSettingData.VirtualQuantity
- Msvm_VssComponentSettingData.Reservation
- Msvm_VssComponentSettingData.Limit
- Msvm_VssComponentSettingData.Weight
- Msvm_VssComponentSettingData.AutomaticAllocation
- Msvm_VssComponentSettingData.AutomaticDeallocation
- Msvm_VssComponentSettingData.Parent
- Msvm_VssComponentSettingData.Connection
- Msvm_VssComponentSettingData.Address
- Msvm_VssComponentSettingData.MappingBehavior
- Msvm_VssComponentSettingData.AddressOnParent
- Msvm_VssComponentSettingData.VirtualQuantityUnits
- Msvm_VssComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5d37f46c10cc702c66a30fb484553a8c5da03d8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529105"
---
# <a name="msvm_vsscomponentsettingdata-class"></a><span data-ttu-id="3a4d8-103">MSVM \_ VssComponentSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="3a4d8-103">Msvm\_VssComponentSettingData class</span></span>

<span data-ttu-id="3a4d8-104">Représente l’état configuré du service Service VSS (VSS).</span><span class="sxs-lookup"><span data-stu-id="3a4d8-104">Represents the configured state of the Volume Shadow Copy Service (VSS) service.</span></span>

<span data-ttu-id="3a4d8-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3a4d8-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a4d8-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a4d8-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VssComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "VSS";
  string  Description = "Microsoft VSS Service Setting Data";
  string  ElementName = "VSS";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:VSS Component";
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource;
  string  AllocationUnits = "count";
  uint64  VirtualQuantity = 1;
  uint64  Reservation = 1;
  uint64  Limit = 1;
  uint32  Weight = 0;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  uint16  EnabledState = 2;
};
```

## <a name="members"></a><span data-ttu-id="3a4d8-107">Membres</span><span class="sxs-lookup"><span data-stu-id="3a4d8-107">Members</span></span>

<span data-ttu-id="3a4d8-108">La classe **MSVM \_ VssComponentSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3a4d8-108">The **Msvm\_VssComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="3a4d8-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3a4d8-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3a4d8-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3a4d8-110">Properties</span></span>

<span data-ttu-id="3a4d8-111">La classe **MSVM \_ VssComponentSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3a4d8-111">The **Msvm\_VssComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3a4d8-112">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a4d8-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a4d8-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a4d8-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a4d8-115">Adresse de la ressource.</span><span class="sxs-lookup"><span data-stu-id="3a4d8-115">The address of the resource.</span></span> <span data-ttu-id="3a4d8-116">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3a4d8-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3a4d8-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a4d8-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a4d8-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a4d8-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a4d8-120">Décrit l’adresse de cette ressource dans le contexte du parent.</span><span class="sxs-lookup"><span data-stu-id="3a4d8-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="3a4d8-121">Les propriétés **parent** et **AddressOnParent** sont utilisées pour décrire la relation du contrôleur, ainsi que l’ordre des appareils sur un contrôleur.</span><span class="sxs-lookup"><span data-stu-id="3a4d8-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="3a4d8-122">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3a4d8-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3a4d8-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a4d8-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a4d8-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a4d8-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a4d8-126">Unités d’allocation utilisées par la **réservation** et les propriétés de la **limite** .</span><span class="sxs-lookup"><span data-stu-id="3a4d8-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="3a4d8-127">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3a4d8-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3a4d8-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a4d8-129">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a4d8-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a4d8-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a4d8-131">Indique si la ressource sera automatiquement allouée.</span><span class="sxs-lookup"><span data-stu-id="3a4d8-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="3a4d8-132">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3a4d8-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3a4d8-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a4d8-134">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a4d8-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a4d8-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a4d8-136">Indique si la ressource sera automatiquement désallouée.</span><span class="sxs-lookup"><span data-stu-id="3a4d8-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="3a4d8-137">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3a4d8-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3a4d8-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a4d8-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a4d8-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a4d8-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a4d8-141">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3a4d8-141">A short description of the object.</span></span> <span data-ttu-id="3a4d8-142">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3a4d8-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3a4d8-143">**Connection**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-143">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a4d8-144">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-144">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3a4d8-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a4d8-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a4d8-146">Élément auquel cette ressource est connectée.</span><span class="sxs-lookup"><span data-stu-id="3a4d8-146">The thing to which this resource is connected.</span></span> <span data-ttu-id="3a4d8-147">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3a4d8-147">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3a4d8-148">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-148">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a4d8-149">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a4d8-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a4d8-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a4d8-151">Visibilité des consommateurs sur la ressource allouée.</span><span class="sxs-lookup"><span data-stu-id="3a4d8-151">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="3a4d8-152">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3a4d8-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="3a4d8-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a4d8-153">Value</span></span>                                                                        | <span data-ttu-id="3a4d8-154">Signification</span><span class="sxs-lookup"><span data-stu-id="3a4d8-154">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="3a4d8-155"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3a4d8-155"><dt>3</dt></span></span> </dl> | <span data-ttu-id="3a4d8-156">Virtualisé</span><span class="sxs-lookup"><span data-stu-id="3a4d8-156">Virtualized</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3a4d8-157">**Description**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a4d8-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a4d8-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a4d8-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a4d8-160">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="3a4d8-160">A description of the object.</span></span> <span data-ttu-id="3a4d8-161">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3a4d8-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3a4d8-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a4d8-163">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a4d8-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a4d8-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a4d8-165">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3a4d8-165">A display name for the object.</span></span> <span data-ttu-id="3a4d8-166">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3a4d8-166">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3a4d8-167">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-167">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a4d8-168">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a4d8-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a4d8-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a4d8-170">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="3a4d8-170">The enabled and disabled states of an element.</span></span> <span data-ttu-id="3a4d8-171">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) et a une valeur par défaut de 2 (activé).</span><span class="sxs-lookup"><span data-stu-id="3a4d8-171">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and has a default value of 2 (Enabled).</span></span>

<span data-ttu-id="3a4d8-172">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3a4d8-172">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<dt>



 <span data-ttu-id="3a4d8-173">(2)</span><span class="sxs-lookup"><span data-stu-id="3a4d8-173">(2)</span></span>


</dt> <dd>

<span data-ttu-id="3a4d8-174">activé</span><span class="sxs-lookup"><span data-stu-id="3a4d8-174">Enabled</span></span>

</dd> <dt>

<span data-ttu-id="3a4d8-175">3</span><span class="sxs-lookup"><span data-stu-id="3a4d8-175">3</span></span>
</dt> <dd>

<span data-ttu-id="3a4d8-176">Désactivé</span><span class="sxs-lookup"><span data-stu-id="3a4d8-176">Disabled</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3a4d8-177">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-177">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a4d8-178">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a4d8-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a4d8-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a4d8-180">Expose une attribution spécifique à l’hôte ou aux ressources sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="3a4d8-180">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="3a4d8-181">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) et a toujours la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="3a4d8-181">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3a4d8-182">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-182">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a4d8-183">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a4d8-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a4d8-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a4d8-185">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-185">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3a4d8-186">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="3a4d8-186">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3a4d8-187">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3a4d8-187">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3a4d8-188">**Limite**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-188">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a4d8-189">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-189">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3a4d8-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a4d8-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a4d8-191">Limite supérieure ou quantité maximale de ressources qui seront accordées pour cette allocation.</span><span class="sxs-lookup"><span data-stu-id="3a4d8-191">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="3a4d8-192">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3a4d8-192">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3a4d8-193">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-193">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a4d8-194">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a4d8-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a4d8-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a4d8-196">Indique comment cette ressource est mappée aux ressources sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="3a4d8-196">Indicates how this resource maps to underlying resources.</span></span> <span data-ttu-id="3a4d8-197">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3a4d8-197">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3a4d8-198">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-198">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a4d8-199">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a4d8-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a4d8-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a4d8-201">Chaîne qui décrit le type de ressource lorsqu’une valeur bien définie n’est pas disponible et que **resourceType** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="3a4d8-201">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="3a4d8-202">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3a4d8-202">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3a4d8-203">**Parent**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-203">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a4d8-204">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a4d8-205">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a4d8-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a4d8-206">Parent de la ressource.</span><span class="sxs-lookup"><span data-stu-id="3a4d8-206">The parent of the resource.</span></span> <span data-ttu-id="3a4d8-207">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3a4d8-207">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3a4d8-208">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-208">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a4d8-209">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a4d8-210">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a4d8-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a4d8-211">ID du pool de ressources à partir duquel la ressource est allouée.</span><span class="sxs-lookup"><span data-stu-id="3a4d8-211">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="3a4d8-212">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3a4d8-212">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3a4d8-213">**Réservation**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-213">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a4d8-214">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-214">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3a4d8-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a4d8-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a4d8-216">Quantité de ressources dont la disponibilité est garantie pour cette allocation.</span><span class="sxs-lookup"><span data-stu-id="3a4d8-216">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="3a4d8-217">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3a4d8-217">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3a4d8-218">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-218">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a4d8-219">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a4d8-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a4d8-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a4d8-221">Chaîne qui décrit un sous-type spécifique à l’implémentation pour cette ressource.</span><span class="sxs-lookup"><span data-stu-id="3a4d8-221">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="3a4d8-222">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) et a toujours la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="3a4d8-222">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3a4d8-223">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-223">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a4d8-224">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-224">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a4d8-225">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a4d8-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a4d8-226">Type de ressource représenté par ce paramètre d’allocation.</span><span class="sxs-lookup"><span data-stu-id="3a4d8-226">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="3a4d8-227">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) et est toujours définie sur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="3a4d8-227">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 1 (Other).</span></span>



| <span data-ttu-id="3a4d8-228">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a4d8-228">Value</span></span>                                                                        | <span data-ttu-id="3a4d8-229">Signification</span><span class="sxs-lookup"><span data-stu-id="3a4d8-229">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="3a4d8-230"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3a4d8-230"><dt>1</dt></span></span> </dl> | <span data-ttu-id="3a4d8-231">Autres</span><span class="sxs-lookup"><span data-stu-id="3a4d8-231">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3a4d8-232">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-232">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a4d8-233">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-233">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3a4d8-234">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a4d8-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a4d8-235">Quantité de ressources présentées au consommateur.</span><span class="sxs-lookup"><span data-stu-id="3a4d8-235">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="3a4d8-236">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3a4d8-236">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3a4d8-237">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-237">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a4d8-238">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a4d8-239">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a4d8-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a4d8-240">Spécifie l’unité de mesure pour cette allocation de ressources.</span><span class="sxs-lookup"><span data-stu-id="3a4d8-240">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="3a4d8-241">La valeur de cette propriété est une valeur légale du qualificateur d’unités de programmation, tel que défini dans l’annexe C. 1 de DSP0004 V 2.5 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3a4d8-241">The value of this property is a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="3a4d8-242">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3a4d8-242">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3a4d8-243">**Poids**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-243">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a4d8-244">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-244">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a4d8-245">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a4d8-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a4d8-246">Priorité relative pour cette allocation par rapport à d’autres allocations à partir du même pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="3a4d8-246">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="3a4d8-247">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3a4d8-247">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3a4d8-248">Notes</span><span class="sxs-lookup"><span data-stu-id="3a4d8-248">Remarks</span></span>

<span data-ttu-id="3a4d8-249">L’accès à la classe **MSVM \_ VssComponentSettingData** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="3a4d8-249">Access to the **Msvm\_VssComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3a4d8-250">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="3a4d8-250">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a4d8-251">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a4d8-251">Requirements</span></span>



| <span data-ttu-id="3a4d8-252">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a4d8-252">Requirement</span></span> | <span data-ttu-id="3a4d8-253">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a4d8-253">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a4d8-254">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a4d8-254">Minimum supported client</span></span><br/> | <span data-ttu-id="3a4d8-255">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3a4d8-255">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3a4d8-256">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a4d8-256">Minimum supported server</span></span><br/> | <span data-ttu-id="3a4d8-257">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3a4d8-257">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3a4d8-258">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3a4d8-258">Namespace</span></span><br/>                | <span data-ttu-id="3a4d8-259">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="3a4d8-259">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3a4d8-260">MOF</span><span class="sxs-lookup"><span data-stu-id="3a4d8-260">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a4d8-261"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a4d8-261"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a4d8-262">DLL</span><span class="sxs-lookup"><span data-stu-id="3a4d8-262">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a4d8-263"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3a4d8-263"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3a4d8-264">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a4d8-264">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a4d8-265">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-265">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="3a4d8-266">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="3a4d8-266">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

