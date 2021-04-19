---
description: Représente l’état configuré du service de pulsation.
ms.assetid: 2946FA02-A751-4576-BB8A-004C80E21E5B
title: Classe Msvm_HeartbeatComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HeartbeatComponentSettingData
- Msvm_HeartbeatComponentSettingData.InstanceID
- Msvm_HeartbeatComponentSettingData.Caption
- Msvm_HeartbeatComponentSettingData.Description
- Msvm_HeartbeatComponentSettingData.ElementName
- Msvm_HeartbeatComponentSettingData.ResourceType
- Msvm_HeartbeatComponentSettingData.OtherResourceType
- Msvm_HeartbeatComponentSettingData.ResourceSubType
- Msvm_HeartbeatComponentSettingData.PoolID
- Msvm_HeartbeatComponentSettingData.ConsumerVisibility
- Msvm_HeartbeatComponentSettingData.HostResource
- Msvm_HeartbeatComponentSettingData.AllocationUnits
- Msvm_HeartbeatComponentSettingData.VirtualQuantity
- Msvm_HeartbeatComponentSettingData.Reservation
- Msvm_HeartbeatComponentSettingData.Limit
- Msvm_HeartbeatComponentSettingData.Weight
- Msvm_HeartbeatComponentSettingData.AutomaticAllocation
- Msvm_HeartbeatComponentSettingData.AutomaticDeallocation
- Msvm_HeartbeatComponentSettingData.Parent
- Msvm_HeartbeatComponentSettingData.Connection
- Msvm_HeartbeatComponentSettingData.Address
- Msvm_HeartbeatComponentSettingData.MappingBehavior
- Msvm_HeartbeatComponentSettingData.AddressOnParent
- Msvm_HeartbeatComponentSettingData.VirtualQuantityUnits
- Msvm_HeartbeatComponentSettingData.EnabledState
- Msvm_HeartbeatComponentSettingData.ErrorThreshold
- Msvm_HeartbeatComponentSettingData.Interval
- Msvm_HeartbeatComponentSettingData.Latency
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a36afbd8ab17a3fc2dfddb99b0a648fddbada415
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521402"
---
# <a name="msvm_heartbeatcomponentsettingdata-class"></a><span data-ttu-id="4cbb0-103">MSVM \_ HeartbeatComponentSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="4cbb0-103">Msvm\_HeartbeatComponentSettingData class</span></span>

<span data-ttu-id="4cbb0-104">Représente l’état configuré du service de pulsation.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-104">Represents the configured state of the heartbeat service.</span></span>

<span data-ttu-id="4cbb0-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cbb0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4cbb0-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HeartbeatComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string  Caption = "Heartbeat";
  string  Description = "Microsoft Heartbeat Service Setting Data";
  string  ElementName = "Heartbeat";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft Heartbeat Component";
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "Integration Components";
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
  uint32  ErrorThreshold = 2;
  uint32  Interval = 2000;
  uint32  Latency = 1000;
};
```

## <a name="members"></a><span data-ttu-id="4cbb0-107">Membres</span><span class="sxs-lookup"><span data-stu-id="4cbb0-107">Members</span></span>

<span data-ttu-id="4cbb0-108">La classe **MSVM \_ HeartbeatComponentSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4cbb0-108">The **Msvm\_HeartbeatComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="4cbb0-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4cbb0-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4cbb0-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4cbb0-110">Properties</span></span>

<span data-ttu-id="4cbb0-111">La classe **MSVM \_ HeartbeatComponentSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-111">The **Msvm\_HeartbeatComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4cbb0-112">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cbb0-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4cbb0-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4cbb0-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cbb0-115">Adresse de la ressource.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-115">The address of the resource.</span></span> <span data-ttu-id="4cbb0-116">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) et a toujours la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4cbb0-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cbb0-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4cbb0-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4cbb0-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cbb0-120">Décrit l’adresse de cette ressource dans le contexte du parent.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="4cbb0-121">Les propriétés AddressOnParent **parentes** /  sont utilisées pour décrire la relation entre le contrôleur et le classement des appareils sur un contrôleur.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-121">The **Parent**/**AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="4cbb0-122">Par exemple, si le parent est un contrôleur PCI, cette propriété spécifie l’emplacement PCI de cet appareil enfant.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-122">For example, if the parent is a PCI Controller, this property would specify the PCI slot of this child device.</span></span> <span data-ttu-id="4cbb0-123">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) et a toujours la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4cbb0-124">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cbb0-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4cbb0-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4cbb0-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cbb0-127">Unités d’allocation utilisées par la **réservation** et les propriétés de la **limite** .</span><span class="sxs-lookup"><span data-stu-id="4cbb0-127">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="4cbb0-128">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) et est toujours définie sur « composants d’intégration ».</span><span class="sxs-lookup"><span data-stu-id="4cbb0-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to "Integration Components".</span></span>

</dd> <dt>

<span data-ttu-id="4cbb0-129">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-129">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cbb0-130">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4cbb0-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4cbb0-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cbb0-132">Indique si la ressource est automatiquement allouée.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-132">Indicates whether the resource is automatically allocated.</span></span> <span data-ttu-id="4cbb0-133">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) et a toujours la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-133">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="4cbb0-134">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-134">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cbb0-135">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4cbb0-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4cbb0-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cbb0-137">Indique si la ressource est automatiquement désallouée.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-137">Indicates whether the resource is automatically de-allocated.</span></span> <span data-ttu-id="4cbb0-138">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) et a toujours la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-138">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="4cbb0-139">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cbb0-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4cbb0-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4cbb0-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cbb0-142">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-142">A short description of the object.</span></span> <span data-ttu-id="4cbb0-143">Cette propriété est héritée de la classe [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) et est toujours définie sur « pulsation ».</span><span class="sxs-lookup"><span data-stu-id="4cbb0-143">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class and is always set to "Heartbeat".</span></span>

</dd> <dt>

<span data-ttu-id="4cbb0-144">**Connection**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-144">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cbb0-145">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-145">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4cbb0-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4cbb0-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cbb0-147">Élément auquel cette ressource est connectée.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-147">The thing to which this resource is connected.</span></span> <span data-ttu-id="4cbb0-148">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) et a toujours la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-148">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4cbb0-149">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-149">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cbb0-150">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4cbb0-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4cbb0-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cbb0-152">Décrit la visibilité des consommateurs sur la ressource allouée.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-152">Describes the consumers' visibility to the allocated resource.</span></span> <span data-ttu-id="4cbb0-153">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) et a toujours la valeur 3 (virtualisé).</span><span class="sxs-lookup"><span data-stu-id="4cbb0-153">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="4cbb0-154">**Description**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-154">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cbb0-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4cbb0-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4cbb0-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cbb0-157">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="4cbb0-157">A description of the object.</span></span> <span data-ttu-id="4cbb0-158">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « données de paramètres du service de pulsation Microsoft ».</span><span class="sxs-lookup"><span data-stu-id="4cbb0-158">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Heartbeat Service Setting Data".</span></span>

</dd> <dt>

<span data-ttu-id="4cbb0-159">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-159">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cbb0-160">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4cbb0-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4cbb0-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cbb0-162">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-162">A display name for the object.</span></span> <span data-ttu-id="4cbb0-163">Cette propriété est héritée de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))et est toujours définie sur « pulsation ».</span><span class="sxs-lookup"><span data-stu-id="4cbb0-163">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Heartbeat".</span></span> <span data-ttu-id="4cbb0-164">La modification de cette propriété entraînera la modification de la propriété **ElementName** de la dérivée [**CIM CIM \_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) associée.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-164">Changing this property will change the **ElementName** property of the associated [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) derivative.</span></span>

<span data-ttu-id="4cbb0-165">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="4cbb0-165">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="4cbb0-166">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-166">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cbb0-167">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4cbb0-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4cbb0-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cbb0-169">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-169">The enabled and disabled states of an element.</span></span>

<span data-ttu-id="4cbb0-170">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="4cbb0-170">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4cbb0-171">**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="4cbb0-171">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4cbb0-172">**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="4cbb0-172">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4cbb0-173">**ErrorThreshold**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-173">**ErrorThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cbb0-174">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4cbb0-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4cbb0-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cbb0-176">Configuration de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-176">An administrator's startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="4cbb0-177">Cette propriété a toujours la valeur 2 (activé).</span><span class="sxs-lookup"><span data-stu-id="4cbb0-177">This property is always set to 2 (Enabled).</span></span>

<span data-ttu-id="4cbb0-178">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="4cbb0-178">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="4cbb0-179">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-179">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cbb0-180">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-180">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4cbb0-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4cbb0-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cbb0-182">Expose une attribution spécifique à l’hôte ou aux ressources sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-182">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="4cbb0-183">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) et a toujours la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-183">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4cbb0-184">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-184">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cbb0-185">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4cbb0-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4cbb0-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4cbb0-187">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-187">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4cbb0-188">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-188">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="4cbb0-189">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)) et est toujours définie sur « Microsoft :*GUID* \\ *DeviceSpecificData*».</span><span class="sxs-lookup"><span data-stu-id="4cbb0-189">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) and is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> <dt>

<span data-ttu-id="4cbb0-190">**Intervalle**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-190">**Interval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cbb0-191">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-191">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4cbb0-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4cbb0-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cbb0-193">Intervalle, en millisecondes, entre les tentatives de test ping.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-193">The interval, in milliseconds, between ping attempts.</span></span> <span data-ttu-id="4cbb0-194">La valeur est toujours 2000.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-194">This is always set to 2000.</span></span>

<span data-ttu-id="4cbb0-195">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="4cbb0-195">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="4cbb0-196">**Latence**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-196">**Latency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cbb0-197">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4cbb0-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4cbb0-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cbb0-199">Latence maximale attendue, en millisecondes, entre une demande ping et une réponse avant qu’une demande donnée soit considérée comme supprimée.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-199">The maximum expected latency, in milliseconds, between a request ping and a response before a given request is considered dropped.</span></span> <span data-ttu-id="4cbb0-200">Cette propriété a toujours la valeur 1000.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-200">This property is always set to 1000.</span></span>

<span data-ttu-id="4cbb0-201">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="4cbb0-201">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="4cbb0-202">**Limite**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-202">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cbb0-203">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4cbb0-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4cbb0-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cbb0-205">Limite supérieure ou quantité maximale de ressources qui seront accordées pour cette allocation.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-205">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="4cbb0-206">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) et a toujours la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-206">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="4cbb0-207">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-207">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cbb0-208">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4cbb0-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4cbb0-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cbb0-210">Spécifie comment cette ressource est mappée aux ressources sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-210">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="4cbb0-211">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) et a toujours la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-211">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4cbb0-212">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-212">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cbb0-213">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4cbb0-214">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4cbb0-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cbb0-215">Chaîne qui décrit le type de ressource lorsqu’une valeur bien définie n’est pas disponible et que la propriété **resourceType** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="4cbb0-215">A string that describes the resource type when a well-defined value is not available and the **ResourceType** property has the value 1 (Other).</span></span> <span data-ttu-id="4cbb0-216">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) et est toujours définie sur « composant de pulsation Microsoft ».</span><span class="sxs-lookup"><span data-stu-id="4cbb0-216">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to "Microsoft Heartbeat Component".</span></span>

</dd> <dt>

<span data-ttu-id="4cbb0-217">**Parent**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-217">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cbb0-218">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4cbb0-219">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4cbb0-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cbb0-220">Parent de la ressource.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-220">The parent of the resource.</span></span> <span data-ttu-id="4cbb0-221">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) et a toujours la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4cbb0-222">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-222">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cbb0-223">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4cbb0-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4cbb0-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cbb0-225">ID du pool de ressources à partir duquel la ressource est allouée.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-225">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="4cbb0-226">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="4cbb0-226">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="4cbb0-227">**Réservation**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-227">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cbb0-228">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4cbb0-229">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4cbb0-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cbb0-230">Quantité de ressources dont la disponibilité est garantie pour cette allocation.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-230">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="4cbb0-231">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) et a toujours la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-231">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="4cbb0-232">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-232">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cbb0-233">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4cbb0-234">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4cbb0-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cbb0-235">Sous-type spécifique à l’implémentation pour cette ressource.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-235">An implementation specific subtype for this resource.</span></span> <span data-ttu-id="4cbb0-236">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) et a toujours la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-236">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4cbb0-237">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-237">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cbb0-238">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4cbb0-239">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4cbb0-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cbb0-240">Type de ressource représenté par ce paramètre d’allocation.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-240">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="4cbb0-241">Cette propriété est héritée de la classe [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) et est toujours définie sur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="4cbb0-241">This property is inherited from the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class and is always set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="4cbb0-242">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-242">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cbb0-243">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-243">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4cbb0-244">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4cbb0-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cbb0-245">Quantité de ressources présentées au consommateur.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-245">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="4cbb0-246">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) et a toujours la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-246">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="4cbb0-247">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-247">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cbb0-248">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4cbb0-249">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4cbb0-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cbb0-250">Spécifie les unités utilisées par la propriété **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="4cbb0-250">Specifies the units used by the **VirtualQuantity** property.</span></span> <span data-ttu-id="4cbb0-251">Par exemple, si ResourceType = Processor, la valeur de la propriété **VirtualQuantityUnits** peut être définie sur « Count », ce qui indique que la valeur de la propriété **VirtualQuantity** est exprimée sous la forme d’un nombre.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-251">For example, if ResourceType=Processor, the value of the **VirtualQuantityUnits** property can be set to "count", indicating that the value of the **VirtualQuantity** property is expressed as a count.</span></span> <span data-ttu-id="4cbb0-252">Si ResourceType = Memory, la valeur de la propriété **VirtualQuantityUnits** peut être définie sur « bytes \* 10 ^ 3 », ce qui indique que la valeur de la propriété **VirtualQuantity** est exprimée en kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-252">If ResourceType=Memory, the value of the **VirtualQuantityUnits** property can be set to "bytes\*10^3", indicating that the value of the **VirtualQuantity** property is expressed in kilobytes.</span></span> <span data-ttu-id="4cbb0-253">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) et a toujours la valeur « Count ».</span><span class="sxs-lookup"><span data-stu-id="4cbb0-253">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to "count".</span></span>

</dd> <dt>

<span data-ttu-id="4cbb0-254">**Poids**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-254">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cbb0-255">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-255">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4cbb0-256">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4cbb0-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cbb0-257">Priorité relative pour cette allocation par rapport à d’autres allocations à partir du même pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-257">The relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="4cbb0-258">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) et est toujours définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-258">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4cbb0-259">Notes</span><span class="sxs-lookup"><span data-stu-id="4cbb0-259">Remarks</span></span>

<span data-ttu-id="4cbb0-260">L’accès à la classe **MSVM \_ HeartbeatComponentSettingData** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-260">Access to the **Msvm\_HeartbeatComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4cbb0-261">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="4cbb0-261">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="4cbb0-262">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4cbb0-262">Requirements</span></span>



| <span data-ttu-id="4cbb0-263">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4cbb0-263">Requirement</span></span> | <span data-ttu-id="4cbb0-264">Valeur</span><span class="sxs-lookup"><span data-stu-id="4cbb0-264">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cbb0-265">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4cbb0-265">Minimum supported client</span></span><br/> | <span data-ttu-id="4cbb0-266">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4cbb0-266">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4cbb0-267">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4cbb0-267">Minimum supported server</span></span><br/> | <span data-ttu-id="4cbb0-268">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4cbb0-268">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4cbb0-269">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4cbb0-269">Namespace</span></span><br/>                | <span data-ttu-id="4cbb0-270">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="4cbb0-270">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4cbb0-271">MOF</span><span class="sxs-lookup"><span data-stu-id="4cbb0-271">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4cbb0-272"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4cbb0-272"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4cbb0-273">DLL</span><span class="sxs-lookup"><span data-stu-id="4cbb0-273">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cbb0-274"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4cbb0-274"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4cbb0-275">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4cbb0-275">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cbb0-276">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-276">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="4cbb0-277">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-277">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="4cbb0-278">**MSVM \_ HeartbeatComponentSettingData**</span><span class="sxs-lookup"><span data-stu-id="4cbb0-278">**Msvm\_HeartbeatComponentSettingData**</span></span>](/previous-versions/windows/desktop/virtual/msvm-heartbeatcomponentsettingdata)
</dt> </dl>

 

