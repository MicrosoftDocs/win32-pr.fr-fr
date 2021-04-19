---
description: Représente les paramètres d’un contrôleur d’affichage 3D synthétique pour un ordinateur virtuel.
ms.assetid: 7162AEED-90CB-41C3-BD44-8B552C00F597
title: Classe Msvm_Synthetic3DDisplayControllerSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DDisplayControllerSettingData
- Msvm_Synthetic3DDisplayControllerSettingData.InstanceID
- Msvm_Synthetic3DDisplayControllerSettingData.Caption
- Msvm_Synthetic3DDisplayControllerSettingData.Description
- Msvm_Synthetic3DDisplayControllerSettingData.ElementName
- Msvm_Synthetic3DDisplayControllerSettingData.ResourceType
- Msvm_Synthetic3DDisplayControllerSettingData.OtherResourceType
- Msvm_Synthetic3DDisplayControllerSettingData.ResourceSubType
- Msvm_Synthetic3DDisplayControllerSettingData.PoolID
- Msvm_Synthetic3DDisplayControllerSettingData.ConsumerVisibility
- Msvm_Synthetic3DDisplayControllerSettingData.HostResource
- Msvm_Synthetic3DDisplayControllerSettingData.AllocationUnits
- Msvm_Synthetic3DDisplayControllerSettingData.VirtualQuantity
- Msvm_Synthetic3DDisplayControllerSettingData.Reservation
- Msvm_Synthetic3DDisplayControllerSettingData.Limit
- Msvm_Synthetic3DDisplayControllerSettingData.Weight
- Msvm_Synthetic3DDisplayControllerSettingData.AutomaticAllocation
- Msvm_Synthetic3DDisplayControllerSettingData.AutomaticDeallocation
- Msvm_Synthetic3DDisplayControllerSettingData.Parent
- Msvm_Synthetic3DDisplayControllerSettingData.Connection
- Msvm_Synthetic3DDisplayControllerSettingData.Address
- Msvm_Synthetic3DDisplayControllerSettingData.MappingBehavior
- Msvm_Synthetic3DDisplayControllerSettingData.AddressOnParent
- Msvm_Synthetic3DDisplayControllerSettingData.VirtualQuantityUnits
- Msvm_Synthetic3DDisplayControllerSettingData.MaximumScreenResolution
- Msvm_Synthetic3DDisplayControllerSettingData.MaximumMonitors
- Msvm_Synthetic3DDisplayControllerSettingData.VRAMSizeBytes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c93bb67cd4a66c4ecc5f6820ff2de7cf3816b2b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521497"
---
# <a name="msvm_synthetic3ddisplaycontrollersettingdata-class"></a><span data-ttu-id="fc1a1-103">MSVM \_ Synthetic3DDisplayControllerSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="fc1a1-103">Msvm\_Synthetic3DDisplayControllerSettingData class</span></span>

<span data-ttu-id="fc1a1-104">Représente les paramètres d’un contrôleur d’affichage 3D synthétique pour un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-104">Represents settings for a synthetic 3-D display controller for a virtual machine.</span></span> <span data-ttu-id="fc1a1-105">Cette classe est utilisée uniquement avec les ordinateurs virtuels qui utilisent RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-105">This class is only used with virtual machines that use RemoteFX.</span></span>

<span data-ttu-id="fc1a1-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc1a1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc1a1-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synthetic3DDisplayControllerSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "3D Display Controller Default Settings";
  string  Description = "Describes the default settings for the 3D video controller resource pool.";
  string  ElementName;
  uint16  ResourceType = 24;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Synthetic 3D Display Controller";
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
  uint8   MaximumScreenResolution;
  uint8   MaximumMonitors;
  uint64  VRAMSizeBytes;
};
```

## <a name="members"></a><span data-ttu-id="fc1a1-108">Membres</span><span class="sxs-lookup"><span data-stu-id="fc1a1-108">Members</span></span>

<span data-ttu-id="fc1a1-109">La classe **MSVM \_ Synthetic3DDisplayControllerSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fc1a1-109">The **Msvm\_Synthetic3DDisplayControllerSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="fc1a1-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fc1a1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fc1a1-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fc1a1-111">Properties</span></span>

<span data-ttu-id="fc1a1-112">La classe **MSVM \_ Synthetic3DDisplayControllerSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-112">The **Msvm\_Synthetic3DDisplayControllerSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fc1a1-113">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-113">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc1a1-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc1a1-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc1a1-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc1a1-116">Adresse de la ressource.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-116">The address of the resource.</span></span> <span data-ttu-id="fc1a1-117">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc1a1-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="fc1a1-118">Il s’agit d’une propriété en lecture seule, mais si la propriété **resourceType** a la valeur 20 (contrôleur Graphics), elle peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="fc1a1-118">This is a read-only property, but if the **ResourceType** property is 20 (Graphics controller), it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="fc1a1-119">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-119">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc1a1-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc1a1-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc1a1-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc1a1-122">Décrit l’adresse de cette ressource dans le contexte du parent.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-122">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="fc1a1-123">Les propriétés **parent** et **AddressOnParent** sont utilisées pour décrire la relation du contrôleur, ainsi que l’ordre des appareils sur un contrôleur.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-123">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="fc1a1-124">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc1a1-124">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc1a1-125">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-125">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc1a1-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc1a1-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc1a1-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc1a1-128">Unités d’allocation utilisées par la **réservation** et les propriétés de la **limite** .</span><span class="sxs-lookup"><span data-stu-id="fc1a1-128">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="fc1a1-129">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc1a1-129">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc1a1-130">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-130">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc1a1-131">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fc1a1-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc1a1-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc1a1-133">Indique si la ressource sera automatiquement allouée.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-133">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="fc1a1-134">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc1a1-134">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc1a1-135">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-135">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc1a1-136">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fc1a1-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc1a1-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc1a1-138">Indique si la ressource sera automatiquement désallouée.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-138">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="fc1a1-139">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc1a1-139">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc1a1-140">**Caption**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-140">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc1a1-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc1a1-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc1a1-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc1a1-143">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="fc1a1-143">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="fc1a1-144">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-144">A short description of the object.</span></span> <span data-ttu-id="fc1a1-145">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fc1a1-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fc1a1-146">**Connection**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-146">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc1a1-147">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fc1a1-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc1a1-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc1a1-149">Appareil auquel cette ressource est connectée.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-149">The device to which this resource is connected.</span></span> <span data-ttu-id="fc1a1-150">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc1a1-150">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="fc1a1-151">Il s’agit d’une propriété en lecture seule, mais si 1) la propriété **resourceType** est 17 (port série) ou 2) la propriété **resourceType** est 21 (extension de stockage) et la propriété **ResourceSubType** est « disque dur virtuel Microsoft », puis elle peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**\_ VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="fc1a1-151">This is a read-only property, but if either 1) the **ResourceType** property is 17 (Serial port), or 2) the **ResourceType** property is 21 (Storage Extent) and the **ResourceSubType** property is "Microsoft Virtual Hard Disk", then it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="fc1a1-152">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-152">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc1a1-153">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc1a1-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc1a1-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc1a1-155">Visibilité du consommateur sur la ressource allouée.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-155">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="fc1a1-156">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc1a1-156">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc1a1-157">**Description**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc1a1-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc1a1-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc1a1-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc1a1-160">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="fc1a1-160">A description of the object.</span></span> <span data-ttu-id="fc1a1-161">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fc1a1-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fc1a1-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc1a1-163">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc1a1-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc1a1-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc1a1-165">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-165">A display name for the object.</span></span> <span data-ttu-id="fc1a1-166">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fc1a1-166">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="fc1a1-167">La modification de cette propriété modifie le nom d’élément du dérivé de l’appareil logique associé.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-167">Changing this property will change the element name of the associated logical device derivative.</span></span>

</dd> <dt>

<span data-ttu-id="fc1a1-168">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-168">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc1a1-169">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-169">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fc1a1-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc1a1-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc1a1-171">Une seule ressource hôte peut être affectée à chaque périphérique de l’ordinateur virtuel, de sorte que seul le premier élément de ce tableau peut être défini.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-171">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="fc1a1-172">Pour les appareils qui prennent en charge cette fonctionnalité, définissez le premier élément du tableau **HostResource** pour qu’il contienne une référence à la ressource hôte sous-jacente qui doit être affectée.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-172">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource that is to be assigned.</span></span> <span data-ttu-id="fc1a1-173">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc1a1-173">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc1a1-174">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-174">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc1a1-175">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc1a1-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc1a1-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc1a1-177">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-177">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="fc1a1-178">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fc1a1-178">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fc1a1-179">**Limite**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-179">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc1a1-180">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-180">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fc1a1-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc1a1-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc1a1-182">Quantité maximale de ressources hôtes correspondantes qui peuvent être consommées par l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-182">The maximum amount of corresponding host resources that can be consumed by the virtual machine.</span></span> <span data-ttu-id="fc1a1-183">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc1a1-183">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc1a1-184">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-184">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc1a1-185">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc1a1-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc1a1-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc1a1-187">Spécifie comment cette ressource est mappée aux ressources sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-187">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="fc1a1-188">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc1a1-188">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc1a1-189">**MaximumMonitors**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-189">**MaximumMonitors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc1a1-190">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-190">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="fc1a1-191">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fc1a1-191">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fc1a1-192">Nombre maximal d’analyses disponibles pour le contrôleur d’affichage 3D.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-192">The maximum number of monitors available to the 3-D display controller.</span></span> <span data-ttu-id="fc1a1-193">Le nombre minimal d’analyses est 1 et la valeur maximale dépend de la résolution d’écran maximale.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-193">The minimum number of monitors is 1 and the maximum is dependent upon the maximum screen resolution.</span></span> <span data-ttu-id="fc1a1-194">Le tableau suivant définit le nombre maximal d’analyses autorisées pour différentes résolutions.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-194">The following table defines the maximum number of monitors allowed for different resolutions.</span></span>



| <span data-ttu-id="fc1a1-195">Résolution</span><span class="sxs-lookup"><span data-stu-id="fc1a1-195">Resolution</span></span>            | <span data-ttu-id="fc1a1-196">Nombre maximal d’écrans</span><span class="sxs-lookup"><span data-stu-id="fc1a1-196">Maximum monitors</span></span> |
|-----------------------|------------------|
| <span data-ttu-id="fc1a1-197">1024 768</span><span class="sxs-lookup"><span data-stu-id="fc1a1-197">1024  768</span></span><br/>  | <span data-ttu-id="fc1a1-198">4</span><span class="sxs-lookup"><span data-stu-id="fc1a1-198">4</span></span><br/>     |
| <span data-ttu-id="fc1a1-199">1280 1024</span><span class="sxs-lookup"><span data-stu-id="fc1a1-199">1280  1024</span></span><br/> | <span data-ttu-id="fc1a1-200">4</span><span class="sxs-lookup"><span data-stu-id="fc1a1-200">4</span></span><br/>     |
| <span data-ttu-id="fc1a1-201">1600 1200</span><span class="sxs-lookup"><span data-stu-id="fc1a1-201">1600  1200</span></span><br/> | <span data-ttu-id="fc1a1-202">3</span><span class="sxs-lookup"><span data-stu-id="fc1a1-202">3</span></span><br/>     |
| <span data-ttu-id="fc1a1-203">1920 1200</span><span class="sxs-lookup"><span data-stu-id="fc1a1-203">1920  1200</span></span><br/> | <span data-ttu-id="fc1a1-204">2</span><span class="sxs-lookup"><span data-stu-id="fc1a1-204">2</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="fc1a1-205">**MaximumScreenResolution**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-205">**MaximumScreenResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc1a1-206">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-206">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="fc1a1-207">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc1a1-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc1a1-208">Spécifie la résolution d’écran maximale pour le contrôleur d’affichage 3D.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-208">Specifies the maximum screen resolution for the 3-D display controller.</span></span> <span data-ttu-id="fc1a1-209">Il doit s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-209">This must be one of the following values.</span></span>

<dt>

<span id="1024___768"></span>

<span data-ttu-id="fc1a1-210"><span id="1024___768"></span>**1024 \* 768** (0)</span><span class="sxs-lookup"><span data-stu-id="fc1a1-210"><span id="1024___768"></span>**1024 \* 768** (0)</span></span>


</dt> <dd>

<span data-ttu-id="fc1a1-211">La résolution maximale est de 1024 768.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-211">The maximum resolution is 1024   768.</span></span>

</dd> <dt>

<span id="1280___1024"></span>

<span data-ttu-id="fc1a1-212"><span id="1280___1024"></span>**1280 \* 1024** (1)</span><span class="sxs-lookup"><span data-stu-id="fc1a1-212"><span id="1280___1024"></span>**1280 \* 1024** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fc1a1-213">La résolution maximale est de 1280 1024.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-213">The maximum resolution is 1280   1024.</span></span>

</dd> <dt>

<span id="1600___1200"></span>

<span data-ttu-id="fc1a1-214"><span id="1600___1200"></span>**1600 \* 1200** (2)</span><span class="sxs-lookup"><span data-stu-id="fc1a1-214"><span id="1600___1200"></span>**1600 \* 1200** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fc1a1-215">La résolution maximale est de 1600 1200.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-215">The maximum resolution is 1600   1200.</span></span>

</dd> <dt>

<span id="1920___1200"></span>

<span data-ttu-id="fc1a1-216"><span id="1920___1200"></span>**1920 \* 1200** (3)</span><span class="sxs-lookup"><span data-stu-id="fc1a1-216"><span id="1920___1200"></span>**1920 \* 1200** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fc1a1-217">La résolution maximale est de 1920 1200.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-217">The maximum resolution is 1920   1200.</span></span>

</dd> <dt>

<span id="2560___1600"></span>

<span data-ttu-id="fc1a1-218"><span id="2560___1600"></span>**2560 \* 1600** (4)</span><span class="sxs-lookup"><span data-stu-id="fc1a1-218"><span id="2560___1600"></span>**2560 \* 1600** (4)</span></span>


</dt> <dd>

<span data-ttu-id="fc1a1-219">La résolution maximale est de 2650 1600.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-219">The maximum resolution is 2650   1600.</span></span>

</dd> <dt>

<span id="3840___2160"></span>

<span data-ttu-id="fc1a1-220"><span id="3840___2160"></span>**3840 \* 2160** (5)</span><span class="sxs-lookup"><span data-stu-id="fc1a1-220"><span id="3840___2160"></span>**3840 \* 2160** (5)</span></span>


</dt> <dd>

<span data-ttu-id="fc1a1-221">La résolution maximale est de 3840 2160.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-221">The maximum resolution is 3840   2160.</span></span>

> [!Note]  
> <span data-ttu-id="fc1a1-222">Ajouté dans Windows 10 et Windows Server 2016. MSVM \_ synte</span><span class="sxs-lookup"><span data-stu-id="fc1a1-222">Added in Windows 10 and Windows Server 2016.msvm\_synte</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fc1a1-223">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-223">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc1a1-224">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc1a1-225">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc1a1-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc1a1-226">Chaîne qui décrit le type de ressource lorsqu’une valeur bien définie n’est pas disponible et que [**resourceType**](msvm-processorsettingdata.md) a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="fc1a1-226">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="fc1a1-227">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc1a1-227">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc1a1-228">**Parent**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-228">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc1a1-229">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc1a1-230">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc1a1-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc1a1-231">Parent de la ressource.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-231">The parent of the resource.</span></span> <span data-ttu-id="fc1a1-232">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc1a1-232">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc1a1-233">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-233">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc1a1-234">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc1a1-235">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc1a1-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc1a1-236">Identificateur du pool de ressources à partir duquel cette ressource a été allouée.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-236">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="fc1a1-237">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc1a1-237">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc1a1-238">**Réservation**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-238">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc1a1-239">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-239">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fc1a1-240">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc1a1-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc1a1-241">Quantité de ressources de processeur réservées pour une utilisation par l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-241">The amount of CPU resources that are reserved for use by the virtual machine.</span></span> <span data-ttu-id="fc1a1-242">Ces ressources sont garanties d’être disponibles pour la consommation par l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-242">These resources are guaranteed to be available for consumption by the virtual machine.</span></span> <span data-ttu-id="fc1a1-243">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc1a1-243">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc1a1-244">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-244">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc1a1-245">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc1a1-246">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc1a1-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc1a1-247">Chaîne qui décrit un sous-type spécifique à l’implémentation pour cette ressource.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-247">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="fc1a1-248">Par exemple, cela peut être utilisé pour distinguer différents modèles du même type de ressource.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-248">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="fc1a1-249">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc1a1-249">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc1a1-250">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-250">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc1a1-251">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-251">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc1a1-252">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc1a1-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc1a1-253">Type de ressource représenté par ce paramètre d’allocation.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-253">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="fc1a1-254">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc1a1-254">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc1a1-255">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-255">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc1a1-256">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-256">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fc1a1-257">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc1a1-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc1a1-258">Nombre total de cœurs dans l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-258">The total number of cores in the virtual machine.</span></span> <span data-ttu-id="fc1a1-259">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc1a1-259">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc1a1-260">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-260">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc1a1-261">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc1a1-262">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc1a1-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc1a1-263">Spécifie l’unité de mesure pour la propriété **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="fc1a1-263">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="fc1a1-264">La valeur de cette propriété doit être une valeur légale du qualificateur d’unités de programmation, tel que défini dans l’annexe C. 1 de DSP0004 V 2.5 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-264">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="fc1a1-265">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc1a1-265">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc1a1-266">**VRAMSizeBytes**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-266">**VRAMSizeBytes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc1a1-267">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-267">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fc1a1-268">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fc1a1-268">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fc1a1-269">Taille de la mémoire vidéo de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-269">The video memory size for the Virtual Machine.</span></span>

> [!Note]  
> <span data-ttu-id="fc1a1-270">Ajouté dans Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-270">Added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>



 <span data-ttu-id="fc1a1-271">(67108864)</span><span class="sxs-lookup"><span data-stu-id="fc1a1-271">(67108864)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="fc1a1-272">(134217728)</span><span class="sxs-lookup"><span data-stu-id="fc1a1-272">(134217728)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="fc1a1-273">(268435456)</span><span class="sxs-lookup"><span data-stu-id="fc1a1-273">(268435456)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="fc1a1-274">(536870912)</span><span class="sxs-lookup"><span data-stu-id="fc1a1-274">(536870912)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="fc1a1-275">(1073741824)</span><span class="sxs-lookup"><span data-stu-id="fc1a1-275">(1073741824)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fc1a1-276">**Poids**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-276">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc1a1-277">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-277">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc1a1-278">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc1a1-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc1a1-279">Entier qui définit le poids de chaque processeur d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-279">An integer that defines the weight for each virtual machine processor.</span></span> <span data-ttu-id="fc1a1-280">Une fois toutes les réserves remplies, la capacité du processeur physique restant de la plateforme d’hébergement sera allouée aux ordinateurs virtuels en fonction de leurs pondérations relatives.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-280">After all reserves have been met, the remaining physical processor capacity of the hosting platform will be allocated to virtual machines based on their relative weights.</span></span> <span data-ttu-id="fc1a1-281">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc1a1-281">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="fc1a1-282">0</span><span class="sxs-lookup"><span data-stu-id="fc1a1-282">0</span></span>

<span data-ttu-id="fc1a1-283">Plage : 0 1000</span><span class="sxs-lookup"><span data-stu-id="fc1a1-283">Range: 0 1000</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fc1a1-284">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc1a1-284">Requirements</span></span>



| <span data-ttu-id="fc1a1-285">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc1a1-285">Requirement</span></span> | <span data-ttu-id="fc1a1-286">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc1a1-286">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc1a1-287">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc1a1-287">Minimum supported client</span></span><br/> | <span data-ttu-id="fc1a1-288">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc1a1-288">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fc1a1-289">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc1a1-289">Minimum supported server</span></span><br/> | <span data-ttu-id="fc1a1-290">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc1a1-290">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fc1a1-291">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fc1a1-291">Namespace</span></span><br/>                | <span data-ttu-id="fc1a1-292">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="fc1a1-292">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fc1a1-293">MOF</span><span class="sxs-lookup"><span data-stu-id="fc1a1-293">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc1a1-294"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc1a1-294"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc1a1-295">DLL</span><span class="sxs-lookup"><span data-stu-id="fc1a1-295">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc1a1-296"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fc1a1-296"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

