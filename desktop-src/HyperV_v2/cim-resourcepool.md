---
description: Représente un pool de ressources, qui est une entité logique fournie par le système hôte pour allouer et assigner des ressources.
ms.assetid: c8e0b701-1814-4409-a073-017f8fea841a
title: Classe CIM_ResourcePool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePool
- CIM_ResourcePool.InstanceID
- CIM_ResourcePool.PoolID
- CIM_ResourcePool.Primordial
- CIM_ResourcePool.Capacity
- CIM_ResourcePool.Reserved
- CIM_ResourcePool.ResourceType
- CIM_ResourcePool.OtherResourceType
- CIM_ResourcePool.ResourceSubType
- CIM_ResourcePool.AllocationUnits
- CIM_ResourcePool.ConsumedResourceUnits
- CIM_ResourcePool.CurrentlyConsumedResource
- CIM_ResourcePool.MaxConsumableResource
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 11a073f817da27dbbd45be26a008486a776470cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113578"
---
# <a name="cim_resourcepool-class"></a><span data-ttu-id="964c7-103">\_Classe CIM ResourcePool</span><span class="sxs-lookup"><span data-stu-id="964c7-103">CIM\_ResourcePool class</span></span>

<span data-ttu-id="964c7-104">Représente un pool de ressources, qui est une entité logique fournie par le système hôte pour allouer et assigner des ressources.</span><span class="sxs-lookup"><span data-stu-id="964c7-104">Represents a resource pool, which is a logical entity provided by the host system to allocate and assign resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="964c7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="964c7-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_ResourcePool : CIM_LogicalElement
{
  string  InstanceID;
  string  PoolID;
  boolean Primordial = FALSE;
  uint64  Capacity;
  uint64  Reserved;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  AllocationUnits;
  string  ConsumedResourceUnits = "count";
  uint64  CurrentlyConsumedResource;
  uint64  MaxConsumableResource;
};
```

## <a name="members"></a><span data-ttu-id="964c7-106">Membres</span><span class="sxs-lookup"><span data-stu-id="964c7-106">Members</span></span>

<span data-ttu-id="964c7-107">La classe **CIM \_ ResourcePool** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="964c7-107">The **CIM\_ResourcePool** class has these types of members:</span></span>

-   [<span data-ttu-id="964c7-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="964c7-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="964c7-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="964c7-109">Properties</span></span>

<span data-ttu-id="964c7-110">La classe **CIM \_ ResourcePool** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="964c7-110">The **CIM\_ResourcePool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="964c7-111">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="964c7-111">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="964c7-112">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="964c7-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="964c7-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="964c7-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="964c7-114">Qualificateurs : **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="964c7-114">Qualifiers: **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="964c7-115">Unités d’allocation utilisées par la **réservation** et les propriétés de la **limite** .</span><span class="sxs-lookup"><span data-stu-id="964c7-115">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="964c7-116">Par exemple, lorsque **resourceType** a la valeur « Processor », **AllocationUnits** peut avoir la valeur « Hertz \* 10 ^ 6 » ou « pourcentage ».</span><span class="sxs-lookup"><span data-stu-id="964c7-116">For example, when **ResourceType** is set to "Processor", **AllocationUnits** may be set to "hertz\*10^6" or "percent".</span></span> <span data-ttu-id="964c7-117">La valeur de cette propriété doit être une valeur légale du qualificateur d’unités de programmation de l’annexe C. 1 de *DSP0004 v 2.4* ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="964c7-117">The value of this property should be a legal value of the Programmatic Units qualifier from Appendix C.1 of *DSP0004 V2.4* or later.</span></span>

</dd> <dt>

<span data-ttu-id="964c7-118">**Capacité**</span><span class="sxs-lookup"><span data-stu-id="964c7-118">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="964c7-119">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="964c7-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="964c7-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="964c7-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="964c7-121">Quantité maximale de réservations que le pool de ressources peut prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="964c7-121">The maximum amount of reservations that the resource pool can support.</span></span> <span data-ttu-id="964c7-122">La propriété **AllocationUnits** spécifie le type d’unité.</span><span class="sxs-lookup"><span data-stu-id="964c7-122">The **AllocationUnits** property specifies the unit type.</span></span>

</dd> <dt>

<span data-ttu-id="964c7-123">**ConsumedResourceUnits**</span><span class="sxs-lookup"><span data-stu-id="964c7-123">**ConsumedResourceUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="964c7-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="964c7-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="964c7-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="964c7-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="964c7-126">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**MaxConsumableResource**","**CIM \_ ResourcePool**.**CurrentlyConsumedResource**"), **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="964c7-126">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**MaxConsumableResource**", "**CIM\_ResourcePool**.**CurrentlyConsumedResource**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="964c7-127">Unités pour le **MaxConsumable** et les propriétés **consommées** .</span><span class="sxs-lookup"><span data-stu-id="964c7-127">The units for the **MaxConsumable** and the **Consumed** properties.</span></span>

</dd> <dt>

<span data-ttu-id="964c7-128">**CurrentlyConsumedResource**</span><span class="sxs-lookup"><span data-stu-id="964c7-128">**CurrentlyConsumedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="964c7-129">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="964c7-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="964c7-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="964c7-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="964c7-131">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**ConsumedResourceUnits**")</span><span class="sxs-lookup"><span data-stu-id="964c7-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**ConsumedResourceUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="964c7-132">Quantité de ressources que le pool de ressources présente actuellement aux consommateurs de ressources.</span><span class="sxs-lookup"><span data-stu-id="964c7-132">The amount of resource that the resource pool currently presents to resource consumers.</span></span> <span data-ttu-id="964c7-133">Cette propriété est différente de la propriété **réservée** , car elle décrit la vue consommateurs de la ressource, tandis que la propriété **réservée** décrit la vue des producteurs de la ressource.</span><span class="sxs-lookup"><span data-stu-id="964c7-133">This property is different from the **Reserved** property because it describes the consumers view of the resource while the **Reserved** property describes the producers view of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="964c7-134">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="964c7-134">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="964c7-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="964c7-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="964c7-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="964c7-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="964c7-137">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="964c7-137">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="964c7-138">Identifie de façon unique une instance de cette classe dans la portée de l’espace de noms conteneur.</span><span class="sxs-lookup"><span data-stu-id="964c7-138">Uniquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="964c7-139">Pour garantir l’unicité au sein de l’espace de noms, la valeur de la propriété **InstanceID** doit être construite au format suivant : *identifiant OrgID*:*LocalID*</span><span class="sxs-lookup"><span data-stu-id="964c7-139">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> -   <span data-ttu-id="964c7-140">*Identifiant OrgID* doit inclure un nom de droits d’auteur, de marque déposée ou un nom unique qui est détenu par l’entité métier qui définit la propriété **InstanceID** , ou être un ID inscrit qui est attribué par une autorité globale reconnue.</span><span class="sxs-lookup"><span data-stu-id="964c7-140">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID** property, or be a registered ID that is assigned by a recognized global authority.</span></span>
> -   <span data-ttu-id="964c7-141">*Identifiant OrgID* ne doit pas contenir de signe deux-points.</span><span class="sxs-lookup"><span data-stu-id="964c7-141">*OrgID* must not contain a colon.</span></span> <span data-ttu-id="964c7-142">Le premier signe deux-points dans **InstanceID** doit être compris entre *identifiant OrgID* et *LocalID*.</span><span class="sxs-lookup"><span data-stu-id="964c7-142">The first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span>
> -   <span data-ttu-id="964c7-143">*LocalID* est choisi par l’entité métier et ne doit pas être réutilisé pour identifier des éléments réels sous-jacents différents.</span><span class="sxs-lookup"><span data-stu-id="964c7-143">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
> -   <span data-ttu-id="964c7-144">Si le modèle ci-dessus n’est pas utilisé, l’entité de définition doit s’assurer que la valeur **InstanceID** obtenue n’est pas réutilisée dans les propriétés **InstanceID** produites par ce fournisseur ou d’autres fournisseurs pour cet espace de noms.</span><span class="sxs-lookup"><span data-stu-id="964c7-144">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
> -   <span data-ttu-id="964c7-145">Pour les instances DMTF définies, le modèle doit être utilisé avec le *identifiant OrgID* défini sur « CIM ».</span><span class="sxs-lookup"><span data-stu-id="964c7-145">For DMTF defined instances, the pattern must be used with the *OrgID* set to "CIM".</span></span>

 

</dd> <dt>

<span data-ttu-id="964c7-146">**MaxConsumableResource**</span><span class="sxs-lookup"><span data-stu-id="964c7-146">**MaxConsumableResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="964c7-147">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="964c7-147">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="964c7-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="964c7-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="964c7-149">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**ConsumedResourceUnits**")</span><span class="sxs-lookup"><span data-stu-id="964c7-149">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**ConsumedResourceUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="964c7-150">Quantité maximale de ressources consommables que le pool de ressources peut présenter aux consommateurs de ressources.</span><span class="sxs-lookup"><span data-stu-id="964c7-150">The maximum of amount of consumable resources that the resource pool can present to resource consumers.</span></span> <span data-ttu-id="964c7-151">Cette propriété est différente de la propriété **Capacity** , car elle décrit la vue consommateurs de la ressource, tandis que la propriété **Capacity** décrit la vue des producteurs de la ressource.</span><span class="sxs-lookup"><span data-stu-id="964c7-151">This property is different from the **Capacity** property because it describes the consumers view of the resource while the **Capacity** property describes the producers view of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="964c7-152">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="964c7-152">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="964c7-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="964c7-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="964c7-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="964c7-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="964c7-155">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**ResourceType**»)</span><span class="sxs-lookup"><span data-stu-id="964c7-155">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="964c7-156">Type de ressource lorsque la propriété **resourceType** est définie sur « 0 » (autre).</span><span class="sxs-lookup"><span data-stu-id="964c7-156">The resource type when the **ResourceType** property is set to "0" (other).</span></span>

</dd> <dt>

<span data-ttu-id="964c7-157">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="964c7-157">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="964c7-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="964c7-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="964c7-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="964c7-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="964c7-160">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**PoolId**")</span><span class="sxs-lookup"><span data-stu-id="964c7-160">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**PoolId**")</span></span>
</dt> </dl>

<span data-ttu-id="964c7-161">Identificateur opaque pour le pool.</span><span class="sxs-lookup"><span data-stu-id="964c7-161">An opaque identifier for the pool.</span></span> <span data-ttu-id="964c7-162">Cette propriété est utilisée pour fournir la corrélation lors de l’enregistrement et de la restauration des données de configuration dans le stockage persistant sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="964c7-162">This property is used to provide correlation when saving and restoring configuration data to underlying persistent storage.</span></span>

</dd> <dt>

<span data-ttu-id="964c7-163">**Primordial**</span><span class="sxs-lookup"><span data-stu-id="964c7-163">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="964c7-164">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="964c7-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="964c7-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="964c7-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="964c7-166">**true** si le pool de ressources est primordial.</span><span class="sxs-lookup"><span data-stu-id="964c7-166">**true** if the resource pool is primordial.</span></span> <span data-ttu-id="964c7-167">**false** si le pool de ressources est un pool de ressources concret.</span><span class="sxs-lookup"><span data-stu-id="964c7-167">**false** if the resource pool is a concrete resource pool.</span></span> <span data-ttu-id="964c7-168">Un pool de ressources primordial est un pool de ressources qui n’est pas créé ou supprimé par les consommateurs de la ressource.</span><span class="sxs-lookup"><span data-stu-id="964c7-168">A primordial resource pool is a resource pool that is not created or deleted by consumers of the resource.</span></span> <span data-ttu-id="964c7-169">Un pool de ressources concret peut être mis à jour par les services d’allocation de ressources.</span><span class="sxs-lookup"><span data-stu-id="964c7-169">A concrete resource pool can be updated by resource allocation services.</span></span>

</dd> <dt>

<span data-ttu-id="964c7-170">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="964c7-170">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="964c7-171">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="964c7-171">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="964c7-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="964c7-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="964c7-173">Le nombre actuel de réservations réparties sur toutes les allocations actives à partir de ce pool.</span><span class="sxs-lookup"><span data-stu-id="964c7-173">The current number of reservations spread across all active allocations from this pool.</span></span> <span data-ttu-id="964c7-174">Dans une configuration hiérarchique, il s’agit de la somme de toutes les réservations descendantes actuelles.</span><span class="sxs-lookup"><span data-stu-id="964c7-174">In a hierarchical configuration, this represents the sum of all current descendant reservations.</span></span> <span data-ttu-id="964c7-175">La propriété **AllocationUnits** spécifie le type d’unité.</span><span class="sxs-lookup"><span data-stu-id="964c7-175">The **AllocationUnits** property specifies the unit type.</span></span>

</dd> <dt>

<span data-ttu-id="964c7-176">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="964c7-176">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="964c7-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="964c7-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="964c7-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="964c7-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="964c7-179">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**ResourceType**»)</span><span class="sxs-lookup"><span data-stu-id="964c7-179">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="964c7-180">Sous-type spécifique à l’implémentation du pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="964c7-180">The implementation specific sub-type for the resource pool.</span></span> <span data-ttu-id="964c7-181">Par exemple, cela peut être utilisé pour distinguer différents modèles du même type de ressource.</span><span class="sxs-lookup"><span data-stu-id="964c7-181">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="964c7-182">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="964c7-182">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="964c7-183">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="964c7-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="964c7-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="964c7-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="964c7-185">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**OtherResourceType**","**CIM \_ ResourcePool**.**ResourceSubType**")</span><span class="sxs-lookup"><span data-stu-id="964c7-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**OtherResourceType**", "**CIM\_ResourcePool**.**ResourceSubType**")</span></span>
</dt> </dl>

<span data-ttu-id="964c7-186">Type de ressource alloué par le pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="964c7-186">The type of resource allocated by the resource pool.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="964c7-187">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="964c7-187">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

<span data-ttu-id="964c7-188">**Système informatique** (2)</span><span class="sxs-lookup"><span data-stu-id="964c7-188">**Computer System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

<span data-ttu-id="964c7-189">**Processeur** (3)</span><span class="sxs-lookup"><span data-stu-id="964c7-189">**Processor** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

<span data-ttu-id="964c7-190">**Mémoire** (4)</span><span class="sxs-lookup"><span data-stu-id="964c7-190">**Memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

<span data-ttu-id="964c7-191">**Contrôleur IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="964c7-191">**IDE Controller** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

<span data-ttu-id="964c7-192">**HBA SCSI parallèle** (6)</span><span class="sxs-lookup"><span data-stu-id="964c7-192">**Parallel SCSI HBA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

<span data-ttu-id="964c7-193">**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="964c7-193">**FC HBA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

<span data-ttu-id="964c7-194">**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="964c7-194">**iSCSI HBA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

<span data-ttu-id="964c7-195">**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="964c7-195">**IB HCA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

<span data-ttu-id="964c7-196">**Carte Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="964c7-196">**Ethernet Adapter** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

<span data-ttu-id="964c7-197">**Autre carte réseau** (11)</span><span class="sxs-lookup"><span data-stu-id="964c7-197">**Other Network Adapter** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

<span data-ttu-id="964c7-198">**Emplacement d’e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="964c7-198">**I/O Slot** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

<span data-ttu-id="964c7-199">**Périphérique d’e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="964c7-199">**I/O Device** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

<span data-ttu-id="964c7-200">**Lecteur de disquette** (14)</span><span class="sxs-lookup"><span data-stu-id="964c7-200">**Floppy Drive** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

<span data-ttu-id="964c7-201">**Lecteur de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="964c7-201">**CD Drive** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

<span data-ttu-id="964c7-202">**Lecteur de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="964c7-202">**DVD drive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="964c7-203">**Lecteur de disque** (17)</span><span class="sxs-lookup"><span data-stu-id="964c7-203">**Disk Drive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

<span data-ttu-id="964c7-204">**Lecteur de bande** (18)</span><span class="sxs-lookup"><span data-stu-id="964c7-204">**Tape Drive** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

<span data-ttu-id="964c7-205">**Extension de stockage** (19)</span><span class="sxs-lookup"><span data-stu-id="964c7-205">**Storage Extent** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

<span data-ttu-id="964c7-206">**Autre dispositif de stockage** (20)</span><span class="sxs-lookup"><span data-stu-id="964c7-206">**Other storage device** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

<span data-ttu-id="964c7-207">**Port série** (21)</span><span class="sxs-lookup"><span data-stu-id="964c7-207">**Serial port** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="964c7-208">**Port parallèle** (22)</span><span class="sxs-lookup"><span data-stu-id="964c7-208">**Parallel port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

<span data-ttu-id="964c7-209">**Contrôleur USB** (23)</span><span class="sxs-lookup"><span data-stu-id="964c7-209">**USB Controller** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

<span data-ttu-id="964c7-210">**Contrôleur Graphics** (24)</span><span class="sxs-lookup"><span data-stu-id="964c7-210">**Graphics controller** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

<span data-ttu-id="964c7-211">**Contrôleur IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="964c7-211">**IEEE 1394 Controller** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

<span data-ttu-id="964c7-212">**Unité partitionnée** (26)</span><span class="sxs-lookup"><span data-stu-id="964c7-212">**Partitionable Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

<span data-ttu-id="964c7-213">**Unité partitionnée de base** (27)</span><span class="sxs-lookup"><span data-stu-id="964c7-213">**Base Partitionable Unit** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="964c7-214">**Puissance** (28)</span><span class="sxs-lookup"><span data-stu-id="964c7-214">**Power** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

<span data-ttu-id="964c7-215">**Capacité de refroidissement** (29)</span><span class="sxs-lookup"><span data-stu-id="964c7-215">**Cooling Capacity** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

<span data-ttu-id="964c7-216">**Port commuté Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="964c7-216">**Ethernet Switch Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

<span data-ttu-id="964c7-217">**Disque logique** (31)</span><span class="sxs-lookup"><span data-stu-id="964c7-217">**Logical Disk** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

<span data-ttu-id="964c7-218">**Volume de stockage** (32)</span><span class="sxs-lookup"><span data-stu-id="964c7-218">**Storage Volume** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

<span data-ttu-id="964c7-219">**Connexion Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="964c7-219">**Ethernet Connection** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="964c7-220">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="964c7-220">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="964c7-221">**Fournisseur réservé** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="964c7-221">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


<span data-ttu-id="964c7-222"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="964c7-222"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="964c7-223">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="964c7-223">Requirements</span></span>



| <span data-ttu-id="964c7-224">Condition requise</span><span class="sxs-lookup"><span data-stu-id="964c7-224">Requirement</span></span> | <span data-ttu-id="964c7-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="964c7-225">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="964c7-226">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="964c7-226">Minimum supported client</span></span><br/> | <span data-ttu-id="964c7-227">Windows 8</span><span class="sxs-lookup"><span data-stu-id="964c7-227">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="964c7-228">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="964c7-228">Minimum supported server</span></span><br/> | <span data-ttu-id="964c7-229">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="964c7-229">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="964c7-230">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="964c7-230">Namespace</span></span><br/>                | <span data-ttu-id="964c7-231">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="964c7-231">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="964c7-232">MOF</span><span class="sxs-lookup"><span data-stu-id="964c7-232">MOF</span></span><br/>                      | <dl> <span data-ttu-id="964c7-233"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="964c7-233"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="964c7-234">DLL</span><span class="sxs-lookup"><span data-stu-id="964c7-234">DLL</span></span><br/>                      | <dl> <span data-ttu-id="964c7-235"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="964c7-235"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="964c7-236">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="964c7-236">See also</span></span>

<dl> <dt>

[<span data-ttu-id="964c7-237">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="964c7-237">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

