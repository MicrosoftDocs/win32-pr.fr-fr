---
description: Représente les données d’état de la fonctionnalité de bande passante du port.
ms.assetid: 1f7be0dd-3d2f-49ef-aff0-cb162389194a
title: Classe Msvm_EthernetSwitchPortBandwidthData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortBandwidthData
- Msvm_EthernetSwitchPortBandwidthData.InstanceID
- Msvm_EthernetSwitchPortBandwidthData.Caption
- Msvm_EthernetSwitchPortBandwidthData.Description
- Msvm_EthernetSwitchPortBandwidthData.ElementName
- Msvm_EthernetSwitchPortBandwidthData.SystemCreationClassName
- Msvm_EthernetSwitchPortBandwidthData.SystemName
- Msvm_EthernetSwitchPortBandwidthData.DeviceCreationClassName
- Msvm_EthernetSwitchPortBandwidthData.DeviceID
- Msvm_EthernetSwitchPortBandwidthData.CreationClassName
- Msvm_EthernetSwitchPortBandwidthData.Name
- Msvm_EthernetSwitchPortBandwidthData.CurrentBandwidthReservationPercentage
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 55e8ad735d712bdd388e42b1f4174ee1a78af184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534360"
---
# <a name="msvm_ethernetswitchportbandwidthdata-class"></a><span data-ttu-id="b2260-103">MSVM \_ EthernetSwitchPortBandwidthData, classe</span><span class="sxs-lookup"><span data-stu-id="b2260-103">Msvm\_EthernetSwitchPortBandwidthData class</span></span>

<span data-ttu-id="b2260-104">Représente les données d’état de la fonctionnalité de bande passante du port.</span><span class="sxs-lookup"><span data-stu-id="b2260-104">Represents the port bandwidth feature status data.</span></span>

<span data-ttu-id="b2260-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b2260-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2260-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2260-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("24AD3CE1-69BD-4978-B2AC-DAAD389D699C"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Bandwidth Feature Status"), AMENDMENT]
class Msvm_EthernetSwitchPortBandwidthData : Msvm_EthernetPortData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port Bandwidth Feature Status";
  string Description = "Represents the port bandwidth feature status data.";
  string ElementName = "Ethernet Switch Port Bandwidth Feature Status";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string DeviceCreationClassName = "Msvm_EthernetSwitchPort";
  string DeviceID;
  string CreationClassName = "Msvm_EthernetSwitchPortBandwidthData";
  string Name;
  uint32 CurrentBandwidthReservationPercentage = 0;
};
```

## <a name="members"></a><span data-ttu-id="b2260-107">Membres</span><span class="sxs-lookup"><span data-stu-id="b2260-107">Members</span></span>

<span data-ttu-id="b2260-108">La classe **MSVM \_ EthernetSwitchPortBandwidthData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b2260-108">The **Msvm\_EthernetSwitchPortBandwidthData** class has these types of members:</span></span>

-   [<span data-ttu-id="b2260-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b2260-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b2260-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b2260-110">Properties</span></span>

<span data-ttu-id="b2260-111">La classe **MSVM \_ EthernetSwitchPortBandwidthData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b2260-111">The **Msvm\_EthernetSwitchPortBandwidthData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b2260-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b2260-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2260-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b2260-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2260-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2260-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2260-115">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b2260-115">A short description of the object.</span></span> <span data-ttu-id="b2260-116">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « état de la fonctionnalité de bande passante du port commuté Ethernet ».</span><span class="sxs-lookup"><span data-stu-id="b2260-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Bandwidth Feature Status".</span></span>

</dd> <dt>

<span data-ttu-id="b2260-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b2260-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2260-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b2260-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2260-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2260-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2260-120">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="b2260-120">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="b2260-121">Nom de la sous-classe utilisée lors de la création de cette instance de données de port.</span><span class="sxs-lookup"><span data-stu-id="b2260-121">The name of the subclass used in the creation of this port data instance.</span></span> <span data-ttu-id="b2260-122">Cette propriété est héritée de [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md)et elle est toujours définie sur « MSVM \_ EthernetSwitchPortBandwidthData ».</span><span class="sxs-lookup"><span data-stu-id="b2260-122">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_EthernetSwitchPortBandwidthData".</span></span>

</dd> <dt>

<span data-ttu-id="b2260-123">**CurrentBandwidthReservationPercentage**</span><span class="sxs-lookup"><span data-stu-id="b2260-123">**CurrentBandwidthReservationPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2260-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b2260-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2260-125">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b2260-125">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b2260-126">Qualificateurs : **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="b2260-126">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="b2260-127">Pourcentage actuel de la bande passante réservée pour ce port.</span><span class="sxs-lookup"><span data-stu-id="b2260-127">The current percentage of bandwidth reserved for this port.</span></span>

</dd> <dt>

<span data-ttu-id="b2260-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="b2260-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2260-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b2260-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2260-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2260-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2260-131">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="b2260-131">A description of the object.</span></span> <span data-ttu-id="b2260-132">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et elle est toujours définie sur « représente les données d’état de la fonctionnalité de bande passante du port. ».</span><span class="sxs-lookup"><span data-stu-id="b2260-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port bandwidth feature status data.".</span></span>

</dd> <dt>

<span data-ttu-id="b2260-133">**DeviceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b2260-133">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2260-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b2260-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2260-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2260-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2260-136">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="b2260-136">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="b2260-137">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="b2260-137">The scoping system's creation class name.</span></span> <span data-ttu-id="b2260-138">Cette propriété est héritée de [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md)et elle est toujours définie sur « MSVM \_ EthernetSwitchPort ».</span><span class="sxs-lookup"><span data-stu-id="b2260-138">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_EthernetSwitchPort".</span></span>

</dd> <dt>

<span data-ttu-id="b2260-139">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b2260-139">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2260-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b2260-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2260-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2260-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2260-142">Qualificateurs : **clé**, **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="b2260-142">Qualifiers: **Key**, **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="b2260-143">ID d’appareil du port qui étend cette instance de données de port.</span><span class="sxs-lookup"><span data-stu-id="b2260-143">The Device ID of the port that scopes this port data instance.</span></span> <span data-ttu-id="b2260-144">Cette propriété est héritée de [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="b2260-144">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2260-145">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b2260-145">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2260-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b2260-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2260-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2260-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2260-148">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b2260-148">A display name for the object.</span></span> <span data-ttu-id="b2260-149">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « état de la fonctionnalité de bande passante du port commuté Ethernet ».</span><span class="sxs-lookup"><span data-stu-id="b2260-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Bandwidth Feature Status".</span></span>

</dd> <dt>

<span data-ttu-id="b2260-150">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b2260-150">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2260-151">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b2260-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2260-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2260-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2260-153">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="b2260-153">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b2260-154">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="b2260-154">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b2260-155">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b2260-155">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b2260-156">**Nom**</span><span class="sxs-lookup"><span data-stu-id="b2260-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2260-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b2260-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2260-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2260-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2260-159">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="b2260-159">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="b2260-160">Chaîne qui identifie de façon unique cette instance de données de port dans l’étendue du commutateur et du port.</span><span class="sxs-lookup"><span data-stu-id="b2260-160">A string that uniquely identifies this port data instance within the scope of the switch and port.</span></span> <span data-ttu-id="b2260-161">Cette propriété est héritée de [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="b2260-161">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2260-162">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b2260-162">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2260-163">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b2260-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2260-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2260-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2260-165">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="b2260-165">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="b2260-166">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="b2260-166">The scoping system's creation class name.</span></span> <span data-ttu-id="b2260-167">Cette propriété est héritée de [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md)et elle est toujours définie sur « MSVM \_ VirtualEthernetSwitch ».</span><span class="sxs-lookup"><span data-stu-id="b2260-167">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_VirtualEthernetSwitch".</span></span>

</dd> <dt>

<span data-ttu-id="b2260-168">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b2260-168">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2260-169">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b2260-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2260-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2260-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2260-171">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="b2260-171">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="b2260-172">Nom du commutateur virtuel qui s’étend à cette instance de données de port.</span><span class="sxs-lookup"><span data-stu-id="b2260-172">The name of the virtual switch that scopes this port data instance.</span></span> <span data-ttu-id="b2260-173">Cette propriété est héritée de [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="b2260-173">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2260-174">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2260-174">Requirements</span></span>



| <span data-ttu-id="b2260-175">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2260-175">Requirement</span></span> | <span data-ttu-id="b2260-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2260-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2260-177">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2260-177">Minimum supported client</span></span><br/> | <span data-ttu-id="b2260-178">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b2260-178">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b2260-179">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2260-179">Minimum supported server</span></span><br/> | <span data-ttu-id="b2260-180">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b2260-180">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b2260-181">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b2260-181">Namespace</span></span><br/>                | <span data-ttu-id="b2260-182">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="b2260-182">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b2260-183">MOF</span><span class="sxs-lookup"><span data-stu-id="b2260-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2260-184"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2260-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2260-185">DLL</span><span class="sxs-lookup"><span data-stu-id="b2260-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2260-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b2260-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

