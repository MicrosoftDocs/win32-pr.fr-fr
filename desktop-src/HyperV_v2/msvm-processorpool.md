---
description: Agrège les ressources du processeur qui peuvent être allouées à un ordinateur virtuel.
ms.assetid: 73424568-fa6c-4ed8-9640-a67a6d2829f0
title: Classe Msvm_ProcessorPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProcessorPool
- Msvm_ProcessorPool.InstanceID
- Msvm_ProcessorPool.Caption
- Msvm_ProcessorPool.Description
- Msvm_ProcessorPool.ElementName
- Msvm_ProcessorPool.InstallDate
- Msvm_ProcessorPool.Name
- Msvm_ProcessorPool.OperationalStatus
- Msvm_ProcessorPool.StatusDescriptions
- Msvm_ProcessorPool.Status
- Msvm_ProcessorPool.HealthState
- Msvm_ProcessorPool.CommunicationStatus
- Msvm_ProcessorPool.DetailedStatus
- Msvm_ProcessorPool.OperatingStatus
- Msvm_ProcessorPool.PrimaryStatus
- Msvm_ProcessorPool.PoolID
- Msvm_ProcessorPool.Primordial
- Msvm_ProcessorPool.Capacity
- Msvm_ProcessorPool.Reserved
- Msvm_ProcessorPool.ResourceType
- Msvm_ProcessorPool.OtherResourceType
- Msvm_ProcessorPool.ResourceSubType
- Msvm_ProcessorPool.AllocationUnits
- Msvm_ProcessorPool.ConsumedResourceUnits
- Msvm_ProcessorPool.CurrentlyConsumedResource
- Msvm_ProcessorPool.MaxConsumableResource
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 93927483c23147fd387e24cdc5a550a1771457cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520988"
---
# <a name="msvm_processorpool-class"></a><span data-ttu-id="f8b3f-103">MSVM \_ ProcessorPool, classe</span><span class="sxs-lookup"><span data-stu-id="f8b3f-103">Msvm\_ProcessorPool class</span></span>

<span data-ttu-id="f8b3f-104">Agrège les ressources du processeur qui peuvent être allouées à un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-104">Aggregates the processor resources that may be allocated to a virtual machine.</span></span>

<span data-ttu-id="f8b3f-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8b3f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8b3f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ProcessorPool : CIM_ResourcePool
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   PoolID = "Microsoft:GUID\Root";
  boolean  Primordial = False;
  uint64   Capacity;
  uint64   Reserved;
  uint16   ResourceType = 4;
  string   OtherResourceType;
  string   ResourceSubType;
  string   AllocationUnits = "Megabyte";
  string   ConsumedResourceUnits = "count";
  uint64   CurrentlyConsumedResource;
  uint64   MaxConsumableResource;
};
```

## <a name="members"></a><span data-ttu-id="f8b3f-107">Membres</span><span class="sxs-lookup"><span data-stu-id="f8b3f-107">Members</span></span>

<span data-ttu-id="f8b3f-108">La classe **MSVM \_ ProcessorPool** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f8b3f-108">The **Msvm\_ProcessorPool** class has these types of members:</span></span>

-   [<span data-ttu-id="f8b3f-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f8b3f-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="f8b3f-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f8b3f-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f8b3f-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f8b3f-111">Methods</span></span>

<span data-ttu-id="f8b3f-112">La classe **MSVM \_ ProcessorPool** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-112">The **Msvm\_ProcessorPool** class has these methods.</span></span>



| <span data-ttu-id="f8b3f-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="f8b3f-113">Method</span></span>                                                                          | <span data-ttu-id="f8b3f-114">Description</span><span class="sxs-lookup"><span data-stu-id="f8b3f-114">Description</span></span>                                           |
|:--------------------------------------------------------------------------------|:------------------------------------------------------|
| [<span data-ttu-id="f8b3f-115">**CalculatePossibleReserve**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-115">**CalculatePossibleReserve**</span></span>](calculatepossiblereserve-msvm-processorpool.md) | <span data-ttu-id="f8b3f-116">Utilisé pour rechercher la réserve de processeur réelle.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-116">Used to find the actual processor reserve.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f8b3f-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f8b3f-117">Properties</span></span>

<span data-ttu-id="f8b3f-118">La classe **MSVM \_ ProcessorPool** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-118">The **Msvm\_ProcessorPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f8b3f-119">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-119">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b3f-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8b3f-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b3f-122">Unités d’allocation utilisées par le pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-122">The units of allocation used by the resource pool.</span></span> <span data-ttu-id="f8b3f-123">Cette propriété est héritée de la [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85))et est définie sur « mégaoctet ».</span><span class="sxs-lookup"><span data-stu-id="f8b3f-123">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to "Megabyte".</span></span>

</dd> <dt>

<span data-ttu-id="f8b3f-124">**Capacité**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-124">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b3f-125">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8b3f-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b3f-127">Quantité maximale (en unités de **AllocationUnits**) de réservations actives que le pool de ressources peut prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-127">The maximum amount (in units of **AllocationUnits**) of active reservations that the resource pool can support.</span></span> <span data-ttu-id="f8b3f-128">Cette propriété est héritée de la [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f8b3f-128">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f8b3f-129">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-129">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b3f-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8b3f-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b3f-132">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-132">A short description of the object.</span></span> <span data-ttu-id="f8b3f-133">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f8b3f-133">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f8b3f-134">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-134">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b3f-135">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8b3f-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b3f-137">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-137">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="f8b3f-138">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-138">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f8b3f-139">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f8b3f-139">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f8b3f-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-141"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-141"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-142"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-142"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-143"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-143"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-144"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-144"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-145"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-145"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-146"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f8b3f-146"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f8b3f-147">)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-147">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f8b3f-148">**ConsumedResourceUnits**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-148">**ConsumedResourceUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b3f-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8b3f-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b3f-151">Spécifie les unités pour les propriétés **MaxConsumableResource** et **CurrentlyConsumedResource** .</span><span class="sxs-lookup"><span data-stu-id="f8b3f-151">Specifies the units for the **MaxConsumableResource** and the **CurrentlyConsumedResource** properties.</span></span> <span data-ttu-id="f8b3f-152">Cette propriété est héritée de la [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f8b3f-152">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f8b3f-153">**CurrentlyConsumedResource**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-153">**CurrentlyConsumedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b3f-154">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-154">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8b3f-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b3f-156">Spécifie la quantité de ressources que le pool de ressources présente actuellement aux consommateurs.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-156">Specifies the amount of resource that the resource pool currently presents to consumers.</span></span> <span data-ttu-id="f8b3f-157">Cette propriété est différente de la propriété **réservée** en ce qu’elle décrit la vue consommateurs de la ressource, tandis que la propriété **réservée** décrit la vue des producteurs de la ressource.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-157">This property is different from the **Reserved** property in that it describes the consumers view of the resource, while the **Reserved** property describes the producers view of the resource.</span></span> <span data-ttu-id="f8b3f-158">Cette propriété est héritée de la [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f8b3f-158">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f8b3f-159">**Description**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-159">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b3f-160">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8b3f-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b3f-162">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="f8b3f-162">A description of the object.</span></span> <span data-ttu-id="f8b3f-163">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f8b3f-163">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f8b3f-164">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-164">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b3f-165">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8b3f-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b3f-167">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-167">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="f8b3f-168">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-168">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f8b3f-169">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f8b3f-169">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f8b3f-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-171"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-171"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-172"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-172"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-173"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-173"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-174"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-174"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-175"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-175"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f8b3f-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f8b3f-178">)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-178">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f8b3f-179">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-179">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b3f-180">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8b3f-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b3f-182">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-182">A display name for the object.</span></span> <span data-ttu-id="f8b3f-183">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f8b3f-183">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f8b3f-184">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-184">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b3f-185">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8b3f-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b3f-187">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-187">The current health of the element.</span></span> <span data-ttu-id="f8b3f-188">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f8b3f-188">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f8b3f-189">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-189">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b3f-190">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-190">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8b3f-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b3f-192">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-192">The date and time when the object was installed.</span></span> <span data-ttu-id="f8b3f-193">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-193">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="f8b3f-194">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f8b3f-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f8b3f-195">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-195">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b3f-196">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8b3f-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-198">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-198">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f8b3f-199">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-199">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f8b3f-200">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f8b3f-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f8b3f-201">**MaxConsumableResource**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-201">**MaxConsumableResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b3f-202">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-202">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8b3f-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b3f-204">Spécifie la quantité maximale de ressources consommables que le pool de ressources peut présenter aux consommateurs.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-204">Specifies the maximum amount of consumable resource that the resource pool can present to consumers.</span></span> <span data-ttu-id="f8b3f-205">Cette propriété est différente de la propriété **Capacity** en ce qu’elle décrit la vue consommateurs de la ressource, tandis que la propriété **Capacity** décrit la vue des producteurs de la ressource.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-205">This property is different from the **Capacity** property in that it describes the consumers view of the resource, while the **Capacity** property describes the producers view of the resource.</span></span> <span data-ttu-id="f8b3f-206">Cette propriété est héritée de la [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f8b3f-206">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f8b3f-207">**Nom**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-207">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b3f-208">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8b3f-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b3f-210">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-210">The label by which the object is known.</span></span> <span data-ttu-id="f8b3f-211">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f8b3f-211">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f8b3f-212">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-212">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b3f-213">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-214">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8b3f-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b3f-215">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="f8b3f-215">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="f8b3f-216">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f8b3f-217">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f8b3f-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f8b3f-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-220"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-220"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-221"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-221"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-222"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-222"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-223"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-223"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-224"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-224"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-225"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-225"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-226"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-226"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-227"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-227"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-228"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-228"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-229"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-229"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-230"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-230"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-231"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-231"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-232"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-232"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-233"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-233"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-234"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-234"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-235"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-235"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-236"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f8b3f-236"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f8b3f-237">)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-237">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f8b3f-238">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-238">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b3f-239">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-239">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-240">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8b3f-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b3f-241">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-241">The current statuses of the object.</span></span> <span data-ttu-id="f8b3f-242">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f8b3f-242">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f8b3f-243">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-243">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b3f-244">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-245">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8b3f-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b3f-246">Chaîne qui décrit le type de ressource lorsqu’une valeur bien définie n’est pas disponible et que **resourceType** a la valeur 0 (« other »).</span><span class="sxs-lookup"><span data-stu-id="f8b3f-246">A string that describes the resource type when a well-defined value is not available and **ResourceType** is set to 0 ("Other").</span></span> <span data-ttu-id="f8b3f-247">Cette propriété est héritée de [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))et a la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-247">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f8b3f-248">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-248">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b3f-249">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-250">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8b3f-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b3f-251">Cette valeur est référencée par les instances [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) qui ont été allouées à partir de ce pool.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-251">This value is referenced by the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) instances which were allocated from this pool.</span></span> <span data-ttu-id="f8b3f-252">Cette propriété est héritée de la [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85))et est toujours définie sur « Microsoft :*GUID* \\ root ».</span><span class="sxs-lookup"><span data-stu-id="f8b3f-252">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is always set to "Microsoft:*GUID*\\Root".</span></span>

</dd> <dt>

<span data-ttu-id="f8b3f-253">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-253">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b3f-254">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-254">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-255">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8b3f-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b3f-256">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-256">Provides high level status information.</span></span> <span data-ttu-id="f8b3f-257">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-257">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="f8b3f-258">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-258">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f8b3f-259">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f8b3f-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f8b3f-260"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-260"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-261"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-261"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-262"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-262"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-263"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-263"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-265"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f8b3f-265"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f8b3f-266">)</span><span class="sxs-lookup"><span data-stu-id="f8b3f-266">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f8b3f-267">**Primordial**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-267">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b3f-268">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-268">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-269">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8b3f-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b3f-270">**True** si ce pool de ressources est la base à partir de laquelle les ressources sont dessinées et retournées dans l’activité de gestion des ressources. Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-270">**True** if this resource pool is the base from which resources are drawn and returned in the activity of resource management; otherwise, **False**.</span></span> <span data-ttu-id="f8b3f-271">Si primordial signifie que ce pool de ressources ne peut pas être créé ou supprimé par les consommateurs de ce modèle.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-271">Being primordial means that this resource pool cannot be created or deleted by consumers of this model.</span></span> <span data-ttu-id="f8b3f-272">Toutefois, d’autres actions, modélisées ou non, peuvent affecter les caractéristiques ou la taille des pools de ressources primordiales.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-272">However, other actions, modeled or not, may affect the characteristics or size of primordial resource pools.</span></span> <span data-ttu-id="f8b3f-273">Cette propriété est héritée de la [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f8b3f-273">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f8b3f-274">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-274">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b3f-275">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-275">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-276">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8b3f-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b3f-277">Les réservations actuelles (en unités de **AllocationUnits**) sont réparties sur toutes les allocations actives à partir de ce pool.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-277">The current reservations (in units of **AllocationUnits**) spread across all active allocations from this pool.</span></span> <span data-ttu-id="f8b3f-278">Dans une configuration hiérarchique, il s’agit de la somme de toutes les réservations actuelles du pool de ressources descendantes.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-278">In a hierarchical configuration, this represents the sum of all descendant resource pool current reservations.</span></span> <span data-ttu-id="f8b3f-279">Cette propriété est héritée de la [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f8b3f-279">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f8b3f-280">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-280">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b3f-281">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-282">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8b3f-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b3f-283">Chaîne qui décrit un sous-type spécifique à l’implémentation pour ce pool.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-283">A string that describes an implementation specific sub-type for this pool.</span></span> <span data-ttu-id="f8b3f-284">Par exemple, cela peut être utilisé pour distinguer différents modèles du même type de ressource.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-284">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="f8b3f-285">Cette propriété est héritée de la [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f8b3f-285">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f8b3f-286">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-286">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b3f-287">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-287">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-288">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8b3f-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b3f-289">Type de ressource que ce pool de ressources peut allouer.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-289">The type of resource this resource pool may allocate.</span></span> <span data-ttu-id="f8b3f-290">Cette propriété est héritée de [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))et est définie sur 4 (« Memory »).</span><span class="sxs-lookup"><span data-stu-id="f8b3f-290">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to 4 ("Memory").</span></span>

</dd> <dt>

<span data-ttu-id="f8b3f-291">**État**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-291">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b3f-292">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-293">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8b3f-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b3f-294">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-294">The current status of the object.</span></span> <span data-ttu-id="f8b3f-295">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-295">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f8b3f-296">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-296">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b3f-297">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-297">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f8b3f-298">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8b3f-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b3f-299">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="f8b3f-299">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="f8b3f-300">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f8b3f-300">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8b3f-301">Notes</span><span class="sxs-lookup"><span data-stu-id="f8b3f-301">Remarks</span></span>

<span data-ttu-id="f8b3f-302">L’accès à la classe **MSVM \_ ProcessorPool** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="f8b3f-302">Access to the **Msvm\_ProcessorPool** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f8b3f-303">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f8b3f-303">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8b3f-304">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8b3f-304">Requirements</span></span>



| <span data-ttu-id="f8b3f-305">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8b3f-305">Requirement</span></span> | <span data-ttu-id="f8b3f-306">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8b3f-306">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8b3f-307">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8b3f-307">Minimum supported client</span></span><br/> | <span data-ttu-id="f8b3f-308">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8b3f-308">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f8b3f-309">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8b3f-309">Minimum supported server</span></span><br/> | <span data-ttu-id="f8b3f-310">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8b3f-310">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f8b3f-311">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f8b3f-311">Namespace</span></span><br/>                | <span data-ttu-id="f8b3f-312">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="f8b3f-312">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f8b3f-313">MOF</span><span class="sxs-lookup"><span data-stu-id="f8b3f-313">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8b3f-314"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8b3f-314"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8b3f-315">DLL</span><span class="sxs-lookup"><span data-stu-id="f8b3f-315">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8b3f-316"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f8b3f-316"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f8b3f-317">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8b3f-317">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8b3f-318">**\_RESOURCEPOOL CIM**</span><span class="sxs-lookup"><span data-stu-id="f8b3f-318">**CIM\_ResourcePool**</span></span>](cim-resourcepool.md)
</dt> <dt>

<span data-ttu-id="f8b3f-319">[**\_RESOURCEPOOL CIM**](/previous-versions//cc136903(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f8b3f-319">[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f8b3f-320">Classes de processeur</span><span class="sxs-lookup"><span data-stu-id="f8b3f-320">Processor Classes</span></span>](processor-classes.md)
</dt> </dl>

 

