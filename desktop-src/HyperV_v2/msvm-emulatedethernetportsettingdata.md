---
description: Représente l’état configuré d’un adaptateur Ethernet émulé.
ms.assetid: 8BFD69D8-65B6-4C6F-9972-BD2F3C4FB5B8
title: Classe Msvm_EmulatedEthernetPortSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EmulatedEthernetPortSettingData
- Msvm_EmulatedEthernetPortSettingData.Caption
- Msvm_EmulatedEthernetPortSettingData.Description
- Msvm_EmulatedEthernetPortSettingData.InstanceID
- Msvm_EmulatedEthernetPortSettingData.ElementName
- Msvm_EmulatedEthernetPortSettingData.ResourceType
- Msvm_EmulatedEthernetPortSettingData.OtherResourceType
- Msvm_EmulatedEthernetPortSettingData.ResourceSubType
- Msvm_EmulatedEthernetPortSettingData.PoolID
- Msvm_EmulatedEthernetPortSettingData.ConsumerVisibility
- Msvm_EmulatedEthernetPortSettingData.HostResource
- Msvm_EmulatedEthernetPortSettingData.AllocationUnits
- Msvm_EmulatedEthernetPortSettingData.VirtualQuantity
- Msvm_EmulatedEthernetPortSettingData.Reservation
- Msvm_EmulatedEthernetPortSettingData.Limit
- Msvm_EmulatedEthernetPortSettingData.Weight
- Msvm_EmulatedEthernetPortSettingData.AutomaticAllocation
- Msvm_EmulatedEthernetPortSettingData.AutomaticDeallocation
- Msvm_EmulatedEthernetPortSettingData.Parent
- Msvm_EmulatedEthernetPortSettingData.Connection
- Msvm_EmulatedEthernetPortSettingData.Address
- Msvm_EmulatedEthernetPortSettingData.MappingBehavior
- Msvm_EmulatedEthernetPortSettingData.AddressOnParent
- Msvm_EmulatedEthernetPortSettingData.VirtualQuantityUnits
- Msvm_EmulatedEthernetPortSettingData.DesiredVLANEndpointMode
- Msvm_EmulatedEthernetPortSettingData.OtherEndpointMode
- Msvm_EmulatedEthernetPortSettingData.StaticMacAddress
- Msvm_EmulatedEthernetPortSettingData.ClusterMonitored
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f80a1f14f7a5bd388aec747f19ef84ecf0a32b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863878"
---
# <a name="msvm_emulatedethernetportsettingdata-class"></a><span data-ttu-id="15534-103">MSVM \_ EmulatedEthernetPortSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="15534-103">Msvm\_EmulatedEthernetPortSettingData class</span></span>

<span data-ttu-id="15534-104">Représente l’état configuré d’un adaptateur Ethernet émulé.</span><span class="sxs-lookup"><span data-stu-id="15534-104">Represents the configured state of an emulated Ethernet adapter.</span></span>

<span data-ttu-id="15534-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="15534-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="15534-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15534-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EmulatedEthernetPortSettingData : CIM_EthernetPortAllocationSettingData
{
  string  Caption = "Ethernet Port";
  string  Description = "Settings for the Microsoft Emulated Ethernet Port";
  string  InstanceID = "Microsoft:VMID\VDID\device-specific-data";
  string  ElementName = "Ethernet Port";
  uint16  ResourceType = 10;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft Emulated Ethernet Port";
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "Ports";
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
  uint16  DesiredVLANEndpointMode;
  string  OtherEndpointMode;
  boolean StaticMacAddress = TRUE;
  boolean ClusterMonitored = TRUE;
};
```

## <a name="members"></a><span data-ttu-id="15534-107">Membres</span><span class="sxs-lookup"><span data-stu-id="15534-107">Members</span></span>

<span data-ttu-id="15534-108">La classe **MSVM \_ EmulatedEthernetPortSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="15534-108">The **Msvm\_EmulatedEthernetPortSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="15534-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="15534-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="15534-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="15534-110">Properties</span></span>

<span data-ttu-id="15534-111">La classe **MSVM \_ EmulatedEthernetPortSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="15534-111">The **Msvm\_EmulatedEthernetPortSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="15534-112">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="15534-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15534-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="15534-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15534-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15534-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15534-115">Adresse de la ressource.</span><span class="sxs-lookup"><span data-stu-id="15534-115">The address of the resource.</span></span> <span data-ttu-id="15534-116">Par exemple, l’adresse MAC d’un port Ethernet.</span><span class="sxs-lookup"><span data-stu-id="15534-116">For example, the MAC address of a Ethernet port.</span></span> <span data-ttu-id="15534-117">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="15534-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="15534-118">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="15534-118">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="15534-119">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="15534-119">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15534-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="15534-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15534-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15534-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15534-122">Décrit l’adresse de cette ressource dans le contexte du parent.</span><span class="sxs-lookup"><span data-stu-id="15534-122">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="15534-123">Les propriétés **parent** et **AddressOnParent** sont utilisées pour décrire la relation du contrôleur, ainsi que l’ordre des appareils sur un contrôleur.</span><span class="sxs-lookup"><span data-stu-id="15534-123">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="15534-124">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="15534-124">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="15534-125">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="15534-125">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15534-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="15534-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15534-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15534-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15534-128">Unités d’allocation utilisées par la **réservation** et les propriétés de la **limite** .</span><span class="sxs-lookup"><span data-stu-id="15534-128">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="15534-129">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)et est toujours définie sur « ports ».</span><span class="sxs-lookup"><span data-stu-id="15534-129">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to "Ports".</span></span>

</dd> <dt>

<span data-ttu-id="15534-130">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="15534-130">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15534-131">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="15534-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="15534-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15534-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15534-133">Indique si la ressource sera automatiquement allouée.</span><span class="sxs-lookup"><span data-stu-id="15534-133">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="15534-134">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)et est toujours définie sur **true**.</span><span class="sxs-lookup"><span data-stu-id="15534-134">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="15534-135">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="15534-135">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15534-136">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="15534-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="15534-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15534-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15534-138">Indique si la ressource sera automatiquement désallouée.</span><span class="sxs-lookup"><span data-stu-id="15534-138">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="15534-139">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)et est toujours définie sur **true**.</span><span class="sxs-lookup"><span data-stu-id="15534-139">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="15534-140">**Caption**</span><span class="sxs-lookup"><span data-stu-id="15534-140">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15534-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="15534-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15534-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15534-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15534-143">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="15534-143">A short description of the object.</span></span> <span data-ttu-id="15534-144">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « port Ethernet ».</span><span class="sxs-lookup"><span data-stu-id="15534-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="15534-145">**ClusterMonitored**</span><span class="sxs-lookup"><span data-stu-id="15534-145">**ClusterMonitored**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15534-146">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="15534-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="15534-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15534-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15534-148">Indique si cette carte Ethernet est surveillée par un cluster.</span><span class="sxs-lookup"><span data-stu-id="15534-148">Indicates whether this ethernet adapter is monitored by a cluster.</span></span> <span data-ttu-id="15534-149">La valeur par défaut de cette propriété est true si elle n’est pas configurée.</span><span class="sxs-lookup"><span data-stu-id="15534-149">This property defaults to true if not configured.</span></span>

<span data-ttu-id="15534-150">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="15534-150">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="15534-151">**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="15534-151">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="15534-152">**Connection**</span><span class="sxs-lookup"><span data-stu-id="15534-152">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15534-153">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="15534-153">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="15534-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15534-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15534-155">Élément auquel cette ressource est connectée.</span><span class="sxs-lookup"><span data-stu-id="15534-155">The thing to which this resource is connected.</span></span> <span data-ttu-id="15534-156">Par exemple, un réseau nommé ou un port commuté.</span><span class="sxs-lookup"><span data-stu-id="15534-156">For example, a named network or switch port.</span></span> <span data-ttu-id="15534-157">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="15534-157">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="15534-158">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="15534-158">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="15534-159">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="15534-159">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15534-160">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="15534-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15534-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15534-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15534-162">Décrit la visibilité des consommateurs sur la ressource allouée.</span><span class="sxs-lookup"><span data-stu-id="15534-162">Describes the consumers visibility to the allocated resource.</span></span> <span data-ttu-id="15534-163">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)et est toujours définie sur 3 (virtualisé).</span><span class="sxs-lookup"><span data-stu-id="15534-163">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="15534-164">**Description**</span><span class="sxs-lookup"><span data-stu-id="15534-164">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15534-165">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="15534-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15534-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15534-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15534-167">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="15534-167">A description of the object.</span></span> <span data-ttu-id="15534-168">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « paramètres du port Ethernet émulé Microsoft ».</span><span class="sxs-lookup"><span data-stu-id="15534-168">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Settings for the Microsoft Emulated Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="15534-169">**DesiredVLANEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="15534-169">**DesiredVLANEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15534-170">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="15534-170">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15534-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15534-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15534-172">Mode de configuration souhaité pour le point de terminaison de réseau local virtuel.</span><span class="sxs-lookup"><span data-stu-id="15534-172">The desired configuration mode for the VLAN endpoint.</span></span> <span data-ttu-id="15534-173">Cette propriété est utilisée pour définir la valeur de la propriété **OperationalEndpointMode** initiale dans l’instance de la classe [**\_ VLANEndpoint de MSVM**](msvm-vlanendpoint.md) associée au port Ethernet ciblé.</span><span class="sxs-lookup"><span data-stu-id="15534-173">This property is used to set the initial **OperationalEndpointMode** property value in the instance of [**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md) class associated with the targeted Ethernet port.</span></span> <span data-ttu-id="15534-174">Pour connaître les valeurs possibles, consultez la propriété **OperationalEndpointMode** de la classe **MSVM \_ VLANEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="15534-174">See the **OperationalEndpointMode** property of the **Msvm\_VLANEndpoint** class for possible values.</span></span> <span data-ttu-id="15534-175">Cette propriété est héritée de la **\_ EthernetPortAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="15534-175">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="15534-176">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="15534-176">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15534-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="15534-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15534-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15534-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15534-179">Nom complet configurable par l’utilisateur pour l’appareil auquel cette instance RASD est associée.</span><span class="sxs-lookup"><span data-stu-id="15534-179">The user-configurable display name for the device this RASD instance is associated with.</span></span> <span data-ttu-id="15534-180">Cette propriété est héritée de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))et est définie sur « port Ethernet ».</span><span class="sxs-lookup"><span data-stu-id="15534-180">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is set to "Ethernet Port".</span></span> <span data-ttu-id="15534-181">La modification de cette propriété modifie le nom d’élément du dérivé de l’appareil logique associé.</span><span class="sxs-lookup"><span data-stu-id="15534-181">Changing this property will change the element name of the associated logical device derivative.</span></span>

<span data-ttu-id="15534-182">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="15534-182">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="15534-183">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="15534-183">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15534-184">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="15534-184">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="15534-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15534-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15534-186">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="15534-186">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="15534-187">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="15534-187">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15534-188">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="15534-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15534-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15534-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15534-190">Dans l’étendue de l’espace de noms d’instanciation, **InstanceID** identifie de façon opaque et unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="15534-190">Within the scope of the instantiating namespace, **InstanceID** opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="15534-191">Cette propriété est héritée de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))et est toujours définie sur « Microsoft :*VMID* \\ *VDID* \\ *Device-Specific-Data*».</span><span class="sxs-lookup"><span data-stu-id="15534-191">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Microsoft:*VMID*\\*VDID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="15534-192">**Limite**</span><span class="sxs-lookup"><span data-stu-id="15534-192">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15534-193">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="15534-193">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="15534-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15534-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15534-195">Limite supérieure ou quantité maximale de ressources qui seront accordées pour cette allocation.</span><span class="sxs-lookup"><span data-stu-id="15534-195">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="15534-196">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)et est toujours définie sur 1.</span><span class="sxs-lookup"><span data-stu-id="15534-196">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="15534-197">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="15534-197">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15534-198">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="15534-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15534-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15534-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15534-200">Spécifie comment cette ressource est mappée aux ressources sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="15534-200">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="15534-201">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="15534-201">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="15534-202">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="15534-202">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15534-203">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="15534-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15534-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15534-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15534-205">Chaîne qui décrit le type de modèle de point de terminaison de réseau local virtuel qui est pris en charge par ce point de terminaison VLAN.</span><span class="sxs-lookup"><span data-stu-id="15534-205">A string that describes the type of VLAN endpoint model that is supported by this VLAN endpoint.</span></span> <span data-ttu-id="15534-206">Cette propriété est utilisée uniquement lorsque la propriété **DesiredVLANEndpointMode** est définie sur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="15534-206">This property is only used when the **DesiredVLANEndpointMode** property is set to 1 (Other).</span></span> <span data-ttu-id="15534-207">Cette propriété doit être définie sur **null** lorsque la propriété **DesiredVLANEndpointMode** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="15534-207">This property should be set to **Null** when the **DesiredVLANEndpointMode** property is any value other than 1.</span></span> <span data-ttu-id="15534-208">Cette propriété est héritée de la **\_ EthernetPortAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="15534-208">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="15534-209">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="15534-209">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15534-210">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="15534-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15534-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15534-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15534-212">Chaîne qui décrit le type de ressource lorsqu’une valeur bien définie n’est pas disponible et que ResourceType a la valeur 0 (« other »).</span><span class="sxs-lookup"><span data-stu-id="15534-212">A string that describes the resource type when a well-defined value is not available and ResourceType is set to 0 ("Other").</span></span> <span data-ttu-id="15534-213">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="15534-213">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="15534-214">**Parent**</span><span class="sxs-lookup"><span data-stu-id="15534-214">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15534-215">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="15534-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15534-216">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15534-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15534-217">Parent de la ressource.</span><span class="sxs-lookup"><span data-stu-id="15534-217">The parent of the resource.</span></span> <span data-ttu-id="15534-218">Par exemple, un contrôleur pour l’allocation actuelle.</span><span class="sxs-lookup"><span data-stu-id="15534-218">For example, a controller for the current allocation.</span></span> <span data-ttu-id="15534-219">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="15534-219">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="15534-220">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="15534-220">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15534-221">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="15534-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15534-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15534-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15534-223">Le pool à partir duquel la ressource est actuellement allouée, ou le pool à partir duquel la ressource est allouée lorsque l’allocation se produit.</span><span class="sxs-lookup"><span data-stu-id="15534-223">The pool the resource is currently allocated from, or the pool the resource will be allocated from when the allocation occurs.</span></span> <span data-ttu-id="15534-224">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="15534-224">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="15534-225">**Réservation**</span><span class="sxs-lookup"><span data-stu-id="15534-225">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15534-226">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="15534-226">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="15534-227">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15534-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15534-228">Quantité de ressources dont la disponibilité est garantie pour cette allocation.</span><span class="sxs-lookup"><span data-stu-id="15534-228">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="15534-229">Sur les systèmes qui prennent en charge le surengagement de ressources, cette valeur est généralement utilisée pour le contrôle d’admission pour empêcher l’acceptation d’une allocation.</span><span class="sxs-lookup"><span data-stu-id="15534-229">On systems that support over-commitment of resources, this value is typically used for admission control to prevent an allocation from being accepted.</span></span> <span data-ttu-id="15534-230">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)et est toujours définie sur 1.</span><span class="sxs-lookup"><span data-stu-id="15534-230">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="15534-231">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="15534-231">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15534-232">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="15534-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15534-233">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15534-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15534-234">Chaîne qui décrit un sous-type spécifique à l’implémentation pour cette ressource.</span><span class="sxs-lookup"><span data-stu-id="15534-234">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="15534-235">Par exemple, cela peut être utilisé pour distinguer différents modèles du même type de ressource.</span><span class="sxs-lookup"><span data-stu-id="15534-235">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="15534-236">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)et est toujours définie sur « port Ethernet émulé Microsoft ».</span><span class="sxs-lookup"><span data-stu-id="15534-236">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to "Microsoft Emulated Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="15534-237">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="15534-237">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15534-238">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="15534-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15534-239">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15534-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15534-240">Type de ressource auquel ce paramètre s’applique.</span><span class="sxs-lookup"><span data-stu-id="15534-240">The type of resource this setting applies to.</span></span> <span data-ttu-id="15534-241">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)et est toujours définie sur 10 (carte Ethernet).</span><span class="sxs-lookup"><span data-stu-id="15534-241">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 10 (Ethernet Adapter).</span></span>

</dd> <dt>

<span data-ttu-id="15534-242">**StaticMacAddress**</span><span class="sxs-lookup"><span data-stu-id="15534-242">**StaticMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15534-243">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="15534-243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="15534-244">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15534-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15534-245">Indique s’il faut utiliser une adresse MAC statique.</span><span class="sxs-lookup"><span data-stu-id="15534-245">Indicates whether to use a static MAC address.</span></span>

<span data-ttu-id="15534-246">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="15534-246">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="15534-247">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="15534-247">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15534-248">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="15534-248">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="15534-249">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15534-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15534-250">Quantité de ressources présentées au consommateur.</span><span class="sxs-lookup"><span data-stu-id="15534-250">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="15534-251">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)et est toujours définie sur 1.</span><span class="sxs-lookup"><span data-stu-id="15534-251">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="15534-252">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="15534-252">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15534-253">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="15534-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15534-254">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15534-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15534-255">Spécifie l’unité de mesure pour cette allocation de ressources.</span><span class="sxs-lookup"><span data-stu-id="15534-255">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="15534-256">La valeur de cette propriété doit être une valeur légale du qualificateur d’unités de programmation, tel que défini dans l’annexe C. 1 de DSP0004 V 2.5 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="15534-256">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="15534-257">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="15534-257">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="15534-258">**Poids**</span><span class="sxs-lookup"><span data-stu-id="15534-258">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15534-259">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="15534-259">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="15534-260">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15534-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15534-261">Priorité relative pour cette allocation par rapport à d’autres allocations à partir du même ResourcePool.</span><span class="sxs-lookup"><span data-stu-id="15534-261">A relative priority for this allocation in relation to other allocations from the same ResourcePool.</span></span> <span data-ttu-id="15534-262">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)et est toujours définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="15534-262">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15534-263">Notes</span><span class="sxs-lookup"><span data-stu-id="15534-263">Remarks</span></span>

<span data-ttu-id="15534-264">L’accès à la classe **MSVM \_ EmulatedEthernetPortSettingData** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="15534-264">Access to the **Msvm\_EmulatedEthernetPortSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="15534-265">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="15534-265">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="15534-266">Exemples</span><span class="sxs-lookup"><span data-stu-id="15534-266">Examples</span></span>

<span data-ttu-id="15534-267">Consultez [interrogation d’objets de mise en réseau](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="15534-267">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="15534-268">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15534-268">Requirements</span></span>



| <span data-ttu-id="15534-269">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15534-269">Requirement</span></span> | <span data-ttu-id="15534-270">Valeur</span><span class="sxs-lookup"><span data-stu-id="15534-270">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15534-271">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15534-271">Minimum supported client</span></span><br/> | <span data-ttu-id="15534-272">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15534-272">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="15534-273">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15534-273">Minimum supported server</span></span><br/> | <span data-ttu-id="15534-274">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15534-274">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="15534-275">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="15534-275">Namespace</span></span><br/>                | <span data-ttu-id="15534-276">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="15534-276">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="15534-277">MOF</span><span class="sxs-lookup"><span data-stu-id="15534-277">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15534-278"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15534-278"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="15534-279">DLL</span><span class="sxs-lookup"><span data-stu-id="15534-279">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15534-280"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="15534-280"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="15534-281">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15534-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15534-282">**\_ETHERNETPORTALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="15534-282">**CIM\_EthernetPortAllocationSettingData**</span></span>](cim-ethernetportallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="15534-283">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="15534-283">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

