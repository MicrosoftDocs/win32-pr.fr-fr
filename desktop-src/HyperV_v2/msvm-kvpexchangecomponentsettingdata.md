---
description: Représente l’état configuré du service d’échange de paires clé/valeur.
ms.assetid: B7ED1091-E49A-4C38-9794-E074E6B9EF48
title: Classe Msvm_KvpExchangeComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_KvpExchangeComponentSettingData
- Msvm_KvpExchangeComponentSettingData.DisableHostKVPItems
- Msvm_KvpExchangeComponentSettingData.InstanceID
- Msvm_KvpExchangeComponentSettingData.Caption
- Msvm_KvpExchangeComponentSettingData.Description
- Msvm_KvpExchangeComponentSettingData.ElementName
- Msvm_KvpExchangeComponentSettingData.ResourceType
- Msvm_KvpExchangeComponentSettingData.OtherResourceType
- Msvm_KvpExchangeComponentSettingData.ResourceSubType
- Msvm_KvpExchangeComponentSettingData.PoolID
- Msvm_KvpExchangeComponentSettingData.ConsumerVisibility
- Msvm_KvpExchangeComponentSettingData.HostResource
- Msvm_KvpExchangeComponentSettingData.AllocationUnits
- Msvm_KvpExchangeComponentSettingData.VirtualQuantity
- Msvm_KvpExchangeComponentSettingData.Reservation
- Msvm_KvpExchangeComponentSettingData.Limit
- Msvm_KvpExchangeComponentSettingData.Weight
- Msvm_KvpExchangeComponentSettingData.AutomaticAllocation
- Msvm_KvpExchangeComponentSettingData.AutomaticDeallocation
- Msvm_KvpExchangeComponentSettingData.Parent
- Msvm_KvpExchangeComponentSettingData.Connection
- Msvm_KvpExchangeComponentSettingData.Address
- Msvm_KvpExchangeComponentSettingData.MappingBehavior
- Msvm_KvpExchangeComponentSettingData.AddressOnParent
- Msvm_KvpExchangeComponentSettingData.VirtualQuantityUnits
- Msvm_KvpExchangeComponentSettingData.EnabledState
- Msvm_KvpExchangeComponentSettingData.HostExchangeItems
- Msvm_KvpExchangeComponentSettingData.HostOnlyItems
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2fe2ef128d3212ba2dfd47a3d71f713c26ba2435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533878"
---
# <a name="msvm_kvpexchangecomponentsettingdata-class"></a><span data-ttu-id="74619-103">MSVM \_ KvpExchangeComponentSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="74619-103">Msvm\_KvpExchangeComponentSettingData class</span></span>

<span data-ttu-id="74619-104">Représente l’état configuré du service d’échange de paires clé/valeur.</span><span class="sxs-lookup"><span data-stu-id="74619-104">Represents the configured state of the key/value pair exchange service.</span></span>

<span data-ttu-id="74619-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="74619-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="74619-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74619-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_KvpExchangeComponentSettingData : CIM_ResourceAllocationSettingData
{
  boolean DisableHostKVPItems;
  string  InstanceID;
  string  Caption = "Key-Value Pair Exchange";
  string  Description = "Microsoft Key-Value Pair Exchange Service Setting Data";
  string  ElementName = "Key-Value Pair Exchange";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:Key-Value Pair Exchange Component";
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
  String  HostExchangeItems[];
  String  HostOnlyItems[];
};
```

## <a name="members"></a><span data-ttu-id="74619-107">Membres</span><span class="sxs-lookup"><span data-stu-id="74619-107">Members</span></span>

<span data-ttu-id="74619-108">La classe **MSVM \_ KvpExchangeComponentSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="74619-108">The **Msvm\_KvpExchangeComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="74619-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="74619-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="74619-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="74619-110">Properties</span></span>

<span data-ttu-id="74619-111">La classe **MSVM \_ KvpExchangeComponentSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="74619-111">The **Msvm\_KvpExchangeComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="74619-112">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="74619-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74619-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="74619-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74619-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74619-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74619-115">Adresse de la ressource.</span><span class="sxs-lookup"><span data-stu-id="74619-115">The address of the resource.</span></span> <span data-ttu-id="74619-116">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) et a toujours la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="74619-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="74619-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="74619-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74619-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="74619-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74619-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74619-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74619-120">Décrit l’adresse de cette ressource dans le contexte du parent.</span><span class="sxs-lookup"><span data-stu-id="74619-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="74619-121">Les propriétés **parent** et **AddressOnParent** sont utilisées pour décrire la relation du contrôleur, ainsi que l’ordre des appareils sur un contrôleur.</span><span class="sxs-lookup"><span data-stu-id="74619-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="74619-122">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="74619-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="74619-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="74619-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74619-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="74619-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74619-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74619-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74619-126">Unités d’allocation utilisées par la **réservation** et les propriétés de la **limite** .</span><span class="sxs-lookup"><span data-stu-id="74619-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="74619-127">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="74619-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="74619-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="74619-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74619-129">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="74619-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74619-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74619-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74619-131">Indique si la ressource sera automatiquement allouée.</span><span class="sxs-lookup"><span data-stu-id="74619-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="74619-132">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="74619-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="74619-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="74619-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74619-134">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="74619-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74619-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74619-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74619-136">Indique si la ressource sera automatiquement désallouée.</span><span class="sxs-lookup"><span data-stu-id="74619-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="74619-137">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="74619-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="74619-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="74619-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74619-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="74619-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74619-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74619-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74619-141">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="74619-141">A short description of the object.</span></span> <span data-ttu-id="74619-142">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="74619-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="74619-143">**Connection**</span><span class="sxs-lookup"><span data-stu-id="74619-143">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74619-144">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="74619-144">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="74619-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74619-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74619-146">Élément auquel cette ressource est connectée.</span><span class="sxs-lookup"><span data-stu-id="74619-146">The thing to which this resource is connected.</span></span> <span data-ttu-id="74619-147">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) et a toujours la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="74619-147">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="74619-148">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="74619-148">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74619-149">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74619-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74619-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74619-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74619-151">Visibilité des consommateurs sur la ressource allouée.</span><span class="sxs-lookup"><span data-stu-id="74619-151">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="74619-152">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="74619-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="74619-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="74619-153">Value</span></span>                                                                        | <span data-ttu-id="74619-154">Signification</span><span class="sxs-lookup"><span data-stu-id="74619-154">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="74619-155"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="74619-155"><dt>3</dt></span></span> </dl> | <span data-ttu-id="74619-156">Virtualisé</span><span class="sxs-lookup"><span data-stu-id="74619-156">Virtualized</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="74619-157">**Description**</span><span class="sxs-lookup"><span data-stu-id="74619-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74619-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="74619-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74619-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74619-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74619-160">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="74619-160">A description of the object.</span></span> <span data-ttu-id="74619-161">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="74619-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="74619-162">**DisableHostKVPItems**</span><span class="sxs-lookup"><span data-stu-id="74619-162">**DisableHostKVPItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74619-163">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="74619-163">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74619-164">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="74619-164">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74619-165">Cette propriété désactive l’hôte de populatinghost automatiquement les informations de nom et de système d’exploitation à l’intérieur de l’invité.</span><span class="sxs-lookup"><span data-stu-id="74619-165">This property disables the host from automatically populatinghost name and OS information inside the guest.</span></span>

> [!Note]  
> <span data-ttu-id="74619-166">Cette propriété a été ajoutée dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="74619-166">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="74619-167">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="74619-167">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74619-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="74619-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74619-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74619-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74619-170">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="74619-170">A display name for the object.</span></span> <span data-ttu-id="74619-171">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="74619-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="74619-172">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="74619-172">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74619-173">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74619-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74619-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74619-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74619-175">État activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="74619-175">The enabled state of the element.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="74619-176">**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="74619-176">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="74619-177">**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="74619-177">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="74619-178">**HostExchangeItems**</span><span class="sxs-lookup"><span data-stu-id="74619-178">**HostExchangeItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74619-179">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="74619-179">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="74619-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74619-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74619-181">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("MSVM \_ KvpExchangeDataItem")</span><span class="sxs-lookup"><span data-stu-id="74619-181">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="74619-182">Tableau d’instances [**MSVM \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) incorporées qui représentent les paires clé/valeur.</span><span class="sxs-lookup"><span data-stu-id="74619-182">An array of embedded [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances that represent the key/value pairs.</span></span>

</dd> <dt>

<span data-ttu-id="74619-183">**HostOnlyItems**</span><span class="sxs-lookup"><span data-stu-id="74619-183">**HostOnlyItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74619-184">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="74619-184">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="74619-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74619-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74619-186">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("MSVM \_ KvpExchangeDataItem")</span><span class="sxs-lookup"><span data-stu-id="74619-186">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="74619-187">Tableau d’instances [**de \_ KvpExchangeDataItem MSVM**](msvm-kvpexchangedataitem.md) contenant les paires clé/valeur qui sont stockées dans le fichier de configuration, mais qui ne sont pas échangées avec le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="74619-187">An array of [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances containing the key/value pairs that are stored in the configuration file but not exchanged with the guest operating system.</span></span> <span data-ttu-id="74619-188">Cela permet aux applications de stocker des données spécifiques à l’ordinateur virtuel qui n’ont pas besoin d’être visibles par le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="74619-188">This allows applications to store virtual machine-specific data that does not need to be visible to the guest operating system.</span></span> <span data-ttu-id="74619-189">Les éléments sont mis en forme de la même façon que les éléments de la propriété **HostExchangeItems** , à l’exception du fait que la propriété **source** de l’instance **MSVM \_ KvpExchangeDataItem** est définie sur 4.</span><span class="sxs-lookup"><span data-stu-id="74619-189">The items are formatted the same as the items in the **HostExchangeItems** property except the **Source** property of the **Msvm\_KvpExchangeDataItem** instance is set to 4.</span></span> <span data-ttu-id="74619-190">Chaque fichier de configuration est limité à 128 paires clé/valeur, où chaque champ de valeur peut avoir une taille maximale de 16 Ko et le champ clé est autorisé à atteindre 512 octets.</span><span class="sxs-lookup"><span data-stu-id="74619-190">Each configuration file is limited to 128 key/value pairs, where each value field is allowed to be up to 16 KB in size and the key field is allowed to be up to 512 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="74619-191">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="74619-191">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74619-192">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="74619-192">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="74619-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74619-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74619-194">Expose une attribution spécifique à l’hôte ou aux ressources sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="74619-194">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="74619-195">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) et a toujours la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="74619-195">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="74619-196">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="74619-196">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74619-197">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="74619-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74619-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74619-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74619-199">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="74619-199">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="74619-200">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="74619-200">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="74619-201">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="74619-201">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="74619-202">**Limite**</span><span class="sxs-lookup"><span data-stu-id="74619-202">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74619-203">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="74619-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="74619-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74619-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74619-205">Limite supérieure ou quantité maximale de ressources qui seront accordées pour cette allocation.</span><span class="sxs-lookup"><span data-stu-id="74619-205">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="74619-206">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="74619-206">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="74619-207">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="74619-207">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74619-208">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74619-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74619-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74619-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74619-210">Spécifie comment cette ressource est mappée aux ressources sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="74619-210">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="74619-211">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) et a toujours la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="74619-211">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="74619-212">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="74619-212">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74619-213">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="74619-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74619-214">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74619-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74619-215">Chaîne qui décrit le type de ressource lorsqu’une valeur bien définie n’est pas disponible et que **resourceType** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="74619-215">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="74619-216">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="74619-216">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="74619-217">**Parent**</span><span class="sxs-lookup"><span data-stu-id="74619-217">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74619-218">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="74619-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74619-219">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74619-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74619-220">Parent de la ressource.</span><span class="sxs-lookup"><span data-stu-id="74619-220">The parent of the resource.</span></span> <span data-ttu-id="74619-221">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) et a toujours la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="74619-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="74619-222">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="74619-222">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74619-223">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="74619-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74619-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74619-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74619-225">ID du pool de ressources à partir duquel la ressource est allouée.</span><span class="sxs-lookup"><span data-stu-id="74619-225">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="74619-226">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="74619-226">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="74619-227">**Réservation**</span><span class="sxs-lookup"><span data-stu-id="74619-227">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74619-228">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="74619-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="74619-229">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74619-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74619-230">Quantité de ressources dont la disponibilité est garantie pour cette allocation.</span><span class="sxs-lookup"><span data-stu-id="74619-230">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="74619-231">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="74619-231">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="74619-232">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="74619-232">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74619-233">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="74619-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74619-234">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74619-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74619-235">Chaîne qui décrit un sous-type spécifique à l’implémentation pour cette ressource.</span><span class="sxs-lookup"><span data-stu-id="74619-235">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="74619-236">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="74619-236">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="74619-237">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="74619-237">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74619-238">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74619-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74619-239">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74619-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74619-240">Type de ressource représenté par ce paramètre d’allocation.</span><span class="sxs-lookup"><span data-stu-id="74619-240">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="74619-241">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="74619-241">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="74619-242">Valeur</span><span class="sxs-lookup"><span data-stu-id="74619-242">Value</span></span>                                                                        | <span data-ttu-id="74619-243">Signification</span><span class="sxs-lookup"><span data-stu-id="74619-243">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="74619-244"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="74619-244"><dt>1</dt></span></span> </dl> | <span data-ttu-id="74619-245">Autres</span><span class="sxs-lookup"><span data-stu-id="74619-245">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="74619-246">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="74619-246">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74619-247">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="74619-247">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="74619-248">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74619-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74619-249">Quantité de ressources présentées au consommateur.</span><span class="sxs-lookup"><span data-stu-id="74619-249">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="74619-250">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="74619-250">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="74619-251">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="74619-251">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74619-252">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="74619-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74619-253">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74619-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74619-254">Spécifie l’unité de mesure pour cette allocation de ressources.</span><span class="sxs-lookup"><span data-stu-id="74619-254">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="74619-255">La valeur de cette propriété doit être une valeur légale du qualificateur d’unités de programmation, tel que défini dans l’annexe C. 1 de DSP0004 V 2.5 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="74619-255">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="74619-256">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="74619-256">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="74619-257">**Poids**</span><span class="sxs-lookup"><span data-stu-id="74619-257">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74619-258">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74619-258">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74619-259">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74619-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74619-260">Priorité relative pour cette allocation par rapport à d’autres allocations à partir du même pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="74619-260">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="74619-261">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="74619-261">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74619-262">Notes</span><span class="sxs-lookup"><span data-stu-id="74619-262">Remarks</span></span>

<span data-ttu-id="74619-263">L’accès à la classe **MSVM \_ KvpExchangeComponentSettingData** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="74619-263">Access to the **Msvm\_KvpExchangeComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="74619-264">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="74619-264">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="74619-265">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74619-265">Requirements</span></span>



| <span data-ttu-id="74619-266">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74619-266">Requirement</span></span> | <span data-ttu-id="74619-267">Valeur</span><span class="sxs-lookup"><span data-stu-id="74619-267">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74619-268">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74619-268">Minimum supported client</span></span><br/> | <span data-ttu-id="74619-269">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74619-269">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="74619-270">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74619-270">Minimum supported server</span></span><br/> | <span data-ttu-id="74619-271">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74619-271">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="74619-272">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="74619-272">Namespace</span></span><br/>                | <span data-ttu-id="74619-273">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="74619-273">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="74619-274">MOF</span><span class="sxs-lookup"><span data-stu-id="74619-274">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74619-275"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="74619-275"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="74619-276">DLL</span><span class="sxs-lookup"><span data-stu-id="74619-276">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74619-277"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="74619-277"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="74619-278">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74619-278">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74619-279">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="74619-279">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="74619-280">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="74619-280">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

