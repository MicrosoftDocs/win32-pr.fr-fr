---
description: Msvm_AbstractResourcePoolSettingData Class-représente les paramètres d’une \_ instance de ResourcePool MSVM qui ne sont pas liés à l’allocation.
ms.assetid: c5954a92-8942-4b45-aae2-6936328dab1a
title: Classe Msvm_AbstractResourcePoolSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AbstractResourcePoolSettingData
- Msvm_AbstractResourcePoolSettingData.InstanceID
- Msvm_AbstractResourcePoolSettingData.Caption
- Msvm_AbstractResourcePoolSettingData.Description
- Msvm_AbstractResourcePoolSettingData.ElementName
- Msvm_AbstractResourcePoolSettingData.PoolID
- Msvm_AbstractResourcePoolSettingData.ResourceType
- Msvm_AbstractResourcePoolSettingData.OtherResourceType
- Msvm_AbstractResourcePoolSettingData.ResourceSubType
- Msvm_AbstractResourcePoolSettingData.LoadBalancingBehavior
- Msvm_AbstractResourcePoolSettingData.MappingBehavior
- Msvm_AbstractResourcePoolSettingData.MappingOrder
- Msvm_AbstractResourcePoolSettingData.Notes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dca3da14ac74a8d6fab1ba96db98f9e2eccd74ea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112117"
---
# <a name="msvm_abstractresourcepoolsettingdata-class"></a><span data-ttu-id="127c8-103">MSVM \_ AbstractResourcePoolSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="127c8-103">Msvm\_AbstractResourcePoolSettingData class</span></span>

<span data-ttu-id="127c8-104">Représente les paramètres d’une instance [**MSVM \_ ResourcePool**](msvm-resourcepool.md) qui ne sont pas liés à l’allocation.</span><span class="sxs-lookup"><span data-stu-id="127c8-104">Represents the settings of a [**Msvm\_ResourcePool**](msvm-resourcepool.md) instance that are not allocation related.</span></span>

<span data-ttu-id="127c8-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="127c8-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="127c8-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="127c8-106">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Msvm_AbstractResourcePoolSettingData : CIM_SettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string PoolID;
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  uint16 LoadBalancingBehavior;
  uint16 MappingBehavior;
  string MappingOrder[];
  string Notes;
};
```

## <a name="members"></a><span data-ttu-id="127c8-107">Membres</span><span class="sxs-lookup"><span data-stu-id="127c8-107">Members</span></span>

<span data-ttu-id="127c8-108">La classe **MSVM \_ AbstractResourcePoolSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="127c8-108">The **Msvm\_AbstractResourcePoolSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="127c8-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="127c8-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="127c8-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="127c8-110">Properties</span></span>

<span data-ttu-id="127c8-111">La classe **MSVM \_ AbstractResourcePoolSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="127c8-111">The **Msvm\_AbstractResourcePoolSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="127c8-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="127c8-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="127c8-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="127c8-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="127c8-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="127c8-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="127c8-115">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="127c8-115">A short description of the object.</span></span> <span data-ttu-id="127c8-116">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="127c8-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="127c8-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="127c8-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="127c8-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="127c8-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="127c8-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="127c8-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="127c8-120">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="127c8-120">A description of the object.</span></span> <span data-ttu-id="127c8-121">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="127c8-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="127c8-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="127c8-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="127c8-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="127c8-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="127c8-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="127c8-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="127c8-125">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="127c8-125">A display name for the object.</span></span> <span data-ttu-id="127c8-126">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="127c8-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="127c8-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="127c8-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="127c8-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="127c8-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="127c8-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="127c8-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="127c8-130">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="127c8-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="127c8-131">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="127c8-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="127c8-132">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="127c8-132">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="127c8-133">**LoadBalancingBehavior**</span><span class="sxs-lookup"><span data-stu-id="127c8-133">**LoadBalancingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="127c8-134">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="127c8-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="127c8-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="127c8-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="127c8-136">Spécifie la stratégie d’allocation à utiliser par le pool de ressources pour équilibrer l’utilisation des ressources sur ses ressources agrégées.</span><span class="sxs-lookup"><span data-stu-id="127c8-136">Specifies the allocation strategy to be used by the resource pool to balance resource usage across its aggregated resources.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="127c8-137">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="127c8-137">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="127c8-138">**Non pris en charge** (2)</span><span class="sxs-lookup"><span data-stu-id="127c8-138">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="127c8-139">**Aucun** (3)</span><span class="sxs-lookup"><span data-stu-id="127c8-139">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Distributed"></span><span id="distributed"></span><span id="DISTRIBUTED"></span>

<span data-ttu-id="127c8-140">**Distribué** (4)</span><span class="sxs-lookup"><span data-stu-id="127c8-140">**Distributed** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Consolidated"></span><span id="consolidated"></span><span id="CONSOLIDATED"></span>

<span data-ttu-id="127c8-141">**Consolidé** (5)</span><span class="sxs-lookup"><span data-stu-id="127c8-141">**Consolidated** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="127c8-142">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="127c8-142">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="127c8-143">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="127c8-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="127c8-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="127c8-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="127c8-145">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**MappingBehavior**")</span><span class="sxs-lookup"><span data-stu-id="127c8-145">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**MappingBehavior**")</span></span>
</dt> </dl>

<span data-ttu-id="127c8-146">Spécifie si le pool de ressources peut tenter d’utiliser d’autres ressources hôtes pour satisfaire la demande d’allocation si les ressources souhaitées ne peuvent pas être allouées.</span><span class="sxs-lookup"><span data-stu-id="127c8-146">Specifies whether the resource pool can attempt to use other host resources to satisfy the allocation request if the desired resources cannot be allocated.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="127c8-147">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="127c8-147">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="127c8-148">**Non pris en charge** (2)</span><span class="sxs-lookup"><span data-stu-id="127c8-148">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="127c8-149">**Dédié** (3)</span><span class="sxs-lookup"><span data-stu-id="127c8-149">**Dedicated** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>

<span data-ttu-id="127c8-150">**Affinité douce** (4)</span><span class="sxs-lookup"><span data-stu-id="127c8-150">**Soft Affinity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>

<span data-ttu-id="127c8-151">**Affinité matérielle** (5)</span><span class="sxs-lookup"><span data-stu-id="127c8-151">**Hard Affinity** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="127c8-152">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="127c8-152">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="127c8-153">**Fournisseur réservé** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="127c8-153">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="127c8-154">**MappingOrder**</span><span class="sxs-lookup"><span data-stu-id="127c8-154">**MappingOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="127c8-155">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="127c8-155">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="127c8-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="127c8-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="127c8-157">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**MSVM \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md).**MappingBehavior**")</span><span class="sxs-lookup"><span data-stu-id="127c8-157">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md).**MappingBehavior**")</span></span>
</dt> </dl>

<span data-ttu-id="127c8-158">Spécifie l’ordre dans lequel les ressources hôtes disponibles via ce pool sont sélectionnées lors de la tentative de satisfaction d’une demande d’allocation, et la ressource hôte demandée n’est pas disponible ou aucune ressource hôte n’est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="127c8-158">Specifies the order in which host resources available through this pool will be selected when attempting to satisfy an allocation request, and the requested host resource is not available or no host resource is specified.</span></span>

</dd> <dt>

<span data-ttu-id="127c8-159">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="127c8-159">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="127c8-160">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="127c8-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="127c8-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="127c8-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="127c8-162">Les notes fournies par l’utilisateur final sont liées à ce pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="127c8-162">End-user supplied notes that are related to this resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="127c8-163">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="127c8-163">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="127c8-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="127c8-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="127c8-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="127c8-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="127c8-166">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**OtherResourceType**")</span><span class="sxs-lookup"><span data-stu-id="127c8-166">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**OtherResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="127c8-167">Chaîne qui décrit le type de ressource lorsqu’une valeur bien définie n’est pas disponible et que **resourceType** a la valeur 0 (autre).</span><span class="sxs-lookup"><span data-stu-id="127c8-167">A string that describes the resource type when a well defined value is not available and **ResourceType** is set to 0 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="127c8-168">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="127c8-168">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="127c8-169">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="127c8-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="127c8-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="127c8-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="127c8-171">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**PoolID**")</span><span class="sxs-lookup"><span data-stu-id="127c8-171">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**PoolID**")</span></span>
</dt> </dl>

<span data-ttu-id="127c8-172">Identificateur du pool.</span><span class="sxs-lookup"><span data-stu-id="127c8-172">An identifier for the pool.</span></span> <span data-ttu-id="127c8-173">Cette propriété est utilisée pour fournir une corrélation entre l’enregistrement et la restauration des données de configuration dans le stockage persistant sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="127c8-173">This property is used to provide correlation across save and restore of configuration data to underlying persistent storage.</span></span>

</dd> <dt>

<span data-ttu-id="127c8-174">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="127c8-174">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="127c8-175">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="127c8-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="127c8-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="127c8-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="127c8-177">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**ResourceSubType**")</span><span class="sxs-lookup"><span data-stu-id="127c8-177">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**ResourceSubType**")</span></span>
</dt> </dl>

<span data-ttu-id="127c8-178">Chaîne qui décrit un sous-type spécifique à l’implémentation pour ce pool.</span><span class="sxs-lookup"><span data-stu-id="127c8-178">A string that describes an implementation specific sub-type for this pool.</span></span> <span data-ttu-id="127c8-179">Par exemple, cela peut être utilisé pour distinguer différents modèles du même type de ressource.</span><span class="sxs-lookup"><span data-stu-id="127c8-179">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="127c8-180">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="127c8-180">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="127c8-181">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="127c8-181">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="127c8-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="127c8-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="127c8-183">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**ResourceType**»)</span><span class="sxs-lookup"><span data-stu-id="127c8-183">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="127c8-184">Type de ressource que ce pool de ressources peut allouer.</span><span class="sxs-lookup"><span data-stu-id="127c8-184">The type of resource this resource pool can allocate.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="127c8-185">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="127c8-185">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

<span data-ttu-id="127c8-186">**Système informatique** (2)</span><span class="sxs-lookup"><span data-stu-id="127c8-186">**Computer System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

<span data-ttu-id="127c8-187">**Processeur** (3)</span><span class="sxs-lookup"><span data-stu-id="127c8-187">**Processor** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

<span data-ttu-id="127c8-188">**Mémoire** (4)</span><span class="sxs-lookup"><span data-stu-id="127c8-188">**Memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

<span data-ttu-id="127c8-189">**Contrôleur IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="127c8-189">**IDE Controller** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

<span data-ttu-id="127c8-190">**HBA SCSI parallèle** (6)</span><span class="sxs-lookup"><span data-stu-id="127c8-190">**Parallel SCSI HBA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

<span data-ttu-id="127c8-191">**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="127c8-191">**FC HBA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

<span data-ttu-id="127c8-192">**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="127c8-192">**iSCSI HBA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

<span data-ttu-id="127c8-193">**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="127c8-193">**IB HCA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

<span data-ttu-id="127c8-194">**Carte Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="127c8-194">**Ethernet Adapter** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

<span data-ttu-id="127c8-195">**Autre carte réseau** (11)</span><span class="sxs-lookup"><span data-stu-id="127c8-195">**Other Network Adapter** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

<span data-ttu-id="127c8-196">**Emplacement d’e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="127c8-196">**I/O Slot** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

<span data-ttu-id="127c8-197">**Périphérique d’e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="127c8-197">**I/O Device** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

<span data-ttu-id="127c8-198">**Lecteur de disquette** (14)</span><span class="sxs-lookup"><span data-stu-id="127c8-198">**Floppy Drive** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

<span data-ttu-id="127c8-199">**Lecteur de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="127c8-199">**CD Drive** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

<span data-ttu-id="127c8-200">**Lecteur de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="127c8-200">**DVD drive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="127c8-201">**Lecteur de disque** (17)</span><span class="sxs-lookup"><span data-stu-id="127c8-201">**Disk Drive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

<span data-ttu-id="127c8-202">**Lecteur de bande** (18)</span><span class="sxs-lookup"><span data-stu-id="127c8-202">**Tape Drive** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

<span data-ttu-id="127c8-203">**Extension de stockage** (19)</span><span class="sxs-lookup"><span data-stu-id="127c8-203">**Storage Extent** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

<span data-ttu-id="127c8-204">**Autre dispositif de stockage** (20)</span><span class="sxs-lookup"><span data-stu-id="127c8-204">**Other storage device** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

<span data-ttu-id="127c8-205">**Port série** (21)</span><span class="sxs-lookup"><span data-stu-id="127c8-205">**Serial port** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="127c8-206">**Port parallèle** (22)</span><span class="sxs-lookup"><span data-stu-id="127c8-206">**Parallel port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

<span data-ttu-id="127c8-207">**Contrôleur USB** (23)</span><span class="sxs-lookup"><span data-stu-id="127c8-207">**USB Controller** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

<span data-ttu-id="127c8-208">**Contrôleur Graphics** (24)</span><span class="sxs-lookup"><span data-stu-id="127c8-208">**Graphics controller** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

<span data-ttu-id="127c8-209">**Contrôleur IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="127c8-209">**IEEE 1394 Controller** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

<span data-ttu-id="127c8-210">**Unité partitionnée** (26)</span><span class="sxs-lookup"><span data-stu-id="127c8-210">**Partitionable Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

<span data-ttu-id="127c8-211">**Unité partitionnée de base** (27)</span><span class="sxs-lookup"><span data-stu-id="127c8-211">**Base Partitionable Unit** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="127c8-212">**Puissance** (28)</span><span class="sxs-lookup"><span data-stu-id="127c8-212">**Power** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

<span data-ttu-id="127c8-213">**Capacité de refroidissement** (29)</span><span class="sxs-lookup"><span data-stu-id="127c8-213">**Cooling Capacity** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

<span data-ttu-id="127c8-214">**Port commuté Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="127c8-214">**Ethernet Switch Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

<span data-ttu-id="127c8-215">**Disque logique** (31)</span><span class="sxs-lookup"><span data-stu-id="127c8-215">**Logical Disk** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

<span data-ttu-id="127c8-216">**Volume de stockage** (32)</span><span class="sxs-lookup"><span data-stu-id="127c8-216">**Storage Volume** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

<span data-ttu-id="127c8-217">**Connexion Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="127c8-217">**Ethernet Connection** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="127c8-218">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="127c8-218">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="127c8-219">**Fournisseur réservé** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="127c8-219">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


<span data-ttu-id="127c8-220"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="127c8-220"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="127c8-221">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="127c8-221">Requirements</span></span>



| <span data-ttu-id="127c8-222">Condition requise</span><span class="sxs-lookup"><span data-stu-id="127c8-222">Requirement</span></span> | <span data-ttu-id="127c8-223">Valeur</span><span class="sxs-lookup"><span data-stu-id="127c8-223">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="127c8-224">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="127c8-224">Minimum supported client</span></span><br/> | <span data-ttu-id="127c8-225">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="127c8-225">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="127c8-226">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="127c8-226">Minimum supported server</span></span><br/> | <span data-ttu-id="127c8-227">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="127c8-227">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="127c8-228">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="127c8-228">Namespace</span></span><br/>                | <span data-ttu-id="127c8-229">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="127c8-229">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="127c8-230">MOF</span><span class="sxs-lookup"><span data-stu-id="127c8-230">MOF</span></span><br/>                      | <dl> <span data-ttu-id="127c8-231"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="127c8-231"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="127c8-232">DLL</span><span class="sxs-lookup"><span data-stu-id="127c8-232">DLL</span></span><br/>                      | <dl> <span data-ttu-id="127c8-233"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="127c8-233"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

