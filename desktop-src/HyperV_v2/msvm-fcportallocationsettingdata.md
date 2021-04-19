---
description: Représente l’état configuré d’un port de Fibre Channel synthétique ou d’un port de commutateur Fibre Channel.
ms.assetid: 680badc4-8dba-47e8-859a-0ed472a15eda
title: Classe Msvm_FcPortAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcPortAllocationSettingData
- Msvm_FcPortAllocationSettingData.InstanceID
- Msvm_FcPortAllocationSettingData.Caption
- Msvm_FcPortAllocationSettingData.Description
- Msvm_FcPortAllocationSettingData.ElementName
- Msvm_FcPortAllocationSettingData.ResourceType
- Msvm_FcPortAllocationSettingData.OtherResourceType
- Msvm_FcPortAllocationSettingData.ResourceSubType
- Msvm_FcPortAllocationSettingData.PoolID
- Msvm_FcPortAllocationSettingData.ConsumerVisibility
- Msvm_FcPortAllocationSettingData.HostResource
- Msvm_FcPortAllocationSettingData.AllocationUnits
- Msvm_FcPortAllocationSettingData.VirtualQuantity
- Msvm_FcPortAllocationSettingData.Reservation
- Msvm_FcPortAllocationSettingData.Limit
- Msvm_FcPortAllocationSettingData.Weight
- Msvm_FcPortAllocationSettingData.AutomaticAllocation
- Msvm_FcPortAllocationSettingData.AutomaticDeallocation
- Msvm_FcPortAllocationSettingData.Parent
- Msvm_FcPortAllocationSettingData.Connection
- Msvm_FcPortAllocationSettingData.Address
- Msvm_FcPortAllocationSettingData.MappingBehavior
- Msvm_FcPortAllocationSettingData.AddressOnParent
- Msvm_FcPortAllocationSettingData.VirtualQuantityUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 824f7077eeb3cb9e00ce8733cb5d2f57761716e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514049"
---
# <a name="msvm_fcportallocationsettingdata-class"></a><span data-ttu-id="9d852-103">MSVM \_ FcPortAllocationSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="9d852-103">Msvm\_FcPortAllocationSettingData class</span></span>

<span data-ttu-id="9d852-104">Représente l’état configuré d’un port de Fibre Channel synthétique ou d’un port de commutateur Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="9d852-104">Represents the configured state of a synthetic Fibre Channel port or a Fibre Channel switch port.</span></span>

<span data-ttu-id="9d852-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9d852-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d852-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d852-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcPortAllocationSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Virtual Fibre Channel VDev Default Settings";
  string  Description = "The default settings for the virtual Fibre Channel connection pool.";
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
};
```

## <a name="members"></a><span data-ttu-id="9d852-107">Membres</span><span class="sxs-lookup"><span data-stu-id="9d852-107">Members</span></span>

<span data-ttu-id="9d852-108">La classe **MSVM \_ FcPortAllocationSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9d852-108">The **Msvm\_FcPortAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="9d852-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9d852-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9d852-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9d852-110">Properties</span></span>

<span data-ttu-id="9d852-111">La classe **MSVM \_ FcPortAllocationSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="9d852-111">The **Msvm\_FcPortAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9d852-112">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="9d852-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d852-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9d852-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d852-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d852-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d852-115">Adresse de la ressource.</span><span class="sxs-lookup"><span data-stu-id="9d852-115">The address of the resource.</span></span> <span data-ttu-id="9d852-116">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9d852-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9d852-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="9d852-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d852-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9d852-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d852-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d852-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d852-120">Décrit l’adresse de cette ressource dans le contexte du parent.</span><span class="sxs-lookup"><span data-stu-id="9d852-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="9d852-121">Les propriétés **parent** et **AddressOnParent** sont utilisées pour décrire la relation du contrôleur, ainsi que l’ordre des appareils sur un contrôleur.</span><span class="sxs-lookup"><span data-stu-id="9d852-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="9d852-122">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9d852-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9d852-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="9d852-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d852-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9d852-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d852-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d852-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d852-126">Unités d’allocation utilisées par la **réservation** et les propriétés de la **limite** .</span><span class="sxs-lookup"><span data-stu-id="9d852-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="9d852-127">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9d852-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9d852-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="9d852-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d852-129">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="9d852-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9d852-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d852-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d852-131">Indique si la ressource sera automatiquement allouée.</span><span class="sxs-lookup"><span data-stu-id="9d852-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="9d852-132">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9d852-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9d852-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="9d852-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d852-134">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="9d852-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9d852-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d852-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d852-136">Indique si la ressource sera automatiquement désallouée.</span><span class="sxs-lookup"><span data-stu-id="9d852-136">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="9d852-137">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9d852-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9d852-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9d852-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d852-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9d852-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d852-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d852-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d852-141">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="9d852-141">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="9d852-142">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9d852-142">A short description of the object.</span></span> <span data-ttu-id="9d852-143">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9d852-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9d852-144">**Connection**</span><span class="sxs-lookup"><span data-stu-id="9d852-144">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d852-145">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="9d852-145">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9d852-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d852-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d852-147">Appareil auquel cette ressource est connectée.</span><span class="sxs-lookup"><span data-stu-id="9d852-147">The device to which this resource is connected.</span></span> <span data-ttu-id="9d852-148">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9d852-148">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9d852-149">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="9d852-149">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d852-150">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d852-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d852-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d852-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d852-152">Visibilité du consommateur sur la ressource allouée.</span><span class="sxs-lookup"><span data-stu-id="9d852-152">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="9d852-153">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9d852-153">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9d852-154">**Description**</span><span class="sxs-lookup"><span data-stu-id="9d852-154">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d852-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9d852-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d852-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d852-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d852-157">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="9d852-157">A description of the object.</span></span> <span data-ttu-id="9d852-158">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9d852-158">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9d852-159">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9d852-159">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d852-160">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9d852-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d852-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d852-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d852-162">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9d852-162">A display name for the object.</span></span> <span data-ttu-id="9d852-163">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9d852-163">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="9d852-164">La modification de cette propriété modifie le nom d’élément du dérivé de l’appareil logique associé.</span><span class="sxs-lookup"><span data-stu-id="9d852-164">Changing this property will change the element name of the associated logical device derivative.</span></span>

<span data-ttu-id="9d852-165">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="9d852-165">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="9d852-166">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="9d852-166">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d852-167">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="9d852-167">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9d852-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d852-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d852-169">Une seule ressource hôte peut être affectée à chaque périphérique de l’ordinateur virtuel, de sorte que seul le premier élément de ce tableau peut être défini.</span><span class="sxs-lookup"><span data-stu-id="9d852-169">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="9d852-170">Pour les appareils qui prennent en charge cette fonctionnalité, définissez le premier élément du tableau **HostResource** pour qu’il contienne une référence à la ressource hôte sous-jacente à assigner.</span><span class="sxs-lookup"><span data-stu-id="9d852-170">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="9d852-171">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9d852-171">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="9d852-172">Il s’agit d’une propriété en lecture seule, mais si la propriété **resourceType** est 22 (Disk) et que la propriété **ResourceSubType** est « lecteur de disque physique Microsoft », elle peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**\_ VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="9d852-172">This is a read-only property, but if the **ResourceType** property is 22 (Disk) and the **ResourceSubType** property is "Microsoft Physical Disk Drive", then it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="9d852-173">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9d852-173">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d852-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9d852-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d852-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d852-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d852-176">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="9d852-176">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9d852-177">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="9d852-177">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="9d852-178">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9d852-178">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9d852-179">**Limite**</span><span class="sxs-lookup"><span data-stu-id="9d852-179">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d852-180">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9d852-180">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9d852-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d852-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d852-182">Quantité maximale de ressources qui seront accordées pour cette allocation.</span><span class="sxs-lookup"><span data-stu-id="9d852-182">The maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="9d852-183">L’unité de mesure de cette propriété est spécifiée par la propriété **VirtualQuantityUnits** .</span><span class="sxs-lookup"><span data-stu-id="9d852-183">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="9d852-184">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9d852-184">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9d852-185">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="9d852-185">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d852-186">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d852-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d852-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d852-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d852-188">Spécifie comment cette ressource est mappée aux ressources sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="9d852-188">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="9d852-189">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9d852-189">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9d852-190">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="9d852-190">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d852-191">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9d852-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d852-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d852-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d852-193">Chaîne qui décrit le type de ressource lorsqu’une valeur bien définie n’est pas disponible et que [**resourceType**](msvm-processorsettingdata.md) a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="9d852-193">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="9d852-194">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9d852-194">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9d852-195">**Parent**</span><span class="sxs-lookup"><span data-stu-id="9d852-195">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d852-196">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9d852-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d852-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d852-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d852-198">Parent de la ressource.</span><span class="sxs-lookup"><span data-stu-id="9d852-198">The parent of the resource.</span></span> <span data-ttu-id="9d852-199">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9d852-199">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9d852-200">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="9d852-200">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d852-201">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9d852-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d852-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d852-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d852-203">Identificateur du pool de ressources à partir duquel cette ressource a été allouée.</span><span class="sxs-lookup"><span data-stu-id="9d852-203">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="9d852-204">Pour les instances associées à une machine virtuelle, il s’agit de « Microsoft :*GUID* \\ *Device-Specific Data*».</span><span class="sxs-lookup"><span data-stu-id="9d852-204">For instances associated with a virtual machine, this will be "Microsoft:*GUID*\\*device-specific data*".</span></span> <span data-ttu-id="9d852-205">Pour les instances qui définissent les paramètres potentiels d’une machine virtuelle, il s’agit de « Microsoft : définition \\ *GUID* \\ *type*», où *type* peut être « maximum », « minimum », « default » ou « Increment ».</span><span class="sxs-lookup"><span data-stu-id="9d852-205">For instances that define potential settings for a virtual machine, this will be "Microsoft:Definition\\*GUID*\\*Type*", where *Type* can be one of "Maximum", "Minimum", "Default", or "Increment".</span></span> <span data-ttu-id="9d852-206">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9d852-206">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9d852-207">**Réservation**</span><span class="sxs-lookup"><span data-stu-id="9d852-207">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d852-208">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9d852-208">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9d852-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d852-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d852-210">Quantité de ressources dont la disponibilité est garantie pour cette allocation.</span><span class="sxs-lookup"><span data-stu-id="9d852-210">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="9d852-211">L’unité de mesure de cette propriété est spécifiée par la propriété **VirtualQuantityUnits** .</span><span class="sxs-lookup"><span data-stu-id="9d852-211">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="9d852-212">Ces ressources sont garanties d’être disponibles pour la consommation par l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="9d852-212">These resources are guaranteed to be available for consumption by the virtual machine.</span></span> <span data-ttu-id="9d852-213">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9d852-213">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9d852-214">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="9d852-214">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d852-215">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9d852-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d852-216">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d852-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d852-217">Chaîne qui décrit un sous-type spécifique à l’implémentation pour cette ressource.</span><span class="sxs-lookup"><span data-stu-id="9d852-217">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="9d852-218">Par exemple, cela peut être utilisé pour distinguer différents modèles du même type de ressource.</span><span class="sxs-lookup"><span data-stu-id="9d852-218">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="9d852-219">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9d852-219">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9d852-220">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="9d852-220">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d852-221">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d852-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d852-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d852-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d852-223">Type de ressource représenté par ce paramètre d’allocation.</span><span class="sxs-lookup"><span data-stu-id="9d852-223">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="9d852-224">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9d852-224">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="9d852-225"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="9d852-225"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-226"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Système informatique** (2)</span><span class="sxs-lookup"><span data-stu-id="9d852-226"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-227"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processeur** (3)</span><span class="sxs-lookup"><span data-stu-id="9d852-227"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-228"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Mémoire** (4)</span><span class="sxs-lookup"><span data-stu-id="9d852-228"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-229"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Contrôleur IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="9d852-229"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-230"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI parallèle** (6)</span><span class="sxs-lookup"><span data-stu-id="9d852-230"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-231"><span id="FC_HBA"></span><span id="fc_hba"></span>**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="9d852-231"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-232"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="9d852-232"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-233"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="9d852-233"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-234"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Carte Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="9d852-234"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-235"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Autre carte réseau** (11)</span><span class="sxs-lookup"><span data-stu-id="9d852-235"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-236"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Emplacement d’e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="9d852-236"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-237"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Périphérique d’e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="9d852-237"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-238"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Lecteur de disquette** (14)</span><span class="sxs-lookup"><span data-stu-id="9d852-238"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-239"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Lecteur de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="9d852-239"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-240"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Lecteur de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="9d852-240"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-241"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Port série** (17)</span><span class="sxs-lookup"><span data-stu-id="9d852-241"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (17)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-242"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Port parallèle** (18)</span><span class="sxs-lookup"><span data-stu-id="9d852-242"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (18)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-243"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Contrôleur USB** (19)</span><span class="sxs-lookup"><span data-stu-id="9d852-243"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (19)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-244"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Contrôleur Graphics** (20)</span><span class="sxs-lookup"><span data-stu-id="9d852-244"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (20)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-245"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extension de stockage** (21)</span><span class="sxs-lookup"><span data-stu-id="9d852-245"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (21)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-246"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disque** (22)</span><span class="sxs-lookup"><span data-stu-id="9d852-246"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disk** (22)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-247"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Bande** (23)</span><span class="sxs-lookup"><span data-stu-id="9d852-247"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Tape** (23)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-248"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Autre dispositif de stockage** (24)</span><span class="sxs-lookup"><span data-stu-id="9d852-248"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other storage device** (24)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-249"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Contrôleur FireWire** (25)</span><span class="sxs-lookup"><span data-stu-id="9d852-249"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-250"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unité partitionnée** (26)</span><span class="sxs-lookup"><span data-stu-id="9d852-250"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-251"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unité partitionnée de base** (27)</span><span class="sxs-lookup"><span data-stu-id="9d852-251"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-252"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Alimentation (28** )</span><span class="sxs-lookup"><span data-stu-id="9d852-252"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-253"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Appareil de refroidissement** (29)</span><span class="sxs-lookup"><span data-stu-id="9d852-253"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-254"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (30 32767)</span><span class="sxs-lookup"><span data-stu-id="9d852-254"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (30 32767)</span></span>
</dt> <dt>

<span data-ttu-id="9d852-255"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="9d852-255"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9d852-256">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="9d852-256">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d852-257">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9d852-257">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9d852-258">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d852-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d852-259">Spécifie la quantité de ressources présentées au consommateur.</span><span class="sxs-lookup"><span data-stu-id="9d852-259">Specifies the quantity of resources presented to the consumer.</span></span> <span data-ttu-id="9d852-260">L’unité de mesure de cette propriété est spécifiée par la propriété **VirtualQuantityUnits** .</span><span class="sxs-lookup"><span data-stu-id="9d852-260">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="9d852-261">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9d852-261">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9d852-262">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="9d852-262">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d852-263">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9d852-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d852-264">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d852-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d852-265">Spécifie l’unité de mesure pour cette allocation de ressources.</span><span class="sxs-lookup"><span data-stu-id="9d852-265">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="9d852-266">La valeur de cette propriété doit être une valeur légale du qualificateur d’unités de programmation, tel que défini dans l’annexe C. 1 de DSP0004 V 2.5 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="9d852-266">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="9d852-267">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9d852-267">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9d852-268">**Poids**</span><span class="sxs-lookup"><span data-stu-id="9d852-268">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d852-269">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d852-269">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d852-270">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d852-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d852-271">Entier qui définit la pondération relative pour chaque processeur d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="9d852-271">An integer that defines the relative weight for each virtual machine processor.</span></span> <span data-ttu-id="9d852-272">Une fois toutes les réserves remplies, la capacité du processeur physique restant de la plateforme d’hébergement sera allouée aux ordinateurs virtuels en fonction de leurs pondérations relatives.</span><span class="sxs-lookup"><span data-stu-id="9d852-272">After all reserves have been met, the remaining physical processor capacity of the hosting platform will be allocated to virtual machines based on their relative weights.</span></span> <span data-ttu-id="9d852-273">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9d852-273">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="9d852-274">Plage : 0 1000</span><span class="sxs-lookup"><span data-stu-id="9d852-274">Range: 0 1000</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d852-275">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d852-275">Requirements</span></span>



| <span data-ttu-id="9d852-276">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d852-276">Requirement</span></span> | <span data-ttu-id="9d852-277">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d852-277">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d852-278">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d852-278">Minimum supported client</span></span><br/> | <span data-ttu-id="9d852-279">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d852-279">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9d852-280">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d852-280">Minimum supported server</span></span><br/> | <span data-ttu-id="9d852-281">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d852-281">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9d852-282">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9d852-282">Namespace</span></span><br/>                | <span data-ttu-id="9d852-283">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="9d852-283">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9d852-284">MOF</span><span class="sxs-lookup"><span data-stu-id="9d852-284">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d852-285"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d852-285"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d852-286">DLL</span><span class="sxs-lookup"><span data-stu-id="9d852-286">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d852-287"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9d852-287"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

