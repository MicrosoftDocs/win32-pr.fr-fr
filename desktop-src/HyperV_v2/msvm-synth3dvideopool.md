---
description: Contient des informations sur les unités de traitement graphique (GPU) vidéo 3D synthétiques disponibles sur le système hôte.
ms.assetid: 771A42C3-4888-49DF-A389-161A2D0E3DBD
title: Classe Msvm_Synth3dVideoPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synth3dVideoPool
- Msvm_Synth3dVideoPool.InstanceID
- Msvm_Synth3dVideoPool.Caption
- Msvm_Synth3dVideoPool.Description
- Msvm_Synth3dVideoPool.ElementName
- Msvm_Synth3dVideoPool.InstallDate
- Msvm_Synth3dVideoPool.Name
- Msvm_Synth3dVideoPool.OperationalStatus
- Msvm_Synth3dVideoPool.StatusDescriptions
- Msvm_Synth3dVideoPool.Status
- Msvm_Synth3dVideoPool.HealthState
- Msvm_Synth3dVideoPool.CommunicationStatus
- Msvm_Synth3dVideoPool.DetailedStatus
- Msvm_Synth3dVideoPool.OperatingStatus
- Msvm_Synth3dVideoPool.PrimaryStatus
- Msvm_Synth3dVideoPool.PoolID
- Msvm_Synth3dVideoPool.Primordial
- Msvm_Synth3dVideoPool.Capacity
- Msvm_Synth3dVideoPool.Reserved
- Msvm_Synth3dVideoPool.ResourceType
- Msvm_Synth3dVideoPool.OtherResourceType
- Msvm_Synth3dVideoPool.ResourceSubType
- Msvm_Synth3dVideoPool.AllocationUnits
- Msvm_Synth3dVideoPool.ConsumedResourceUnits
- Msvm_Synth3dVideoPool.CurrentlyConsumedResource
- Msvm_Synth3dVideoPool.MaxConsumableResource
- Msvm_Synth3dVideoPool.Is3dVideoSupported
- Msvm_Synth3dVideoPool.IsSLATCapable
- Msvm_Synth3dVideoPool.IsGPUCapable
- Msvm_Synth3dVideoPool.DirectXVersion
- Msvm_Synth3dVideoPool.RequiredMinimumDirectXVersion
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1afad0f1b2e80a747bb518cb3eafc75d494de62a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951647"
---
# <a name="msvm_synth3dvideopool-class"></a><span data-ttu-id="00211-103">MSVM \_ Synth3dVideoPool, classe</span><span class="sxs-lookup"><span data-stu-id="00211-103">Msvm\_Synth3dVideoPool class</span></span>

<span data-ttu-id="00211-104">Contient des informations sur les unités de traitement graphique (GPU) vidéo 3D synthétiques disponibles sur le système hôte.</span><span class="sxs-lookup"><span data-stu-id="00211-104">Contains information about the synthetic 3-D video graphics processing units (GPUs) available on the host system.</span></span> <span data-ttu-id="00211-105">Cette classe est utilisée uniquement avec les systèmes hôtes qui prennent en charge RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="00211-105">This class is only used with host systems that support RemoteFX.</span></span>

<span data-ttu-id="00211-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="00211-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="00211-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00211-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synth3dVideoPool : CIM_ResourcePool
{
  string   InstanceID;
  string   Caption = "3D Display Controller Resource Pool";
  string   Description = "Resource pool used to allocate synthetic 3D video controller resources to a virtual machine.";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[] = {"OK"};
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   PoolID;
  boolean  Primordial = True;
  uint64   Capacity;
  uint64   Reserved = 0;
  uint16   ResourceType;
  string   OtherResourceType;
  string   ResourceSubType = "Microsoft:Hyper-V:Synthetic 3D Display Controller";
  string   AllocationUnits = "count";
  string   ConsumedResourceUnits = "count";
  uint64   CurrentlyConsumedResource;
  uint64   MaxConsumableResource;
  boolean  Is3dVideoSupported;
  boolean  IsSLATCapable;
  boolean  IsGPUCapable;
  string   DirectXVersion;
  string   RequiredMinimumDirectXVersion;
};
```

## <a name="members"></a><span data-ttu-id="00211-108">Membres</span><span class="sxs-lookup"><span data-stu-id="00211-108">Members</span></span>

<span data-ttu-id="00211-109">La classe **MSVM \_ Synth3dVideoPool** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="00211-109">The **Msvm\_Synth3dVideoPool** class has these types of members:</span></span>

-   [<span data-ttu-id="00211-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="00211-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="00211-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="00211-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="00211-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="00211-112">Methods</span></span>

<span data-ttu-id="00211-113">La classe **MSVM \_ Synth3dVideoPool** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="00211-113">The **Msvm\_Synth3dVideoPool** class has these methods.</span></span>



| <span data-ttu-id="00211-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="00211-114">Method</span></span>                                                                                             | <span data-ttu-id="00211-115">Description</span><span class="sxs-lookup"><span data-stu-id="00211-115">Description</span></span>                                                                               |
|:---------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00211-116">**CalculateVideoMemoryRequirements**</span><span class="sxs-lookup"><span data-stu-id="00211-116">**CalculateVideoMemoryRequirements**</span></span>](msvm-synth3dvideopool-calculatevideomemoryrequirements.md) | <span data-ttu-id="00211-117">Calcule la quantité de mémoire vidéo requise pour une machine virtuelle RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="00211-117">Calculates the amount of video memory required for a RemoteFX virtual machine.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="00211-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="00211-118">Properties</span></span>

<span data-ttu-id="00211-119">La classe **MSVM \_ Synth3dVideoPool** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="00211-119">The **Msvm\_Synth3dVideoPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="00211-120">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="00211-120">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00211-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00211-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00211-123">Unités d’allocation utilisées par le pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="00211-123">The units of allocation used by the resource pool.</span></span> <span data-ttu-id="00211-124">Cette propriété est héritée de la [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="00211-124">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="00211-125">**Capacité**</span><span class="sxs-lookup"><span data-stu-id="00211-125">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-126">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="00211-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="00211-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00211-128">Quantité maximale (en unités de **AllocationUnits**) de réservations actives que le pool de ressources peut prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="00211-128">The maximum amount (in units of **AllocationUnits**) of active reservations that the resource pool can support.</span></span> <span data-ttu-id="00211-129">Cette propriété est héritée de la [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="00211-129">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="00211-130">**Caption**</span><span class="sxs-lookup"><span data-stu-id="00211-130">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00211-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00211-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00211-133">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="00211-133">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="00211-134">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="00211-134">A short description of the object.</span></span> <span data-ttu-id="00211-135">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="00211-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="00211-136">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="00211-136">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-137">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="00211-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="00211-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00211-139">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="00211-139">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="00211-140">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="00211-140">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="00211-141">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="00211-141">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="00211-142"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="00211-142"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="00211-143"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="00211-143"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="00211-144"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="00211-144"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="00211-145"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="00211-145"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="00211-146"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="00211-146"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="00211-147"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="00211-147"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="00211-148"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="00211-148"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="00211-149">)</span><span class="sxs-lookup"><span data-stu-id="00211-149">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="00211-150">**ConsumedResourceUnits**</span><span class="sxs-lookup"><span data-stu-id="00211-150">**ConsumedResourceUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-151">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00211-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00211-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00211-153">Spécifie les unités pour les propriétés **MaxConsumableResource** et **CurrentlyConsumedResource** .</span><span class="sxs-lookup"><span data-stu-id="00211-153">Specifies the units for the **MaxConsumableResource** and the **CurrentlyConsumedResource** properties.</span></span> <span data-ttu-id="00211-154">Cette propriété est héritée de la [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="00211-154">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="00211-155">**CurrentlyConsumedResource**</span><span class="sxs-lookup"><span data-stu-id="00211-155">**CurrentlyConsumedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-156">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="00211-156">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="00211-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00211-158">Spécifie la quantité de ressources que le pool de ressources présente actuellement aux consommateurs.</span><span class="sxs-lookup"><span data-stu-id="00211-158">Specifies the amount of resource that the resource pool currently presents to consumers.</span></span> <span data-ttu-id="00211-159">Cette propriété est différente de la propriété **réservée** en ce qu’elle décrit la vue consommateurs de la ressource, tandis que la propriété **réservée** décrit la vue des producteurs de la ressource.</span><span class="sxs-lookup"><span data-stu-id="00211-159">This property is different from the **Reserved** property in that it describes the consumers view of the resource, while the **Reserved** property describes the producers view of the resource.</span></span> <span data-ttu-id="00211-160">Cette propriété est héritée de la [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="00211-160">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="00211-161">**Description**</span><span class="sxs-lookup"><span data-stu-id="00211-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00211-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00211-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00211-164">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="00211-164">A description of the object.</span></span> <span data-ttu-id="00211-165">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="00211-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="00211-166">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="00211-166">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-167">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="00211-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="00211-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00211-169">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="00211-169">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="00211-170">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="00211-170">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="00211-171">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="00211-171">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="00211-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="00211-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="00211-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="00211-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="00211-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="00211-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="00211-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="00211-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="00211-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="00211-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="00211-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="00211-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="00211-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="00211-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="00211-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="00211-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="00211-180">)</span><span class="sxs-lookup"><span data-stu-id="00211-180">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="00211-181">**DirectXVersion**</span><span class="sxs-lookup"><span data-stu-id="00211-181">**DirectXVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-182">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00211-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00211-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00211-184">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="00211-184">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="00211-185">Spécifie la version de DirectX la plus ancienne prise en charge par les cartes au sein du pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="00211-185">Specifies the lowest version of DirectX that is supported by the cards within the resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="00211-186">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="00211-186">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-187">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00211-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00211-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00211-189">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="00211-189">A display name for the object.</span></span> <span data-ttu-id="00211-190">Cette propriété permet à chaque instance de définir un nom complet en plus de ses propriétés de clé, données d’identité et informations de description.</span><span class="sxs-lookup"><span data-stu-id="00211-190">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="00211-191">La propriété [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) de la **classe \_ ManagedSystemElement CIM** est également définie comme un nom complet, mais elle est souvent sous-classée comme clé.</span><span class="sxs-lookup"><span data-stu-id="00211-191">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name, but it is often subclassed to be a Key.</span></span> <span data-ttu-id="00211-192">Il n’est pas raisonnable que la même propriété puisse transmettre à la fois l’identité et un nom d’affichage, sans incohérence.</span><span class="sxs-lookup"><span data-stu-id="00211-192">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="00211-193">Où le [**nom**](msvm-keyboard.md) existe et n’est pas une clé (par exemple, pour les instances de LogicalDevice), les mêmes informations peuvent être présentes dans les propriétés **Name** et **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="00211-193">Where [**Name**](msvm-keyboard.md) exists and is not a Key (such as for instances of LogicalDevice), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="00211-194">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="00211-194">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="00211-195">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="00211-195">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-196">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="00211-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="00211-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00211-198">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="00211-198">The current health of the element.</span></span> <span data-ttu-id="00211-199">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="00211-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="00211-200">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="00211-200">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-201">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="00211-201">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="00211-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00211-203">Date et heure de création de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="00211-203">The date and time at which the virtual machine was created.</span></span> <span data-ttu-id="00211-204">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="00211-204">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="00211-205">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="00211-205">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-206">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00211-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00211-207">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00211-208">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="00211-208">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="00211-209">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="00211-209">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="00211-210">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="00211-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="00211-211">**Is3dVideoSupported**</span><span class="sxs-lookup"><span data-stu-id="00211-211">**Is3dVideoSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-212">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="00211-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="00211-213">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00211-214">Spécifie si la vidéo 3D est prise en charge par le système hôte.</span><span class="sxs-lookup"><span data-stu-id="00211-214">Specifies whether 3-D video is supported by the host system.</span></span> <span data-ttu-id="00211-215">Contient une valeur différente de zéro si la vidéo 3D est prise en charge, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="00211-215">Contains a nonzero value if 3-D video is supported, or zero otherwise.</span></span> <span data-ttu-id="00211-216">Pour prendre en charge la vidéo 3D, l’hôte RemoteFX doit posséder des fonctionnalités de traduction d’adresses de second niveau (SLAT) et disposer d’au moins un GPU physique qui prend en charge RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="00211-216">To support 3-D video, the RemoteFX host must have second level address translation (SLAT) capabilities and have at least one physical GPU that supports RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="00211-217">**IsGPUCapable**</span><span class="sxs-lookup"><span data-stu-id="00211-217">**IsGPUCapable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-218">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="00211-218">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="00211-219">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00211-220">Spécifie si l’hôte possède des GPU qui prennent en charge RemoteFX et si leurs versions DirectX satisfont à la configuration minimale requise.</span><span class="sxs-lookup"><span data-stu-id="00211-220">Specifies whether the host has GPUs that support RemoteFX and whether their DirectX versions meet the minimum requirement.</span></span>

</dd> <dt>

<span data-ttu-id="00211-221">**IsSLATCapable**</span><span class="sxs-lookup"><span data-stu-id="00211-221">**IsSLATCapable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-222">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="00211-222">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="00211-223">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00211-224">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) (« aucune valeur »)</span><span class="sxs-lookup"><span data-stu-id="00211-224">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="00211-225">Spécifie si l’hôte dispose d’un processeur compatible avec la traduction d’adresses de second niveau (SLAT).</span><span class="sxs-lookup"><span data-stu-id="00211-225">Specifies whether the host has a second level address translation (SLAT) capable CPU.</span></span>

> [!Note]  
> <span data-ttu-id="00211-226">Déconseillé dans Windows 10, version 1703 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="00211-226">Deprecated in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="00211-227">**MaxConsumableResource**</span><span class="sxs-lookup"><span data-stu-id="00211-227">**MaxConsumableResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-228">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="00211-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="00211-229">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00211-230">Spécifie la quantité maximale de ressources consommables que le pool de ressources peut présenter aux consommateurs.</span><span class="sxs-lookup"><span data-stu-id="00211-230">Specifies the maximum amount of consumable resource that the resource pool can present to consumers.</span></span> <span data-ttu-id="00211-231">Cette propriété est différente de la propriété **Capacity** en ce qu’elle décrit la vue consommateurs de la ressource, tandis que la propriété **Capacity** décrit la vue des producteurs de la ressource.</span><span class="sxs-lookup"><span data-stu-id="00211-231">This property is different from the **Capacity** property in that it describes the consumers view of the resource, while the **Capacity** property describes the producers view of the resource.</span></span> <span data-ttu-id="00211-232">Cette propriété est héritée de la [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="00211-232">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="00211-233">**Nom**</span><span class="sxs-lookup"><span data-stu-id="00211-233">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-234">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00211-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00211-235">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00211-236">Qualificateurs : **MaxLen** (1024)</span><span class="sxs-lookup"><span data-stu-id="00211-236">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="00211-237">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="00211-237">The label by which the object is known.</span></span> <span data-ttu-id="00211-238">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="00211-238">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="00211-239">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="00211-239">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="00211-240">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="00211-240">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-241">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="00211-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="00211-242">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00211-243">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="00211-243">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="00211-244">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="00211-244">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="00211-245">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="00211-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="00211-246"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="00211-246"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="00211-247"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="00211-247"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="00211-248"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="00211-248"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="00211-249"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="00211-249"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="00211-250"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="00211-250"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="00211-251"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="00211-251"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="00211-252"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="00211-252"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="00211-253"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="00211-253"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="00211-254"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="00211-254"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="00211-255"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="00211-255"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="00211-256"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="00211-256"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="00211-257"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="00211-257"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="00211-258"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="00211-258"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="00211-259"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="00211-259"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="00211-260"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="00211-260"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="00211-261"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="00211-261"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="00211-262"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="00211-262"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="00211-263"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="00211-263"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="00211-264"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="00211-264"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="00211-265">)</span><span class="sxs-lookup"><span data-stu-id="00211-265">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="00211-266">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="00211-266">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-267">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="00211-267">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="00211-268">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00211-269">État actuel de l’élément.</span><span class="sxs-lookup"><span data-stu-id="00211-269">The current status of the element.</span></span> <span data-ttu-id="00211-270">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="00211-270">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 (OK).</span></span> <span data-ttu-id="00211-271">Hyper-V n’utilise jamais le premier élément de ce tableau.</span><span class="sxs-lookup"><span data-stu-id="00211-271">Hyper-V will only ever use the first element of this array.</span></span>

</dd> <dt>

<span data-ttu-id="00211-272">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="00211-272">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-273">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00211-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00211-274">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00211-275">Chaîne qui décrit le type de ressource lorsqu’une valeur bien définie n’est pas disponible et que [**resourceType**](msvm-processorpool.md) a la valeur 0 (« other »).</span><span class="sxs-lookup"><span data-stu-id="00211-275">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorpool.md) is set to 0 ("Other").</span></span> <span data-ttu-id="00211-276">Cette propriété est héritée de [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))et a la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="00211-276">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="00211-277">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="00211-277">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-278">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00211-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00211-279">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00211-280">Cette valeur est référencée par les instances [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) qui ont été allouées à partir de ce pool.</span><span class="sxs-lookup"><span data-stu-id="00211-280">This value is referenced by the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) instances which were allocated from this pool.</span></span> <span data-ttu-id="00211-281">Cette propriété est héritée de la [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85))et est toujours définie sur « Microsoft :*GUID* \\ root ».</span><span class="sxs-lookup"><span data-stu-id="00211-281">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is always set to "Microsoft:*GUID*\\Root".</span></span>

</dd> <dt>

<span data-ttu-id="00211-282">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="00211-282">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-283">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="00211-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="00211-284">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00211-285">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="00211-285">Provides high level status information.</span></span> <span data-ttu-id="00211-286">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="00211-286">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="00211-287">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="00211-287">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="00211-288">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="00211-288">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="00211-289"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="00211-289"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="00211-290"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="00211-290"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="00211-291"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="00211-291"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="00211-292"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="00211-292"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="00211-293"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="00211-293"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="00211-294"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="00211-294"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="00211-295">)</span><span class="sxs-lookup"><span data-stu-id="00211-295">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="00211-296">**Primordial**</span><span class="sxs-lookup"><span data-stu-id="00211-296">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-297">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="00211-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="00211-298">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00211-299">**True** si ce pool de ressources est la base à partir de laquelle les ressources sont dessinées et retournées dans l’activité de gestion des ressources. Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="00211-299">**True** if this resource pool is the base from which resources are drawn and returned in the activity of resource management; otherwise, **False**.</span></span> <span data-ttu-id="00211-300">Si primordial signifie que ce pool de ressources ne peut pas être créé ou supprimé par les consommateurs de ce modèle.</span><span class="sxs-lookup"><span data-stu-id="00211-300">Being primordial means that this resource pool cannot be created or deleted by consumers of this model.</span></span> <span data-ttu-id="00211-301">Toutefois, d’autres actions, modélisées ou non, peuvent affecter les caractéristiques ou la taille des pools de ressources primordiales.</span><span class="sxs-lookup"><span data-stu-id="00211-301">However, other actions, modeled or not, may affect the characteristics or size of primordial resource pools.</span></span> <span data-ttu-id="00211-302">Cette propriété est héritée de la [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="00211-302">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="00211-303">**RequiredMinimumDirectXVersion**</span><span class="sxs-lookup"><span data-stu-id="00211-303">**RequiredMinimumDirectXVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-304">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00211-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00211-305">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00211-306">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="00211-306">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="00211-307">Spécifie la version la plus basse de DirectX requise par les cartes dans le pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="00211-307">Specifies the lowest version of DirectX that is required by the cards within the resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="00211-308">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="00211-308">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-309">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="00211-309">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="00211-310">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00211-311">Les réservations actuelles (en unités de **AllocationUnits**) sont réparties sur toutes les allocations actives à partir de ce pool.</span><span class="sxs-lookup"><span data-stu-id="00211-311">The current reservations (in units of **AllocationUnits**) spread across all active allocations from this pool.</span></span> <span data-ttu-id="00211-312">Dans une configuration hiérarchique, il s’agit de la somme de toutes les réservations actuelles du pool de ressources descendantes.</span><span class="sxs-lookup"><span data-stu-id="00211-312">In a hierarchical configuration, this represents the sum of all descendant resource pool current reservations.</span></span> <span data-ttu-id="00211-313">Cette propriété est héritée de la [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="00211-313">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="00211-314">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="00211-314">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-315">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00211-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00211-316">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00211-317">Chaîne qui décrit un sous-type spécifique à l’implémentation pour ce pool.</span><span class="sxs-lookup"><span data-stu-id="00211-317">A string that describes an implementation specific subtype for this pool.</span></span> <span data-ttu-id="00211-318">Par exemple, cela peut être utilisé pour distinguer différents modèles du même type de ressource.</span><span class="sxs-lookup"><span data-stu-id="00211-318">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="00211-319">Cette propriété est héritée de la [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="00211-319">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="00211-320">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="00211-320">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-321">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="00211-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="00211-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00211-323">Type de ressource que ce pool de ressources peut allouer.</span><span class="sxs-lookup"><span data-stu-id="00211-323">The type of resource this resource pool can allocate.</span></span> <span data-ttu-id="00211-324">Cette propriété est héritée de la [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85))et est toujours définie sur 4 (« mémoire »).</span><span class="sxs-lookup"><span data-stu-id="00211-324">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is always set to 4 ("Memory").</span></span>

</dd> <dt>

<span data-ttu-id="00211-325">**État**</span><span class="sxs-lookup"><span data-stu-id="00211-325">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-326">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00211-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00211-327">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00211-328">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="00211-328">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="00211-329">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="00211-329">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00211-330">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="00211-330">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="00211-331">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00211-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00211-332">Chaînes qui décrivent les différentes valeurs de tableau [**OperationalStatus**](msvm-bioselement.md) .</span><span class="sxs-lookup"><span data-stu-id="00211-332">Strings that describe the various [**OperationalStatus**](msvm-bioselement.md) array values.</span></span> <span data-ttu-id="00211-333">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur « OK ».</span><span class="sxs-lookup"><span data-stu-id="00211-333">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span> <span data-ttu-id="00211-334">Hyper-V n’utilise jamais le premier élément de ce tableau.</span><span class="sxs-lookup"><span data-stu-id="00211-334">Hyper-V will only ever use the first element of this array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="00211-335">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00211-335">Requirements</span></span>



| <span data-ttu-id="00211-336">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00211-336">Requirement</span></span> | <span data-ttu-id="00211-337">Valeur</span><span class="sxs-lookup"><span data-stu-id="00211-337">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00211-338">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00211-338">Minimum supported client</span></span><br/> | <span data-ttu-id="00211-339">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="00211-339">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="00211-340">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00211-340">Minimum supported server</span></span><br/> | <span data-ttu-id="00211-341">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="00211-341">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="00211-342">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="00211-342">Namespace</span></span><br/>                | <span data-ttu-id="00211-343">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="00211-343">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="00211-344">MOF</span><span class="sxs-lookup"><span data-stu-id="00211-344">MOF</span></span><br/>                      | <dl> <span data-ttu-id="00211-345"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="00211-345"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="00211-346">DLL</span><span class="sxs-lookup"><span data-stu-id="00211-346">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00211-347"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="00211-347"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="00211-348">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00211-348">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00211-349">**\_RESOURCEPOOL CIM**</span><span class="sxs-lookup"><span data-stu-id="00211-349">**CIM\_ResourcePool**</span></span>](cim-resourcepool.md)
</dt> </dl>

 

