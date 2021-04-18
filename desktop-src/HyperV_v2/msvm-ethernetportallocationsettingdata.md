---
description: Représente une demande d’allocation pour un port de commutateur statique ou dynamique, ou représente la configuration active d’un port de commutateur statique ou dynamique actuellement alloué.
ms.assetid: ef70b72f-75a0-448e-a648-6a28c12f0da1
title: Classe Msvm_EthernetPortAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortAllocationSettingData
- Msvm_EthernetPortAllocationSettingData.InstanceID
- Msvm_EthernetPortAllocationSettingData.Caption
- Msvm_EthernetPortAllocationSettingData.Description
- Msvm_EthernetPortAllocationSettingData.ElementName
- Msvm_EthernetPortAllocationSettingData.ResourceType
- Msvm_EthernetPortAllocationSettingData.OtherResourceType
- Msvm_EthernetPortAllocationSettingData.ResourceSubType
- Msvm_EthernetPortAllocationSettingData.PoolID
- Msvm_EthernetPortAllocationSettingData.ConsumerVisibility
- Msvm_EthernetPortAllocationSettingData.HostResource
- Msvm_EthernetPortAllocationSettingData.AllocationUnits
- Msvm_EthernetPortAllocationSettingData.VirtualQuantity
- Msvm_EthernetPortAllocationSettingData.Reservation
- Msvm_EthernetPortAllocationSettingData.Limit
- Msvm_EthernetPortAllocationSettingData.Weight
- Msvm_EthernetPortAllocationSettingData.AutomaticAllocation
- Msvm_EthernetPortAllocationSettingData.AutomaticDeallocation
- Msvm_EthernetPortAllocationSettingData.Parent
- Msvm_EthernetPortAllocationSettingData.Connection
- Msvm_EthernetPortAllocationSettingData.Address
- Msvm_EthernetPortAllocationSettingData.MappingBehavior
- Msvm_EthernetPortAllocationSettingData.AddressOnParent
- Msvm_EthernetPortAllocationSettingData.VirtualQuantityUnits
- Msvm_EthernetPortAllocationSettingData.DesiredVLANEndpointMode
- Msvm_EthernetPortAllocationSettingData.OtherEndpointMode
- Msvm_EthernetPortAllocationSettingData.EnabledState
- Msvm_EthernetPortAllocationSettingData.LastKnownSwitchName
- Msvm_EthernetPortAllocationSettingData.RequiredFeatures
- Msvm_EthernetPortAllocationSettingData.RequiredFeatureHints
- Msvm_EthernetPortAllocationSettingData.TestReplicaPoolID
- Msvm_EthernetPortAllocationSettingData.TestReplicaSwitchName
- Msvm_EthernetPortAllocationSettingData.CompartmentGuid
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a310daf30127aec5069efcf7ca4fd5ead9277e6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519732"
---
# <a name="msvm_ethernetportallocationsettingdata-class"></a><span data-ttu-id="76644-103">MSVM \_ EthernetPortAllocationSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="76644-103">Msvm\_EthernetPortAllocationSettingData class</span></span>

<span data-ttu-id="76644-104">Représente une demande d’allocation pour un port de commutateur statique ou dynamique, ou représente la configuration active d’un port de commutateur statique ou dynamique actuellement alloué.</span><span class="sxs-lookup"><span data-stu-id="76644-104">Represents an allocation request for a static or dynamic switch port, or represents the active configuration of a currently allocated static or dynamic switch port.</span></span> <span data-ttu-id="76644-105">Une demande d’allocation pour un port de commutateur dynamique est également connue sous le nom de demande de connexion.</span><span class="sxs-lookup"><span data-stu-id="76644-105">An allocation request for a dynamic switch port is also known as a connection request.</span></span>

<span data-ttu-id="76644-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="76644-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="76644-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76644-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortAllocationSettingData : CIM_EthernetPortAllocationSettingData
{
  string  InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string  Caption = "Ethernet Switch Port Settings";
  string  Description = "Ethernet Switch Port Settings";
  string  ElementName;
  uint16  ResourceType = 33;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight = 0;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  uint16  DesiredVLANEndpointMode;
  string  OtherEndpointMode;
  uint16  EnabledState;
  string  LastKnownSwitchName;
  string  RequiredFeatures[];
  string  RequiredFeatureHints[];
  string  TestReplicaPoolID;
  string  TestReplicaSwitchName;
  string  CompartmentGuid;
};
```

## <a name="members"></a><span data-ttu-id="76644-108">Membres</span><span class="sxs-lookup"><span data-stu-id="76644-108">Members</span></span>

<span data-ttu-id="76644-109">La classe **MSVM \_ EthernetPortAllocationSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="76644-109">The **Msvm\_EthernetPortAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="76644-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="76644-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="76644-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="76644-111">Properties</span></span>

<span data-ttu-id="76644-112">La classe **MSVM \_ EthernetPortAllocationSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="76644-112">The **Msvm\_EthernetPortAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="76644-113">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="76644-113">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76644-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76644-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76644-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76644-116">Adresse de la ressource.</span><span class="sxs-lookup"><span data-stu-id="76644-116">The address of the resource.</span></span> <span data-ttu-id="76644-117">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="76644-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="76644-118">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="76644-118">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76644-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76644-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76644-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76644-121">Décrit l’adresse de cette ressource dans le contexte du parent.</span><span class="sxs-lookup"><span data-stu-id="76644-121">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="76644-122">Les propriétés **parent** et **AddressOnParent** sont utilisées pour décrire la relation du contrôleur, ainsi que l’ordre des appareils sur un contrôleur.</span><span class="sxs-lookup"><span data-stu-id="76644-122">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="76644-123">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="76644-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="76644-124">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="76644-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76644-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76644-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76644-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76644-127">Unité d’allocation utilisée par les propriétés de **réservation** et de **limite** .</span><span class="sxs-lookup"><span data-stu-id="76644-127">The unit of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="76644-128">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="76644-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="76644-129">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="76644-129">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-130">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="76644-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="76644-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76644-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76644-132">Indique si la ressource sera automatiquement allouée.</span><span class="sxs-lookup"><span data-stu-id="76644-132">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="76644-133">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="76644-133">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="76644-134">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="76644-134">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-135">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="76644-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="76644-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76644-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76644-137">Indique si la ressource sera automatiquement désallouée.</span><span class="sxs-lookup"><span data-stu-id="76644-137">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="76644-138">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="76644-138">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="76644-139">**Caption**</span><span class="sxs-lookup"><span data-stu-id="76644-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76644-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76644-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76644-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76644-142">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="76644-142">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="76644-143">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="76644-143">A short description of the object.</span></span> <span data-ttu-id="76644-144">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « paramètres de port de commutateur Ethernet ».</span><span class="sxs-lookup"><span data-stu-id="76644-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Settings".</span></span>

</dd> <dt>

<span data-ttu-id="76644-145">**CompartmentGuid**</span><span class="sxs-lookup"><span data-stu-id="76644-145">**CompartmentGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76644-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76644-147">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="76644-147">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="76644-148">Cette propriété spécifie le compartiment réseau cible pour le port.</span><span class="sxs-lookup"><span data-stu-id="76644-148">This property specifies the target network compartment for the port.</span></span> <span data-ttu-id="76644-149">Il est uniquement pris en charge pour les adaptateurs internes.</span><span class="sxs-lookup"><span data-stu-id="76644-149">It is only supported for internal adapters.</span></span>

> [!Note]  
> <span data-ttu-id="76644-150">Propriété ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="76644-150">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="76644-151">**Connection**</span><span class="sxs-lookup"><span data-stu-id="76644-151">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-152">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="76644-152">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="76644-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76644-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76644-154">Appareil auquel cette ressource est connectée.</span><span class="sxs-lookup"><span data-stu-id="76644-154">The device to which this resource is connected.</span></span> <span data-ttu-id="76644-155">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="76644-155">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="76644-156">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="76644-156">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-157">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76644-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76644-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76644-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76644-159">Visibilité du consommateur sur la ressource allouée.</span><span class="sxs-lookup"><span data-stu-id="76644-159">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="76644-160">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)et est toujours définie sur 3 (virtualisé).</span><span class="sxs-lookup"><span data-stu-id="76644-160">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="76644-161">**Description**</span><span class="sxs-lookup"><span data-stu-id="76644-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76644-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76644-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76644-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76644-164">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="76644-164">A description of the object.</span></span> <span data-ttu-id="76644-165">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « paramètres de port de commutateur Ethernet ».</span><span class="sxs-lookup"><span data-stu-id="76644-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Settings".</span></span>

</dd> <dt>

<span data-ttu-id="76644-166">**DesiredVLANEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="76644-166">**DesiredVLANEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-167">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76644-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76644-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76644-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76644-169">Mode de configuration souhaité pour le point de terminaison de réseau local virtuel.</span><span class="sxs-lookup"><span data-stu-id="76644-169">The desired configuration mode for the VLAN endpoint.</span></span> <span data-ttu-id="76644-170">Cette propriété est utilisée pour définir la valeur de la propriété **OperationalEndpointMode** initiale dans l’instance de la classe [**\_ VLANEndpoint de MSVM**](msvm-vlanendpoint.md) associée au port Ethernet ciblé.</span><span class="sxs-lookup"><span data-stu-id="76644-170">This property is used to set the initial **OperationalEndpointMode** property value in the instance of [**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md) class associated with the targeted Ethernet port.</span></span> <span data-ttu-id="76644-171">Pour connaître les valeurs possibles, consultez la propriété **OperationalEndpointMode** de la classe **MSVM \_ VLANEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="76644-171">See the **OperationalEndpointMode** property of the **Msvm\_VLANEndpoint** class for possible values.</span></span> <span data-ttu-id="76644-172">Cette propriété est héritée de la **\_ EthernetPortAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="76644-172">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="76644-173">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="76644-173">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76644-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76644-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76644-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76644-176">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="76644-176">A display name for the object.</span></span> <span data-ttu-id="76644-177">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="76644-177">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="76644-178">La modification de cette propriété modifie le nom d’élément du dérivé de l’appareil logique associé.</span><span class="sxs-lookup"><span data-stu-id="76644-178">Changing this property will change the element name of the associated logical device derivative.</span></span>

</dd> <dt>

<span data-ttu-id="76644-179">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="76644-179">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-180">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76644-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76644-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76644-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76644-182">Indique si la demande d’allocation est activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="76644-182">Indicates whether the allocation request is enabled or disabled.</span></span> <span data-ttu-id="76644-183">Quand une demande d’allocation est marquée comme désactivée (3), l’allocation n’est pas traitée.</span><span class="sxs-lookup"><span data-stu-id="76644-183">When an allocation request is marked as Disabled (3), then the allocation is not processed.</span></span> <span data-ttu-id="76644-184">**EnabledState** pour une configuration active est toujours marqué comme activé (2).</span><span class="sxs-lookup"><span data-stu-id="76644-184">The **EnabledState** for an active configuration is always marked as Enabled (2).</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="76644-185">**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="76644-185">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="76644-186">**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="76644-186">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="76644-187">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="76644-187">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-188">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="76644-188">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="76644-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76644-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76644-190">Une seule ressource hôte peut être assignée à chaque périphérique dans le commutateur virtuel, de sorte que seul le premier élément de ce tableau peut être défini.</span><span class="sxs-lookup"><span data-stu-id="76644-190">Only one host resource can be assigned to each device in the virtual switch, so only the first element of this array can be set.</span></span> <span data-ttu-id="76644-191">Pour les appareils qui prennent en charge cette fonctionnalité, définissez le premier élément du tableau **HostResource** pour qu’il contienne une référence à la ressource hôte sous-jacente à assigner.</span><span class="sxs-lookup"><span data-stu-id="76644-191">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="76644-192">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="76644-192">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="76644-193">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="76644-193">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-194">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76644-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76644-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76644-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76644-196">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="76644-196">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="76644-197">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="76644-197">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="76644-198">Cette propriété est héritée de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))et est toujours définie sur « Microsoft :*GUID* \\ *DeviceSpecificData*».</span><span class="sxs-lookup"><span data-stu-id="76644-198">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> <dt>

<span data-ttu-id="76644-199">**LastKnownSwitchName**</span><span class="sxs-lookup"><span data-stu-id="76644-199">**LastKnownSwitchName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-200">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76644-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76644-201">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76644-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76644-202">Dernier nom convivial connu du commutateur auquel ce port avait une affinité matérielle, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="76644-202">The last known friendly name of the switch this port had a hard affinity to, if any.</span></span>

> [!Note]  
> <span data-ttu-id="76644-203">Propriété ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="76644-203">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="76644-204">**Limite**</span><span class="sxs-lookup"><span data-stu-id="76644-204">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-205">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="76644-205">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="76644-206">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76644-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76644-207">Quantité maximale de ressources hôtes correspondantes qui peuvent être consommées par le commutateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="76644-207">The maximum amount of corresponding host resources that can be consumed by the virtual switch.</span></span> <span data-ttu-id="76644-208">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="76644-208">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="76644-209">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="76644-209">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-210">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76644-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76644-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76644-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76644-212">Spécifie comment cette ressource est mappée aux ressources sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="76644-212">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="76644-213">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="76644-213">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="76644-214">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="76644-214">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-215">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76644-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76644-216">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76644-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76644-217">Chaîne qui décrit le type de modèle de point de terminaison de réseau local virtuel qui est pris en charge par ce point de terminaison VLAN.</span><span class="sxs-lookup"><span data-stu-id="76644-217">A string that describes the type of VLAN endpoint model that is supported by this VLAN endpoint.</span></span> <span data-ttu-id="76644-218">Cette propriété est utilisée uniquement lorsque la propriété **DesiredVLANEndpointMode** est définie sur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="76644-218">This property is only used when the **DesiredVLANEndpointMode** property is set to 1 (Other).</span></span> <span data-ttu-id="76644-219">Cette propriété doit être définie sur **null** lorsque la propriété **DesiredVLANEndpointMode** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="76644-219">This property should be set to **Null** when the **DesiredVLANEndpointMode** property is any value other than 1.</span></span> <span data-ttu-id="76644-220">Cette propriété est héritée de la **\_ EthernetPortAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="76644-220">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="76644-221">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="76644-221">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-222">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76644-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76644-223">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76644-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76644-224">Chaîne qui décrit le type de ressource lorsqu’une valeur bien définie n’est pas disponible et que [**resourceType**](msvm-processorsettingdata.md) a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="76644-224">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1 (Other).</span></span> <span data-ttu-id="76644-225">Cette propriété est héritée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="76644-225">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="76644-226">**Parent**</span><span class="sxs-lookup"><span data-stu-id="76644-226">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-227">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76644-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76644-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76644-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76644-229">Parent de la ressource.</span><span class="sxs-lookup"><span data-stu-id="76644-229">The parent of the resource.</span></span> <span data-ttu-id="76644-230">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="76644-230">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="76644-231">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="76644-231">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-232">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76644-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76644-233">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76644-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76644-234">Identificateur du pool de ressources à partir duquel cette ressource a été allouée.</span><span class="sxs-lookup"><span data-stu-id="76644-234">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="76644-235">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="76644-235">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="76644-236">**RequiredFeatureHints**</span><span class="sxs-lookup"><span data-stu-id="76644-236">**RequiredFeatureHints**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-237">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="76644-237">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="76644-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76644-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76644-239">Liste des noms complets qui correspondent à chaque entrée dans le tableau **RequiredFeatures** .</span><span class="sxs-lookup"><span data-stu-id="76644-239">The list of display names that correspond to each entry in the **RequiredFeatures** array.</span></span>

</dd> <dt>

<span data-ttu-id="76644-240">**RequiredFeatures**</span><span class="sxs-lookup"><span data-stu-id="76644-240">**RequiredFeatures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-241">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="76644-241">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="76644-242">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="76644-242">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="76644-243">Liste des identificateurs de fonctionnalités qui représentent toutes les fonctionnalités requises pour un port.</span><span class="sxs-lookup"><span data-stu-id="76644-243">The list of feature identifiers that represent all the features that are required for a port.</span></span>

</dd> <dt>

<span data-ttu-id="76644-244">**Réservation**</span><span class="sxs-lookup"><span data-stu-id="76644-244">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-245">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="76644-245">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="76644-246">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76644-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76644-247">Quantité de ressources réservées pour une utilisation par le commutateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="76644-247">The amount of resources that are reserved for use by the virtual switch.</span></span> <span data-ttu-id="76644-248">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="76644-248">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="76644-249">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="76644-249">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-250">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76644-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76644-251">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76644-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76644-252">Chaîne qui décrit un sous-type spécifique à l’implémentation pour cette ressource.</span><span class="sxs-lookup"><span data-stu-id="76644-252">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="76644-253">Par exemple, cela peut être utilisé pour distinguer différents modèles du même type de ressource.</span><span class="sxs-lookup"><span data-stu-id="76644-253">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="76644-254">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="76644-254">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="76644-255">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="76644-255">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-256">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76644-256">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76644-257">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76644-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76644-258">Type de ressource représenté par ce paramètre d’allocation.</span><span class="sxs-lookup"><span data-stu-id="76644-258">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="76644-259">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)et est toujours définie sur 33 (connexion Ethernet).</span><span class="sxs-lookup"><span data-stu-id="76644-259">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 33 (Ethernet connection).</span></span>

</dd> <dt>

<span data-ttu-id="76644-260">**TestReplicaPoolID**</span><span class="sxs-lookup"><span data-stu-id="76644-260">**TestReplicaPoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-261">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76644-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76644-262">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="76644-262">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="76644-263">Spécifie le pool de ressources réseau à partir duquel une connexion sera allouée au système de réplication de test lors de sa création.</span><span class="sxs-lookup"><span data-stu-id="76644-263">Specifies the network resource pool from which a connection will be allocated to the test replica system when it is created.</span></span>

</dd> <dt>

<span data-ttu-id="76644-264">**TestReplicaSwitchName**</span><span class="sxs-lookup"><span data-stu-id="76644-264">**TestReplicaSwitchName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-265">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76644-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76644-266">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="76644-266">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="76644-267">Spécifie le nom complet du commutateur réseau virtuel auquel une connexion sera allouée pour le système de réplication de test lors de sa création.</span><span class="sxs-lookup"><span data-stu-id="76644-267">Specifies the display name of the virtual network switch to which a connection will be allocated for the test replica system when it is created.</span></span>

</dd> <dt>

<span data-ttu-id="76644-268">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="76644-268">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-269">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="76644-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="76644-270">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76644-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76644-271">Nombre total de ports dans le commutateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="76644-271">The total number of ports in the virtual switch.</span></span> <span data-ttu-id="76644-272">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="76644-272">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="76644-273">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="76644-273">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-274">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76644-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76644-275">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76644-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76644-276">Spécifie l’unité de mesure pour la propriété **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="76644-276">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="76644-277">La valeur de cette propriété doit être une valeur légale du qualificateur d’unités de programmation, tel que défini dans l’annexe C. 1 de DSP0004 V 2.5 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="76644-277">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="76644-278">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="76644-278">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="76644-279">**Poids**</span><span class="sxs-lookup"><span data-stu-id="76644-279">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76644-280">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="76644-280">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="76644-281">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76644-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76644-282">Entier qui définit le poids de chaque commutateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="76644-282">An integer that defines the weight for each virtual switch.</span></span> <span data-ttu-id="76644-283">Cette propriété est héritée de la [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="76644-283">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="76644-284">Plage : 0 1000</span><span class="sxs-lookup"><span data-stu-id="76644-284">Range: 0 1000</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="76644-285">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76644-285">Requirements</span></span>



| <span data-ttu-id="76644-286">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76644-286">Requirement</span></span> | <span data-ttu-id="76644-287">Valeur</span><span class="sxs-lookup"><span data-stu-id="76644-287">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76644-288">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76644-288">Minimum supported client</span></span><br/> | <span data-ttu-id="76644-289">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76644-289">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="76644-290">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76644-290">Minimum supported server</span></span><br/> | <span data-ttu-id="76644-291">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76644-291">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="76644-292">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="76644-292">Namespace</span></span><br/>                | <span data-ttu-id="76644-293">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="76644-293">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="76644-294">MOF</span><span class="sxs-lookup"><span data-stu-id="76644-294">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76644-295"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="76644-295"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="76644-296">DLL</span><span class="sxs-lookup"><span data-stu-id="76644-296">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76644-297"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="76644-297"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

