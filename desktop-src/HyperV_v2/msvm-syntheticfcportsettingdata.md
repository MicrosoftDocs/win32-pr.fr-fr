---
description: Représente l’état configuré d’un port de Fibre Channel synthétique.
ms.assetid: 5d47dd80-de34-4ae4-a300-c16da1cd4974
title: Classe Msvm_SyntheticFcPortSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticFcPortSettingData
- Msvm_SyntheticFcPortSettingData.InstanceID
- Msvm_SyntheticFcPortSettingData.Caption
- Msvm_SyntheticFcPortSettingData.Description
- Msvm_SyntheticFcPortSettingData.ElementName
- Msvm_SyntheticFcPortSettingData.ResourceType
- Msvm_SyntheticFcPortSettingData.OtherResourceType
- Msvm_SyntheticFcPortSettingData.ResourceSubType
- Msvm_SyntheticFcPortSettingData.PoolID
- Msvm_SyntheticFcPortSettingData.ConsumerVisibility
- Msvm_SyntheticFcPortSettingData.HostResource
- Msvm_SyntheticFcPortSettingData.AllocationUnits
- Msvm_SyntheticFcPortSettingData.VirtualQuantity
- Msvm_SyntheticFcPortSettingData.Reservation
- Msvm_SyntheticFcPortSettingData.Limit
- Msvm_SyntheticFcPortSettingData.Weight
- Msvm_SyntheticFcPortSettingData.AutomaticAllocation
- Msvm_SyntheticFcPortSettingData.AutomaticDeallocation
- Msvm_SyntheticFcPortSettingData.Parent
- Msvm_SyntheticFcPortSettingData.Connection
- Msvm_SyntheticFcPortSettingData.Address
- Msvm_SyntheticFcPortSettingData.MappingBehavior
- Msvm_SyntheticFcPortSettingData.AddressOnParent
- Msvm_SyntheticFcPortSettingData.VirtualQuantityUnits
- Msvm_SyntheticFcPortSettingData.VirtualPortWWPN
- Msvm_SyntheticFcPortSettingData.VirtualPortWWNN
- Msvm_SyntheticFcPortSettingData.SecondaryWWPN
- Msvm_SyntheticFcPortSettingData.SecondaryWWNN
- Msvm_SyntheticFcPortSettingData.VirtualSystemIdentifiers
- Msvm_SyntheticFcPortSettingData.ChapEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bdd0342f5429f5314f5c744a3a760101dbaa043b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750197"
---
# <a name="msvm_syntheticfcportsettingdata-class"></a><span data-ttu-id="87f83-103">MSVM \_ SyntheticFcPortSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="87f83-103">Msvm\_SyntheticFcPortSettingData class</span></span>

<span data-ttu-id="87f83-104">Représente l’état configuré d’un port de Fibre Channel synthétique.</span><span class="sxs-lookup"><span data-stu-id="87f83-104">Represents the configured state of a synthetic Fibre Channel port.</span></span>

<span data-ttu-id="87f83-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="87f83-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="87f83-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87f83-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticFcPortSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Virtual Fibre Channel Port Default Settings";
  string  Description = "Describes the default settings for the virtual Fibre Channel port resources.";
  string  ElementName;
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
  string  VirtualPortWWPN;
  string  VirtualPortWWNN;
  string  SecondaryWWPN;
  string  SecondaryWWNN;
  string  VirtualSystemIdentifiers[];
  boolean ChapEnabled;
};
```

## <a name="members"></a><span data-ttu-id="87f83-107">Membres</span><span class="sxs-lookup"><span data-stu-id="87f83-107">Members</span></span>

<span data-ttu-id="87f83-108">La classe **MSVM \_ SyntheticFcPortSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="87f83-108">The **Msvm\_SyntheticFcPortSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="87f83-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="87f83-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="87f83-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="87f83-110">Properties</span></span>

<span data-ttu-id="87f83-111">La classe **MSVM \_ SyntheticFcPortSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="87f83-111">The **Msvm\_SyntheticFcPortSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="87f83-112">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="87f83-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f83-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="87f83-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87f83-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87f83-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87f83-115">Adresse de la ressource.</span><span class="sxs-lookup"><span data-stu-id="87f83-115">The address of the resource.</span></span> <span data-ttu-id="87f83-116">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87f83-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87f83-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="87f83-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f83-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="87f83-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87f83-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87f83-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87f83-120">Décrit l’adresse de cette ressource dans le contexte du parent.</span><span class="sxs-lookup"><span data-stu-id="87f83-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="87f83-121">Les propriétés **parent** et **AddressOnParent** sont utilisées pour décrire la relation du contrôleur, ainsi que l’ordre des appareils sur un contrôleur.</span><span class="sxs-lookup"><span data-stu-id="87f83-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="87f83-122">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87f83-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87f83-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="87f83-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f83-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="87f83-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87f83-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87f83-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87f83-126">Unité d’allocation utilisée par les propriétés de **réservation** et de **limite** .</span><span class="sxs-lookup"><span data-stu-id="87f83-126">The unit of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="87f83-127">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87f83-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87f83-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="87f83-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f83-129">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="87f83-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="87f83-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87f83-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87f83-131">Indique si la ressource sera automatiquement allouée.</span><span class="sxs-lookup"><span data-stu-id="87f83-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="87f83-132">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87f83-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87f83-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="87f83-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f83-134">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="87f83-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="87f83-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87f83-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87f83-136">Indique si la ressource sera automatiquement désallouée.</span><span class="sxs-lookup"><span data-stu-id="87f83-136">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="87f83-137">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87f83-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87f83-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="87f83-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f83-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="87f83-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87f83-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87f83-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87f83-141">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="87f83-141">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="87f83-142">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="87f83-142">A short description of the object.</span></span> <span data-ttu-id="87f83-143">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="87f83-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="87f83-144">**ChapEnabled**</span><span class="sxs-lookup"><span data-stu-id="87f83-144">**ChapEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f83-145">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="87f83-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="87f83-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87f83-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87f83-147">Indique que ce port a été configuré avec un secret partagé à l’aide de DH-CHAP, ce qui permet à l’infrastructure Fibre Channel de s’authentifier que cette machine virtuelle peut légitimement utiliser les noms WWN affectés à ce port.</span><span class="sxs-lookup"><span data-stu-id="87f83-147">Indicates that this port has been configured with a shared secret using DH-CHAP, which allows the Fibre Channel fabric to authenticate that this virtual machine can legitimately use the world wide names that are assigned to this port.</span></span>

</dd> <dt>

<span data-ttu-id="87f83-148">**Connection**</span><span class="sxs-lookup"><span data-stu-id="87f83-148">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f83-149">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="87f83-149">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="87f83-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87f83-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87f83-151">Appareil auquel cette ressource est connectée.</span><span class="sxs-lookup"><span data-stu-id="87f83-151">The device to which this resource is connected.</span></span> <span data-ttu-id="87f83-152">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87f83-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87f83-153">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="87f83-153">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f83-154">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="87f83-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="87f83-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87f83-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87f83-156">Visibilité du consommateur sur la ressource allouée.</span><span class="sxs-lookup"><span data-stu-id="87f83-156">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="87f83-157">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87f83-157">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87f83-158">**Description**</span><span class="sxs-lookup"><span data-stu-id="87f83-158">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f83-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="87f83-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87f83-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87f83-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87f83-161">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="87f83-161">A description of the object.</span></span> <span data-ttu-id="87f83-162">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="87f83-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="87f83-163">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="87f83-163">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f83-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="87f83-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87f83-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87f83-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87f83-166">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="87f83-166">A display name for the object.</span></span> <span data-ttu-id="87f83-167">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="87f83-167">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="87f83-168">La modification de cette propriété modifie le nom d’élément du dérivé de l’appareil logique associé.</span><span class="sxs-lookup"><span data-stu-id="87f83-168">Changing this property will change the element name of the associated logical device derivative.</span></span>

<span data-ttu-id="87f83-169">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="87f83-169">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="87f83-170">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="87f83-170">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f83-171">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="87f83-171">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="87f83-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87f83-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87f83-173">Une seule ressource hôte peut être affectée à chaque périphérique de l’ordinateur virtuel, de sorte que seul le premier élément de ce tableau peut être défini.</span><span class="sxs-lookup"><span data-stu-id="87f83-173">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="87f83-174">Pour les appareils qui prennent en charge cette fonctionnalité, définissez le premier élément du tableau **HostResource** pour qu’il contienne une référence à la ressource hôte sous-jacente à assigner.</span><span class="sxs-lookup"><span data-stu-id="87f83-174">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="87f83-175">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87f83-175">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87f83-176">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="87f83-176">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f83-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="87f83-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87f83-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87f83-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87f83-179">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="87f83-179">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="87f83-180">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="87f83-180">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="87f83-181">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="87f83-181">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="87f83-182">**Limite**</span><span class="sxs-lookup"><span data-stu-id="87f83-182">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f83-183">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="87f83-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="87f83-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87f83-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87f83-185">Quantité maximale de ressources hôtes correspondantes qui peuvent être consommées par l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="87f83-185">The maximum amount of corresponding host resources that can be consumed by the virtual machine.</span></span> <span data-ttu-id="87f83-186">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87f83-186">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87f83-187">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="87f83-187">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f83-188">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="87f83-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="87f83-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87f83-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87f83-190">Spécifie comment cette ressource est mappée aux ressources sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="87f83-190">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="87f83-191">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87f83-191">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87f83-192">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="87f83-192">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f83-193">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="87f83-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87f83-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87f83-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87f83-195">Chaîne qui décrit le type de ressource lorsqu’une valeur bien définie n’est pas disponible et que [**resourceType**](msvm-processorsettingdata.md) a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="87f83-195">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="87f83-196">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), mais n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="87f83-196">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="87f83-197">**Parent**</span><span class="sxs-lookup"><span data-stu-id="87f83-197">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f83-198">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="87f83-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87f83-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87f83-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87f83-200">Parent de la ressource.</span><span class="sxs-lookup"><span data-stu-id="87f83-200">The parent of the resource.</span></span> <span data-ttu-id="87f83-201">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87f83-201">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87f83-202">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="87f83-202">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f83-203">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="87f83-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87f83-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87f83-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87f83-205">Identificateur du pool de ressources à partir duquel cette ressource a été allouée.</span><span class="sxs-lookup"><span data-stu-id="87f83-205">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="87f83-206">Pour les instances associées à une machine virtuelle, il s’agit de « Microsoft :*GUID* \\ *Device-Specific Data*».</span><span class="sxs-lookup"><span data-stu-id="87f83-206">For instances associated with a virtual machine, this will be "Microsoft:*GUID*\\*device-specific data*".</span></span> <span data-ttu-id="87f83-207">Pour les instances qui définissent les paramètres potentiels d’une machine virtuelle, il s’agit de « Microsoft : définition \\ *GUID* \\ *type*», où *type* peut être « maximum », « minimum », « default » ou « Increment ».</span><span class="sxs-lookup"><span data-stu-id="87f83-207">For instances that define potential settings for a virtual machine, this will be "Microsoft:Definition\\*GUID*\\*Type*", where *Type* can be one of "Maximum", "Minimum", "Default", or "Increment".</span></span> <span data-ttu-id="87f83-208">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87f83-208">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87f83-209">**Réservation**</span><span class="sxs-lookup"><span data-stu-id="87f83-209">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f83-210">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="87f83-210">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="87f83-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87f83-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87f83-212">Quantité de ressources réservées pour une utilisation par l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="87f83-212">The amount of resources that are reserved for use by the virtual machine.</span></span> <span data-ttu-id="87f83-213">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), mais n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="87f83-213">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="87f83-214">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="87f83-214">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f83-215">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="87f83-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87f83-216">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87f83-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87f83-217">Chaîne qui décrit un sous-type spécifique à l’implémentation pour cette ressource.</span><span class="sxs-lookup"><span data-stu-id="87f83-217">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="87f83-218">Par exemple, cela peut être utilisé pour distinguer différents modèles du même type de ressource.</span><span class="sxs-lookup"><span data-stu-id="87f83-218">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="87f83-219">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87f83-219">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87f83-220">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="87f83-220">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f83-221">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="87f83-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="87f83-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87f83-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87f83-223">Type de ressource représenté par ce paramètre d’allocation.</span><span class="sxs-lookup"><span data-stu-id="87f83-223">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="87f83-224">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87f83-224">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="87f83-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="87f83-225">Value</span></span>                                                                                                                                                                                          | <span data-ttu-id="87f83-226">Signification</span><span class="sxs-lookup"><span data-stu-id="87f83-226">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="FC_HBA"></span><span id="fc_hba"></span><dl> <span data-ttu-id="87f83-227"><dt>**FC HBA**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="87f83-227"><dt>**FC HBA**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="87f83-228">Fibre Channel</span><span class="sxs-lookup"><span data-stu-id="87f83-228">Fibre Channel</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="87f83-229">**SecondaryWWNN**</span><span class="sxs-lookup"><span data-stu-id="87f83-229">**SecondaryWWNN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f83-230">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="87f83-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87f83-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87f83-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87f83-232">Indique le nom du port de l’adaptateur de bus hôte virtuel à utiliser au cours de la migration dynamique de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="87f83-232">Indicates the world wide node name of the virtual HBA port to be used during live migration of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="87f83-233">**SecondaryWWPN**</span><span class="sxs-lookup"><span data-stu-id="87f83-233">**SecondaryWWPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f83-234">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="87f83-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87f83-235">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87f83-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87f83-236">Indique le nom de port WWN du port d’adaptateur de bus hôte virtuel à utiliser lors de la migration dynamique de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="87f83-236">Indicates the world wide port name of the virtual HBA port to be used during live migration of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="87f83-237">**VirtualPortWWNN**</span><span class="sxs-lookup"><span data-stu-id="87f83-237">**VirtualPortWWNN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f83-238">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="87f83-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87f83-239">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87f83-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87f83-240">Indique le nom de nœud WWPN du port de l’adaptateur de bus hôte virtuel.</span><span class="sxs-lookup"><span data-stu-id="87f83-240">Indicates the world wide node name of the virtual HBA port.</span></span>

</dd> <dt>

<span data-ttu-id="87f83-241">**VirtualPortWWPN**</span><span class="sxs-lookup"><span data-stu-id="87f83-241">**VirtualPortWWPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f83-242">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="87f83-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87f83-243">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87f83-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87f83-244">Indique le nom WWN du port HBA virtuel.</span><span class="sxs-lookup"><span data-stu-id="87f83-244">Indicates the world wide port name of the virtual HBA port.</span></span>

</dd> <dt>

<span data-ttu-id="87f83-245">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="87f83-245">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f83-246">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="87f83-246">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="87f83-247">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87f83-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87f83-248">Spécifie la quantité de ressources présentées au consommateur.</span><span class="sxs-lookup"><span data-stu-id="87f83-248">Specifies the quantity of resources presented to the consumer.</span></span> <span data-ttu-id="87f83-249">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87f83-249">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87f83-250">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="87f83-250">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f83-251">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="87f83-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87f83-252">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87f83-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87f83-253">Spécifie l’unité de mesure pour la propriété **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="87f83-253">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="87f83-254">La valeur de cette propriété doit être une valeur légale du qualificateur d’unités de programmation, tel que défini dans l’annexe C. 1 de DSP0004 V 2.5 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="87f83-254">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="87f83-255">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87f83-255">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87f83-256">**VirtualSystemIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="87f83-256">**VirtualSystemIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f83-257">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="87f83-257">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="87f83-258">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87f83-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87f83-259">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="87f83-259">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="87f83-260">Tableau de chaînes des identificateurs de cette ressource présentée au système d’exploitation de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="87f83-260">A string array of identifiers of this resource presented to the virtual machine's operating system.</span></span> <span data-ttu-id="87f83-261">Les index et valeurs par index sont définis par ressource (c’est-à-dire, pour chaque valeur de **resourceType** énumérée).</span><span class="sxs-lookup"><span data-stu-id="87f83-261">The indexes and values per index are defined on a per resource basis (that is, for each enumerated **ResourceType** value).</span></span> <span data-ttu-id="87f83-262">Cette propriété n’est pas utilisée</span><span class="sxs-lookup"><span data-stu-id="87f83-262">This property is not used</span></span>

</dd> <dt>

<span data-ttu-id="87f83-263">**Poids**</span><span class="sxs-lookup"><span data-stu-id="87f83-263">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f83-264">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="87f83-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="87f83-265">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87f83-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87f83-266">Entier qui définit la pondération relative pour chaque processeur d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="87f83-266">An integer that defines the relative weight for each virtual machine processor.</span></span> <span data-ttu-id="87f83-267">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), mais n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="87f83-267">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), but is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="87f83-268">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87f83-268">Requirements</span></span>



| <span data-ttu-id="87f83-269">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87f83-269">Requirement</span></span> | <span data-ttu-id="87f83-270">Valeur</span><span class="sxs-lookup"><span data-stu-id="87f83-270">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87f83-271">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87f83-271">Minimum supported client</span></span><br/> | <span data-ttu-id="87f83-272">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87f83-272">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="87f83-273">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87f83-273">Minimum supported server</span></span><br/> | <span data-ttu-id="87f83-274">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87f83-274">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="87f83-275">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="87f83-275">Namespace</span></span><br/>                | <span data-ttu-id="87f83-276">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="87f83-276">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="87f83-277">MOF</span><span class="sxs-lookup"><span data-stu-id="87f83-277">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87f83-278"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="87f83-278"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="87f83-279">DLL</span><span class="sxs-lookup"><span data-stu-id="87f83-279">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87f83-280"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="87f83-280"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

