---
description: Représente l’état de la ressource de basculement de la bande passante.
ms.assetid: 9aa3e57e-9452-4c60-a052-83ae35b3607c
title: Classe Msvm_EthernetSwitchBandwidthData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchBandwidthData
- Msvm_EthernetSwitchBandwidthData.InstanceID
- Msvm_EthernetSwitchBandwidthData.Caption
- Msvm_EthernetSwitchBandwidthData.Description
- Msvm_EthernetSwitchBandwidthData.ElementName
- Msvm_EthernetSwitchBandwidthData.SystemCreationClassName
- Msvm_EthernetSwitchBandwidthData.SystemName
- Msvm_EthernetSwitchBandwidthData.CreationClassName
- Msvm_EthernetSwitchBandwidthData.Name
- Msvm_EthernetSwitchBandwidthData.Capacity
- Msvm_EthernetSwitchBandwidthData.Reservation
- Msvm_EthernetSwitchBandwidthData.DefaultFlowReservationPercentage
- Msvm_EthernetSwitchBandwidthData.DefaultFlowReservation
- Msvm_EthernetSwitchBandwidthData.DefaultFlowWeight
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d238b8ddc40506a3eae8a6c7c089de2ebd87db5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516645"
---
# <a name="msvm_ethernetswitchbandwidthdata-class"></a><span data-ttu-id="df7f6-103">MSVM \_ EthernetSwitchBandwidthData, classe</span><span class="sxs-lookup"><span data-stu-id="df7f6-103">Msvm\_EthernetSwitchBandwidthData class</span></span>

<span data-ttu-id="df7f6-104">Représente l’état de la ressource de basculement de la bande passante.</span><span class="sxs-lookup"><span data-stu-id="df7f6-104">Represents the switch bandwidth resource status.</span></span>

<span data-ttu-id="df7f6-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="df7f6-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="df7f6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df7f6-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("8F425906-034D-42AB-BD16-EDB31CEC55EF"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Bandwidth data"), AMENDMENT]
class Msvm_EthernetSwitchBandwidthData : Msvm_EthernetSwitchData
{
  string InstanceID;
  string Caption = "Ethernet Switch Bandwidth data";
  string Description = "Represents the switch bandwidth resource status.";
  string ElementName = "Ethernet Switch Bandwidth data";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string CreationClassName = "Msvm_EthernetSwitchBandwidthData";
  string Name;
  uint64 Capacity = 100000000;
  uint64 Reservation = 100000000;
  uint32 DefaultFlowReservationPercentage = 10;
  uint64 DefaultFlowReservation = 100000000;
  uint64 DefaultFlowWeight = 0;
};
```

## <a name="members"></a><span data-ttu-id="df7f6-107">Membres</span><span class="sxs-lookup"><span data-stu-id="df7f6-107">Members</span></span>

<span data-ttu-id="df7f6-108">La classe **MSVM \_ EthernetSwitchBandwidthData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="df7f6-108">The **Msvm\_EthernetSwitchBandwidthData** class has these types of members:</span></span>

-   [<span data-ttu-id="df7f6-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="df7f6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="df7f6-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="df7f6-110">Properties</span></span>

<span data-ttu-id="df7f6-111">La classe **MSVM \_ EthernetSwitchBandwidthData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="df7f6-111">The **Msvm\_EthernetSwitchBandwidthData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="df7f6-112">**Capacité**</span><span class="sxs-lookup"><span data-stu-id="df7f6-112">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df7f6-113">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="df7f6-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="df7f6-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df7f6-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df7f6-115">Qualificateurs : **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="df7f6-115">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="df7f6-116">Bande passante maximale disponible sur le commutateur.</span><span class="sxs-lookup"><span data-stu-id="df7f6-116">The maximum bandwidth available on the switch.</span></span>

</dd> <dt>

<span data-ttu-id="df7f6-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="df7f6-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df7f6-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="df7f6-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df7f6-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df7f6-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df7f6-120">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="df7f6-120">A short description of the object.</span></span> <span data-ttu-id="df7f6-121">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="df7f6-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="df7f6-122">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="df7f6-122">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df7f6-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="df7f6-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df7f6-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df7f6-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df7f6-125">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="df7f6-125">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="df7f6-126">Nom de la classe ou de la sous-classe utilisée dans la création de cette instance.</span><span class="sxs-lookup"><span data-stu-id="df7f6-126">The name of the class or subclass used in the creation of this instance.</span></span>

</dd> <dt>

<span data-ttu-id="df7f6-127">**DefaultFlowReservation**</span><span class="sxs-lookup"><span data-stu-id="df7f6-127">**DefaultFlowReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df7f6-128">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="df7f6-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="df7f6-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df7f6-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df7f6-130">Qualificateurs : **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="df7f6-130">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="df7f6-131">Bande passante absolue actuelle réservée sur le commutateur pour le workflow par défaut.</span><span class="sxs-lookup"><span data-stu-id="df7f6-131">The current absolute bandwidth reserved on the switch for default flow.</span></span>

</dd> <dt>

<span data-ttu-id="df7f6-132">**DefaultFlowReservationPercentage**</span><span class="sxs-lookup"><span data-stu-id="df7f6-132">**DefaultFlowReservationPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df7f6-133">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="df7f6-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df7f6-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df7f6-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df7f6-135">Qualificateurs : **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="df7f6-135">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="df7f6-136">Pourcentage actuel de la bande passante réservée sur le commutateur pour le workflow par défaut.</span><span class="sxs-lookup"><span data-stu-id="df7f6-136">The current percentage of bandwidth reserved on the switch for default flow.</span></span>

</dd> <dt>

<span data-ttu-id="df7f6-137">**DefaultFlowWeight**</span><span class="sxs-lookup"><span data-stu-id="df7f6-137">**DefaultFlowWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df7f6-138">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="df7f6-138">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="df7f6-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df7f6-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df7f6-140">Qualificateurs : **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="df7f6-140">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="df7f6-141">Poids actuel du déroulement par défaut sur le commutateur.</span><span class="sxs-lookup"><span data-stu-id="df7f6-141">The current weight for the default flow on the switch.</span></span>

</dd> <dt>

<span data-ttu-id="df7f6-142">**Description**</span><span class="sxs-lookup"><span data-stu-id="df7f6-142">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df7f6-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="df7f6-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df7f6-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df7f6-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df7f6-145">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="df7f6-145">A description of the object.</span></span> <span data-ttu-id="df7f6-146">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="df7f6-146">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="df7f6-147">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="df7f6-147">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df7f6-148">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="df7f6-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df7f6-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df7f6-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df7f6-150">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="df7f6-150">A display name for the object.</span></span> <span data-ttu-id="df7f6-151">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="df7f6-151">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="df7f6-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="df7f6-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df7f6-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="df7f6-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df7f6-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df7f6-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df7f6-155">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="df7f6-155">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="df7f6-156">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="df7f6-156">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="df7f6-157">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="df7f6-157">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="df7f6-158">**Nom**</span><span class="sxs-lookup"><span data-stu-id="df7f6-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df7f6-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="df7f6-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df7f6-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df7f6-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df7f6-161">Qualificateurs : **clé**, **remplacement**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="df7f6-161">Qualifiers: **Key**, **Override**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="df7f6-162">Nom unique de la ressource.</span><span class="sxs-lookup"><span data-stu-id="df7f6-162">The unique name of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="df7f6-163">**Réservation**</span><span class="sxs-lookup"><span data-stu-id="df7f6-163">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df7f6-164">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="df7f6-164">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="df7f6-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df7f6-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df7f6-166">Qualificateurs : **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="df7f6-166">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="df7f6-167">Bande passante actuelle réservée sur le commutateur.</span><span class="sxs-lookup"><span data-stu-id="df7f6-167">The current bandwidth reserved on the switch.</span></span>

</dd> <dt>

<span data-ttu-id="df7f6-168">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="df7f6-168">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df7f6-169">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="df7f6-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df7f6-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df7f6-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df7f6-171">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="df7f6-171">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="df7f6-172">Nom de la classe de création du système d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="df7f6-172">The hosting system's creation class name.</span></span> <span data-ttu-id="df7f6-173">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="df7f6-173">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="df7f6-174">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="df7f6-174">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df7f6-175">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="df7f6-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df7f6-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df7f6-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df7f6-177">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="df7f6-177">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="df7f6-178">Nom du commutateur virtuel auquel l’instance de ressource associée est liée.</span><span class="sxs-lookup"><span data-stu-id="df7f6-178">The name of the virtual switch to which the associated resource instance is bound.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="df7f6-179">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df7f6-179">Requirements</span></span>



| <span data-ttu-id="df7f6-180">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df7f6-180">Requirement</span></span> | <span data-ttu-id="df7f6-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="df7f6-181">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df7f6-182">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df7f6-182">Minimum supported client</span></span><br/> | <span data-ttu-id="df7f6-183">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df7f6-183">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="df7f6-184">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df7f6-184">Minimum supported server</span></span><br/> | <span data-ttu-id="df7f6-185">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df7f6-185">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="df7f6-186">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="df7f6-186">Namespace</span></span><br/>                | <span data-ttu-id="df7f6-187">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="df7f6-187">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="df7f6-188">MOF</span><span class="sxs-lookup"><span data-stu-id="df7f6-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df7f6-189"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="df7f6-189"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="df7f6-190">DLL</span><span class="sxs-lookup"><span data-stu-id="df7f6-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df7f6-191"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="df7f6-191"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

