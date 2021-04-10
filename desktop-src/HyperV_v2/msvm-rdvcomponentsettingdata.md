---
description: Représente l’état configuré du composant de virtualisation des Bureau à distance (RDV). L’État par défaut est activé.
ms.assetid: 058432d7-4439-47ec-9909-82a405d69a6e
title: Classe Msvm_RdvComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RdvComponentSettingData
- Msvm_RdvComponentSettingData.InstanceID
- Msvm_RdvComponentSettingData.Caption
- Msvm_RdvComponentSettingData.Description
- Msvm_RdvComponentSettingData.ElementName
- Msvm_RdvComponentSettingData.ResourceType
- Msvm_RdvComponentSettingData.OtherResourceType
- Msvm_RdvComponentSettingData.ResourceSubType
- Msvm_RdvComponentSettingData.PoolID
- Msvm_RdvComponentSettingData.ConsumerVisibility
- Msvm_RdvComponentSettingData.HostResource
- Msvm_RdvComponentSettingData.AllocationUnits
- Msvm_RdvComponentSettingData.VirtualQuantity
- Msvm_RdvComponentSettingData.Reservation
- Msvm_RdvComponentSettingData.Limit
- Msvm_RdvComponentSettingData.Weight
- Msvm_RdvComponentSettingData.AutomaticAllocation
- Msvm_RdvComponentSettingData.AutomaticDeallocation
- Msvm_RdvComponentSettingData.Parent
- Msvm_RdvComponentSettingData.Connection
- Msvm_RdvComponentSettingData.Address
- Msvm_RdvComponentSettingData.MappingBehavior
- Msvm_RdvComponentSettingData.AddressOnParent
- Msvm_RdvComponentSettingData.VirtualQuantityUnits
- Msvm_RdvComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dfc8decda2bf0c505331c9d681069d55f40687f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865526"
---
# <a name="msvm_rdvcomponentsettingdata-class"></a><span data-ttu-id="9495c-104">MSVM \_ RdvComponentSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="9495c-104">Msvm\_RdvComponentSettingData class</span></span>

<span data-ttu-id="9495c-105">Représente l’état configuré du composant de virtualisation des Bureau à distance (RDV).</span><span class="sxs-lookup"><span data-stu-id="9495c-105">Represents the configured state of the Remote Desktop Virtualization (RDV) component.</span></span> <span data-ttu-id="9495c-106">L’État par défaut est activé.</span><span class="sxs-lookup"><span data-stu-id="9495c-106">The default state is Enabled.</span></span>

<span data-ttu-id="9495c-107">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9495c-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9495c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9495c-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RdvComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Remote Desktop Virtualization Service Default Settings";
  string  Description = "Describes the default settings for the Remote Desktop Virtualization Service resources.";
  string  ElementName;
  uint16  ResourceType = 33;
  string  OtherResourceType;
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
};
```

## <a name="members"></a><span data-ttu-id="9495c-109">Membres</span><span class="sxs-lookup"><span data-stu-id="9495c-109">Members</span></span>

<span data-ttu-id="9495c-110">La classe **MSVM \_ RdvComponentSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9495c-110">The **Msvm\_RdvComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="9495c-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9495c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9495c-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9495c-112">Properties</span></span>

<span data-ttu-id="9495c-113">La classe **MSVM \_ RdvComponentSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="9495c-113">The **Msvm\_RdvComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9495c-114">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="9495c-114">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9495c-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9495c-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9495c-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9495c-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9495c-117">Adresse de la ressource.</span><span class="sxs-lookup"><span data-stu-id="9495c-117">The address of the resource.</span></span> <span data-ttu-id="9495c-118">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9495c-118">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9495c-119">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="9495c-119">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9495c-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9495c-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9495c-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9495c-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9495c-122">Décrit l’adresse de cette ressource dans le contexte du parent.</span><span class="sxs-lookup"><span data-stu-id="9495c-122">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="9495c-123">Les propriétés **parent** et **AddressOnParent** sont utilisées pour décrire la relation du contrôleur, ainsi que l’ordre des appareils sur un contrôleur.</span><span class="sxs-lookup"><span data-stu-id="9495c-123">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="9495c-124">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9495c-124">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9495c-125">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="9495c-125">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9495c-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9495c-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9495c-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9495c-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9495c-128">Unité d’allocation utilisée par les propriétés de **réservation** et de **limite** .</span><span class="sxs-lookup"><span data-stu-id="9495c-128">The unit of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="9495c-129">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9495c-129">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9495c-130">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="9495c-130">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9495c-131">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="9495c-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9495c-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9495c-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9495c-133">Indique si la ressource sera automatiquement allouée.</span><span class="sxs-lookup"><span data-stu-id="9495c-133">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="9495c-134">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9495c-134">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9495c-135">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="9495c-135">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9495c-136">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="9495c-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9495c-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9495c-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9495c-138">Indique si la ressource sera automatiquement désallouée.</span><span class="sxs-lookup"><span data-stu-id="9495c-138">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="9495c-139">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9495c-139">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9495c-140">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9495c-140">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9495c-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9495c-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9495c-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9495c-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9495c-143">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="9495c-143">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="9495c-144">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9495c-144">A short description of the object.</span></span> <span data-ttu-id="9495c-145">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « paramètres de port de commutateur Ethernet ».</span><span class="sxs-lookup"><span data-stu-id="9495c-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Settings".</span></span>

</dd> <dt>

<span data-ttu-id="9495c-146">**Connection**</span><span class="sxs-lookup"><span data-stu-id="9495c-146">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9495c-147">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="9495c-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9495c-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9495c-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9495c-149">Appareil auquel cette ressource est connectée.</span><span class="sxs-lookup"><span data-stu-id="9495c-149">The device to which this resource is connected.</span></span> <span data-ttu-id="9495c-150">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9495c-150">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9495c-151">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="9495c-151">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9495c-152">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9495c-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9495c-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9495c-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9495c-154">Visibilité du consommateur sur la ressource allouée.</span><span class="sxs-lookup"><span data-stu-id="9495c-154">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="9495c-155">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)et est toujours définie sur 3 (virtualisé).</span><span class="sxs-lookup"><span data-stu-id="9495c-155">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="9495c-156">**Description**</span><span class="sxs-lookup"><span data-stu-id="9495c-156">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9495c-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9495c-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9495c-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9495c-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9495c-159">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="9495c-159">A description of the object.</span></span> <span data-ttu-id="9495c-160">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « paramètres de port de commutateur Ethernet ».</span><span class="sxs-lookup"><span data-stu-id="9495c-160">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Settings".</span></span>

</dd> <dt>

<span data-ttu-id="9495c-161">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9495c-161">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9495c-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9495c-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9495c-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9495c-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9495c-164">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9495c-164">A display name for the object.</span></span> <span data-ttu-id="9495c-165">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9495c-165">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="9495c-166">La modification de cette propriété modifie le nom d’élément du dérivé de l’appareil logique associé.</span><span class="sxs-lookup"><span data-stu-id="9495c-166">Changing this property will change the element name of the associated logical device derivative.</span></span>

</dd> <dt>

<span data-ttu-id="9495c-167">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="9495c-167">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9495c-168">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9495c-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9495c-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9495c-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9495c-170">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="9495c-170">The enabled and disabled states of an element.</span></span> <span data-ttu-id="9495c-171">Les valeurs valides sont 2 (activé) et 3 (désactivé).</span><span class="sxs-lookup"><span data-stu-id="9495c-171">Valid values are 2 (enabled) and 3 (disabled).</span></span> <span data-ttu-id="9495c-172">La valeur par défaut est 2 (activé).</span><span class="sxs-lookup"><span data-stu-id="9495c-172">The default value is 2 (enabled).</span></span> <span data-ttu-id="9495c-173">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="9495c-173">This is a read-only property, but it can be changed by using the [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="9495c-174">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="9495c-174">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9495c-175">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="9495c-175">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9495c-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9495c-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9495c-177">Une seule ressource hôte peut être assignée à chaque périphérique dans le commutateur virtuel, de sorte que seul le premier élément de ce tableau peut être défini.</span><span class="sxs-lookup"><span data-stu-id="9495c-177">Only one host resource can be assigned to each device in the virtual switch, so only the first element of this array can be set.</span></span> <span data-ttu-id="9495c-178">Pour les appareils qui prennent en charge cette fonctionnalité, définissez le premier élément du tableau **HostResource** pour qu’il contienne une référence à la ressource hôte sous-jacente à assigner.</span><span class="sxs-lookup"><span data-stu-id="9495c-178">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="9495c-179">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9495c-179">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9495c-180">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9495c-180">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9495c-181">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9495c-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9495c-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9495c-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9495c-183">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="9495c-183">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9495c-184">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="9495c-184">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="9495c-185">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9495c-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9495c-186">**Limite**</span><span class="sxs-lookup"><span data-stu-id="9495c-186">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9495c-187">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9495c-187">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9495c-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9495c-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9495c-189">Quantité maximale de ressources hôtes correspondantes qui peuvent être consommées par le commutateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="9495c-189">The maximum amount of corresponding host resources that can be consumed by the virtual switch.</span></span> <span data-ttu-id="9495c-190">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9495c-190">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9495c-191">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="9495c-191">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9495c-192">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9495c-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9495c-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9495c-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9495c-194">Spécifie comment cette ressource est mappée aux ressources sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="9495c-194">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="9495c-195">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9495c-195">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9495c-196">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="9495c-196">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9495c-197">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9495c-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9495c-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9495c-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9495c-199">Chaîne qui décrit le type de ressource lorsqu’une valeur bien définie n’est pas disponible et que [**resourceType**](msvm-processorsettingdata.md) a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="9495c-199">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1 (Other).</span></span> <span data-ttu-id="9495c-200">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="9495c-200">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9495c-201">**Parent**</span><span class="sxs-lookup"><span data-stu-id="9495c-201">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9495c-202">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9495c-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9495c-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9495c-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9495c-204">Parent de la ressource.</span><span class="sxs-lookup"><span data-stu-id="9495c-204">The parent of the resource.</span></span> <span data-ttu-id="9495c-205">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9495c-205">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9495c-206">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="9495c-206">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9495c-207">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9495c-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9495c-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9495c-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9495c-209">Identificateur du pool de ressources à partir duquel cette ressource a été allouée.</span><span class="sxs-lookup"><span data-stu-id="9495c-209">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="9495c-210">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9495c-210">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9495c-211">**Réservation**</span><span class="sxs-lookup"><span data-stu-id="9495c-211">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9495c-212">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9495c-212">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9495c-213">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9495c-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9495c-214">Quantité de ressources réservées pour une utilisation par le commutateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="9495c-214">The amount of resources that are reserved for use by the virtual switch.</span></span> <span data-ttu-id="9495c-215">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9495c-215">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9495c-216">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="9495c-216">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9495c-217">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9495c-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9495c-218">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9495c-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9495c-219">Chaîne qui décrit un sous-type spécifique à l’implémentation pour cette ressource.</span><span class="sxs-lookup"><span data-stu-id="9495c-219">A string that describes an implementation-specific subtype for this resource.</span></span> <span data-ttu-id="9495c-220">Par exemple, cela peut être utilisé pour distinguer différents modèles du même type de ressource.</span><span class="sxs-lookup"><span data-stu-id="9495c-220">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="9495c-221">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9495c-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9495c-222">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="9495c-222">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9495c-223">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9495c-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9495c-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9495c-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9495c-225">Type de ressource représenté par ce paramètre d’allocation.</span><span class="sxs-lookup"><span data-stu-id="9495c-225">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="9495c-226">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)et est toujours définie sur 33 (connexion Ethernet).</span><span class="sxs-lookup"><span data-stu-id="9495c-226">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 33 (Ethernet connection).</span></span>

</dd> <dt>

<span data-ttu-id="9495c-227">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="9495c-227">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9495c-228">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9495c-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9495c-229">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9495c-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9495c-230">Nombre total de ports dans le commutateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="9495c-230">The total number of ports in the virtual switch.</span></span> <span data-ttu-id="9495c-231">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9495c-231">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9495c-232">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="9495c-232">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9495c-233">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9495c-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9495c-234">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9495c-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9495c-235">Spécifie l’unité de mesure pour la propriété **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="9495c-235">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="9495c-236">La valeur de cette propriété doit être une valeur légale du qualificateur d’unités de programmation, tel que défini dans l’annexe C. 1 de DSP0004 V 2.5 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="9495c-236">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="9495c-237">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9495c-237">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9495c-238">**Poids**</span><span class="sxs-lookup"><span data-stu-id="9495c-238">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9495c-239">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9495c-239">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9495c-240">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9495c-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9495c-241">Entier qui définit le poids de chaque commutateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="9495c-241">An integer that defines the weight for each virtual switch.</span></span> <span data-ttu-id="9495c-242">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9495c-242">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="9495c-243">Plage : 0 1000</span><span class="sxs-lookup"><span data-stu-id="9495c-243">Range: 0 1000</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9495c-244">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9495c-244">Requirements</span></span>



| <span data-ttu-id="9495c-245">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9495c-245">Requirement</span></span> | <span data-ttu-id="9495c-246">Valeur</span><span class="sxs-lookup"><span data-stu-id="9495c-246">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9495c-247">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9495c-247">Minimum supported client</span></span><br/> | <span data-ttu-id="9495c-248">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9495c-248">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9495c-249">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9495c-249">Minimum supported server</span></span><br/> | <span data-ttu-id="9495c-250">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9495c-250">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9495c-251">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9495c-251">Namespace</span></span><br/>                | <span data-ttu-id="9495c-252">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="9495c-252">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9495c-253">MOF</span><span class="sxs-lookup"><span data-stu-id="9495c-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9495c-254"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9495c-254"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9495c-255">DLL</span><span class="sxs-lookup"><span data-stu-id="9495c-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9495c-256"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9495c-256"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

