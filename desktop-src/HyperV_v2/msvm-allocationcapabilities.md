---
description: Définit le moyen par lequel un client peut découvrir la plage valide de paramètres par défaut pour une ressource virtuelle.
ms.assetid: AC516723-7CD2-4F10-B8BF-EF9D458D3E5B
title: Classe Msvm_AllocationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AllocationCapabilities
- Msvm_AllocationCapabilities.InstanceID
- Msvm_AllocationCapabilities.Caption
- Msvm_AllocationCapabilities.Description
- Msvm_AllocationCapabilities.ElementName
- Msvm_AllocationCapabilities.ResourceType
- Msvm_AllocationCapabilities.OtherResourceType
- Msvm_AllocationCapabilities.ResourceSubType
- Msvm_AllocationCapabilities.RequestTypesSupported
- Msvm_AllocationCapabilities.SharingMode
- Msvm_AllocationCapabilities.SupportedAddStates
- Msvm_AllocationCapabilities.SupportedRemoveStates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7642d1b590affcb3704f7d854d65edb5481c2285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526262"
---
# <a name="msvm_allocationcapabilities-class"></a><span data-ttu-id="fd8d5-103">MSVM \_ AllocationCapabilities, classe</span><span class="sxs-lookup"><span data-stu-id="fd8d5-103">Msvm\_AllocationCapabilities class</span></span>

<span data-ttu-id="fd8d5-104">Définit le moyen par lequel un client peut découvrir la plage valide de paramètres par défaut pour une ressource virtuelle.</span><span class="sxs-lookup"><span data-stu-id="fd8d5-104">Defines the means by which a client can discover the valid range of default settings for a virtual resource.</span></span> <span data-ttu-id="fd8d5-105">Un objet **MSVM \_ AllocationCapabilities** est associé à chaque liste de ressources partagées.</span><span class="sxs-lookup"><span data-stu-id="fd8d5-105">A **Msvm\_AllocationCapabilities** object is associated with each resource pool.</span></span> <span data-ttu-id="fd8d5-106">Quatre [**objets \_ ResourceAllocationSettingData MSVM**](msvm-resourceallocationsettingdata.md) sont associés à l' **objet \_ MSVM AllocationCapabilities** pour décrire les valeurs minimales, maximales, par défaut et incrémentielles pour l’allocation de la ressource donnée.</span><span class="sxs-lookup"><span data-stu-id="fd8d5-106">Four [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) objects are associated with the **Msvm\_AllocationCapabilities** object to describe the minimum, maximum, default, and incremental values for the given resource's allocation.</span></span> <span data-ttu-id="fd8d5-107">Ensemble, ces classes décrivent la plage globale des fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="fd8d5-107">Together, these classes describe the overall range of supported capabilities.</span></span>

<span data-ttu-id="fd8d5-108">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="fd8d5-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd8d5-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd8d5-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AllocationCapabilities : CIM_AllocationCapabilities
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  uint16 RequestTypesSupported;
  uint16 SharingMode;
  uint16 SupportedAddStates[];
  uint16 SupportedRemoveStates[];
};
```

## <a name="members"></a><span data-ttu-id="fd8d5-110">Membres</span><span class="sxs-lookup"><span data-stu-id="fd8d5-110">Members</span></span>

<span data-ttu-id="fd8d5-111">La classe **MSVM \_ AllocationCapabilities** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fd8d5-111">The **Msvm\_AllocationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="fd8d5-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fd8d5-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fd8d5-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fd8d5-113">Properties</span></span>

<span data-ttu-id="fd8d5-114">La classe **MSVM \_ AllocationCapabilities** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="fd8d5-114">The **Msvm\_AllocationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fd8d5-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="fd8d5-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd8d5-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd8d5-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd8d5-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-118">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-118">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="fd8d5-119">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fd8d5-119">A short description of the object.</span></span> <span data-ttu-id="fd8d5-120">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fd8d5-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fd8d5-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="fd8d5-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd8d5-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd8d5-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd8d5-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd8d5-124">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="fd8d5-124">A description of the object.</span></span> <span data-ttu-id="fd8d5-125">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fd8d5-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fd8d5-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="fd8d5-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd8d5-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd8d5-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd8d5-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd8d5-129">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fd8d5-129">A display name for the object.</span></span> <span data-ttu-id="fd8d5-130">Cette propriété permet à chaque instance de définir un nom complet en plus de ses propriétés de clé, données d’identité et informations de description.</span><span class="sxs-lookup"><span data-stu-id="fd8d5-130">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="fd8d5-131">La propriété [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) de la **classe \_ ManagedSystemElement CIM** est également définie en tant que nom complet.</span><span class="sxs-lookup"><span data-stu-id="fd8d5-131">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name.</span></span> <span data-ttu-id="fd8d5-132">Toutefois, il est souvent sous-classé comme une clé.</span><span class="sxs-lookup"><span data-stu-id="fd8d5-132">But, it is often subclassed to be a Key.</span></span> <span data-ttu-id="fd8d5-133">Il n’est pas raisonnable que la même propriété puisse transmettre à la fois l’identité et un nom d’affichage, sans incohérence.</span><span class="sxs-lookup"><span data-stu-id="fd8d5-133">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="fd8d5-134">Où le [**nom**](msvm-keyboard.md) existe et n’est pas une clé (par exemple, pour les instances d’un périphérique logique), les mêmes informations peuvent être présentes dans les propriétés **Name** et **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="fd8d5-134">Where [**Name**](msvm-keyboard.md) exists and is not a Key (such as for instances of a logical device), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="fd8d5-135">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fd8d5-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fd8d5-136">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fd8d5-136">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd8d5-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd8d5-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd8d5-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd8d5-139">Identificateur unique de ce pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="fd8d5-139">A unique identifier for this resource pool.</span></span> <span data-ttu-id="fd8d5-140">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fd8d5-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fd8d5-141">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="fd8d5-141">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd8d5-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd8d5-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd8d5-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd8d5-144">Chaîne qui décrit le type de ressource lorsqu’une valeur bien définie n’est pas disponible et que **resourceType** a la valeur « other ».</span><span class="sxs-lookup"><span data-stu-id="fd8d5-144">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value "Other".</span></span> <span data-ttu-id="fd8d5-145">Cette propriété est héritée de la [**\_ AllocationCapabilities CIM**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="fd8d5-145">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

</dd> <dt>

<span data-ttu-id="fd8d5-146">**RequestTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="fd8d5-146">**RequestTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd8d5-147">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd8d5-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd8d5-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd8d5-149">Indique si la demande d’une ressource spécifique est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="fd8d5-149">Indicates whether requesting a specific resource is supported.</span></span> <span data-ttu-id="fd8d5-150">Cette propriété est héritée de la [**\_ AllocationCapabilities CIM**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="fd8d5-150">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>



| <span data-ttu-id="fd8d5-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd8d5-151">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="fd8d5-152">Signification</span><span class="sxs-lookup"><span data-stu-id="fd8d5-152">Meaning</span></span>                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="fd8d5-153"><dt>**Inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fd8d5-153"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="fd8d5-154">Unknown</span><span class="sxs-lookup"><span data-stu-id="fd8d5-154">Unknown</span></span><br/>                                                         |
| <span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span><dl> <span data-ttu-id="fd8d5-155"><dt></dt> <dt>2</dt> spécifiques</span><span class="sxs-lookup"><span data-stu-id="fd8d5-155"><dt>**Specific**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="fd8d5-156">La demande peut inclure une demande pour une ressource spécifique.</span><span class="sxs-lookup"><span data-stu-id="fd8d5-156">The request can include a request for a specific resource.</span></span><br/>      |
| <span id="General"></span><span id="general"></span><span id="GENERAL"></span><dl> <span data-ttu-id="fd8d5-157"><dt>**Général**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="fd8d5-157"><dt>**General**</dt> <dt>3</dt></span></span> </dl>     | <span data-ttu-id="fd8d5-158">La demande n’inclut pas de demande pour une ressource spécifique.</span><span class="sxs-lookup"><span data-stu-id="fd8d5-158">The request does not include a request for a specific resource.</span></span><br/> |
| <span id="Both"></span><span id="both"></span><span id="BOTH"></span><dl> <span data-ttu-id="fd8d5-159"><dt>**Les deux**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="fd8d5-159"><dt>**Both**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="fd8d5-160">Les requêtes spécifiques et générales sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="fd8d5-160">Both specific and general requests are supported.</span></span><br/>               |



 

</dd> <dt>

<span data-ttu-id="fd8d5-161">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="fd8d5-161">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd8d5-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd8d5-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd8d5-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd8d5-164">Chaîne qui décrit un sous-type spécifique à l’implémentation pour cette ressource.</span><span class="sxs-lookup"><span data-stu-id="fd8d5-164">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="fd8d5-165">Par exemple, cela peut être utilisé pour distinguer différents modèles du même type de ressource.</span><span class="sxs-lookup"><span data-stu-id="fd8d5-165">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="fd8d5-166">Cette propriété est héritée de la [**\_ AllocationCapabilities CIM**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="fd8d5-166">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

</dd> <dt>

<span data-ttu-id="fd8d5-167">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="fd8d5-167">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd8d5-168">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd8d5-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd8d5-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd8d5-170">Type de ressource représenté par ce paramètre d’allocation.</span><span class="sxs-lookup"><span data-stu-id="fd8d5-170">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="fd8d5-171">Cette propriété est héritée de la [**\_ AllocationCapabilities CIM**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="fd8d5-171">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

<dl> <dt>

<span data-ttu-id="fd8d5-172"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-172"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-173"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Système informatique** (2)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-173"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-174"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processeur** (3)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-174"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-175"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Mémoire** (4)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-175"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-176"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Contrôleur IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-176"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-177"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI parallèle** (6)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-177"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-178"><span id="FC_HBA"></span><span id="fc_hba"></span>**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-178"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-179"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-179"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-180"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-180"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-181"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Carte Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-181"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-182"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Autre carte réseau** (11)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-182"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-183"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Emplacement d’e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-183"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-184"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Périphérique d’e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-184"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-185"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Lecteur de disquette** (14)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-185"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-186"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Lecteur de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-186"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-187"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Lecteur de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-187"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-188"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Lecteur de disque** (17)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-188"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Disk Drive** (17)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-189"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Lecteur de bande** (18)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-189"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Tape Drive** (18)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-190"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extension de stockage** (19)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-190"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (19)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-191"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Autre dispositif de stockage** (20)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-191"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other Storage Device** (20)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-192"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Port série** (21)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-192"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (21)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-193"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Port parallèle** (22)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-193"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (22)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-194"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Contrôleur USB** (23)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-194"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (23)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-195"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Contrôleur Graphics** (24)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-195"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (24)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-196"><span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**Contrôleur IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-196"><span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-197"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unité partitionnée** (26)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-197"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-198"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unité partitionnée de base** (27)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-198"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-199"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Puissance** (28)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-199"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (28)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-200"><span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Capacité de refroidissement** (29)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-200"><span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Cooling Capacity** (29)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-201"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Port commuté Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-201"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet Switch Port** (30)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-202"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Disque logique** (31)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-202"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logical Disk** (31)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-203"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Volume de stockage** (32)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-203"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-204"><span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Connexion Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-204"><span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet Connection** (33)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-205"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-205"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-206"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="fd8d5-206"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..0xFFFF )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fd8d5-207">**SharingMode**</span><span class="sxs-lookup"><span data-stu-id="fd8d5-207">**SharingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd8d5-208">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd8d5-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd8d5-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd8d5-210">Indique comment l’accès à une ressource sous-jacente est accordé.</span><span class="sxs-lookup"><span data-stu-id="fd8d5-210">Indicates how access to an underlying resource is granted.</span></span> <span data-ttu-id="fd8d5-211">Cette propriété est héritée de la [**\_ AllocationCapabilities CIM**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="fd8d5-211">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>



| <span data-ttu-id="fd8d5-212">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd8d5-212">Value</span></span>                                                                                                                                                                                                                               | <span data-ttu-id="fd8d5-213">Signification</span><span class="sxs-lookup"><span data-stu-id="fd8d5-213">Meaning</span></span>                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="fd8d5-214"><dt>**Inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fd8d5-214"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="fd8d5-215">Unknown</span><span class="sxs-lookup"><span data-stu-id="fd8d5-215">Unknown</span></span><br/>                                     |
| <span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span><dl> <span data-ttu-id="fd8d5-216"><dt>**Dédié**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="fd8d5-216"><dt>**Dedicated**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="fd8d5-217">Accès exclusif à une ressource sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="fd8d5-217">Exclusive access to an underlying resource.</span></span><br/> |
| <span id="Shared"></span><span id="shared"></span><span id="SHARED"></span><dl> <span data-ttu-id="fd8d5-218"><dt>**Partagé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="fd8d5-218"><dt>**Shared**</dt> <dt>3</dt></span></span> </dl>             | <span data-ttu-id="fd8d5-219">Utilisation partagée d’une ressource sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="fd8d5-219">Shared use of an underlying resource.</span></span><br/>       |



 

</dd> <dt>

<span data-ttu-id="fd8d5-220">**SupportedAddStates**</span><span class="sxs-lookup"><span data-stu-id="fd8d5-220">**SupportedAddStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd8d5-221">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd8d5-221">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd8d5-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd8d5-223">Indique les États auxquels le système auquel la ressource sera associée peut se trouver lorsqu’une nouvelle ressource est créée.</span><span class="sxs-lookup"><span data-stu-id="fd8d5-223">Indicates the states that the system to which the resource will be associated can be in when a new resource is created.</span></span> <span data-ttu-id="fd8d5-224">Cette propriété est héritée de la [**\_ AllocationCapabilities CIM**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="fd8d5-224">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

<dl> <dt>

<span data-ttu-id="fd8d5-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-226"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-226"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-227"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-227"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-228"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-228"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-229"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-229"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-230"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Activé mais hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-230"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-231"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans test** (7)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-231"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-232"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Différé** (8)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-232"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-233"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-233"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-234"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (10)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-234"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (10)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-235"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (11)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-235"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (11)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-236"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspendu** (12)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-236"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (12)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-237"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-237"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-238"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="fd8d5-238"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..0xFFFF )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fd8d5-239">**SupportedRemoveStates**</span><span class="sxs-lookup"><span data-stu-id="fd8d5-239">**SupportedRemoveStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd8d5-240">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd8d5-240">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-241">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd8d5-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd8d5-242">Indique les États auxquels le système auquel la ressource est associée peut se trouver lorsque la ressource est supprimée.</span><span class="sxs-lookup"><span data-stu-id="fd8d5-242">Indicates the states that the system to which the resource is associated can be in when the resource is removed.</span></span> <span data-ttu-id="fd8d5-243">Cette propriété est héritée de la [**\_ AllocationCapabilities CIM**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="fd8d5-243">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

<dl> <dt>

<span data-ttu-id="fd8d5-244"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-244"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-245"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-245"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-246"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-246"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-247"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-247"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-248"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-248"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-249"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Activé mais hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-249"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-250"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans test** (7)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-250"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-251"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Différé** (8)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-251"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-252"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-252"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-253"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (10)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-253"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (10)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-254"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (11)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-254"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (11)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-255"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspendu** (12)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-255"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (12)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-256"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="fd8d5-256"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fd8d5-257"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="fd8d5-257"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..0xFFFF )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd8d5-258">Notes</span><span class="sxs-lookup"><span data-stu-id="fd8d5-258">Remarks</span></span>

<span data-ttu-id="fd8d5-259">L’accès à la classe **MSVM \_ AllocationCapabilities** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="fd8d5-259">Access to the **Msvm\_AllocationCapabilities** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="fd8d5-260">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="fd8d5-260">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd8d5-261">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd8d5-261">Requirements</span></span>



| <span data-ttu-id="fd8d5-262">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd8d5-262">Requirement</span></span> | <span data-ttu-id="fd8d5-263">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd8d5-263">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd8d5-264">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd8d5-264">Minimum supported client</span></span><br/> | <span data-ttu-id="fd8d5-265">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd8d5-265">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fd8d5-266">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd8d5-266">Minimum supported server</span></span><br/> | <span data-ttu-id="fd8d5-267">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd8d5-267">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fd8d5-268">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fd8d5-268">Namespace</span></span><br/>                | <span data-ttu-id="fd8d5-269">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="fd8d5-269">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fd8d5-270">MOF</span><span class="sxs-lookup"><span data-stu-id="fd8d5-270">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd8d5-271"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd8d5-271"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd8d5-272">DLL</span><span class="sxs-lookup"><span data-stu-id="fd8d5-272">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd8d5-273"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fd8d5-273"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fd8d5-274">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd8d5-274">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd8d5-275">**\_ALLOCATIONCAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="fd8d5-275">**CIM\_AllocationCapabilities**</span></span>](cim-allocationcapabilities.md)
</dt> <dt>

[<span data-ttu-id="fd8d5-276">**\_ALLOCATIONCAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="fd8d5-276">**CIM\_AllocationCapabilities**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)
</dt> <dt>

[<span data-ttu-id="fd8d5-277">**MSVM \_ AllocationCapabilities (v1)**</span><span class="sxs-lookup"><span data-stu-id="fd8d5-277">**Msvm\_AllocationCapabilities (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-allocationcapabilities)
</dt> <dt>

[<span data-ttu-id="fd8d5-278">Classes de gestion des ressources</span><span class="sxs-lookup"><span data-stu-id="fd8d5-278">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

