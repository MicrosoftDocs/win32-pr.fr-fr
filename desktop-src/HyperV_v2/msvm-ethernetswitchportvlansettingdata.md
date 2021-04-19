---
description: Représente les données de paramètre de réseau local virtuel (VLAN).
ms.assetid: c3a49021-5256-4751-a5a5-81bf1c6d6e6d
title: Classe Msvm_EthernetSwitchPortVlanSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortVlanSettingData
- Msvm_EthernetSwitchPortVlanSettingData.InstanceID
- Msvm_EthernetSwitchPortVlanSettingData.Caption
- Msvm_EthernetSwitchPortVlanSettingData.Description
- Msvm_EthernetSwitchPortVlanSettingData.ElementName
- Msvm_EthernetSwitchPortVlanSettingData.OperationMode
- Msvm_EthernetSwitchPortVlanSettingData.AccessVlanId
- Msvm_EthernetSwitchPortVlanSettingData.NativeVlanId
- Msvm_EthernetSwitchPortVlanSettingData.PvlanMode
- Msvm_EthernetSwitchPortVlanSettingData.PrimaryVlanId
- Msvm_EthernetSwitchPortVlanSettingData.SecondaryVlanId
- Msvm_EthernetSwitchPortVlanSettingData.PruneVlanIdArray
- Msvm_EthernetSwitchPortVlanSettingData.TrunkVlanIdArray
- Msvm_EthernetSwitchPortVlanSettingData.SecondaryVlanIdArray
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6fce6416696a99e5d928b774e2ba2a05b1dc21d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538728"
---
# <a name="msvm_ethernetswitchportvlansettingdata-class"></a><span data-ttu-id="3f610-103">MSVM \_ EthernetSwitchPortVlanSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="3f610-103">Msvm\_EthernetSwitchPortVlanSettingData class</span></span>

<span data-ttu-id="3f610-104">Représente les données de paramètre de réseau local virtuel (VLAN).</span><span class="sxs-lookup"><span data-stu-id="3f610-104">Represents the virtual LAN (VLAN) setting data.</span></span>

<span data-ttu-id="3f610-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3f610-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f610-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f610-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("952C5004-4465-451C-8CB8-FA9AB382B773"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port VLAN Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortVlanSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port VLAN Settings";
  string Description = "Represents the vlan setting data.";
  string ElementName = "Ethernet Switch Port VLAN Settings";
  uint32 OperationMode = 0;
  uint16 AccessVlanId = 0;
  uint16 NativeVlanId = 0;
  uint32 PvlanMode = 0;
  uint16 PrimaryVlanId = 0;
  uint16 SecondaryVlanId = 0;
  uint16 PruneVlanIdArray[] = {};
  uint16 TrunkVlanIdArray[] = {};
  uint16 SecondaryVlanIdArray[] = {};
};
```

## <a name="members"></a><span data-ttu-id="3f610-107">Membres</span><span class="sxs-lookup"><span data-stu-id="3f610-107">Members</span></span>

<span data-ttu-id="3f610-108">La classe **MSVM \_ EthernetSwitchPortVlanSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3f610-108">The **Msvm\_EthernetSwitchPortVlanSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="3f610-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3f610-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3f610-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3f610-110">Properties</span></span>

<span data-ttu-id="3f610-111">La classe **MSVM \_ EthernetSwitchPortVlanSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3f610-111">The **Msvm\_EthernetSwitchPortVlanSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3f610-112">**AccessVlanId**</span><span class="sxs-lookup"><span data-stu-id="3f610-112">**AccessVlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f610-113">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f610-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f610-114">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3f610-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3f610-115">Qualificateurs : **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="3f610-115">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="3f610-116">Spécifie l’identificateur de réseau local virtuel en mode d’accès.</span><span class="sxs-lookup"><span data-stu-id="3f610-116">Specifies the VLAN identifier in access mode.</span></span>

</dd> <dt>

<span data-ttu-id="3f610-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3f610-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f610-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3f610-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f610-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f610-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f610-120">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3f610-120">A short description of the object.</span></span> <span data-ttu-id="3f610-121">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « paramètres du réseau local virtuel du port commuté ».</span><span class="sxs-lookup"><span data-stu-id="3f610-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port VLAN Settings".</span></span>

</dd> <dt>

<span data-ttu-id="3f610-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="3f610-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f610-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3f610-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f610-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f610-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f610-125">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="3f610-125">A description of the object.</span></span> <span data-ttu-id="3f610-126">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et elle est toujours définie sur « représente les données de paramètre de réseau local virtuel ».</span><span class="sxs-lookup"><span data-stu-id="3f610-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the vlan setting data.".</span></span>

</dd> <dt>

<span data-ttu-id="3f610-127">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3f610-127">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f610-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3f610-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f610-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f610-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f610-130">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3f610-130">A display name for the object.</span></span> <span data-ttu-id="3f610-131">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « paramètres du réseau local virtuel du port commuté ».</span><span class="sxs-lookup"><span data-stu-id="3f610-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port VLAN Settings".</span></span>

</dd> <dt>

<span data-ttu-id="3f610-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3f610-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f610-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3f610-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f610-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f610-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f610-135">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="3f610-135">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3f610-136">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="3f610-136">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3f610-137">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3f610-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3f610-138">**NativeVlanId**</span><span class="sxs-lookup"><span data-stu-id="3f610-138">**NativeVlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f610-139">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f610-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f610-140">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3f610-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3f610-141">Qualificateurs : **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="3f610-141">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="3f610-142">Spécifie l’identificateur de réseau local virtuel en mode Trunk.</span><span class="sxs-lookup"><span data-stu-id="3f610-142">Specifies the VLAN identifier in trunk mode.</span></span>

</dd> <dt>

<span data-ttu-id="3f610-143">**OperationMode**</span><span class="sxs-lookup"><span data-stu-id="3f610-143">**OperationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f610-144">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3f610-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3f610-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3f610-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3f610-146">Qualificateurs : **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="3f610-146">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="3f610-147">Spécifie le mode de fonctionnement du réseau local virtuel.</span><span class="sxs-lookup"><span data-stu-id="3f610-147">Specifies the VLAN operation mode.</span></span>

<dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

<span data-ttu-id="3f610-148">**Accès** (1)</span><span class="sxs-lookup"><span data-stu-id="3f610-148">**Access** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

<span data-ttu-id="3f610-149">**Trunk** (2)</span><span class="sxs-lookup"><span data-stu-id="3f610-149">**Trunk** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Private"></span><span id="private"></span><span id="PRIVATE"></span>

<span data-ttu-id="3f610-150">**Privé** (3)</span><span class="sxs-lookup"><span data-stu-id="3f610-150">**Private** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3f610-151">**PrimaryVlanId**</span><span class="sxs-lookup"><span data-stu-id="3f610-151">**PrimaryVlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f610-152">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f610-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f610-153">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3f610-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3f610-154">Qualificateurs : **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="3f610-154">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="3f610-155">Spécifie l’identificateur VLAN principal en mode privé.</span><span class="sxs-lookup"><span data-stu-id="3f610-155">Specifies the primary VLAN identifier in private mode.</span></span>

</dd> <dt>

<span data-ttu-id="3f610-156">**PruneVlanIdArray**</span><span class="sxs-lookup"><span data-stu-id="3f610-156">**PruneVlanIdArray**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f610-157">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f610-157">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3f610-158">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3f610-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3f610-159">Qualificateurs : **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="3f610-159">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="3f610-160">Spécifie l’image bitmap de l’identificateur VLAN prune en mode Trunk.</span><span class="sxs-lookup"><span data-stu-id="3f610-160">Specifies the prune VLAN identifier bitmap in trunk mode.</span></span>

</dd> <dt>

<span data-ttu-id="3f610-161">**PvlanMode**</span><span class="sxs-lookup"><span data-stu-id="3f610-161">**PvlanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f610-162">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3f610-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3f610-163">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3f610-163">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3f610-164">Qualificateurs : **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="3f610-164">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="3f610-165">Spécifie le mode de réseau local virtuel privé.</span><span class="sxs-lookup"><span data-stu-id="3f610-165">Specifies the private VLAN mode.</span></span>

<dt>

<span id="Isolated"></span><span id="isolated"></span><span id="ISOLATED"></span>

<span data-ttu-id="3f610-166">**Isolé** (1)</span><span class="sxs-lookup"><span data-stu-id="3f610-166">**Isolated** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Community"></span><span id="community"></span><span id="COMMUNITY"></span>

<span data-ttu-id="3f610-167">**Communauté** (2)</span><span class="sxs-lookup"><span data-stu-id="3f610-167">**Community** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Promiscuous"></span><span id="promiscuous"></span><span id="PROMISCUOUS"></span>

<span data-ttu-id="3f610-168">**Promiscuité** (3)</span><span class="sxs-lookup"><span data-stu-id="3f610-168">**Promiscuous** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3f610-169">**SecondaryVlanId**</span><span class="sxs-lookup"><span data-stu-id="3f610-169">**SecondaryVlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f610-170">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f610-170">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f610-171">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3f610-171">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3f610-172">Qualificateurs : **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="3f610-172">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="3f610-173">Spécifie l’identificateur VLAN secondaire en mode privé.</span><span class="sxs-lookup"><span data-stu-id="3f610-173">Specifies the secondary VLAN identifier in private mode.</span></span>

</dd> <dt>

<span data-ttu-id="3f610-174">**SecondaryVlanIdArray**</span><span class="sxs-lookup"><span data-stu-id="3f610-174">**SecondaryVlanIdArray**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f610-175">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f610-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3f610-176">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3f610-176">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3f610-177">Qualificateurs : **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="3f610-177">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="3f610-178">Spécifie l’image bitmap de l’identificateur VLAN secondaire en mode privé.</span><span class="sxs-lookup"><span data-stu-id="3f610-178">Specifies the secondary VLAN identifier bitmap in private mode.</span></span>

</dd> <dt>

<span data-ttu-id="3f610-179">**TrunkVlanIdArray**</span><span class="sxs-lookup"><span data-stu-id="3f610-179">**TrunkVlanIdArray**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f610-180">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f610-180">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3f610-181">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3f610-181">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3f610-182">Qualificateurs : **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="3f610-182">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="3f610-183">Spécifie l’image bitmap de l’identificateur VLAN Trunk en mode Trunk.</span><span class="sxs-lookup"><span data-stu-id="3f610-183">Specifies the trunk VLAN identifier bitmap in trunk mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3f610-184">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f610-184">Requirements</span></span>



| <span data-ttu-id="3f610-185">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f610-185">Requirement</span></span> | <span data-ttu-id="3f610-186">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f610-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f610-187">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f610-187">Minimum supported client</span></span><br/> | <span data-ttu-id="3f610-188">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f610-188">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3f610-189">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f610-189">Minimum supported server</span></span><br/> | <span data-ttu-id="3f610-190">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f610-190">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3f610-191">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3f610-191">Namespace</span></span><br/>                | <span data-ttu-id="3f610-192">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="3f610-192">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3f610-193">MOF</span><span class="sxs-lookup"><span data-stu-id="3f610-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3f610-194"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3f610-194"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3f610-195">DLL</span><span class="sxs-lookup"><span data-stu-id="3f610-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f610-196"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3f610-196"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

