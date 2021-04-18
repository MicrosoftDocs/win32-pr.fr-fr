---
description: Représente l’état configuré d’une carte Ethernet synthétique.
ms.assetid: BE895BAF-7766-43A2-9659-3ABA97A16134
title: Classe Msvm_SyntheticEthernetPortSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticEthernetPortSettingData
- Msvm_SyntheticEthernetPortSettingData.InstanceID
- Msvm_SyntheticEthernetPortSettingData.Caption
- Msvm_SyntheticEthernetPortSettingData.Description
- Msvm_SyntheticEthernetPortSettingData.ElementName
- Msvm_SyntheticEthernetPortSettingData.ResourceType
- Msvm_SyntheticEthernetPortSettingData.OtherResourceType
- Msvm_SyntheticEthernetPortSettingData.ResourceSubType
- Msvm_SyntheticEthernetPortSettingData.PoolID
- Msvm_SyntheticEthernetPortSettingData.ConsumerVisibility
- Msvm_SyntheticEthernetPortSettingData.HostResource
- Msvm_SyntheticEthernetPortSettingData.AllocationUnits
- Msvm_SyntheticEthernetPortSettingData.VirtualQuantity
- Msvm_SyntheticEthernetPortSettingData.Reservation
- Msvm_SyntheticEthernetPortSettingData.Limit
- Msvm_SyntheticEthernetPortSettingData.Weight
- Msvm_SyntheticEthernetPortSettingData.AutomaticAllocation
- Msvm_SyntheticEthernetPortSettingData.AutomaticDeallocation
- Msvm_SyntheticEthernetPortSettingData.Parent
- Msvm_SyntheticEthernetPortSettingData.Connection
- Msvm_SyntheticEthernetPortSettingData.Address
- Msvm_SyntheticEthernetPortSettingData.MappingBehavior
- Msvm_SyntheticEthernetPortSettingData.AddressOnParent
- Msvm_SyntheticEthernetPortSettingData.VirtualQuantityUnits
- Msvm_SyntheticEthernetPortSettingData.DesiredVLANEndpointMode
- Msvm_SyntheticEthernetPortSettingData.OtherEndpointMode
- Msvm_SyntheticEthernetPortSettingData.VirtualSystemIdentifiers
- Msvm_SyntheticEthernetPortSettingData.DeviceNamingEnabled
- Msvm_SyntheticEthernetPortSettingData.AllowPacketDirect
- Msvm_SyntheticEthernetPortSettingData.StaticMacAddress
- Msvm_SyntheticEthernetPortSettingData.ClusterMonitored
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5b31b02782c0f215f70f3bb5d2767b01294c7261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519259"
---
# <a name="msvm_syntheticethernetportsettingdata-class"></a><span data-ttu-id="d8391-103">MSVM \_ SyntheticEthernetPortSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="d8391-103">Msvm\_SyntheticEthernetPortSettingData class</span></span>

<span data-ttu-id="d8391-104">Représente l’état configuré d’une carte Ethernet synthétique.</span><span class="sxs-lookup"><span data-stu-id="d8391-104">Represents the configured state of a synthetic Ethernet adapter.</span></span>

<span data-ttu-id="d8391-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d8391-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8391-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8391-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticEthernetPortSettingData : CIM_EthernetPortAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Virtual Ethernet Port Default Settings";
  string  Description = "Describes the default settings for the virtual Ethernet port resources.";
  string  ElementName;
  uint16  ResourceType = 10;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Synthetic Ethernet Port";
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
  uint16  DesiredVLANEndpointMode;
  string  OtherEndpointMode;
  string  VirtualSystemIdentifiers[];
  boolean DeviceNamingEnabled = FALSE;
  boolean AllowPacketDirect = FALSE;
  boolean StaticMacAddress = False;
  boolean ClusterMonitored = TRUE;
};
```

## <a name="members"></a><span data-ttu-id="d8391-107">Membres</span><span class="sxs-lookup"><span data-stu-id="d8391-107">Members</span></span>

<span data-ttu-id="d8391-108">La classe **MSVM \_ SyntheticEthernetPortSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d8391-108">The **Msvm\_SyntheticEthernetPortSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="d8391-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d8391-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d8391-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d8391-110">Properties</span></span>

<span data-ttu-id="d8391-111">La classe **MSVM \_ SyntheticEthernetPortSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d8391-111">The **Msvm\_SyntheticEthernetPortSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d8391-112">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="d8391-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8391-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8391-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8391-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8391-115">Adresse de la ressource.</span><span class="sxs-lookup"><span data-stu-id="d8391-115">The address of the resource.</span></span> <span data-ttu-id="d8391-116">Par exemple, l’adresse MAC d’un port Ethernet.</span><span class="sxs-lookup"><span data-stu-id="d8391-116">For example, the MAC address of a Ethernet port.</span></span> <span data-ttu-id="d8391-117">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8391-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d8391-118">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="d8391-118">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8391-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8391-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8391-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8391-121">Décrit l’adresse de cette ressource dans le contexte du parent.</span><span class="sxs-lookup"><span data-stu-id="d8391-121">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="d8391-122">Les propriétés **parent** et **AddressOnParent** sont utilisées pour décrire la relation du contrôleur, ainsi que l’ordre des appareils sur un contrôleur.</span><span class="sxs-lookup"><span data-stu-id="d8391-122">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="d8391-123">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8391-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d8391-124">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="d8391-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8391-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8391-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8391-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8391-127">Unités d’allocation utilisées par la **réservation** et les propriétés de la **limite** .</span><span class="sxs-lookup"><span data-stu-id="d8391-127">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="d8391-128">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8391-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d8391-129">**AllowPacketDirect**</span><span class="sxs-lookup"><span data-stu-id="d8391-129">**AllowPacketDirect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-130">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d8391-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d8391-131">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d8391-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d8391-132">Indique si la projection d’un PacketDirect est activée pour la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="d8391-132">Indicates if PacketDirect projection is enabled for the VM.</span></span>

> [!Note]  
> <span data-ttu-id="d8391-133">Ajouté dans Windows 10, version 1703 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="d8391-133">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="d8391-134">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="d8391-134">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-135">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d8391-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d8391-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8391-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8391-137">Indique si la ressource sera automatiquement allouée.</span><span class="sxs-lookup"><span data-stu-id="d8391-137">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="d8391-138">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8391-138">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d8391-139">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="d8391-139">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-140">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d8391-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d8391-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8391-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8391-142">Indique si la ressource sera automatiquement désallouée.</span><span class="sxs-lookup"><span data-stu-id="d8391-142">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="d8391-143">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8391-143">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d8391-144">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d8391-144">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8391-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8391-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8391-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8391-147">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d8391-147">A short description of the object.</span></span> <span data-ttu-id="d8391-148">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d8391-148">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d8391-149">**ClusterMonitored**</span><span class="sxs-lookup"><span data-stu-id="d8391-149">**ClusterMonitored**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-150">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d8391-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d8391-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8391-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8391-152">Indique si cette carte Ethernet est surveillée par un cluster.</span><span class="sxs-lookup"><span data-stu-id="d8391-152">Indicates whether this ethernet adapter is monitored by a cluster.</span></span> <span data-ttu-id="d8391-153">La valeur par défaut de cette propriété est true si elle n’est pas configurée.</span><span class="sxs-lookup"><span data-stu-id="d8391-153">This property defaults to true if not configured.</span></span>

<span data-ttu-id="d8391-154">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="d8391-154">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="d8391-155">**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="d8391-155">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="d8391-156">**Connection**</span><span class="sxs-lookup"><span data-stu-id="d8391-156">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-157">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="d8391-157">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d8391-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8391-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8391-159">Élément auquel cette ressource est connectée.</span><span class="sxs-lookup"><span data-stu-id="d8391-159">The thing to which this resource is connected.</span></span> <span data-ttu-id="d8391-160">Par exemple, un réseau nommé ou un port commuté.</span><span class="sxs-lookup"><span data-stu-id="d8391-160">For example, a named network or switch port.</span></span> <span data-ttu-id="d8391-161">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8391-161">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d8391-162">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="d8391-162">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-163">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8391-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d8391-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8391-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8391-165">Visibilité des consommateurs sur la ressource allouée.</span><span class="sxs-lookup"><span data-stu-id="d8391-165">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="d8391-166">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)et est toujours définie sur 3 (virtualisé).</span><span class="sxs-lookup"><span data-stu-id="d8391-166">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="d8391-167">**Description**</span><span class="sxs-lookup"><span data-stu-id="d8391-167">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8391-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8391-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8391-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8391-170">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="d8391-170">A description of the object.</span></span> <span data-ttu-id="d8391-171">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d8391-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d8391-172">**DesiredVLANEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="d8391-172">**DesiredVLANEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-173">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8391-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d8391-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8391-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8391-175">Mode de configuration souhaité pour le point de terminaison de réseau local virtuel.</span><span class="sxs-lookup"><span data-stu-id="d8391-175">The desired configuration mode for the VLAN endpoint.</span></span> <span data-ttu-id="d8391-176">Cette propriété est utilisée pour définir la valeur de la propriété **OperationalEndpointMode** initiale dans l’instance de la classe [**MSVM \_ VLANEndpoint**](msvm-vlanendpoint.md) associée au port Ethernet ciblé.</span><span class="sxs-lookup"><span data-stu-id="d8391-176">This property is used to set the initial **OperationalEndpointMode** property value in the instance of the [**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md) class associated with the targeted Ethernet port.</span></span> <span data-ttu-id="d8391-177">Pour connaître les valeurs possibles, consultez la propriété **OperationalEndpointMode** de la classe **MSVM \_ VLANEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="d8391-177">See the **OperationalEndpointMode** property of the **Msvm\_VLANEndpoint** class for possible values.</span></span> <span data-ttu-id="d8391-178">Cette propriété est héritée de la **\_ EthernetPortAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="d8391-178">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="d8391-179">**DeviceNamingEnabled**</span><span class="sxs-lookup"><span data-stu-id="d8391-179">**DeviceNamingEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-180">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d8391-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d8391-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8391-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8391-182">Indique si cette carte Ethernet prend en charge les noms d’appareil.</span><span class="sxs-lookup"><span data-stu-id="d8391-182">Indicates whether this ethernet adapter supports device naming.</span></span>

<span data-ttu-id="d8391-183">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyVirtualSystemResources**](https://www.bing.com/search?q=**ModifyVirtualSystemResources**) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="d8391-183">This is a read-only property, but it can be changed using the [**ModifyVirtualSystemResources**](https://www.bing.com/search?q=**ModifyVirtualSystemResources**) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="d8391-184">Ajouté dans Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="d8391-184">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="d8391-185">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d8391-185">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-186">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8391-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8391-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8391-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8391-188">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d8391-188">A short description of the object.</span></span> <span data-ttu-id="d8391-189">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d8391-189">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d8391-190">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="d8391-190">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-191">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="d8391-191">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d8391-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8391-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8391-193">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="d8391-193">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d8391-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d8391-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-195">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8391-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8391-196">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8391-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8391-197">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="d8391-197">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d8391-198">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="d8391-198">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d8391-199">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d8391-199">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d8391-200">**Limite**</span><span class="sxs-lookup"><span data-stu-id="d8391-200">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-201">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d8391-201">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d8391-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8391-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8391-203">Limite supérieure ou quantité maximale de ressources qui seront accordées pour cette allocation.</span><span class="sxs-lookup"><span data-stu-id="d8391-203">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="d8391-204">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8391-204">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d8391-205">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="d8391-205">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-206">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8391-206">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d8391-207">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8391-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8391-208">Spécifie comment cette ressource est mappée aux ressources sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="d8391-208">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="d8391-209">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8391-209">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d8391-210">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="d8391-210">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-211">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8391-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8391-212">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8391-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8391-213">Chaîne qui décrit le type de modèle de point de terminaison de réseau local virtuel qui est pris en charge par ce point de terminaison VLAN.</span><span class="sxs-lookup"><span data-stu-id="d8391-213">A string that describes the type of VLAN endpoint model that is supported by this VLAN endpoint.</span></span> <span data-ttu-id="d8391-214">Cette propriété est utilisée uniquement lorsque la propriété **DesiredVLANEndpointMode** est définie sur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="d8391-214">This property is only used when the **DesiredVLANEndpointMode** property is set to 1 (Other).</span></span> <span data-ttu-id="d8391-215">Cette propriété doit être définie sur **null** lorsque la propriété **DesiredVLANEndpointMode** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="d8391-215">This property should be set to **Null** when the **DesiredVLANEndpointMode** property is any value other than 1.</span></span> <span data-ttu-id="d8391-216">Cette propriété est héritée de la **\_ EthernetPortAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="d8391-216">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="d8391-217">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="d8391-217">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-218">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8391-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8391-219">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8391-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8391-220">Chaîne qui décrit le type de ressource lorsqu’une valeur bien définie n’est pas disponible et que **resourceType** a la valeur « Other » (0).</span><span class="sxs-lookup"><span data-stu-id="d8391-220">A string that describes the resource type when a well-defined value is not available and **ResourceType** is set to "Other" (0).</span></span> <span data-ttu-id="d8391-221">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="d8391-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d8391-222">**Parent**</span><span class="sxs-lookup"><span data-stu-id="d8391-222">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-223">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8391-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8391-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8391-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8391-225">Parent de la ressource.</span><span class="sxs-lookup"><span data-stu-id="d8391-225">The parent of the resource.</span></span> <span data-ttu-id="d8391-226">Par exemple, un contrôleur pour l’allocation actuelle.</span><span class="sxs-lookup"><span data-stu-id="d8391-226">For example, a controller for the current allocation.</span></span> <span data-ttu-id="d8391-227">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8391-227">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d8391-228">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="d8391-228">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-229">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8391-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8391-230">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8391-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8391-231">Le pool à partir duquel la ressource est actuellement allouée, ou le pool à partir duquel la ressource sera allouée lorsque l’allocation aura lieu.</span><span class="sxs-lookup"><span data-stu-id="d8391-231">The pool the resource is currently allocated from, or which pool the resource will be allocated from when the allocation occurs.</span></span> <span data-ttu-id="d8391-232">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8391-232">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d8391-233">**Réservation**</span><span class="sxs-lookup"><span data-stu-id="d8391-233">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-234">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d8391-234">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d8391-235">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8391-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8391-236">Quantité de ressources dont la disponibilité est garantie pour cette allocation.</span><span class="sxs-lookup"><span data-stu-id="d8391-236">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="d8391-237">Sur les systèmes qui prennent en charge le surengagement de ressources, cette valeur est généralement utilisée pour le contrôle d’admission pour empêcher l’acceptation d’une allocation.</span><span class="sxs-lookup"><span data-stu-id="d8391-237">On systems that support over-commitment of resources, this value is typically used for admission control to prevent an allocation from being accepted.</span></span> <span data-ttu-id="d8391-238">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8391-238">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d8391-239">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="d8391-239">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-240">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8391-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8391-241">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8391-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8391-242">Chaîne qui décrit un sous-type spécifique à l’implémentation pour cette ressource.</span><span class="sxs-lookup"><span data-stu-id="d8391-242">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="d8391-243">Par exemple, cela peut être utilisé pour distinguer différents modèles du même type de ressource.</span><span class="sxs-lookup"><span data-stu-id="d8391-243">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="d8391-244">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8391-244">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d8391-245">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="d8391-245">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-246">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8391-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d8391-247">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8391-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8391-248">Type de ressource auquel ce paramètre s’applique.</span><span class="sxs-lookup"><span data-stu-id="d8391-248">The type of resource this setting applies to.</span></span> <span data-ttu-id="d8391-249">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)et est toujours définie sur 10 (carte Ethernet).</span><span class="sxs-lookup"><span data-stu-id="d8391-249">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 10 (Ethernet Adapter).</span></span>

</dd> <dt>

<span data-ttu-id="d8391-250">**StaticMacAddress**</span><span class="sxs-lookup"><span data-stu-id="d8391-250">**StaticMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-251">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d8391-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d8391-252">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8391-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8391-253">Spécifie si l’adresse MAC est statique.</span><span class="sxs-lookup"><span data-stu-id="d8391-253">Specifies if the MAC address is static.</span></span>

</dd> <dt>

<span data-ttu-id="d8391-254">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="d8391-254">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-255">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d8391-255">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d8391-256">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8391-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8391-257">Quantité de ressources présentées au consommateur.</span><span class="sxs-lookup"><span data-stu-id="d8391-257">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="d8391-258">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8391-258">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d8391-259">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="d8391-259">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-260">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8391-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8391-261">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8391-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8391-262">Spécifie l’unité de mesure pour la propriété **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="d8391-262">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="d8391-263">La valeur de cette propriété doit être une valeur légale du qualificateur d’unités de programmation, tel que défini dans l’annexe C. 1 de DSP0004 V 2.5 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d8391-263">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="d8391-264">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8391-264">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d8391-265">**VirtualSystemIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="d8391-265">**VirtualSystemIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-266">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="d8391-266">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d8391-267">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8391-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8391-268">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="d8391-268">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="d8391-269">Tableau de chaînes des identificateurs de cette ressource présentée au système d’exploitation de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="d8391-269">A string array of identifiers of this resource presented to the virtual machine's operating system.</span></span> <span data-ttu-id="d8391-270">Les index et les valeurs par index sont définis par ressource (c’est-à-dire, pour chaque valeur de propriété **resourceType** énumérée).</span><span class="sxs-lookup"><span data-stu-id="d8391-270">The indexes and values per index are defined on a per resource basis (that is, for each enumerated **ResourceType** property value).</span></span>

</dd> <dt>

<span data-ttu-id="d8391-271">**Poids**</span><span class="sxs-lookup"><span data-stu-id="d8391-271">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8391-272">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d8391-272">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d8391-273">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8391-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8391-274">Priorité relative pour cette allocation par rapport à d’autres allocations à partir du même pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="d8391-274">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="d8391-275">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8391-275">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8391-276">Notes</span><span class="sxs-lookup"><span data-stu-id="d8391-276">Remarks</span></span>

<span data-ttu-id="d8391-277">L’accès à la classe **MSVM \_ SyntheticEthernetPortSettingData** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="d8391-277">Access to the **Msvm\_SyntheticEthernetPortSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d8391-278">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d8391-278">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="d8391-279">Exemples</span><span class="sxs-lookup"><span data-stu-id="d8391-279">Examples</span></span>

<span data-ttu-id="d8391-280">Consultez [interrogation d’objets de mise en réseau](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d8391-280">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d8391-281">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8391-281">Requirements</span></span>



| <span data-ttu-id="d8391-282">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8391-282">Requirement</span></span> | <span data-ttu-id="d8391-283">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8391-283">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8391-284">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8391-284">Minimum supported client</span></span><br/> | <span data-ttu-id="d8391-285">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8391-285">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d8391-286">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8391-286">Minimum supported server</span></span><br/> | <span data-ttu-id="d8391-287">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8391-287">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d8391-288">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d8391-288">Namespace</span></span><br/>                | <span data-ttu-id="d8391-289">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="d8391-289">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d8391-290">MOF</span><span class="sxs-lookup"><span data-stu-id="d8391-290">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8391-291"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8391-291"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8391-292">DLL</span><span class="sxs-lookup"><span data-stu-id="d8391-292">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8391-293"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d8391-293"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d8391-294">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8391-294">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8391-295">**\_ETHERNETPORTALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="d8391-295">**CIM\_EthernetPortAllocationSettingData**</span></span>](cim-ethernetportallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="d8391-296">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="d8391-296">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

