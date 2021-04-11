---
description: Décrit un type de ressource virtuelle disponible pour une utilisation dans des ordinateurs virtuels.
ms.assetid: A93D990E-D921-4113-8D88-218D0F84EFA0
title: Classe Msvm_ResourcePool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePool
- Msvm_ResourcePool.InstanceID
- Msvm_ResourcePool.Caption
- Msvm_ResourcePool.Description
- Msvm_ResourcePool.ElementName
- Msvm_ResourcePool.InstallDate
- Msvm_ResourcePool.Name
- Msvm_ResourcePool.OperationalStatus
- Msvm_ResourcePool.StatusDescriptions
- Msvm_ResourcePool.Status
- Msvm_ResourcePool.HealthState
- Msvm_ResourcePool.CommunicationStatus
- Msvm_ResourcePool.DetailedStatus
- Msvm_ResourcePool.OperatingStatus
- Msvm_ResourcePool.PrimaryStatus
- Msvm_ResourcePool.PoolID
- Msvm_ResourcePool.Primordial
- Msvm_ResourcePool.Capacity
- Msvm_ResourcePool.Reserved
- Msvm_ResourcePool.ResourceType
- Msvm_ResourcePool.OtherResourceType
- Msvm_ResourcePool.ResourceSubType
- Msvm_ResourcePool.AllocationUnits
- Msvm_ResourcePool.ConsumedResourceUnits
- Msvm_ResourcePool.CurrentlyConsumedResource
- Msvm_ResourcePool.MaxConsumableResource
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7c45f67a3e1b7c2b4b5291b24beddcdd4cf5e964
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203412"
---
# <a name="msvm_resourcepool-class"></a><span data-ttu-id="5f145-103">MSVM \_ ResourcePool, classe</span><span class="sxs-lookup"><span data-stu-id="5f145-103">Msvm\_ResourcePool class</span></span>

<span data-ttu-id="5f145-104">Décrit un type de ressource virtuelle disponible pour une utilisation dans des ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="5f145-104">Describes a type of virtual resource available for use in virtual machines.</span></span> <span data-ttu-id="5f145-105">Le pool de ressources agrège les ressources physiques et est utilisé pour allouer des ressources aux ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="5f145-105">The resource pool aggregates physical resources and is used to allocate resources to virtual machines.</span></span> <span data-ttu-id="5f145-106">Dans Hyper-V, tous les pools de ressources sont primordials et il existe exactement un pool pour chaque type de ressource spécifique qui peut être alloué à un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="5f145-106">In Hyper-V, all resource pools are primordial, and there is exactly one pool for each specific type of resource which may be allocated to a virtual machine.</span></span>

<span data-ttu-id="5f145-107">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="5f145-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f145-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f145-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourcePool : CIM_ResourcePool
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

## <a name="members"></a><span data-ttu-id="5f145-109">Membres</span><span class="sxs-lookup"><span data-stu-id="5f145-109">Members</span></span>

<span data-ttu-id="5f145-110">La classe **MSVM \_ ResourcePool** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5f145-110">The **Msvm\_ResourcePool** class has these types of members:</span></span>

-   [<span data-ttu-id="5f145-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5f145-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5f145-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5f145-112">Properties</span></span>

<span data-ttu-id="5f145-113">La classe **MSVM \_ ResourcePool** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="5f145-113">The **Msvm\_ResourcePool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5f145-114">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="5f145-114">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f145-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5f145-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f145-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f145-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f145-117">Unités d’allocation utilisées par le pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="5f145-117">The units of allocation used by the resource pool.</span></span> <span data-ttu-id="5f145-118">Cette propriété est héritée de la [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85))et est définie sur « mégaoctet ».</span><span class="sxs-lookup"><span data-stu-id="5f145-118">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to "Megabyte".</span></span>

</dd> <dt>

<span data-ttu-id="5f145-119">**Capacité**</span><span class="sxs-lookup"><span data-stu-id="5f145-119">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f145-120">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5f145-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5f145-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f145-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f145-122">Quantité maximale (en unités de **AllocationUnits**) de réservations actives que le pool de ressources peut prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="5f145-122">The maximum amount (in units of **AllocationUnits**) of active reservations that the resource pool can support.</span></span> <span data-ttu-id="5f145-123">Cette propriété est héritée de la [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5f145-123">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5f145-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5f145-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f145-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5f145-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f145-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f145-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f145-127">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5f145-127">A short description of the object.</span></span> <span data-ttu-id="5f145-128">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5f145-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5f145-129">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="5f145-129">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f145-130">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5f145-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f145-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f145-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f145-132">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="5f145-132">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="5f145-133">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="5f145-133">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5f145-134">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5f145-134">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5f145-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="5f145-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-136"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="5f145-136"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-137"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="5f145-137"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-138"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="5f145-138"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-139"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="5f145-139"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-140"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="5f145-140"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-141"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="5f145-141"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5f145-142">)</span><span class="sxs-lookup"><span data-stu-id="5f145-142">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5f145-143">**ConsumedResourceUnits**</span><span class="sxs-lookup"><span data-stu-id="5f145-143">**ConsumedResourceUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f145-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5f145-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f145-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f145-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f145-146">Spécifie les unités pour les propriétés **MaxConsumableResource** et **CurrentlyConsumedResource** .</span><span class="sxs-lookup"><span data-stu-id="5f145-146">Specifies the units for the **MaxConsumableResource** and the **CurrentlyConsumedResource** properties.</span></span>

</dd> <dt>

<span data-ttu-id="5f145-147">**CurrentlyConsumedResource**</span><span class="sxs-lookup"><span data-stu-id="5f145-147">**CurrentlyConsumedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f145-148">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5f145-148">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5f145-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f145-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f145-150">Spécifie la quantité de ressources que le pool de ressources présente actuellement aux consommateurs.</span><span class="sxs-lookup"><span data-stu-id="5f145-150">Specifies the amount of resource that the resource pool currently presents to consumers.</span></span> <span data-ttu-id="5f145-151">Cette propriété est différente de la propriété **réservée** en ce qu’elle décrit la vue consommateurs de la ressource, tandis que la propriété **réservée** décrit la vue des producteurs de la ressource.</span><span class="sxs-lookup"><span data-stu-id="5f145-151">This property is different from the **Reserved** property in that it describes the consumers view of the resource, while the **Reserved** property describes the producers view of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="5f145-152">**Description**</span><span class="sxs-lookup"><span data-stu-id="5f145-152">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f145-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5f145-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f145-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f145-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f145-155">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="5f145-155">A description of the object.</span></span> <span data-ttu-id="5f145-156">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5f145-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5f145-157">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="5f145-157">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f145-158">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5f145-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f145-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f145-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f145-160">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="5f145-160">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="5f145-161">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="5f145-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5f145-162">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5f145-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5f145-163"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="5f145-163"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-164"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="5f145-164"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-165"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="5f145-165"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-166"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="5f145-166"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-167"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="5f145-167"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-168"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="5f145-168"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-169"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="5f145-169"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-170"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="5f145-170"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5f145-171">)</span><span class="sxs-lookup"><span data-stu-id="5f145-171">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5f145-172">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5f145-172">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f145-173">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5f145-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f145-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f145-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f145-175">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5f145-175">A display name for the object.</span></span> <span data-ttu-id="5f145-176">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5f145-176">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5f145-177">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="5f145-177">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f145-178">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5f145-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f145-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f145-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f145-180">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="5f145-180">The current health of the element.</span></span> <span data-ttu-id="5f145-181">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5f145-181">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5f145-182">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5f145-182">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f145-183">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5f145-183">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5f145-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f145-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f145-185">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5f145-185">The date and time when the object was installed.</span></span> <span data-ttu-id="5f145-186">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="5f145-186">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="5f145-187">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5f145-187">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5f145-188">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5f145-188">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f145-189">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5f145-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f145-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f145-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f145-191">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="5f145-191">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5f145-192">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="5f145-192">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="5f145-193">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5f145-193">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5f145-194">**MaxConsumableResource**</span><span class="sxs-lookup"><span data-stu-id="5f145-194">**MaxConsumableResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f145-195">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5f145-195">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5f145-196">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f145-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f145-197">Spécifie la quantité maximale de ressources consommables que le pool de ressources peut présenter aux consommateurs.</span><span class="sxs-lookup"><span data-stu-id="5f145-197">Specifies the maximum amount of consumable resource that the resource pool can present to consumers.</span></span> <span data-ttu-id="5f145-198">Cette propriété est différente de la propriété **Capacity** en ce qu’elle décrit la vue consommateurs de la ressource, tandis que la propriété **Capacity** décrit la vue des producteurs de la ressource.</span><span class="sxs-lookup"><span data-stu-id="5f145-198">This property is different from the **Capacity** property in that it describes the consumers view of the resource, while the **Capacity** property describes the producers view of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="5f145-199">**Nom**</span><span class="sxs-lookup"><span data-stu-id="5f145-199">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f145-200">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5f145-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f145-201">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f145-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f145-202">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="5f145-202">The label by which the object is known.</span></span> <span data-ttu-id="5f145-203">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5f145-203">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5f145-204">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="5f145-204">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f145-205">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5f145-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f145-206">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f145-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f145-207">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="5f145-207">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="5f145-208">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="5f145-208">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5f145-209">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5f145-209">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5f145-210"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="5f145-210"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-211"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="5f145-211"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-212"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="5f145-212"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-213"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="5f145-213"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-214"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="5f145-214"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-215"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="5f145-215"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-216"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="5f145-216"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-217"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="5f145-217"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-218"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="5f145-218"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-219"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="5f145-219"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-220"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="5f145-220"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-221"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="5f145-221"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-222"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="5f145-222"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-223"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="5f145-223"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-224"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="5f145-224"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-225"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="5f145-225"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-226"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="5f145-226"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="5f145-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="5f145-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5f145-229">)</span><span class="sxs-lookup"><span data-stu-id="5f145-229">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5f145-230">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="5f145-230">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f145-231">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5f145-231">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5f145-232">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f145-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f145-233">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span><span class="sxs-lookup"><span data-stu-id="5f145-233">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="5f145-234">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5f145-234">The current statuses of the object.</span></span> <span data-ttu-id="5f145-235">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5f145-235">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="5f145-236">Si aucune condition liée à la qualité de service n’a été détectée, l’état principal (OperationalStatus \[ 0 \] ) est défini sur OK (2).</span><span class="sxs-lookup"><span data-stu-id="5f145-236">If no QoS related conditions have been detected, the primary status (OperationalStatus\[0\]) is set to OK (2).</span></span> <span data-ttu-id="5f145-237">Dans le cas contraire, l’état principal est défini sur détérioré (3) et une ou plusieurs valeurs d’État secondaires sont remplies dans le tableau, en commençant à l’index 1, qui signale des conditions plus spécifiques, en fonction de cette table.</span><span class="sxs-lookup"><span data-stu-id="5f145-237">Otherwise, the primary status is set to Degraded (3), and one or more secondary status values is filled in the array, starting at index 1, which report more specific conditions, according to this table.</span></span>



| <span data-ttu-id="5f145-238">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f145-238">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="5f145-239">Description</span><span class="sxs-lookup"><span data-stu-id="5f145-239">Description</span></span>                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f145-240"><span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> Débit insuffisant (32788)</span><span class="sxs-lookup"><span data-stu-id="5f145-240"><span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> Insufficient Throughput  (32788)</span></span><br/> | <span data-ttu-id="5f145-241">Au moins un des disques virtuels alloués à partir du pool signale actuellement un état de débit insuffisant.</span><span class="sxs-lookup"><span data-stu-id="5f145-241">At least one of the virtual disks allocated from the pool is currently reporting an  Insufficient Throughput  status.</span></span><br/> |



 

<span data-ttu-id="5f145-242">Le fournisseur WMI Hyper-V déclenche un événement [**MSVM \_ StorageAlert**](msvm-storagealert.md) chaque fois que le OperationalStatus de la classe **\_ ResourcePool MSVM** change.</span><span class="sxs-lookup"><span data-stu-id="5f145-242">The Hyper-V WMI provider raises an [**Msvm\_StorageAlert**](msvm-storagealert.md) event each time the OperationalStatus of the **Msvm\_ResourcePool** class changes.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5f145-243">**OK** (2)</span><span class="sxs-lookup"><span data-stu-id="5f145-243">**OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5f145-244">**Détérioré** (3)</span><span class="sxs-lookup"><span data-stu-id="5f145-244">**Degraded** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="5f145-245">**Erreur non récupérable** (7)</span><span class="sxs-lookup"><span data-stu-id="5f145-245">**Non-Recoverable Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5f145-246">**Aucun contact** (12)</span><span class="sxs-lookup"><span data-stu-id="5f145-246">**No Contact** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="5f145-247">**Perte de communication** (13)</span><span class="sxs-lookup"><span data-stu-id="5f145-247">**Lost Communication** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>

<span data-ttu-id="5f145-248">**Incompatibilité de protocole** (32775)</span><span class="sxs-lookup"><span data-stu-id="5f145-248">**Protocol Mismatch** (32775)</span></span>


</dt> <dd></dd> <dt>

<span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>

<span data-ttu-id="5f145-249">**Débit insuffisant** (32788)</span><span class="sxs-lookup"><span data-stu-id="5f145-249">**Insufficient Throughput** (32788)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5f145-250">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="5f145-250">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f145-251">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5f145-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f145-252">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f145-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f145-253">Chaîne qui décrit le type de ressource lorsqu’une valeur bien définie n’est pas disponible et que [**resourceType**](msvm-processorpool.md) a la valeur 0 (« other »).</span><span class="sxs-lookup"><span data-stu-id="5f145-253">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorpool.md) is set to 0 ("Other").</span></span> <span data-ttu-id="5f145-254">Cette propriété est héritée de [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)) et a la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="5f145-254">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)) and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5f145-255">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="5f145-255">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f145-256">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5f145-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f145-257">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f145-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f145-258">Cette valeur est référencée par les instances [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) qui ont été allouées à partir de ce pool.</span><span class="sxs-lookup"><span data-stu-id="5f145-258">This value is referenced by the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) instances which were allocated from this pool.</span></span> <span data-ttu-id="5f145-259">Cette propriété est héritée de la [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85))et est toujours définie sur « Microsoft :*GUID* \\ root ».</span><span class="sxs-lookup"><span data-stu-id="5f145-259">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is always set to "Microsoft:*GUID*\\Root".</span></span>

</dd> <dt>

<span data-ttu-id="5f145-260">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="5f145-260">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f145-261">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5f145-261">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f145-262">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f145-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f145-263">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="5f145-263">Provides high level status information.</span></span> <span data-ttu-id="5f145-264">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="5f145-264">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="5f145-265">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="5f145-265">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5f145-266">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5f145-266">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5f145-267"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="5f145-267"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-268"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="5f145-268"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-269"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="5f145-269"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-270"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="5f145-270"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-271"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="5f145-271"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5f145-272"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="5f145-272"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5f145-273">)</span><span class="sxs-lookup"><span data-stu-id="5f145-273">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5f145-274">**Primordial**</span><span class="sxs-lookup"><span data-stu-id="5f145-274">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f145-275">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5f145-275">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5f145-276">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f145-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f145-277">**True** si ce pool de ressources est la base à partir de laquelle les ressources sont dessinées et retournées dans l’activité de gestion des ressources. Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="5f145-277">**True** if this resource pool is the base from which resources are drawn and returned in the activity of resource management; otherwise, **False**.</span></span> <span data-ttu-id="5f145-278">Si primordial signifie que ce pool de ressources ne peut pas être créé ou supprimé par les consommateurs de ce modèle.</span><span class="sxs-lookup"><span data-stu-id="5f145-278">Being primordial means that this resource pool cannot be created or deleted by consumers of this model.</span></span> <span data-ttu-id="5f145-279">Toutefois, d’autres actions, modélisées ou non, peuvent affecter les caractéristiques ou la taille des pools de ressources primordiales.</span><span class="sxs-lookup"><span data-stu-id="5f145-279">However, other actions, modeled or not, may affect the characteristics or size of primordial resource pools.</span></span> <span data-ttu-id="5f145-280">Cette propriété est héritée de la [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5f145-280">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5f145-281">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="5f145-281">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f145-282">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5f145-282">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5f145-283">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f145-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f145-284">Les réservations actuelles (en unités de **AllocationUnits**) sont réparties sur toutes les allocations actives à partir de ce pool.</span><span class="sxs-lookup"><span data-stu-id="5f145-284">The current reservations (in units of **AllocationUnits**) spread across all active allocations from this pool.</span></span> <span data-ttu-id="5f145-285">Dans une configuration hiérarchique, il s’agit de la somme de toutes les réservations actuelles du pool de ressources descendantes.</span><span class="sxs-lookup"><span data-stu-id="5f145-285">In a hierarchical configuration, this represents the sum of all descendant resource pool current reservations.</span></span> <span data-ttu-id="5f145-286">Cette propriété est héritée de la [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5f145-286">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5f145-287">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="5f145-287">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f145-288">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5f145-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f145-289">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f145-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f145-290">Chaîne qui décrit un sous-type spécifique à l’implémentation pour ce pool.</span><span class="sxs-lookup"><span data-stu-id="5f145-290">A string that describes an implementation specific sub-type for this pool.</span></span> <span data-ttu-id="5f145-291">Par exemple, cela peut être utilisé pour distinguer différents modèles du même type de ressource.</span><span class="sxs-lookup"><span data-stu-id="5f145-291">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="5f145-292">Cette propriété est héritée de la [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5f145-292">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5f145-293">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="5f145-293">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f145-294">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5f145-294">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f145-295">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f145-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f145-296">Type de ressource que ce pool de ressources peut allouer.</span><span class="sxs-lookup"><span data-stu-id="5f145-296">The type of resource this resource pool may allocate.</span></span> <span data-ttu-id="5f145-297">Cette propriété est héritée de [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))et est définie sur 4 (« Memory »).</span><span class="sxs-lookup"><span data-stu-id="5f145-297">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to 4 ("Memory").</span></span>

</dd> <dt>

<span data-ttu-id="5f145-298">**État**</span><span class="sxs-lookup"><span data-stu-id="5f145-298">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f145-299">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5f145-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f145-300">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f145-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f145-301">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5f145-301">The current status of the object.</span></span> <span data-ttu-id="5f145-302">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="5f145-302">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5f145-303">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="5f145-303">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f145-304">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="5f145-304">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5f145-305">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f145-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f145-306">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="5f145-306">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="5f145-307">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5f145-307">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5f145-308">Notes</span><span class="sxs-lookup"><span data-stu-id="5f145-308">Remarks</span></span>

<span data-ttu-id="5f145-309">L’accès à la classe **MSVM \_ ResourcePool** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="5f145-309">Access to the **Msvm\_ResourcePool** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="5f145-310">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="5f145-310">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="5f145-311">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f145-311">Requirements</span></span>



| <span data-ttu-id="5f145-312">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f145-312">Requirement</span></span> | <span data-ttu-id="5f145-313">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f145-313">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f145-314">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f145-314">Minimum supported client</span></span><br/> | <span data-ttu-id="5f145-315">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f145-315">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5f145-316">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f145-316">Minimum supported server</span></span><br/> | <span data-ttu-id="5f145-317">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f145-317">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5f145-318">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5f145-318">Namespace</span></span><br/>                | <span data-ttu-id="5f145-319">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="5f145-319">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5f145-320">MOF</span><span class="sxs-lookup"><span data-stu-id="5f145-320">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f145-321"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f145-321"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f145-322">DLL</span><span class="sxs-lookup"><span data-stu-id="5f145-322">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f145-323"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5f145-323"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5f145-324">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f145-324">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f145-325">**\_RESOURCEPOOL CIM**</span><span class="sxs-lookup"><span data-stu-id="5f145-325">**CIM\_ResourcePool**</span></span>](cim-resourcepool.md)
</dt> <dt>

<span data-ttu-id="5f145-326">[**\_RESOURCEPOOL CIM**](/previous-versions//cc136903(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5f145-326">[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5f145-327">**MSVM \_ ResourcePool (v1)**</span><span class="sxs-lookup"><span data-stu-id="5f145-327">**Msvm\_ResourcePool (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-resourcepool)
</dt> <dt>

[<span data-ttu-id="5f145-328">**MSVM \_ StorageAlert**</span><span class="sxs-lookup"><span data-stu-id="5f145-328">**Msvm\_StorageAlert**</span></span>](msvm-storagealert.md)
</dt> <dt>

[<span data-ttu-id="5f145-329">Classes de gestion des ressources</span><span class="sxs-lookup"><span data-stu-id="5f145-329">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

