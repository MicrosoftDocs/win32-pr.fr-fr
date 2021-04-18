---
description: Représente l’état configuré du composant d’interface de service invité.
ms.assetid: 82B58459-9819-4F51-BEE5-AB57E444CF55
title: Classe Msvm_GuestServiceInterfaceComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponentSettingData
- Msvm_GuestServiceInterfaceComponentSettingData.ElementName
- Msvm_GuestServiceInterfaceComponentSettingData.InstanceID
- Msvm_GuestServiceInterfaceComponentSettingData.ResourceType
- Msvm_GuestServiceInterfaceComponentSettingData.OtherResourceType
- Msvm_GuestServiceInterfaceComponentSettingData.ResourceSubType
- Msvm_GuestServiceInterfaceComponentSettingData.PoolID
- Msvm_GuestServiceInterfaceComponentSettingData.ConsumerVisibility
- Msvm_GuestServiceInterfaceComponentSettingData.HostResource
- Msvm_GuestServiceInterfaceComponentSettingData.AllocationUnits
- Msvm_GuestServiceInterfaceComponentSettingData.VirtualQuantity
- Msvm_GuestServiceInterfaceComponentSettingData.Reservation
- Msvm_GuestServiceInterfaceComponentSettingData.Limit
- Msvm_GuestServiceInterfaceComponentSettingData.Weight
- Msvm_GuestServiceInterfaceComponentSettingData.AutomaticAllocation
- Msvm_GuestServiceInterfaceComponentSettingData.AutomaticDeallocation
- Msvm_GuestServiceInterfaceComponentSettingData.Parent
- Msvm_GuestServiceInterfaceComponentSettingData.Connection
- Msvm_GuestServiceInterfaceComponentSettingData.Address
- Msvm_GuestServiceInterfaceComponentSettingData.MappingBehavior
- Msvm_GuestServiceInterfaceComponentSettingData.EnabledState
- Msvm_GuestServiceInterfaceComponentSettingData.DefaultEnabledStatePolicy
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ada39e4428040cf7e6732232ce789f7d837c9c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513185"
---
# <a name="msvm_guestserviceinterfacecomponentsettingdata-class"></a><span data-ttu-id="5fb57-103">MSVM \_ GuestServiceInterfaceComponentSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="5fb57-103">Msvm\_GuestServiceInterfaceComponentSettingData class</span></span>

<span data-ttu-id="5fb57-104">Représente l’état configuré du composant d’interface de service invité.</span><span class="sxs-lookup"><span data-stu-id="5fb57-104">Represents the configured state of the guest service interface component.</span></span> <span data-ttu-id="5fb57-105">Cette classe dérive de la classe [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) .</span><span class="sxs-lookup"><span data-stu-id="5fb57-105">This class derives from the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class.</span></span>

<span data-ttu-id="5fb57-106">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="5fb57-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fb57-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5fb57-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  ElementName;
  string  InstanceID;
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
  uint16  EnabledState = 3;
  uint16  DefaultEnabledStatePolicy = 2;
};
```

## <a name="members"></a><span data-ttu-id="5fb57-108">Membres</span><span class="sxs-lookup"><span data-stu-id="5fb57-108">Members</span></span>

<span data-ttu-id="5fb57-109">La classe **MSVM \_ GuestServiceInterfaceComponentSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5fb57-109">The **Msvm\_GuestServiceInterfaceComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="5fb57-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5fb57-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5fb57-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5fb57-111">Properties</span></span>

<span data-ttu-id="5fb57-112">La classe **MSVM \_ GuestServiceInterfaceComponentSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="5fb57-112">The **Msvm\_GuestServiceInterfaceComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5fb57-113">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="5fb57-113">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fb57-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5fb57-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5fb57-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5fb57-116">Adresse de la ressource.</span><span class="sxs-lookup"><span data-stu-id="5fb57-116">The address of the resource.</span></span> <span data-ttu-id="5fb57-117">Par exemple, l’adresse MAC d’un port Ethernet.</span><span class="sxs-lookup"><span data-stu-id="5fb57-117">For example, the MAC address of a Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="5fb57-118">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="5fb57-118">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fb57-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5fb57-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5fb57-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5fb57-121">Cette propriété spécifie les unités d’allocation utilisées par la réservation et les propriétés de la limite.</span><span class="sxs-lookup"><span data-stu-id="5fb57-121">This property specifies the units of allocation used by the Reservation and Limit properties.</span></span> <span data-ttu-id="5fb57-122">Par exemple, si ResourceType = Processor, AllocationUnits peut avoir la valeur MHz.</span><span class="sxs-lookup"><span data-stu-id="5fb57-122">For example, when ResourceType=Processor, AllocationUnits may be set to MHz.</span></span> <span data-ttu-id="5fb57-123">Si ResourceType = Memory, AllocationUnits peut avoir la valeur MB</span><span class="sxs-lookup"><span data-stu-id="5fb57-123">When ResourceType=Memory, AllocationUnits may be set to MB</span></span>

</dd> <dt>

<span data-ttu-id="5fb57-124">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="5fb57-124">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fb57-125">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5fb57-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5fb57-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5fb57-127">Cette propriété spécifie si la ressource sera automatiquement allouée.</span><span class="sxs-lookup"><span data-stu-id="5fb57-127">This property specifies if the resource will be automatically allocated.</span></span> <span data-ttu-id="5fb57-128">Par exemple, si la valeur est true, lorsque le système d’ordinateur virtuel consommatrice est sous tension, cette ressource sera allouée.</span><span class="sxs-lookup"><span data-stu-id="5fb57-128">For example when set to true, when the consuming virtual computer system is powered on, this resource would be allocated.</span></span> <span data-ttu-id="5fb57-129">La valeur false indique que la ressource doit être allouée de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="5fb57-129">A value of false indicates the resource must be explicitly allocated.</span></span> <span data-ttu-id="5fb57-130">Par exemple, le paramètre peut représenter un support amovible (à partir d’un CD-ROM ou d’une disquette) où le support n’est pas présent.</span><span class="sxs-lookup"><span data-stu-id="5fb57-130">For example, the setting may represent removable media (that is, cdrom or floppy) where at power on time, the media is not present.</span></span> <span data-ttu-id="5fb57-131">Une opération explicite est requise pour allouer la ressource.</span><span class="sxs-lookup"><span data-stu-id="5fb57-131">An explicit operation is required to allocate the resource.</span></span>

</dd> <dt>

<span data-ttu-id="5fb57-132">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="5fb57-132">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fb57-133">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5fb57-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5fb57-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5fb57-135">Cette propriété spécifie si la ressource sera automatiquement désallouée.</span><span class="sxs-lookup"><span data-stu-id="5fb57-135">This property specifies if the resource will be automatically deallocated.</span></span> <span data-ttu-id="5fb57-136">Par exemple, si la valeur est true, lorsque le système d’ordinateur virtuel consommatrice est hors tension, cette ressource est désallouée.</span><span class="sxs-lookup"><span data-stu-id="5fb57-136">For example, when set to true, when the consuming virtual computer system is powered off, this resource would be deallocated.</span></span> <span data-ttu-id="5fb57-137">Quand la valeur est false, la ressource reste allouée et doit être désallouée de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="5fb57-137">When set to false, the resource will remain allocated and must be explicitly deallocated.</span></span>

</dd> <dt>

<span data-ttu-id="5fb57-138">**Connection**</span><span class="sxs-lookup"><span data-stu-id="5fb57-138">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fb57-139">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="5fb57-139">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5fb57-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5fb57-141">Élément auquel cette ressource est connectée.</span><span class="sxs-lookup"><span data-stu-id="5fb57-141">The thing to which this resource is connected.</span></span> <span data-ttu-id="5fb57-142">Par exemple, un réseau nommé ou un port commuté.</span><span class="sxs-lookup"><span data-stu-id="5fb57-142">For example, a named network or switch port.</span></span>

</dd> <dt>

<span data-ttu-id="5fb57-143">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="5fb57-143">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fb57-144">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5fb57-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5fb57-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5fb57-146">Décrit la visibilité des consommateurs sur la ressource allouée.</span><span class="sxs-lookup"><span data-stu-id="5fb57-146">Describes the consumers visibility to the allocated resource.</span></span>



| <span data-ttu-id="5fb57-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="5fb57-147">Value</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="5fb57-148">Signification</span><span class="sxs-lookup"><span data-stu-id="5fb57-148">Meaning</span></span>                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="5fb57-149"><dt>**Inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5fb57-149"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                            | <span data-ttu-id="5fb57-150">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="5fb57-150">Unknown.</span></span><br/>                                                                                                                                                                                                                                         |
| <span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span><dl> <span data-ttu-id="5fb57-151"><dt>**Passe-à-**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5fb57-151"><dt>**Passed-Through**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="5fb57-152">La ressource hôte ou sous-jacente est utilisée et transmise au consommateur, éventuellement à l’aide du partitionnement.</span><span class="sxs-lookup"><span data-stu-id="5fb57-152">The underlying or host resource is utilized and passed through to the consumer, possibly using partitioning.</span></span> <span data-ttu-id="5fb57-153">Au moins un élément doit être présent dans la propriété DeviceID.</span><span class="sxs-lookup"><span data-stu-id="5fb57-153">At least one item shall be present in the DeviceID property.</span></span><br/>                                                                        |
| <span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span><dl> <span data-ttu-id="5fb57-154"><dt>**Virtualisé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="5fb57-154"><dt>**Virtualized**</dt> <dt>3</dt></span></span> </dl>                            | <span data-ttu-id="5fb57-155">La ressource est virtualisée et peut ne pas être directement mappée à une ressource hôte/sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="5fb57-155">The resource is virtualized and may not map directly to an underlying/host resource.</span></span> <span data-ttu-id="5fb57-156">Certaines implémentations peuvent prendre en charge une attribution spécifique pour les ressources virtualisées, auquel cas la ou les ressources hôtes sont exposées à l’aide de la propriété DeviceID.</span><span class="sxs-lookup"><span data-stu-id="5fb57-156">Some implementations may support specific assignment for virtualized resources, in which case the host resource(s) are exposed using the DeviceID property.</span></span><br/> |
| <span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span><dl> <span data-ttu-id="5fb57-157"><dt>**Non représenté**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="5fb57-157"><dt>**Not represented**</dt> <dt>4</dt></span></span> </dl>            | <span data-ttu-id="5fb57-158">Une représentation de la ressource n’existe pas dans le contexte du consommateur de ressources.</span><span class="sxs-lookup"><span data-stu-id="5fb57-158">A representation of the resource does not exist within the context of the resource consumer.</span></span><br/>                                                                                                                                                     |
| <span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="5fb57-159"><dt>**DMTF réservé**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="5fb57-159"><dt>**DMTF reserved**</dt> <dt>..</dt></span></span> </dl>                   |                                                                                                                                                                                                                                                             |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="5fb57-160">32767 <dt>**réservé au fournisseur**</dt> <dt>.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="5fb57-160"><dt>**Vendor Reserved**</dt> <dt>32767..65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="5fb57-161">**DefaultEnabledStatePolicy**</span><span class="sxs-lookup"><span data-stu-id="5fb57-161">**DefaultEnabledStatePolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fb57-162">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5fb57-162">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5fb57-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5fb57-164">États activés et désactivés des services de communication invité par défaut.</span><span class="sxs-lookup"><span data-stu-id="5fb57-164">The enabled and disabled states of guest communication services by default.</span></span>

<span data-ttu-id="5fb57-165">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="5fb57-165">This is a read-only property, but it can be changed using the [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="5fb57-166">Ajouté dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5fb57-166">Added in Windows 10.</span></span>

 

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5fb57-167">**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="5fb57-167">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5fb57-168">**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="5fb57-168">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5fb57-169">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5fb57-169">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fb57-170">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5fb57-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5fb57-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5fb57-172">Nom complet de cette instance de SettingData.</span><span class="sxs-lookup"><span data-stu-id="5fb57-172">The display name for this instance of SettingData.</span></span> <span data-ttu-id="5fb57-173">En outre, le nom complet peut être utilisé comme propriété d’index pour une recherche ou une requête.</span><span class="sxs-lookup"><span data-stu-id="5fb57-173">In addition, the display name can be used as an index property for a search or query.</span></span> <span data-ttu-id="5fb57-174">(Remarque : il n’est pas nécessaire que le nom soit unique au sein d’un espace de noms.)</span><span class="sxs-lookup"><span data-stu-id="5fb57-174">(Note: The name does not have to be unique within a namespace.)</span></span>

</dd> <dt>

<span data-ttu-id="5fb57-175">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="5fb57-175">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fb57-176">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5fb57-176">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5fb57-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5fb57-178">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="5fb57-178">The enabled and disabled states of an element.</span></span>

<span data-ttu-id="5fb57-179">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) (ou [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) dans Windows 10 ou version ultérieure) de la classe [**\_ VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="5fb57-179">This is a read-only property, but it can be changed by using the [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) method (or [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) in Windows 10 or later) of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="5fb57-180">Les valeurs autorisées sont :</span><span class="sxs-lookup"><span data-stu-id="5fb57-180">Valid values are:</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5fb57-181">**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="5fb57-181">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5fb57-182">**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="5fb57-182">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5fb57-183">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="5fb57-183">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fb57-184">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="5fb57-184">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5fb57-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5fb57-186">Cette propriété expose une attribution spécifique à l’hôte ou aux ressources sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="5fb57-186">This property exposes specific assignment to host or underlying resources.</span></span> <span data-ttu-id="5fb57-187">Les instances incorporées doivent contenir uniquement des propriétés de clé et être traitées comme des chemins d’accès d’objet.</span><span class="sxs-lookup"><span data-stu-id="5fb57-187">The embedded instances shall contain only key properties and be treated as Object Paths.</span></span> <span data-ttu-id="5fb57-188">Si la ressource virtuelle peut être planifiée sur un certain nombre de ressources sous-jacentes, cette propriété doit rester **null**.</span><span class="sxs-lookup"><span data-stu-id="5fb57-188">If the virtual resource may be scheduled on a number of underlying resources, this property should remain **NULL**.</span></span> <span data-ttu-id="5fb57-189">Dans ce cas, les associations DeviceAllocatedFromPool ou ResourceAllocationFromPool peuvent être utilisées pour déterminer le pool de ressources hôtes sur lequel cette ressource virtuelle peut être planifiée.</span><span class="sxs-lookup"><span data-stu-id="5fb57-189">In that case, the DeviceAllocatedFromPool or ResourceAllocationFromPool associations may be used to determine the pool of host resources on which this virtual resource may be scheduled.</span></span> <span data-ttu-id="5fb57-190">Si une attribution spécifique est utilisée, toutes les ressources sous-jacentes utilisées par cette ressource virtuelle seront listées dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="5fb57-190">If specific assignment is utilized, all underlying resources used by this virtual resource shall be listed in this array.</span></span> <span data-ttu-id="5fb57-191">En règle générale, le tableau contient un seul élément, mais pour les allocations d’agrégats, telles que plusieurs processeurs, plusieurs ressources hôtes peuvent être spécifiées.</span><span class="sxs-lookup"><span data-stu-id="5fb57-191">Typically, the array will contain one item, however for aggregate allocations, such as multiple processors, multiple host resources may be specified.</span></span>

</dd> <dt>

<span data-ttu-id="5fb57-192">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5fb57-192">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fb57-193">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5fb57-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5fb57-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-195">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="5fb57-195">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5fb57-196">Dans l’étendue de l’espace de noms d’instanciation, InstanceID identifie de façon opaque et unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="5fb57-196">Within the scope of the instantiating Namespace, InstanceID opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="5fb57-197">Pour garantir l’unicité dans l’espace de noms, la valeur d’InstanceID doit être construite à l’aide de l’algorithme « préféré » suivant : *identifiant OrgID*:*LocalID* où *identifiant OrgID* et *LocalID* sont séparés par un signe deux-points ( :), et où *identifiant OrgID* doit inclure un nom de droits d’auteur, de marque déposée ou autre que celui qui est détenu par l’entité commerciale qui crée ou définit l’InstanceId ou qui est un ID inscrit affecté à l’entité métier</span><span class="sxs-lookup"><span data-stu-id="5fb57-197">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm: *OrgID*:*LocalID* Where *OrgID* and *LocalID* are separated by a colon (:), and where *OrgID* must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="5fb57-198">(Cette spécification est semblable à celle de *SchemaName* \_ Structure *className* des noms de classes de schéma.) En outre, pour garantir l’unicité, *identifiant OrgID* ne doit pas contenir de deux-points ( :).</span><span class="sxs-lookup"><span data-stu-id="5fb57-198">(This requirement is similar to the *SchemaName*\_*ClassName* structure of Schema class names.) In addition, to ensure uniqueness, *OrgID* must not contain a colon (:).</span></span> <span data-ttu-id="5fb57-199">Lors de l’utilisation de cet algorithme, le premier signe deux-points devant apparaître dans InstanceID doit apparaître entre *identifiant OrgID* et *LocalID*.</span><span class="sxs-lookup"><span data-stu-id="5fb57-199">When using this algorithm, the first colon to appear in InstanceID must appear between *OrgID* and *LocalID*.</span></span> <span data-ttu-id="5fb57-200">*LocalID* est choisi par l’entité métier et ne doit pas être réutilisé pour identifier les différents éléments sous-jacents (réels).</span><span class="sxs-lookup"><span data-stu-id="5fb57-200">*LocalID* is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="5fb57-201">Si l’algorithme « préféré » ci-dessus n’est pas utilisé, l’entité de définition doit s’assurer que l’InstanceID qui en résulte n’est pas réutilisé dans les InstanceIDs produits par ce ou d’autres fournisseurs pour l’espace de noms de cette instance.</span><span class="sxs-lookup"><span data-stu-id="5fb57-201">If the above "preferred" algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span> <span data-ttu-id="5fb57-202">Pour les instances définies par DMTF, l’algorithme « préféré » doit être utilisé avec le *identifiant OrgID* défini sur CIM.</span><span class="sxs-lookup"><span data-stu-id="5fb57-202">For DMTF-defined instances, the "preferred" algorithm must be used with the *OrgID* set to CIM.</span></span>

</dd> <dt>

<span data-ttu-id="5fb57-203">**Limite**</span><span class="sxs-lookup"><span data-stu-id="5fb57-203">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fb57-204">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5fb57-204">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-205">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5fb57-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5fb57-206">Cette propriété spécifie la limite supérieure ou la quantité maximale de ressources qui seront accordées pour cette allocation.</span><span class="sxs-lookup"><span data-stu-id="5fb57-206">This property specifies the upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="5fb57-207">Par exemple, un système qui prend en charge la pagination de la mémoire peut prendre en charge la définition de la limite d’une allocation de mémoire inférieure à celle du VirtualQuantity, forçant ainsi la pagination à se produire pour cette allocation.</span><span class="sxs-lookup"><span data-stu-id="5fb57-207">For example, a system which supports memory paging may support setting the Limit of a Memory allocation below that of the VirtualQuantity, thus forcing paging to occur for this allocation.</span></span>

</dd> <dt>

<span data-ttu-id="5fb57-208">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="5fb57-208">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fb57-209">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5fb57-209">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-210">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5fb57-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5fb57-211">Spécifie comment cette ressource est mappée aux ressources sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="5fb57-211">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="5fb57-212">Si le tableau HostResource contient des entrées, cette propriété reflète la manière dont la ressource est mappée à ces ressources spécifiques.</span><span class="sxs-lookup"><span data-stu-id="5fb57-212">If the HostResource array contains any entries, this property reflects how the resource maps to those specific resources.</span></span>

<dl> <dt>

<span data-ttu-id="5fb57-213"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="5fb57-213"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-214"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="5fb57-214"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-215"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dédié** (2)</span><span class="sxs-lookup"><span data-stu-id="5fb57-215"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-216"><span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Affinité douce** (3)</span><span class="sxs-lookup"><span data-stu-id="5fb57-216"><span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Soft Affinity** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-217"><span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Affinité matérielle** (4)</span><span class="sxs-lookup"><span data-stu-id="5fb57-217"><span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Hard Affinity** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-218"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="5fb57-218"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-219"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="5fb57-219"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32767..65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5fb57-220">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="5fb57-220">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fb57-221">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5fb57-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5fb57-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5fb57-223">Chaîne qui décrit le type de ressource lorsqu’une valeur bien définie n’est pas disponible et que ResourceType a la valeur « other ».</span><span class="sxs-lookup"><span data-stu-id="5fb57-223">A string that describes the resource type when a well defined value is not available and ResourceType has the value "Other".</span></span>

</dd> <dt>

<span data-ttu-id="5fb57-224">**Parent**</span><span class="sxs-lookup"><span data-stu-id="5fb57-224">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fb57-225">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5fb57-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-226">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5fb57-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5fb57-227">Parent de la ressource.</span><span class="sxs-lookup"><span data-stu-id="5fb57-227">The Parent of the resource.</span></span> <span data-ttu-id="5fb57-228">Par exemple, un contrôleur pour l’allocation actuelle.</span><span class="sxs-lookup"><span data-stu-id="5fb57-228">For example, a controller for the current allocation.</span></span>

</dd> <dt>

<span data-ttu-id="5fb57-229">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="5fb57-229">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fb57-230">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5fb57-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5fb57-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5fb57-232">Cette propriété spécifie le ResourcePool à partir duquel la ressource est actuellement allouée, ou à partir de quelle ResourcePool la ressource sera allouée lorsque l’allocation aura lieu.</span><span class="sxs-lookup"><span data-stu-id="5fb57-232">This property specifies which ResourcePool the resource is currently allocated from, or which ResourcePool the resource will be allocated from when the allocation occurs.</span></span>

</dd> <dt>

<span data-ttu-id="5fb57-233">**Réservation**</span><span class="sxs-lookup"><span data-stu-id="5fb57-233">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fb57-234">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5fb57-234">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-235">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5fb57-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5fb57-236">Cette propriété spécifie la quantité de ressources dont la disponibilité est garantie pour cette allocation.</span><span class="sxs-lookup"><span data-stu-id="5fb57-236">This property specifies the amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="5fb57-237">Sur un système qui prend en charge le surengagement de ressources, cette valeur est généralement utilisée pour le contrôle d’admission afin d’éviter qu’une allocation d’allocation soit acceptée, empêchant ainsi l’épuisement des ressources.</span><span class="sxs-lookup"><span data-stu-id="5fb57-237">On system which support over-commitment of resources, this value is typically used for admission control to prevent an an allocation from being accepted thus preventing resource depletion.</span></span>

</dd> <dt>

<span data-ttu-id="5fb57-238">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="5fb57-238">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fb57-239">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5fb57-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-240">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5fb57-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5fb57-241">Chaîne décrivant un sous-type spécifique à l’implémentation de cette ressource.</span><span class="sxs-lookup"><span data-stu-id="5fb57-241">A string describing an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="5fb57-242">Par exemple, cela peut être utilisé pour distinguer différents modèles du même type de ressource.</span><span class="sxs-lookup"><span data-stu-id="5fb57-242">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="5fb57-243">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="5fb57-243">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fb57-244">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5fb57-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-245">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5fb57-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5fb57-246">Type de ressource représenté par ce paramètre d’allocation.</span><span class="sxs-lookup"><span data-stu-id="5fb57-246">The type of resource this allocation setting represents.</span></span>

<dl> <dt>

<span data-ttu-id="5fb57-247"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="5fb57-247"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-248"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Système informatique** (2)</span><span class="sxs-lookup"><span data-stu-id="5fb57-248"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-249"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processeur** (3)</span><span class="sxs-lookup"><span data-stu-id="5fb57-249"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-250"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Mémoire** (4)</span><span class="sxs-lookup"><span data-stu-id="5fb57-250"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-251"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Contrôleur IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="5fb57-251"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-252"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI parallèle** (6)</span><span class="sxs-lookup"><span data-stu-id="5fb57-252"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-253"><span id="FC_HBA"></span><span id="fc_hba"></span>**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="5fb57-253"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-254"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="5fb57-254"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-255"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="5fb57-255"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-256"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Carte Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="5fb57-256"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-257"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Autre carte réseau** (11)</span><span class="sxs-lookup"><span data-stu-id="5fb57-257"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-258"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Emplacement d’e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="5fb57-258"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-259"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Périphérique d’e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="5fb57-259"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-260"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Lecteur de disquette** (14)</span><span class="sxs-lookup"><span data-stu-id="5fb57-260"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-261"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Lecteur de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="5fb57-261"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-262"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Lecteur de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="5fb57-262"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-263"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Port série** (17)</span><span class="sxs-lookup"><span data-stu-id="5fb57-263"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (17)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-264"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Port parallèle** (18)</span><span class="sxs-lookup"><span data-stu-id="5fb57-264"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (18)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-265"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Contrôleur USB** (19)</span><span class="sxs-lookup"><span data-stu-id="5fb57-265"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (19)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-266"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Contrôleur Graphics** (20)</span><span class="sxs-lookup"><span data-stu-id="5fb57-266"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (20)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-267"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extension de stockage** (21)</span><span class="sxs-lookup"><span data-stu-id="5fb57-267"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (21)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-268"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disque** (22)</span><span class="sxs-lookup"><span data-stu-id="5fb57-268"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disk** (22)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-269"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Bande** (23)</span><span class="sxs-lookup"><span data-stu-id="5fb57-269"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Tape** (23)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-270"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Autre dispositif de stockage** (24)</span><span class="sxs-lookup"><span data-stu-id="5fb57-270"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other storage device** (24)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-271"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Contrôleur FireWire** (25)</span><span class="sxs-lookup"><span data-stu-id="5fb57-271"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-272"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unité partitionnée** (26)</span><span class="sxs-lookup"><span data-stu-id="5fb57-272"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-273"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unité partitionnée de base** (27)</span><span class="sxs-lookup"><span data-stu-id="5fb57-273"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-274"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Alimentation (28** )</span><span class="sxs-lookup"><span data-stu-id="5fb57-274"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-275"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Appareil de refroidissement** (29)</span><span class="sxs-lookup"><span data-stu-id="5fb57-275"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-276"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="5fb57-276"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-277"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="5fb57-277"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32767..65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5fb57-278">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="5fb57-278">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fb57-279">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5fb57-279">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-280">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5fb57-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5fb57-281">Cette propriété spécifie la quantité de ressources présentées au consommateur.</span><span class="sxs-lookup"><span data-stu-id="5fb57-281">This property specifies the quantity of resources presented to the consumer.</span></span> <span data-ttu-id="5fb57-282">Par exemple, lorsque ResourceType = Processor, cette propriété reflète le nombre de processeurs discrets présentés au système d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="5fb57-282">For example, when ResourceType=Processor, this property would reflect the number of discrete Processors presented to the virtual computer system.</span></span> <span data-ttu-id="5fb57-283">Si ResourceType = Memory, cette propriété peut refléter le nombre de Mo signalés au système de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="5fb57-283">When ResourceType=Memory, this property could reflect the number of MB reported to the virtual computer system.</span></span>

</dd> <dt>

<span data-ttu-id="5fb57-284">**Poids**</span><span class="sxs-lookup"><span data-stu-id="5fb57-284">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fb57-285">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5fb57-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fb57-286">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5fb57-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5fb57-287">Cette propriété spécifie une priorité relative pour cette allocation par rapport à d’autres allocations à partir du même ResourcePool.</span><span class="sxs-lookup"><span data-stu-id="5fb57-287">This property specifies a relative priority for this allocation in relation to other allocations from the same ResourcePool.</span></span> <span data-ttu-id="5fb57-288">Cette propriété n’a aucune unité de mesure et est uniquement pertinente par rapport à d’autres allocations en concurrence pour les mêmes ressources hôte.</span><span class="sxs-lookup"><span data-stu-id="5fb57-288">This property has no unit of measure, and is only relevant when compared to other allocations competing for the same host resources.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5fb57-289">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5fb57-289">Requirements</span></span>



| <span data-ttu-id="5fb57-290">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5fb57-290">Requirement</span></span> | <span data-ttu-id="5fb57-291">Valeur</span><span class="sxs-lookup"><span data-stu-id="5fb57-291">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fb57-292">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5fb57-292">Minimum supported client</span></span><br/> | <span data-ttu-id="5fb57-293">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5fb57-293">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="5fb57-294">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5fb57-294">Minimum supported server</span></span><br/> | <span data-ttu-id="5fb57-295">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5fb57-295">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5fb57-296">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5fb57-296">Namespace</span></span><br/>                | <span data-ttu-id="5fb57-297">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="5fb57-297">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5fb57-298">MOF</span><span class="sxs-lookup"><span data-stu-id="5fb57-298">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5fb57-299"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5fb57-299"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5fb57-300">DLL</span><span class="sxs-lookup"><span data-stu-id="5fb57-300">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fb57-301"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5fb57-301"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5fb57-302">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fb57-302">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fb57-303">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="5fb57-303">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="5fb57-304">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="5fb57-304">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

