---
description: Représente les paramètres d’une ressource allouée qui se trouvent en dehors de la portée de la classe CIM généralement utilisée pour représenter la ressource elle-même.
ms.assetid: 6261bab9-aa51-479e-bd6a-43c4a9b294a6
title: Classe CIM_ResourceAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourceAllocationSettingData
- CIM_ResourceAllocationSettingData.ResourceType
- CIM_ResourceAllocationSettingData.OtherResourceType
- CIM_ResourceAllocationSettingData.ResourceSubType
- CIM_ResourceAllocationSettingData.PoolID
- CIM_ResourceAllocationSettingData.ConsumerVisibility
- CIM_ResourceAllocationSettingData.HostResource
- CIM_ResourceAllocationSettingData.AllocationUnits
- CIM_ResourceAllocationSettingData.VirtualQuantity
- CIM_ResourceAllocationSettingData.Reservation
- CIM_ResourceAllocationSettingData.Limit
- CIM_ResourceAllocationSettingData.Weight
- CIM_ResourceAllocationSettingData.AutomaticAllocation
- CIM_ResourceAllocationSettingData.AutomaticDeallocation
- CIM_ResourceAllocationSettingData.Parent
- CIM_ResourceAllocationSettingData.Connection
- CIM_ResourceAllocationSettingData.Address
- CIM_ResourceAllocationSettingData.MappingBehavior
- CIM_ResourceAllocationSettingData.AddressOnParent
- CIM_ResourceAllocationSettingData.VirtualQuantityUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 22289511f454e0d3b128d0e73d32687924c7a7ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520573"
---
# <a name="cim_resourceallocationsettingdata-class"></a><span data-ttu-id="a9b7e-103">\_Classe CIM ResourceAllocationSettingData</span><span class="sxs-lookup"><span data-stu-id="a9b7e-103">CIM\_ResourceAllocationSettingData class</span></span>

<span data-ttu-id="a9b7e-104">Représente les paramètres d’une ressource allouée qui se trouvent en dehors de la portée de la classe CIM généralement utilisée pour représenter la ressource elle-même.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-104">Represents settings for an allocated resource that are outside the scope of the CIM class typically used to represent the resource itself.</span></span> <span data-ttu-id="a9b7e-105">Ces paramètres incluent des informations spécifiques à l’allocation qui peuvent ne pas être visibles par le consommateur de la ressource.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-105">These settings include information specific to the allocation that may not be visible to the consumer of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9b7e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9b7e-106">Syntax</span></span>

``` syntax
[Abstract, Version("2.24.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_ResourceAllocationSettingData : CIM_SettingData
{
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

## <a name="members"></a><span data-ttu-id="a9b7e-107">Membres</span><span class="sxs-lookup"><span data-stu-id="a9b7e-107">Members</span></span>

<span data-ttu-id="a9b7e-108">La classe **CIM \_ ResourceAllocationSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a9b7e-108">The **CIM\_ResourceAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="a9b7e-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a9b7e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a9b7e-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a9b7e-110">Properties</span></span>

<span data-ttu-id="a9b7e-111">La classe **CIM \_ ResourceAllocationSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-111">The **CIM\_ResourceAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a9b7e-112">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b7e-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9b7e-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9b7e-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b7e-115">Adresse de la ressource, par exemple, l’adresse MAC d’un port Ethernet.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-115">The address of the resource, for example, the MAC address of a Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="a9b7e-116">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-116">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b7e-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9b7e-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9b7e-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b7e-119">Adresse de cette ressource à partir du contexte du parent.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-119">The address of this resource from the context of the parent.</span></span> <span data-ttu-id="a9b7e-120">Cette propriété est utilisée pour décrire une relation de contrôleur et l’ordre des appareils sur un contrôleur.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-120">This property is used to describe a controller relationship and the ordering of devices on a controller.</span></span> <span data-ttu-id="a9b7e-121">Par exemple, si le parent est un contrôleur PCI, cette propriété spécifie l’emplacement PCI de cet appareil enfant.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-121">For example, if the parent is a PCI Controller, this property would specify the PCI slot of this child device.</span></span>

</dd> <dt>

<span data-ttu-id="a9b7e-122">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-122">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b7e-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9b7e-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9b7e-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9b7e-125">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**Réservation**« , »**CIM \_ ResourceAllocationSettingData**.**Limit**"), **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-125">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**Reservation**", "**CIM\_ResourceAllocationSettingData**.**Limit**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="a9b7e-126">Unités d’allocation utilisées par la **réservation** et les propriétés de la **limite** .</span><span class="sxs-lookup"><span data-stu-id="a9b7e-126">The allocation units used by the **Reservation** and **Limit** properties.</span></span>

</dd> <dt>

<span data-ttu-id="a9b7e-127">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-127">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b7e-128">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a9b7e-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9b7e-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b7e-130">**true** pour allouer automatiquement la ressource ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-130">**true** to automatically allocate the resource; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="a9b7e-131">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-131">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b7e-132">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a9b7e-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9b7e-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b7e-134">**true** pour libérer automatiquement la ressource ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-134">**true** to automatically deallocate the resource; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="a9b7e-135">**Connection**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-135">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b7e-136">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-136">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a9b7e-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9b7e-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b7e-138">Tableau qui indique les objets connectés à la ressource, par exemple un réseau nommé ou un port commuté.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-138">An array that indicates the objects connected to the resource, such as a named network or switch port.</span></span>

</dd> <dt>

<span data-ttu-id="a9b7e-139">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-139">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b7e-140">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9b7e-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9b7e-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b7e-142">Visibilité des consommateurs sur la ressource allouée.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-142">The consumers visibility to the allocated resource.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a9b7e-143">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-143">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span>

<span data-ttu-id="a9b7e-144">**Passe-à-** (2)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-144">**Passed-Through** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span>

<span data-ttu-id="a9b7e-145">**Virtualisé** (3)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-145">**Virtualized** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span>

<span data-ttu-id="a9b7e-146">**Non représenté** (4)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-146">**Not represented** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="a9b7e-147">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-147">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="a9b7e-148">**Fournisseur réservé** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-148">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a9b7e-149">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-149">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b7e-150">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-150">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a9b7e-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9b7e-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9b7e-152">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**ConsumerVisibility**","**CIM \_ ResourceAllocationSettingData**.**MappingBehavior**")</span><span class="sxs-lookup"><span data-stu-id="a9b7e-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**ConsumerVisibility**", "**CIM\_ResourceAllocationSettingData**.**MappingBehavior**")</span></span>
</dt> </dl>

<span data-ttu-id="a9b7e-153">Tableau qui contient l’assignation des ressources allouées.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-153">An array that contains the assignment of the allocated resources.</span></span> <span data-ttu-id="a9b7e-154">Chaque valeur non null de cette propriété doit être mise en forme en tant qu’URI basé sur norme RFC 3986.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-154">Each non-null value of this property must be formated as an RFC3986 based URI.</span></span> <span data-ttu-id="a9b7e-155">Si la ressource est modélisée, la valeur doit être un URI WBEM.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-155">If the resource is modeled, then the value should be a WBEM URI.</span></span>

</dd> <dt>

<span data-ttu-id="a9b7e-156">**Limite**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-156">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b7e-157">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-157">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a9b7e-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9b7e-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9b7e-159">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**AllocationUnits**")</span><span class="sxs-lookup"><span data-stu-id="a9b7e-159">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**AllocationUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="a9b7e-160">Quantité maximale de ressources à accorder à l’allocation.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-160">The maximum amount of resource to grant to the allocation.</span></span> <span data-ttu-id="a9b7e-161">Le type d’unité de cette propriété est spécifié par la propriété **AllocationUnits** .</span><span class="sxs-lookup"><span data-stu-id="a9b7e-161">The unit type of this property is specified by the **AllocationUnits** property.</span></span>

</dd> <dt>

<span data-ttu-id="a9b7e-162">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-162">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b7e-163">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9b7e-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9b7e-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b7e-165">Indique comment la ressource est mappée aux ressources sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-165">Indicates how the resource maps to underlying resources.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a9b7e-166">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-166">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="a9b7e-167">**Non pris en charge** (2)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-167">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="a9b7e-168">**Dédié** (3)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-168">**Dedicated** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>

<span data-ttu-id="a9b7e-169">**Affinité douce** (4)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-169">**Soft Affinity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>

<span data-ttu-id="a9b7e-170">**Affinité matérielle** (5)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-170">**Hard Affinity** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="a9b7e-171">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-171">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="a9b7e-172">**Fournisseur réservé** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-172">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a9b7e-173">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-173">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b7e-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9b7e-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9b7e-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9b7e-176">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**ResourceType**»)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-176">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="a9b7e-177">Description du type de ressource lorsque la propriété **resourceType** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="a9b7e-177">A description of the resource type when the **ResourceType** property is set to 1 (other).</span></span>

</dd> <dt>

<span data-ttu-id="a9b7e-178">**Parent**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-178">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b7e-179">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9b7e-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9b7e-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b7e-181">Parent de la ressource, par exemple, un contrôleur pour l’allocation actuelle.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-181">The parent of the resource, for example, a controller for the current allocation.</span></span>

</dd> <dt>

<span data-ttu-id="a9b7e-182">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-182">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b7e-183">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9b7e-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9b7e-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9b7e-185">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**PoolId**")</span><span class="sxs-lookup"><span data-stu-id="a9b7e-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**PoolId**")</span></span>
</dt> </dl>

<span data-ttu-id="a9b7e-186">ID du pool de ressources qui a généré la ressource.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-186">The ID of the resource pool that generated the resource.</span></span>

</dd> <dt>

<span data-ttu-id="a9b7e-187">**Réservation**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-187">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b7e-188">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a9b7e-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9b7e-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9b7e-190">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**AllocationUnits**")</span><span class="sxs-lookup"><span data-stu-id="a9b7e-190">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**AllocationUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="a9b7e-191">Nombre de ressources dont la disponibilité est garantie pour cette allocation.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-191">The number of resource that are guaranteed to be available for this allocation.</span></span> <span data-ttu-id="a9b7e-192">Sur les systèmes qui prennent en charge le surengagement de ressources, cette valeur est généralement utilisée pour le contrôle d’admission.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-192">On systems that support over-commitment of resources, this value is typically used for admission control.</span></span>

<span data-ttu-id="a9b7e-193">Le type d’unité de cette propriété est spécifié par la propriété **AllocationUnits** .</span><span class="sxs-lookup"><span data-stu-id="a9b7e-193">The unit type of this property is specified by the **AllocationUnits** property.</span></span>

</dd> <dt>

<span data-ttu-id="a9b7e-194">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-194">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b7e-195">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9b7e-196">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9b7e-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9b7e-197">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**ResourceType**»)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-197">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="a9b7e-198">Sous-type spécifique à l’implémentation de cette ressource.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-198">An implementation specific sub-type for this resource.</span></span> <span data-ttu-id="a9b7e-199">Par exemple, cela peut être utilisé pour distinguer différents modèles du même type de ressource.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-199">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="a9b7e-200">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-200">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b7e-201">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9b7e-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9b7e-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9b7e-203">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**OtherResourceType**","**CIM \_ ResourceAllocationSettingData**.**ResourceSubType**")</span><span class="sxs-lookup"><span data-stu-id="a9b7e-203">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**OtherResourceType**", "**CIM\_ResourceAllocationSettingData**.**ResourceSubType**")</span></span>
</dt> </dl>

<span data-ttu-id="a9b7e-204">Type de ressource représenté par les paramètres d’allocation.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-204">The type of resource that is represented by the allocation settings.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a9b7e-205">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-205">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

<span data-ttu-id="a9b7e-206">**Système informatique** (2)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-206">**Computer System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

<span data-ttu-id="a9b7e-207">**Processeur** (3)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-207">**Processor** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

<span data-ttu-id="a9b7e-208">**Mémoire** (4)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-208">**Memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

<span data-ttu-id="a9b7e-209">**Contrôleur IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-209">**IDE Controller** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

<span data-ttu-id="a9b7e-210">**HBA SCSI parallèle** (6)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-210">**Parallel SCSI HBA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

<span data-ttu-id="a9b7e-211">**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-211">**FC HBA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

<span data-ttu-id="a9b7e-212">**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-212">**iSCSI HBA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

<span data-ttu-id="a9b7e-213">**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-213">**IB HCA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

<span data-ttu-id="a9b7e-214">**Carte Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-214">**Ethernet Adapter** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

<span data-ttu-id="a9b7e-215">**Autre carte réseau** (11)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-215">**Other Network Adapter** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

<span data-ttu-id="a9b7e-216">**Emplacement d’e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-216">**I/O Slot** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

<span data-ttu-id="a9b7e-217">**Périphérique d’e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-217">**I/O Device** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

<span data-ttu-id="a9b7e-218">**Lecteur de disquette** (14)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-218">**Floppy Drive** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

<span data-ttu-id="a9b7e-219">**Lecteur de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-219">**CD Drive** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

<span data-ttu-id="a9b7e-220">**Lecteur de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-220">**DVD drive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="a9b7e-221">**Lecteur de disque** (17)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-221">**Disk Drive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

<span data-ttu-id="a9b7e-222">**Lecteur de bande** (18)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-222">**Tape Drive** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

<span data-ttu-id="a9b7e-223">**Extension de stockage** (19)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-223">**Storage Extent** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

<span data-ttu-id="a9b7e-224">**Autre dispositif de stockage** (20)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-224">**Other storage device** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

<span data-ttu-id="a9b7e-225">**Port série** (21)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-225">**Serial port** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="a9b7e-226">**Port parallèle** (22)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-226">**Parallel port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

<span data-ttu-id="a9b7e-227">**Contrôleur USB** (23)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-227">**USB Controller** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

<span data-ttu-id="a9b7e-228">**Contrôleur Graphics** (24)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-228">**Graphics controller** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

<span data-ttu-id="a9b7e-229">**Contrôleur IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-229">**IEEE 1394 Controller** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

<span data-ttu-id="a9b7e-230">**Unité partitionnée** (26)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-230">**Partitionable Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

<span data-ttu-id="a9b7e-231">**Unité partitionnée de base** (27)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-231">**Base Partitionable Unit** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="a9b7e-232">**Puissance** (28)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-232">**Power** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

<span data-ttu-id="a9b7e-233">**Capacité de refroidissement** (29)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-233">**Cooling Capacity** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

<span data-ttu-id="a9b7e-234">**Port commuté Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-234">**Ethernet Switch Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

<span data-ttu-id="a9b7e-235">**Disque logique** (31)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-235">**Logical Disk** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

<span data-ttu-id="a9b7e-236">**Volume de stockage** (32)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-236">**Storage Volume** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

<span data-ttu-id="a9b7e-237">**Connexion Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-237">**Ethernet Connection** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="a9b7e-238">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-238">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="a9b7e-239">**Fournisseur réservé** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="a9b7e-239">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a9b7e-240">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-240">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b7e-241">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-241">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a9b7e-242">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9b7e-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9b7e-243">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**VirtualQuantityUnits**")</span><span class="sxs-lookup"><span data-stu-id="a9b7e-243">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**VirtualQuantityUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="a9b7e-244">Nombre de ressources présentées au consommateur de la ressource.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-244">The number of resources presented to the consumer of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="a9b7e-245">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-245">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b7e-246">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9b7e-247">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9b7e-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9b7e-248">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**VirtualQuantity**"), **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-248">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**VirtualQuantity**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="a9b7e-249">Unités utilisées par la propriété **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="a9b7e-249">The units used by the **VirtualQuantity** property.</span></span>

</dd> <dt>

<span data-ttu-id="a9b7e-250">**Poids**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-250">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b7e-251">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-251">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a9b7e-252">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9b7e-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b7e-253">Priorité relative pour cette allocation par rapport à d’autres allocations à partir du même pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-253">The relative priority for this allocation in relation to other allocations from the same resource pool.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a9b7e-254">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9b7e-254">Requirements</span></span>



| <span data-ttu-id="a9b7e-255">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9b7e-255">Requirement</span></span> | <span data-ttu-id="a9b7e-256">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9b7e-256">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9b7e-257">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9b7e-257">Minimum supported client</span></span><br/> | <span data-ttu-id="a9b7e-258">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a9b7e-258">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="a9b7e-259">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9b7e-259">Minimum supported server</span></span><br/> | <span data-ttu-id="a9b7e-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a9b7e-260">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="a9b7e-261">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a9b7e-261">Namespace</span></span><br/>                | <span data-ttu-id="a9b7e-262">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="a9b7e-262">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a9b7e-263">MOF</span><span class="sxs-lookup"><span data-stu-id="a9b7e-263">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9b7e-264"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9b7e-264"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9b7e-265">DLL</span><span class="sxs-lookup"><span data-stu-id="a9b7e-265">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9b7e-266"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a9b7e-266"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a9b7e-267">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9b7e-267">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9b7e-268">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="a9b7e-268">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

