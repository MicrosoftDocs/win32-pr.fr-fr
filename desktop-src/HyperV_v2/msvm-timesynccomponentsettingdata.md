---
description: Représente l’état configuré du service de synchronisation de l’heure.
ms.assetid: AACEDE11-3F5B-42AB-A16F-0474FA98D3FD
title: Classe Msvm_TimeSyncComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TimeSyncComponentSettingData
- Msvm_TimeSyncComponentSettingData.InstanceID
- Msvm_TimeSyncComponentSettingData.Caption
- Msvm_TimeSyncComponentSettingData.Description
- Msvm_TimeSyncComponentSettingData.ElementName
- Msvm_TimeSyncComponentSettingData.ResourceType
- Msvm_TimeSyncComponentSettingData.OtherResourceType
- Msvm_TimeSyncComponentSettingData.ResourceSubType
- Msvm_TimeSyncComponentSettingData.PoolID
- Msvm_TimeSyncComponentSettingData.ConsumerVisibility
- Msvm_TimeSyncComponentSettingData.HostResource
- Msvm_TimeSyncComponentSettingData.AllocationUnits
- Msvm_TimeSyncComponentSettingData.VirtualQuantity
- Msvm_TimeSyncComponentSettingData.Reservation
- Msvm_TimeSyncComponentSettingData.Limit
- Msvm_TimeSyncComponentSettingData.Weight
- Msvm_TimeSyncComponentSettingData.AutomaticAllocation
- Msvm_TimeSyncComponentSettingData.AutomaticDeallocation
- Msvm_TimeSyncComponentSettingData.Parent
- Msvm_TimeSyncComponentSettingData.Connection
- Msvm_TimeSyncComponentSettingData.Address
- Msvm_TimeSyncComponentSettingData.MappingBehavior
- Msvm_TimeSyncComponentSettingData.AddressOnParent
- Msvm_TimeSyncComponentSettingData.VirtualQuantityUnits
- Msvm_TimeSyncComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 063c0f7904976d50d7c1914f810e71ff84f740b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951437"
---
# <a name="msvm_timesynccomponentsettingdata-class"></a><span data-ttu-id="56df6-103">MSVM \_ TimeSyncComponentSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="56df6-103">Msvm\_TimeSyncComponentSettingData class</span></span>

<span data-ttu-id="56df6-104">Représente l’état configuré du service de synchronisation de l’heure.</span><span class="sxs-lookup"><span data-stu-id="56df6-104">Represents the configured state of the time synchronization service.</span></span>

<span data-ttu-id="56df6-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="56df6-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="56df6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56df6-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TimeSyncComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Time Synchronization";
  string  Description = "Microsoft Time Synchronization Service Setting Data";
  string  ElementName = "Time Synchronization";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:Time Synchronization Component";
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
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

## <a name="members"></a><span data-ttu-id="56df6-107">Membres</span><span class="sxs-lookup"><span data-stu-id="56df6-107">Members</span></span>

<span data-ttu-id="56df6-108">La classe **MSVM \_ TimeSyncComponentSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="56df6-108">The **Msvm\_TimeSyncComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="56df6-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="56df6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="56df6-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="56df6-110">Properties</span></span>

<span data-ttu-id="56df6-111">La classe **MSVM \_ TimeSyncComponentSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="56df6-111">The **Msvm\_TimeSyncComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="56df6-112">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="56df6-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56df6-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="56df6-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56df6-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="56df6-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56df6-115">Adresse de la ressource.</span><span class="sxs-lookup"><span data-stu-id="56df6-115">The address of the resource.</span></span> <span data-ttu-id="56df6-116">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56df6-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="56df6-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="56df6-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56df6-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="56df6-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56df6-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="56df6-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56df6-120">Décrit l’adresse de cette ressource dans le contexte du parent.</span><span class="sxs-lookup"><span data-stu-id="56df6-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="56df6-121">Les propriétés **parent** et **AddressOnParent** sont utilisées pour décrire la relation du contrôleur, ainsi que l’ordre des appareils sur un contrôleur.</span><span class="sxs-lookup"><span data-stu-id="56df6-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="56df6-122">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56df6-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="56df6-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="56df6-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56df6-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="56df6-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56df6-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="56df6-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56df6-126">Unités d’allocation utilisées par la **réservation** et les propriétés de la **limite** .</span><span class="sxs-lookup"><span data-stu-id="56df6-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="56df6-127">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56df6-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="56df6-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="56df6-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56df6-129">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="56df6-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="56df6-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="56df6-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56df6-131">Indique si la ressource sera automatiquement allouée.</span><span class="sxs-lookup"><span data-stu-id="56df6-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="56df6-132">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56df6-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="56df6-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="56df6-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56df6-134">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="56df6-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="56df6-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="56df6-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56df6-136">Indique si la ressource sera automatiquement désallouée.</span><span class="sxs-lookup"><span data-stu-id="56df6-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="56df6-137">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56df6-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="56df6-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="56df6-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56df6-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="56df6-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56df6-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="56df6-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56df6-141">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="56df6-141">A short description of the object.</span></span> <span data-ttu-id="56df6-142">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="56df6-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="56df6-143">**Connection**</span><span class="sxs-lookup"><span data-stu-id="56df6-143">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56df6-144">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="56df6-144">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="56df6-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="56df6-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56df6-146">Élément auquel cette ressource est connectée.</span><span class="sxs-lookup"><span data-stu-id="56df6-146">The thing to which this resource is connected.</span></span> <span data-ttu-id="56df6-147">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56df6-147">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="56df6-148">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="56df6-148">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56df6-149">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="56df6-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="56df6-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="56df6-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56df6-151">Visibilité des consommateurs sur la ressource allouée.</span><span class="sxs-lookup"><span data-stu-id="56df6-151">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="56df6-152">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56df6-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="56df6-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="56df6-153">Value</span></span>                                                                        | <span data-ttu-id="56df6-154">Signification</span><span class="sxs-lookup"><span data-stu-id="56df6-154">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="56df6-155"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="56df6-155"><dt>3</dt></span></span> </dl> | <span data-ttu-id="56df6-156">Virtualisé</span><span class="sxs-lookup"><span data-stu-id="56df6-156">Virtualized</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="56df6-157">**Description**</span><span class="sxs-lookup"><span data-stu-id="56df6-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56df6-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="56df6-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56df6-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="56df6-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56df6-160">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="56df6-160">A description of the object.</span></span> <span data-ttu-id="56df6-161">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="56df6-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="56df6-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="56df6-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56df6-163">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="56df6-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56df6-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="56df6-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56df6-165">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="56df6-165">A display name for the object.</span></span> <span data-ttu-id="56df6-166">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="56df6-166">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="56df6-167">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="56df6-167">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56df6-168">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="56df6-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="56df6-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="56df6-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56df6-170">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="56df6-170">The enabled and disabled states of an element.</span></span> <span data-ttu-id="56df6-171">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="56df6-171">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span></span>

<dt>



 <span data-ttu-id="56df6-172">(2)</span><span class="sxs-lookup"><span data-stu-id="56df6-172">(2)</span></span>


</dt> <dd>

<span data-ttu-id="56df6-173">activé</span><span class="sxs-lookup"><span data-stu-id="56df6-173">Enabled</span></span>

</dd> <dt>

<span data-ttu-id="56df6-174">3</span><span class="sxs-lookup"><span data-stu-id="56df6-174">3</span></span>
</dt> <dd>

<span data-ttu-id="56df6-175">Désactivé</span><span class="sxs-lookup"><span data-stu-id="56df6-175">Disabled</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="56df6-176">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="56df6-176">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56df6-177">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="56df6-177">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="56df6-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="56df6-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56df6-179">Expose une attribution spécifique à l’hôte ou aux ressources sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="56df6-179">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="56df6-180">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="56df6-180">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="56df6-181">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="56df6-181">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56df6-182">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="56df6-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56df6-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="56df6-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56df6-184">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="56df6-184">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="56df6-185">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="56df6-185">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="56df6-186">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="56df6-186">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="56df6-187">**Limite**</span><span class="sxs-lookup"><span data-stu-id="56df6-187">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56df6-188">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="56df6-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="56df6-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="56df6-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56df6-190">Limite supérieure ou quantité maximale de ressources qui seront accordées pour cette allocation.</span><span class="sxs-lookup"><span data-stu-id="56df6-190">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="56df6-191">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56df6-191">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="56df6-192">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="56df6-192">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56df6-193">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="56df6-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="56df6-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="56df6-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56df6-195">Spécifie comment cette ressource est mappée aux ressources sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="56df6-195">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="56df6-196">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56df6-196">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="56df6-197">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="56df6-197">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56df6-198">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="56df6-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56df6-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="56df6-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56df6-200">Le type de ressource lorsqu’une valeur bien définie n’est pas disponible et que **resourceType** a la valeur « other ».</span><span class="sxs-lookup"><span data-stu-id="56df6-200">The resource type when a well-defined value is not available and **ResourceType** has the value "Other".</span></span> <span data-ttu-id="56df6-201">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56df6-201">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="56df6-202">**Parent**</span><span class="sxs-lookup"><span data-stu-id="56df6-202">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56df6-203">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="56df6-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56df6-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="56df6-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56df6-205">Parent de la ressource.</span><span class="sxs-lookup"><span data-stu-id="56df6-205">The parent of the resource.</span></span> <span data-ttu-id="56df6-206">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56df6-206">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="56df6-207">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="56df6-207">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56df6-208">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="56df6-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56df6-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="56df6-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56df6-210">ID du pool de ressources à partir duquel la ressource est allouée.</span><span class="sxs-lookup"><span data-stu-id="56df6-210">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="56df6-211">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56df6-211">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="56df6-212">**Réservation**</span><span class="sxs-lookup"><span data-stu-id="56df6-212">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56df6-213">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="56df6-213">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="56df6-214">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="56df6-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56df6-215">Quantité de ressources dont la disponibilité est garantie pour cette allocation.</span><span class="sxs-lookup"><span data-stu-id="56df6-215">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="56df6-216">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56df6-216">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="56df6-217">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="56df6-217">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56df6-218">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="56df6-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56df6-219">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="56df6-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56df6-220">Chaîne qui décrit un sous-type spécifique à l’implémentation pour cette ressource.</span><span class="sxs-lookup"><span data-stu-id="56df6-220">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="56df6-221">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="56df6-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="56df6-222">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="56df6-222">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56df6-223">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="56df6-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="56df6-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="56df6-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56df6-225">Type de ressource représenté par ce paramètre d’allocation.</span><span class="sxs-lookup"><span data-stu-id="56df6-225">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="56df6-226">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56df6-226">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="56df6-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="56df6-227">Value</span></span>                                                                        | <span data-ttu-id="56df6-228">Signification</span><span class="sxs-lookup"><span data-stu-id="56df6-228">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="56df6-229"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="56df6-229"><dt>1</dt></span></span> </dl> | <span data-ttu-id="56df6-230">Autres</span><span class="sxs-lookup"><span data-stu-id="56df6-230">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="56df6-231">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="56df6-231">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56df6-232">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="56df6-232">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="56df6-233">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="56df6-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56df6-234">Quantité de ressources présentées au consommateur.</span><span class="sxs-lookup"><span data-stu-id="56df6-234">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="56df6-235">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56df6-235">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="56df6-236">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="56df6-236">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56df6-237">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="56df6-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56df6-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="56df6-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56df6-239">Spécifie l’unité de mesure pour cette allocation de ressources.</span><span class="sxs-lookup"><span data-stu-id="56df6-239">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="56df6-240">La valeur de cette propriété doit être une valeur légale du qualificateur d’unités de programmation, tel que défini dans l’annexe C. 1 de DSP0004 V 2.5 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="56df6-240">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="56df6-241">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56df6-241">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="56df6-242">**Poids**</span><span class="sxs-lookup"><span data-stu-id="56df6-242">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56df6-243">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="56df6-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="56df6-244">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="56df6-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56df6-245">Priorité relative pour cette allocation par rapport à d’autres allocations à partir du même pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="56df6-245">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="56df6-246">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56df6-246">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56df6-247">Notes</span><span class="sxs-lookup"><span data-stu-id="56df6-247">Remarks</span></span>

<span data-ttu-id="56df6-248">L’accès à la classe **MSVM \_ TimeSyncComponentSettingData** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="56df6-248">Access to the **Msvm\_TimeSyncComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="56df6-249">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="56df6-249">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="56df6-250">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56df6-250">Requirements</span></span>



| <span data-ttu-id="56df6-251">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56df6-251">Requirement</span></span> | <span data-ttu-id="56df6-252">Valeur</span><span class="sxs-lookup"><span data-stu-id="56df6-252">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56df6-253">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56df6-253">Minimum supported client</span></span><br/> | <span data-ttu-id="56df6-254">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56df6-254">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="56df6-255">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56df6-255">Minimum supported server</span></span><br/> | <span data-ttu-id="56df6-256">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56df6-256">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="56df6-257">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="56df6-257">Namespace</span></span><br/>                | <span data-ttu-id="56df6-258">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="56df6-258">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="56df6-259">MOF</span><span class="sxs-lookup"><span data-stu-id="56df6-259">MOF</span></span><br/>                      | <dl> <span data-ttu-id="56df6-260"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="56df6-260"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="56df6-261">DLL</span><span class="sxs-lookup"><span data-stu-id="56df6-261">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56df6-262"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="56df6-262"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="56df6-263">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56df6-263">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56df6-264">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="56df6-264">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="56df6-265">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="56df6-265">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

