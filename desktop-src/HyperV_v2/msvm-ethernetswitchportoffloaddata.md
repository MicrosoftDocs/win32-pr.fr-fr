---
description: Représente les données d’état de la fonctionnalité de déchargement de port.
ms.assetid: 1117b9e4-cff7-4c9e-bf5e-74499297e84e
title: Classe Msvm_EthernetSwitchPortOffloadData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortOffloadData
- Msvm_EthernetSwitchPortOffloadData.InstanceID
- Msvm_EthernetSwitchPortOffloadData.Caption
- Msvm_EthernetSwitchPortOffloadData.Description
- Msvm_EthernetSwitchPortOffloadData.ElementName
- Msvm_EthernetSwitchPortOffloadData.SystemCreationClassName
- Msvm_EthernetSwitchPortOffloadData.SystemName
- Msvm_EthernetSwitchPortOffloadData.DeviceCreationClassName
- Msvm_EthernetSwitchPortOffloadData.DeviceID
- Msvm_EthernetSwitchPortOffloadData.CreationClassName
- Msvm_EthernetSwitchPortOffloadData.Name
- Msvm_EthernetSwitchPortOffloadData.IpsecCurrentOffloadSaCount
- Msvm_EthernetSwitchPortOffloadData.IovOffloadUsage
- Msvm_EthernetSwitchPortOffloadData.VMQOffloadUsage
- Msvm_EthernetSwitchPortOffloadData.VMQId
- Msvm_EthernetSwitchPortOffloadData.IovVfId
- Msvm_EthernetSwitchPortOffloadData.IovVfDataPathActive
- Msvm_EthernetSwitchPortOffloadData.IovQueuePairUsage
- Msvm_EthernetSwitchPortOffloadData.VmmqQueuePairs
- Msvm_EthernetSwitchPortOffloadData.VrssVmbusChannelAffinityPolicy
- Msvm_EthernetSwitchPortOffloadData.VrssIndependentHostSpreading
- Msvm_EthernetSwitchPortOffloadData.VrssExcludePrimaryProcessor
- Msvm_EthernetSwitchPortOffloadData.VrssQueueSchedulingMode
- Msvm_EthernetSwitchPortOffloadData.VrssMinQueuePairs
- Msvm_EthernetSwitchPortOffloadData.VmmqEnabled
- Msvm_EthernetSwitchPortOffloadData.VrssEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fd60e98c8df12b539bb51c60b34e7931b762dc03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538407"
---
# <a name="msvm_ethernetswitchportoffloaddata-class"></a><span data-ttu-id="08097-103">MSVM \_ EthernetSwitchPortOffloadData, classe</span><span class="sxs-lookup"><span data-stu-id="08097-103">Msvm\_EthernetSwitchPortOffloadData class</span></span>

<span data-ttu-id="08097-104">Représente les données d’état de la fonctionnalité de déchargement de port.</span><span class="sxs-lookup"><span data-stu-id="08097-104">Represents the port offload feature status data.</span></span>

<span data-ttu-id="08097-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="08097-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="08097-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08097-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("C885BFD1-ABB7-418F-8163-9F379C9F7166"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("3"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Offload Feature Status"), AMENDMENT]
class Msvm_EthernetSwitchPortOffloadData : Msvm_EthernetPortData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Offload Feature Status";
  string  Description = "Represents the port offload feature status data.";
  string  ElementName = "Ethernet Switch Port Offload Feature Status";
  string  SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string  SystemName;
  string  DeviceCreationClassName = "Msvm_EthernetSwitchPort";
  string  DeviceID;
  string  CreationClassName = "Msvm_EthernetSwitchPortOffloadData";
  string  Name;
  uint32  IpsecCurrentOffloadSaCount = 0;
  uint32  IovOffloadUsage = 0;
  uint32  VMQOffloadUsage = 0;
  uint32  VMQId = 0;
  uint16  IovVfId = 0;
  boolean IovVfDataPathActive = FALSE;
  uint32  IovQueuePairUsage = 0;
  uint32  VmmqQueuePairs = 0;
  uint32  VrssVmbusChannelAffinityPolicy = 0;
  boolean VrssIndependentHostSpreading = FALSE;
  boolean VrssExcludePrimaryProcessor = FALSE;
  uint32  VrssQueueSchedulingMode = 0;
  uint32  VrssMinQueuePairs = 0;
  boolean VmmqEnabled = FALSE;
  boolean VrssEnabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="08097-107">Membres</span><span class="sxs-lookup"><span data-stu-id="08097-107">Members</span></span>

<span data-ttu-id="08097-108">La classe **MSVM \_ EthernetSwitchPortOffloadData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="08097-108">The **Msvm\_EthernetSwitchPortOffloadData** class has these types of members:</span></span>

-   [<span data-ttu-id="08097-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="08097-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="08097-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="08097-110">Properties</span></span>

<span data-ttu-id="08097-111">La classe **MSVM \_ EthernetSwitchPortOffloadData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="08097-111">The **Msvm\_EthernetSwitchPortOffloadData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="08097-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="08097-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08097-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="08097-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08097-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08097-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08097-115">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="08097-115">A short description of the object.</span></span> <span data-ttu-id="08097-116">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « état de la fonctionnalité de déchargement du port du commutateur Ethernet ».</span><span class="sxs-lookup"><span data-stu-id="08097-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Offload Feature Status".</span></span>

</dd> <dt>

<span data-ttu-id="08097-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="08097-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08097-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="08097-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08097-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08097-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08097-120">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="08097-120">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="08097-121">Nom de la sous-classe utilisée lors de la création de cette instance de données de port.</span><span class="sxs-lookup"><span data-stu-id="08097-121">The name of the subclass used in the creation of this port data instance.</span></span> <span data-ttu-id="08097-122">Cette propriété est héritée de [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md)et elle est toujours définie sur « MSVM \_ EthernetSwitchPortOffloadData ».</span><span class="sxs-lookup"><span data-stu-id="08097-122">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_EthernetSwitchPortOffloadData".</span></span>

</dd> <dt>

<span data-ttu-id="08097-123">**Description**</span><span class="sxs-lookup"><span data-stu-id="08097-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08097-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="08097-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08097-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08097-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08097-126">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="08097-126">A description of the object.</span></span> <span data-ttu-id="08097-127">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et elle est toujours définie sur « représente les données d’état de la fonctionnalité de déchargement de port ».</span><span class="sxs-lookup"><span data-stu-id="08097-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port offload feature status data.".</span></span>

</dd> <dt>

<span data-ttu-id="08097-128">**DeviceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="08097-128">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08097-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="08097-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08097-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08097-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08097-131">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="08097-131">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="08097-132">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="08097-132">The scoping system's creation class name.</span></span> <span data-ttu-id="08097-133">Cette propriété est héritée de [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md)et elle est toujours définie sur « MSVM \_ EthernetSwitchPort ».</span><span class="sxs-lookup"><span data-stu-id="08097-133">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_EthernetSwitchPort".</span></span>

</dd> <dt>

<span data-ttu-id="08097-134">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="08097-134">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08097-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="08097-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08097-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08097-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08097-137">Qualificateurs : **clé**, **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="08097-137">Qualifiers: **Key**, **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="08097-138">ID d’appareil du port qui étend cette instance de données de port.</span><span class="sxs-lookup"><span data-stu-id="08097-138">The Device ID of the port that scopes this port data instance.</span></span> <span data-ttu-id="08097-139">Cette propriété est héritée de [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="08097-139">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="08097-140">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="08097-140">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08097-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="08097-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08097-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08097-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08097-143">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="08097-143">A display name for the object.</span></span> <span data-ttu-id="08097-144">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « état de la fonctionnalité de déchargement du port du commutateur Ethernet ».</span><span class="sxs-lookup"><span data-stu-id="08097-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Offload Feature Status".</span></span>

</dd> <dt>

<span data-ttu-id="08097-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="08097-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08097-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="08097-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08097-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08097-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08097-148">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="08097-148">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="08097-149">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="08097-149">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="08097-150">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="08097-150">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="08097-151">**IovOffloadUsage**</span><span class="sxs-lookup"><span data-stu-id="08097-151">**IovOffloadUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08097-152">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08097-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08097-153">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="08097-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="08097-154">Qualificateurs : **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="08097-154">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="08097-155">Utilisation du déchargement de la virtualisation d’e/s en cours (IOV).</span><span class="sxs-lookup"><span data-stu-id="08097-155">The current I/O virtualization (IOV) offload usage.</span></span>

</dd> <dt>

<span data-ttu-id="08097-156">**IovQueuePairUsage**</span><span class="sxs-lookup"><span data-stu-id="08097-156">**IovQueuePairUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08097-157">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08097-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08097-158">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="08097-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="08097-159">Qualificateurs : **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="08097-159">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="08097-160">Nombre actuel de paires de files d’attente utilisées par le port.</span><span class="sxs-lookup"><span data-stu-id="08097-160">The current number of queue pairs being used by the port.</span></span>

</dd> <dt>

<span data-ttu-id="08097-161">**IovVfDataPathActive**</span><span class="sxs-lookup"><span data-stu-id="08097-161">**IovVfDataPathActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08097-162">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="08097-162">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08097-163">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="08097-163">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="08097-164">Qualificateurs : **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="08097-164">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="08097-165">Indique si le chemin de données IOV VF est actif.</span><span class="sxs-lookup"><span data-stu-id="08097-165">Indicates whether the IOV VF data path is active.</span></span>

</dd> <dt>

<span data-ttu-id="08097-166">**IovVfId**</span><span class="sxs-lookup"><span data-stu-id="08097-166">**IovVfId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08097-167">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08097-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08097-168">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="08097-168">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="08097-169">Qualificateurs : **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="08097-169">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="08097-170">Identificateur IOV VF actuel assigné au port.</span><span class="sxs-lookup"><span data-stu-id="08097-170">The current IOV VF identifier that is assigned to the port.</span></span> <span data-ttu-id="08097-171">Cette valeur est valide si **IovOffloadUsage** n’est pas égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="08097-171">This is valid if **IovOffloadUsage** is not zero.</span></span>

</dd> <dt>

<span data-ttu-id="08097-172">**IpsecCurrentOffloadSaCount**</span><span class="sxs-lookup"><span data-stu-id="08097-172">**IpsecCurrentOffloadSaCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08097-173">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08097-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08097-174">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="08097-174">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="08097-175">Qualificateurs : **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="08097-175">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="08097-176">Nombre actuel d’emplacements de déchargement d’association de sécurité en cours d’utilisation sur le port.</span><span class="sxs-lookup"><span data-stu-id="08097-176">The current number of security association (SA) offload slots in use on the port.</span></span>

</dd> <dt>

<span data-ttu-id="08097-177">**Nom**</span><span class="sxs-lookup"><span data-stu-id="08097-177">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08097-178">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="08097-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08097-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08097-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08097-180">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="08097-180">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="08097-181">Chaîne qui identifie de façon unique cette instance de données de port dans l’étendue du commutateur et du port.</span><span class="sxs-lookup"><span data-stu-id="08097-181">A string that uniquely identifies this port data instance within the scope of the switch and port.</span></span> <span data-ttu-id="08097-182">Cette propriété est héritée de [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="08097-182">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="08097-183">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="08097-183">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08097-184">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="08097-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08097-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08097-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08097-186">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="08097-186">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="08097-187">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="08097-187">The scoping system's creation class name.</span></span> <span data-ttu-id="08097-188">Cette propriété est héritée de [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md)et elle est toujours définie sur « MSVM \_ VirtualEthernetSwitch ».</span><span class="sxs-lookup"><span data-stu-id="08097-188">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_VirtualEthernetSwitch".</span></span>

</dd> <dt>

<span data-ttu-id="08097-189">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="08097-189">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08097-190">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="08097-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08097-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08097-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08097-192">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="08097-192">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="08097-193">Nom du commutateur virtuel qui s’étend à cette instance de données de port.</span><span class="sxs-lookup"><span data-stu-id="08097-193">The name of the virtual switch that scopes this port data instance.</span></span> <span data-ttu-id="08097-194">Cette propriété est héritée de [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="08097-194">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="08097-195">**VmmqEnabled**</span><span class="sxs-lookup"><span data-stu-id="08097-195">**VmmqEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08097-196">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="08097-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08097-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08097-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08097-198">Qualificateurs : **WmiDataId** (9), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="08097-198">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="08097-199">Indique si VMMQ est actif.</span><span class="sxs-lookup"><span data-stu-id="08097-199">Indicates if VMMQ is active.</span></span>

> [!Note]  
> <span data-ttu-id="08097-200">Cette propriété a été ajoutée dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="08097-200">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="08097-201">**VmmqQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="08097-201">**VmmqQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08097-202">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08097-202">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08097-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08097-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08097-204">Qualificateurs : **WmiDataId** (10), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="08097-204">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="08097-205">Indique le nombre de files d’attente utilisées pour VRSS/VMMQ.</span><span class="sxs-lookup"><span data-stu-id="08097-205">Indicates how many queues are used for VRSS/VMMQ.</span></span>

> [!Note]  
> <span data-ttu-id="08097-206">Cette propriété a été ajoutée dans Windows 10, version 1703 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="08097-206">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="08097-207">**VMQId**</span><span class="sxs-lookup"><span data-stu-id="08097-207">**VMQId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08097-208">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08097-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08097-209">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="08097-209">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="08097-210">Qualificateurs : **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="08097-210">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="08097-211">Identificateur de la file d’attente de l’ordinateur virtuel actuel qui est affecté au port.</span><span class="sxs-lookup"><span data-stu-id="08097-211">The current virtual machine queue identifier that is assigned to the port.</span></span> <span data-ttu-id="08097-212">Cette valeur est valide si **VMQOffloadUsage** n’est pas égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="08097-212">This is valid if **VMQOffloadUsage** is not zero.</span></span>

</dd> <dt>

<span data-ttu-id="08097-213">**VMQOffloadUsage**</span><span class="sxs-lookup"><span data-stu-id="08097-213">**VMQOffloadUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08097-214">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08097-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08097-215">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="08097-215">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="08097-216">Qualificateurs : **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="08097-216">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="08097-217">Utilisation du déchargement de la file d’attente d’ordinateurs virtuels actuelle.</span><span class="sxs-lookup"><span data-stu-id="08097-217">The current virtual machine queue (VMQ) offload usage.</span></span>

</dd> <dt>

<span data-ttu-id="08097-218">**VrssEnabled**</span><span class="sxs-lookup"><span data-stu-id="08097-218">**VrssEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08097-219">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="08097-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08097-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08097-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08097-221">Qualificateurs : **WmiDataId** (8), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="08097-221">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="08097-222">Indique si le vRSS est actif.</span><span class="sxs-lookup"><span data-stu-id="08097-222">Indicates if vRSS is active.</span></span>

> [!Note]  
> <span data-ttu-id="08097-223">Cette propriété a été ajoutée dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="08097-223">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="08097-224">**VrssExcludePrimaryProcessor**</span><span class="sxs-lookup"><span data-stu-id="08097-224">**VrssExcludePrimaryProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08097-225">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="08097-225">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08097-226">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08097-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08097-227">Qualificateurs : **WmiDataId** (13), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="08097-227">Qualifiers: **WmiDataId** (13), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="08097-228">Indique si l’UC de l’unité centrale principale est exclue de la table d’indirection VRSS/VMMQ.</span><span class="sxs-lookup"><span data-stu-id="08097-228">Indicates whether the primary VMQ CPU is excluded from the VRSS/VMMQ indirection table.</span></span>

> [!Note]  
> <span data-ttu-id="08097-229">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="08097-229">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="08097-230">**VrssIndependentHostSpreading**</span><span class="sxs-lookup"><span data-stu-id="08097-230">**VrssIndependentHostSpreading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08097-231">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="08097-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08097-232">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08097-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08097-233">Qualificateurs : **WmiDataId** (14), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="08097-233">Qualifiers: **WmiDataId** (14), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="08097-234">Indique si la diffusion VRSS/VMMQ côté hôte se produit, quels que soient les paramètres RSS de la carte réseau virtuelle.</span><span class="sxs-lookup"><span data-stu-id="08097-234">Indicates whether host side VRSS/VMMQ spreading happens, regardless of RSS settings of the virtual NIC.</span></span>

> [!Note]  
> <span data-ttu-id="08097-235">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="08097-235">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="08097-236">**VrssMinQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="08097-236">**VrssMinQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08097-237">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08097-237">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08097-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08097-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08097-239">Qualificateurs : **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="08097-239">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="08097-240">Indique le nombre minimal de files d’attente utilisées pour VRSS/VMMQ.</span><span class="sxs-lookup"><span data-stu-id="08097-240">Indicates minimum number of queues used for VRSS/VMMQ.</span></span>

> [!Note]  
> <span data-ttu-id="08097-241">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="08097-241">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="08097-242">**VrssQueueSchedulingMode**</span><span class="sxs-lookup"><span data-stu-id="08097-242">**VrssQueueSchedulingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08097-243">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08097-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08097-244">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08097-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08097-245">Qualificateurs : **WmiDataId** (12), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="08097-245">Qualifiers: **WmiDataId** (12), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="08097-246">Indique comment les files d’attente VRSS/VMMQ sont directrices sur différents processeurs hôtes.</span><span class="sxs-lookup"><span data-stu-id="08097-246">Indicates how VRSS/VMMQ queues are steered to different host processors.</span></span>

> [!Note]  
> <span data-ttu-id="08097-247">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="08097-247">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="08097-248">**VrssVmbusChannelAffinityPolicy**</span><span class="sxs-lookup"><span data-stu-id="08097-248">**VrssVmbusChannelAffinityPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08097-249">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08097-249">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08097-250">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08097-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08097-251">Qualificateurs : **WmiDataId** (15), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="08097-251">Qualifiers: **WmiDataId** (15), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="08097-252">Indique comment les canaux VMBus sont affinité aux processeurs hôtes.</span><span class="sxs-lookup"><span data-stu-id="08097-252">Indicates how Vmbus channels are affinitized to host processors.</span></span>

> [!Note]  
> <span data-ttu-id="08097-253">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="08097-253">Added in Windows 10, version 1709.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="08097-254">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08097-254">Requirements</span></span>



| <span data-ttu-id="08097-255">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08097-255">Requirement</span></span> | <span data-ttu-id="08097-256">Valeur</span><span class="sxs-lookup"><span data-stu-id="08097-256">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08097-257">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08097-257">Minimum supported client</span></span><br/> | <span data-ttu-id="08097-258">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08097-258">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="08097-259">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08097-259">Minimum supported server</span></span><br/> | <span data-ttu-id="08097-260">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08097-260">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="08097-261">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="08097-261">Namespace</span></span><br/>                | <span data-ttu-id="08097-262">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="08097-262">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="08097-263">MOF</span><span class="sxs-lookup"><span data-stu-id="08097-263">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08097-264"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08097-264"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="08097-265">DLL</span><span class="sxs-lookup"><span data-stu-id="08097-265">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08097-266"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="08097-266"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

