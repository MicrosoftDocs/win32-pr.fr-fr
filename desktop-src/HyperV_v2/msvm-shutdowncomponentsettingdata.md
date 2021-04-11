---
description: Représente l’état configuré du service d’arrêt.
ms.assetid: 434DE26A-E78A-403A-AFAB-2F9272426A16
title: Classe Msvm_ShutdownComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponentSettingData
- Msvm_ShutdownComponentSettingData.InstanceID
- Msvm_ShutdownComponentSettingData.Caption
- Msvm_ShutdownComponentSettingData.Description
- Msvm_ShutdownComponentSettingData.ElementName
- Msvm_ShutdownComponentSettingData.ResourceType
- Msvm_ShutdownComponentSettingData.OtherResourceType
- Msvm_ShutdownComponentSettingData.ResourceSubType
- Msvm_ShutdownComponentSettingData.PoolID
- Msvm_ShutdownComponentSettingData.ConsumerVisibility
- Msvm_ShutdownComponentSettingData.HostResource
- Msvm_ShutdownComponentSettingData.AllocationUnits
- Msvm_ShutdownComponentSettingData.VirtualQuantity
- Msvm_ShutdownComponentSettingData.Reservation
- Msvm_ShutdownComponentSettingData.Limit
- Msvm_ShutdownComponentSettingData.Weight
- Msvm_ShutdownComponentSettingData.AutomaticAllocation
- Msvm_ShutdownComponentSettingData.AutomaticDeallocation
- Msvm_ShutdownComponentSettingData.Parent
- Msvm_ShutdownComponentSettingData.Connection
- Msvm_ShutdownComponentSettingData.Address
- Msvm_ShutdownComponentSettingData.MappingBehavior
- Msvm_ShutdownComponentSettingData.AddressOnParent
- Msvm_ShutdownComponentSettingData.VirtualQuantityUnits
- Msvm_ShutdownComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8ee2fcb910dc788b01a58544bbfe6a06ba215585
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201968"
---
# <a name="msvm_shutdowncomponentsettingdata-class"></a><span data-ttu-id="ab022-103">MSVM \_ ShutdownComponentSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="ab022-103">Msvm\_ShutdownComponentSettingData class</span></span>

<span data-ttu-id="ab022-104">Représente l’état configuré du service d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="ab022-104">Represents the configured state of the shutdown service.</span></span>

<span data-ttu-id="ab022-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ab022-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab022-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab022-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ShutdownComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Shutdown";
  string  Description = "Microsoft Shutdown Service Setting Data";
  string  ElementName = "Shutdown";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:Shutdown Component";
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

## <a name="members"></a><span data-ttu-id="ab022-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ab022-107">Members</span></span>

<span data-ttu-id="ab022-108">La classe **MSVM \_ ShutdownComponentSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ab022-108">The **Msvm\_ShutdownComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="ab022-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ab022-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ab022-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ab022-110">Properties</span></span>

<span data-ttu-id="ab022-111">La classe **MSVM \_ ShutdownComponentSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ab022-111">The **Msvm\_ShutdownComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ab022-112">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="ab022-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab022-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ab022-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab022-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab022-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab022-115">Adresse de la ressource.</span><span class="sxs-lookup"><span data-stu-id="ab022-115">The address of the resource.</span></span> <span data-ttu-id="ab022-116">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab022-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab022-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="ab022-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab022-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ab022-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab022-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab022-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab022-120">Décrit l’adresse de cette ressource dans le contexte du parent.</span><span class="sxs-lookup"><span data-stu-id="ab022-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="ab022-121">Les propriétés **parent** et **AddressOnParent** sont utilisées pour décrire la relation du contrôleur, ainsi que l’ordre des appareils sur un contrôleur.</span><span class="sxs-lookup"><span data-stu-id="ab022-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="ab022-122">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab022-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab022-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="ab022-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab022-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ab022-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab022-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab022-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab022-126">Unités d’allocation utilisées par la **réservation** et les propriétés de la **limite** .</span><span class="sxs-lookup"><span data-stu-id="ab022-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="ab022-127">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab022-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab022-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="ab022-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab022-129">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ab022-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ab022-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab022-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab022-131">Indique si la ressource sera automatiquement allouée.</span><span class="sxs-lookup"><span data-stu-id="ab022-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="ab022-132">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab022-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab022-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="ab022-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab022-134">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ab022-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ab022-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab022-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab022-136">Indique si la ressource sera automatiquement désallouée.</span><span class="sxs-lookup"><span data-stu-id="ab022-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="ab022-137">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab022-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab022-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ab022-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab022-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ab022-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab022-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab022-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab022-141">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ab022-141">A short description of the object.</span></span> <span data-ttu-id="ab022-142">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « Shutdown ».</span><span class="sxs-lookup"><span data-stu-id="ab022-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Shutdown".</span></span>

</dd> <dt>

<span data-ttu-id="ab022-143">**Connection**</span><span class="sxs-lookup"><span data-stu-id="ab022-143">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab022-144">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ab022-144">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ab022-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab022-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab022-146">Élément auquel cette ressource est connectée.</span><span class="sxs-lookup"><span data-stu-id="ab022-146">The thing to which this resource is connected.</span></span> <span data-ttu-id="ab022-147">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab022-147">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab022-148">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="ab022-148">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab022-149">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ab022-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ab022-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab022-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab022-151">Visibilité des consommateurs sur la ressource allouée.</span><span class="sxs-lookup"><span data-stu-id="ab022-151">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="ab022-152">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab022-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="ab022-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab022-153">Value</span></span>                                                                        | <span data-ttu-id="ab022-154">Signification</span><span class="sxs-lookup"><span data-stu-id="ab022-154">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="ab022-155"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ab022-155"><dt>3</dt></span></span> </dl> | <span data-ttu-id="ab022-156">Virtualisé</span><span class="sxs-lookup"><span data-stu-id="ab022-156">Virtualized</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ab022-157">**Description**</span><span class="sxs-lookup"><span data-stu-id="ab022-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab022-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ab022-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab022-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab022-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab022-160">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="ab022-160">A description of the object.</span></span> <span data-ttu-id="ab022-161">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ab022-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ab022-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ab022-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab022-163">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ab022-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab022-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab022-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab022-165">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ab022-165">A display name for the object.</span></span> <span data-ttu-id="ab022-166">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ab022-166">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ab022-167">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="ab022-167">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab022-168">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ab022-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ab022-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab022-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab022-170">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="ab022-170">The enabled and disabled states of an element.</span></span> <span data-ttu-id="ab022-171">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ab022-171">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ab022-172">**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="ab022-172">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ab022-173">**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="ab022-173">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ab022-174">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="ab022-174">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab022-175">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ab022-175">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ab022-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab022-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab022-177">Expose une attribution spécifique à l’hôte ou aux ressources sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="ab022-177">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="ab022-178">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab022-178">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab022-179">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ab022-179">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab022-180">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ab022-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab022-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab022-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab022-182">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="ab022-182">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ab022-183">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="ab022-183">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ab022-184">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ab022-184">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ab022-185">**Limite**</span><span class="sxs-lookup"><span data-stu-id="ab022-185">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab022-186">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ab022-186">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ab022-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab022-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab022-188">Limite supérieure ou quantité maximale de ressources qui seront accordées pour cette allocation.</span><span class="sxs-lookup"><span data-stu-id="ab022-188">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="ab022-189">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab022-189">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab022-190">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="ab022-190">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab022-191">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ab022-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ab022-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab022-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab022-193">Spécifie comment cette ressource est mappée aux ressources sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="ab022-193">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="ab022-194">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab022-194">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab022-195">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="ab022-195">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab022-196">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ab022-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab022-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab022-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab022-198">Chaîne qui décrit le type de ressource lorsqu’une valeur bien définie n’est pas disponible et que **resourceType** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="ab022-198">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="ab022-199">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab022-199">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab022-200">**Parent**</span><span class="sxs-lookup"><span data-stu-id="ab022-200">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab022-201">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ab022-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab022-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab022-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab022-203">Parent de la ressource.</span><span class="sxs-lookup"><span data-stu-id="ab022-203">The parent of the resource.</span></span> <span data-ttu-id="ab022-204">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab022-204">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab022-205">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="ab022-205">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab022-206">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ab022-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab022-207">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab022-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab022-208">ID du pool de ressources à partir duquel la ressource est allouée.</span><span class="sxs-lookup"><span data-stu-id="ab022-208">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="ab022-209">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab022-209">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab022-210">**Réservation**</span><span class="sxs-lookup"><span data-stu-id="ab022-210">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab022-211">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ab022-211">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ab022-212">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab022-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab022-213">Quantité de ressources dont la disponibilité est garantie pour cette allocation.</span><span class="sxs-lookup"><span data-stu-id="ab022-213">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="ab022-214">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab022-214">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab022-215">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="ab022-215">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab022-216">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ab022-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab022-217">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab022-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab022-218">Chaîne qui décrit un sous-type spécifique à l’implémentation pour cette ressource.</span><span class="sxs-lookup"><span data-stu-id="ab022-218">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="ab022-219">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab022-219">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab022-220">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="ab022-220">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab022-221">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ab022-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ab022-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab022-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab022-223">Type de ressource représenté par ce paramètre d’allocation.</span><span class="sxs-lookup"><span data-stu-id="ab022-223">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="ab022-224">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab022-224">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="ab022-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab022-225">Value</span></span>                                                                        | <span data-ttu-id="ab022-226">Signification</span><span class="sxs-lookup"><span data-stu-id="ab022-226">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="ab022-227"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ab022-227"><dt>1</dt></span></span> </dl> | <span data-ttu-id="ab022-228">Autres</span><span class="sxs-lookup"><span data-stu-id="ab022-228">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ab022-229">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="ab022-229">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab022-230">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ab022-230">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ab022-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab022-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab022-232">Quantité de ressources présentées au consommateur.</span><span class="sxs-lookup"><span data-stu-id="ab022-232">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="ab022-233">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab022-233">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab022-234">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="ab022-234">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab022-235">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ab022-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab022-236">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab022-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab022-237">Spécifie l’unité de mesure pour cette allocation de ressources.</span><span class="sxs-lookup"><span data-stu-id="ab022-237">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="ab022-238">La valeur de cette propriété doit être une valeur légale du qualificateur d’unités de programmation, tel que défini dans l’annexe C. 1 de DSP0004 V 2.5 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ab022-238">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="ab022-239">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab022-239">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab022-240">**Poids**</span><span class="sxs-lookup"><span data-stu-id="ab022-240">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab022-241">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab022-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab022-242">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab022-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab022-243">Priorité relative pour cette allocation par rapport à d’autres allocations à partir du même pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="ab022-243">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="ab022-244">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab022-244">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab022-245">Notes</span><span class="sxs-lookup"><span data-stu-id="ab022-245">Remarks</span></span>

<span data-ttu-id="ab022-246">L’accès à la classe **MSVM \_ ShutdownComponentSettingData** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="ab022-246">Access to the **Msvm\_ShutdownComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ab022-247">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ab022-247">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab022-248">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab022-248">Requirements</span></span>



| <span data-ttu-id="ab022-249">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab022-249">Requirement</span></span> | <span data-ttu-id="ab022-250">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab022-250">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab022-251">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab022-251">Minimum supported client</span></span><br/> | <span data-ttu-id="ab022-252">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab022-252">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ab022-253">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab022-253">Minimum supported server</span></span><br/> | <span data-ttu-id="ab022-254">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab022-254">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ab022-255">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ab022-255">Namespace</span></span><br/>                | <span data-ttu-id="ab022-256">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ab022-256">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ab022-257">MOF</span><span class="sxs-lookup"><span data-stu-id="ab022-257">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab022-258"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab022-258"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab022-259">DLL</span><span class="sxs-lookup"><span data-stu-id="ab022-259">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab022-260"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ab022-260"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ab022-261">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab022-261">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab022-262">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="ab022-262">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="ab022-263">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="ab022-263">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

