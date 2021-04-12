---
description: Représente les États d’allocation actuels et enregistrés d’une ressource virtuelle.
ms.assetid: 5C180933-2013-4E16-A9BD-653D5426F468
title: Classe Msvm_ResourceAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceAllocationSettingData
- Msvm_ResourceAllocationSettingData.InstanceID
- Msvm_ResourceAllocationSettingData.Caption
- Msvm_ResourceAllocationSettingData.Description
- Msvm_ResourceAllocationSettingData.ElementName
- Msvm_ResourceAllocationSettingData.ResourceType
- Msvm_ResourceAllocationSettingData.OtherResourceType
- Msvm_ResourceAllocationSettingData.ResourceSubType
- Msvm_ResourceAllocationSettingData.PoolID
- Msvm_ResourceAllocationSettingData.ConsumerVisibility
- Msvm_ResourceAllocationSettingData.HostResource
- Msvm_ResourceAllocationSettingData.AllocationUnits
- Msvm_ResourceAllocationSettingData.VirtualQuantity
- Msvm_ResourceAllocationSettingData.Reservation
- Msvm_ResourceAllocationSettingData.Limit
- Msvm_ResourceAllocationSettingData.Weight
- Msvm_ResourceAllocationSettingData.AutomaticAllocation
- Msvm_ResourceAllocationSettingData.AutomaticDeallocation
- Msvm_ResourceAllocationSettingData.Parent
- Msvm_ResourceAllocationSettingData.Connection
- Msvm_ResourceAllocationSettingData.Address
- Msvm_ResourceAllocationSettingData.MappingBehavior
- Msvm_ResourceAllocationSettingData.AddressOnParent
- Msvm_ResourceAllocationSettingData.VirtualQuantityUnits
- Msvm_ResourceAllocationSettingData.VirtualSystemIdentifiers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6d1cb2f97dcb3fa144db5cf27c1a82690214b11d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319397"
---
# <a name="msvm_resourceallocationsettingdata-class"></a><span data-ttu-id="570f4-103">MSVM \_ ResourceAllocationSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="570f4-103">Msvm\_ResourceAllocationSettingData class</span></span>

<span data-ttu-id="570f4-104">Représente les États d’allocation actuels et enregistrés d’une ressource virtuelle.</span><span class="sxs-lookup"><span data-stu-id="570f4-104">Represents the current and recorded allocation states of a virtual resource.</span></span>

<span data-ttu-id="570f4-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="570f4-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="570f4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="570f4-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourceAllocationSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string  Caption;
  string  Description;
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
  string  VirtualSystemIdentifiers[] = { "GUID" };
};
```

## <a name="members"></a><span data-ttu-id="570f4-107">Membres</span><span class="sxs-lookup"><span data-stu-id="570f4-107">Members</span></span>

<span data-ttu-id="570f4-108">La classe **MSVM \_ ResourceAllocationSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="570f4-108">The **Msvm\_ResourceAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="570f4-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="570f4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="570f4-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="570f4-110">Properties</span></span>

<span data-ttu-id="570f4-111">La classe **MSVM \_ ResourceAllocationSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="570f4-111">The **Msvm\_ResourceAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="570f4-112">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="570f4-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="570f4-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="570f4-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="570f4-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="570f4-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="570f4-115">Adresse de la ressource.</span><span class="sxs-lookup"><span data-stu-id="570f4-115">The address of the resource.</span></span> <span data-ttu-id="570f4-116">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="570f4-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="570f4-117">Il s’agit d’une propriété en lecture seule, mais si la propriété **resourceType** a la valeur 20 (contrôleur Graphics), elle peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="570f4-117">This is a read-only property, but if the **ResourceType** property is 20 (Graphics controller), it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="570f4-118">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="570f4-118">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="570f4-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="570f4-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="570f4-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="570f4-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="570f4-121">Décrit l’adresse de cette ressource dans le contexte du parent.</span><span class="sxs-lookup"><span data-stu-id="570f4-121">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="570f4-122">Les propriétés **parent** et **AddressOnParent** sont utilisées pour décrire la relation du contrôleur, ainsi que l’ordre des appareils sur un contrôleur.</span><span class="sxs-lookup"><span data-stu-id="570f4-122">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="570f4-123">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="570f4-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="570f4-124">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="570f4-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="570f4-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="570f4-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="570f4-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="570f4-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="570f4-127">Unité d’allocation utilisée par les propriétés de **réservation** et de **limite** .</span><span class="sxs-lookup"><span data-stu-id="570f4-127">The unit of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="570f4-128">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="570f4-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="570f4-129">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="570f4-129">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="570f4-130">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="570f4-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="570f4-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="570f4-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="570f4-132">Indique si la ressource sera automatiquement allouée.</span><span class="sxs-lookup"><span data-stu-id="570f4-132">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="570f4-133">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="570f4-133">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="570f4-134">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="570f4-134">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="570f4-135">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="570f4-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="570f4-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="570f4-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="570f4-137">Indique si la ressource sera automatiquement désallouée.</span><span class="sxs-lookup"><span data-stu-id="570f4-137">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="570f4-138">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="570f4-138">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="570f4-139">**Caption**</span><span class="sxs-lookup"><span data-stu-id="570f4-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="570f4-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="570f4-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="570f4-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="570f4-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="570f4-142">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="570f4-142">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="570f4-143">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="570f4-143">A short description of the object.</span></span> <span data-ttu-id="570f4-144">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="570f4-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="570f4-145">**Connection**</span><span class="sxs-lookup"><span data-stu-id="570f4-145">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="570f4-146">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="570f4-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="570f4-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="570f4-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="570f4-148">Appareil auquel cette ressource est connectée.</span><span class="sxs-lookup"><span data-stu-id="570f4-148">The device to which this resource is connected.</span></span> <span data-ttu-id="570f4-149">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="570f4-149">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="570f4-150">Il s’agit d’une propriété en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="570f4-150">This is a read-only property.</span></span> <span data-ttu-id="570f4-151">Toutefois, si la propriété **resourceType** est 21 (port série) et que la propriété **ResourceSubType** est « Microsoft : Hyper-V : Serial Port », la propriété de **connexion** peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**\_ VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="570f4-151">But if the **ResourceType** property is 21 (Serial port) and the **ResourceSubType** property is "Microsoft:Hyper-V:Serial Port", the **Connection** property can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="570f4-152">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="570f4-152">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="570f4-153">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="570f4-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="570f4-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="570f4-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="570f4-155">Visibilité du consommateur sur la ressource allouée.</span><span class="sxs-lookup"><span data-stu-id="570f4-155">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="570f4-156">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="570f4-156">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="570f4-157">**Description**</span><span class="sxs-lookup"><span data-stu-id="570f4-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="570f4-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="570f4-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="570f4-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="570f4-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="570f4-160">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="570f4-160">A description of the object.</span></span> <span data-ttu-id="570f4-161">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="570f4-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="570f4-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="570f4-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="570f4-163">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="570f4-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="570f4-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="570f4-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="570f4-165">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="570f4-165">A display name for the object.</span></span> <span data-ttu-id="570f4-166">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="570f4-166">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="570f4-167">La modification de cette propriété modifie le nom d’élément du dérivé de l’appareil logique associé.</span><span class="sxs-lookup"><span data-stu-id="570f4-167">Changing this property will change the element name of the associated logical device derivative.</span></span>

<span data-ttu-id="570f4-168">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="570f4-168">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="570f4-169">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="570f4-169">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="570f4-170">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="570f4-170">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="570f4-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="570f4-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="570f4-172">Une seule ressource hôte peut être affectée à chaque périphérique de l’ordinateur virtuel, de sorte que seul le premier élément de ce tableau peut être défini.</span><span class="sxs-lookup"><span data-stu-id="570f4-172">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="570f4-173">Pour les appareils qui prennent en charge cette fonctionnalité, définissez le premier élément du tableau **HostResource** pour qu’il contienne une référence à la ressource hôte sous-jacente à assigner.</span><span class="sxs-lookup"><span data-stu-id="570f4-173">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="570f4-174">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="570f4-174">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="570f4-175">Il s’agit d’une propriété en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="570f4-175">This is a read-only property.</span></span> <span data-ttu-id="570f4-176">Toutefois, si la propriété **resourceType** est 17 (Disk) et que la propriété **ResourceSubType** est « Microsoft : Hyper-V : Physical Disk Drive », la propriété **HostResource** peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="570f4-176">But if the **ResourceType** property is 17 (Disk) and the **ResourceSubType** property is "Microsoft:Hyper-V:Physical Disk Drive", the **HostResource** property can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="570f4-177">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="570f4-177">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="570f4-178">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="570f4-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="570f4-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="570f4-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="570f4-180">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="570f4-180">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="570f4-181">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="570f4-181">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="570f4-182">Cette propriété est héritée de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))et est toujours définie sur « Microsoft :*GUID* \\ *DeviceSpecificData*».</span><span class="sxs-lookup"><span data-stu-id="570f4-182">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> <dt>

<span data-ttu-id="570f4-183">**Limite**</span><span class="sxs-lookup"><span data-stu-id="570f4-183">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="570f4-184">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="570f4-184">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="570f4-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="570f4-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="570f4-186">Quantité maximale de ressources qui seront accordées pour cette allocation.</span><span class="sxs-lookup"><span data-stu-id="570f4-186">The maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="570f4-187">L’unité de mesure de cette propriété est spécifiée par la propriété **VirtualQuantityUnits** .</span><span class="sxs-lookup"><span data-stu-id="570f4-187">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="570f4-188">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="570f4-188">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="570f4-189">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="570f4-189">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="570f4-190">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="570f4-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="570f4-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="570f4-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="570f4-192">Spécifie comment cette ressource est mappée aux ressources sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="570f4-192">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="570f4-193">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="570f4-193">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="570f4-194">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="570f4-194">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="570f4-195">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="570f4-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="570f4-196">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="570f4-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="570f4-197">Chaîne qui décrit le type de ressource lorsqu’une valeur bien définie n’est pas disponible et que [**resourceType**](msvm-processorsettingdata.md) a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="570f4-197">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="570f4-198">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="570f4-198">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="570f4-199">**Parent**</span><span class="sxs-lookup"><span data-stu-id="570f4-199">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="570f4-200">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="570f4-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="570f4-201">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="570f4-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="570f4-202">Parent de la ressource.</span><span class="sxs-lookup"><span data-stu-id="570f4-202">The parent of the resource.</span></span> <span data-ttu-id="570f4-203">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="570f4-203">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="570f4-204">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="570f4-204">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="570f4-205">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="570f4-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="570f4-206">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="570f4-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="570f4-207">Identificateur du pool de ressources à partir duquel cette ressource a été allouée.</span><span class="sxs-lookup"><span data-stu-id="570f4-207">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="570f4-208">Pour les instances associées à une machine virtuelle, il s’agit de « Microsoft :*GUID* \\ *Device-Specific Data*».</span><span class="sxs-lookup"><span data-stu-id="570f4-208">For instances associated with a virtual machine, this will be "Microsoft:*GUID*\\*device-specific data*".</span></span> <span data-ttu-id="570f4-209">Pour les instances qui définissent les paramètres potentiels d’une machine virtuelle, il s’agit de « Microsoft : définition \\ *GUID* \\ *type*», où *type* peut être « maximum », « minimum », « default » ou « Increment ».</span><span class="sxs-lookup"><span data-stu-id="570f4-209">For instances that define potential settings for a virtual machine, this will be "Microsoft:Definition\\*GUID*\\*Type*", where *Type* can be one of "Maximum", "Minimum", "Default", or "Increment".</span></span> <span data-ttu-id="570f4-210">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="570f4-210">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="570f4-211">**Réservation**</span><span class="sxs-lookup"><span data-stu-id="570f4-211">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="570f4-212">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="570f4-212">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="570f4-213">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="570f4-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="570f4-214">Quantité de ressources dont la disponibilité est garantie pour cette allocation.</span><span class="sxs-lookup"><span data-stu-id="570f4-214">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="570f4-215">L’unité de mesure de cette propriété est spécifiée par la propriété **VirtualQuantityUnits** .</span><span class="sxs-lookup"><span data-stu-id="570f4-215">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="570f4-216">Ces ressources sont garanties d’être disponibles pour la consommation par l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="570f4-216">These resources are guaranteed to be available for consumption by the virtual machine.</span></span> <span data-ttu-id="570f4-217">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="570f4-217">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="570f4-218">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="570f4-218">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="570f4-219">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="570f4-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="570f4-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="570f4-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="570f4-221">Chaîne qui décrit un sous-type spécifique à l’implémentation pour cette ressource.</span><span class="sxs-lookup"><span data-stu-id="570f4-221">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="570f4-222">Par exemple, cela peut être utilisé pour distinguer différents modèles du même type de ressource.</span><span class="sxs-lookup"><span data-stu-id="570f4-222">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="570f4-223">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="570f4-223">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="570f4-224">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="570f4-224">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="570f4-225">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="570f4-225">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="570f4-226">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="570f4-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="570f4-227">Type de ressource représenté par ce paramètre d’allocation.</span><span class="sxs-lookup"><span data-stu-id="570f4-227">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="570f4-228">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="570f4-228">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="570f4-229"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="570f4-229"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-230"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Système informatique** (2)</span><span class="sxs-lookup"><span data-stu-id="570f4-230"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-231"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processeur** (3)</span><span class="sxs-lookup"><span data-stu-id="570f4-231"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-232"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Mémoire** (4)</span><span class="sxs-lookup"><span data-stu-id="570f4-232"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-233"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Contrôleur IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="570f4-233"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-234"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI parallèle** (6)</span><span class="sxs-lookup"><span data-stu-id="570f4-234"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-235"><span id="FC_HBA"></span><span id="fc_hba"></span>**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="570f4-235"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-236"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="570f4-236"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-237"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="570f4-237"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-238"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Carte Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="570f4-238"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-239"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Autre carte réseau** (11)</span><span class="sxs-lookup"><span data-stu-id="570f4-239"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-240"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Emplacement d’e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="570f4-240"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-241"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Périphérique d’e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="570f4-241"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-242"><span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Lecteur de disquette** (14)</span><span class="sxs-lookup"><span data-stu-id="570f4-242"><span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Diskette Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-243"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Lecteur de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="570f4-243"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-244"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Lecteur de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="570f4-244"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-245"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Lecteur de disque** (17)</span><span class="sxs-lookup"><span data-stu-id="570f4-245"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Disk Drive** (17)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-246"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Lecteur de bande** (18)</span><span class="sxs-lookup"><span data-stu-id="570f4-246"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Tape Drive** (18)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-247"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extension de stockage** (19)</span><span class="sxs-lookup"><span data-stu-id="570f4-247"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (19)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-248"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Autre dispositif de stockage** (20)</span><span class="sxs-lookup"><span data-stu-id="570f4-248"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other Storage Device** (20)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-249"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Port série** (21)</span><span class="sxs-lookup"><span data-stu-id="570f4-249"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (21)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-250"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Port parallèle** (22)</span><span class="sxs-lookup"><span data-stu-id="570f4-250"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (22)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-251"><span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Contrôleur USB** (23)</span><span class="sxs-lookup"><span data-stu-id="570f4-251"><span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB controller** (23)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-252"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Contrôleur Graphics** (24)</span><span class="sxs-lookup"><span data-stu-id="570f4-252"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (24)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-253"><span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**Contrôleur IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="570f4-253"><span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-254"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unité partitionnée** (26)</span><span class="sxs-lookup"><span data-stu-id="570f4-254"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-255"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unité partitionnée de base** (27)</span><span class="sxs-lookup"><span data-stu-id="570f4-255"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-256"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Alimentation (28** )</span><span class="sxs-lookup"><span data-stu-id="570f4-256"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-257"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Appareil de refroidissement** (29)</span><span class="sxs-lookup"><span data-stu-id="570f4-257"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-258"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Port commuté Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="570f4-258"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet Switch Port** (30)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-259"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Disque logique** (31)</span><span class="sxs-lookup"><span data-stu-id="570f4-259"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logical Disk** (31)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-260"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Volume de stockage** (32)</span><span class="sxs-lookup"><span data-stu-id="570f4-260"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-261"><span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Connexion Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="570f4-261"><span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet connection** (33)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-262"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (30 32767)</span><span class="sxs-lookup"><span data-stu-id="570f4-262"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (30 32767)</span></span>
</dt> <dt>

<span data-ttu-id="570f4-263"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="570f4-263"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="570f4-264">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="570f4-264">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="570f4-265">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="570f4-265">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="570f4-266">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="570f4-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="570f4-267">Spécifie la quantité de ressources présentées au consommateur.</span><span class="sxs-lookup"><span data-stu-id="570f4-267">Specifies the quantity of resources presented to the consumer.</span></span> <span data-ttu-id="570f4-268">L’unité de mesure de cette propriété est spécifiée par la propriété **VirtualQuantityUnits** .</span><span class="sxs-lookup"><span data-stu-id="570f4-268">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="570f4-269">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="570f4-269">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="570f4-270">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="570f4-270">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="570f4-271">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="570f4-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="570f4-272">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="570f4-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="570f4-273">Spécifie l’unité de mesure pour cette allocation de ressources.</span><span class="sxs-lookup"><span data-stu-id="570f4-273">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="570f4-274">La valeur de cette propriété doit être une valeur légale du qualificateur d’unités de programmation, tel que défini dans l’annexe C. 1 de DSP0004 V 2.5 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="570f4-274">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="570f4-275">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="570f4-275">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="570f4-276">**VirtualSystemIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="570f4-276">**VirtualSystemIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="570f4-277">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="570f4-277">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="570f4-278">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="570f4-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="570f4-279">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="570f4-279">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="570f4-280">Tableau de chaînes des identificateurs de cette ressource présentée au système d’exploitation de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="570f4-280">A string array of identifiers of this resource presented to the virtual machine's operating system.</span></span> <span data-ttu-id="570f4-281">Ces valeurs sont utilisées uniquement si la propriété **resourceType** est définie sur 6 (adaptateur de bus hôte SCSI parallèle) et que la propriété **ResourceSubType** est définie sur « contrôleur SCSI Microsoft synthétique ».</span><span class="sxs-lookup"><span data-stu-id="570f4-281">These values are used only if the **ResourceType** property is set to 6 (Parallel SCSI HBA) and the **ResourceSubType** property is set to "Microsoft Synthetic SCSI Controller".</span></span> <span data-ttu-id="570f4-282">Cette propriété est définie sur «*GUID*».</span><span class="sxs-lookup"><span data-stu-id="570f4-282">This property is set to "*GUID*".</span></span>

<span data-ttu-id="570f4-283">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="570f4-283">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="570f4-284">**Poids**</span><span class="sxs-lookup"><span data-stu-id="570f4-284">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="570f4-285">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="570f4-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="570f4-286">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="570f4-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="570f4-287">Entier qui définit la pondération relative pour chaque processeur d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="570f4-287">An integer that defines the relative weight for each virtual machine processor.</span></span> <span data-ttu-id="570f4-288">Une fois toutes les réserves remplies, la capacité du processeur physique restant de la plateforme d’hébergement sera allouée aux ordinateurs virtuels en fonction de leurs pondérations relatives.</span><span class="sxs-lookup"><span data-stu-id="570f4-288">After all reserves have been met, the remaining physical processor capacity of the hosting platform will be allocated to virtual machines based on their relative weights.</span></span> <span data-ttu-id="570f4-289">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="570f4-289">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="570f4-290">Plage : 0 1000</span><span class="sxs-lookup"><span data-stu-id="570f4-290">Range: 0 1000</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="570f4-291">Notes</span><span class="sxs-lookup"><span data-stu-id="570f4-291">Remarks</span></span>

<span data-ttu-id="570f4-292">L’accès à la classe **MSVM \_ ResourceAllocationSettingData** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="570f4-292">Access to the **Msvm\_ResourceAllocationSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="570f4-293">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="570f4-293">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="570f4-294">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="570f4-294">Requirements</span></span>



| <span data-ttu-id="570f4-295">Condition requise</span><span class="sxs-lookup"><span data-stu-id="570f4-295">Requirement</span></span> | <span data-ttu-id="570f4-296">Valeur</span><span class="sxs-lookup"><span data-stu-id="570f4-296">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="570f4-297">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="570f4-297">Minimum supported client</span></span><br/> | <span data-ttu-id="570f4-298">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="570f4-298">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="570f4-299">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="570f4-299">Minimum supported server</span></span><br/> | <span data-ttu-id="570f4-300">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="570f4-300">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="570f4-301">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="570f4-301">Namespace</span></span><br/>                | <span data-ttu-id="570f4-302">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="570f4-302">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="570f4-303">MOF</span><span class="sxs-lookup"><span data-stu-id="570f4-303">MOF</span></span><br/>                      | <dl> <span data-ttu-id="570f4-304"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="570f4-304"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="570f4-305">DLL</span><span class="sxs-lookup"><span data-stu-id="570f4-305">DLL</span></span><br/>                      | <dl> <span data-ttu-id="570f4-306"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="570f4-306"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="570f4-307">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="570f4-307">See also</span></span>

<dl> <dt>

[<span data-ttu-id="570f4-308">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="570f4-308">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="570f4-309">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="570f4-309">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="570f4-310">**MSVM \_ ResourceAllocationSettingData (v1)**</span><span class="sxs-lookup"><span data-stu-id="570f4-310">**Msvm\_ResourceAllocationSettingData (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="570f4-311">Classes de gestion des ressources</span><span class="sxs-lookup"><span data-stu-id="570f4-311">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

