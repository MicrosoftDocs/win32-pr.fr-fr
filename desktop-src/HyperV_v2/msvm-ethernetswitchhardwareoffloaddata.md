---
description: Représente l’état du déchargement matériel du commutateur.
ms.assetid: 77a34df7-e3c4-4d91-af5a-91a03dd8246d
title: Classe Msvm_EthernetSwitchHardwareOffloadData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchHardwareOffloadData
- Msvm_EthernetSwitchHardwareOffloadData.InstanceID
- Msvm_EthernetSwitchHardwareOffloadData.Caption
- Msvm_EthernetSwitchHardwareOffloadData.Description
- Msvm_EthernetSwitchHardwareOffloadData.ElementName
- Msvm_EthernetSwitchHardwareOffloadData.SystemCreationClassName
- Msvm_EthernetSwitchHardwareOffloadData.SystemName
- Msvm_EthernetSwitchHardwareOffloadData.CreationClassName
- Msvm_EthernetSwitchHardwareOffloadData.Name
- Msvm_EthernetSwitchHardwareOffloadData.IovVfCapacity
- Msvm_EthernetSwitchHardwareOffloadData.IovVfUsage
- Msvm_EthernetSwitchHardwareOffloadData.VmqCapacity
- Msvm_EthernetSwitchHardwareOffloadData.VmqUsage
- Msvm_EthernetSwitchHardwareOffloadData.IPsecSACapacity
- Msvm_EthernetSwitchHardwareOffloadData.IPsecSAUsage
- Msvm_EthernetSwitchHardwareOffloadData.IovQueuePairCapacity
- Msvm_EthernetSwitchHardwareOffloadData.IovQueuePairUsage
- Msvm_EthernetSwitchHardwareOffloadData.PacketDirectInUse
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVmmqQueuePairs
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssIndependentHostSpreading
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssExcludePrimaryProcessor
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssQueueSchedulingMode
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssMinQueuePairs
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVmmqEnabled
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b64762b824cea7d3b064636e7f7f87777e053daf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520205"
---
# <a name="msvm_ethernetswitchhardwareoffloaddata-class"></a><span data-ttu-id="93bf6-103">MSVM \_ EthernetSwitchHardwareOffloadData, classe</span><span class="sxs-lookup"><span data-stu-id="93bf6-103">Msvm\_EthernetSwitchHardwareOffloadData class</span></span>

<span data-ttu-id="93bf6-104">Représente l’état du déchargement matériel du commutateur.</span><span class="sxs-lookup"><span data-stu-id="93bf6-104">Represents the switch hardware offload status.</span></span>

<span data-ttu-id="93bf6-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="93bf6-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="93bf6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93bf6-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("1C37E01C-0CD6-496F-9076-90C131033DC2"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("4"), InterfaceRevision("0"), DisplayName("Ethernet Switch Offload Resource Status"), AMENDMENT]
class Msvm_EthernetSwitchHardwareOffloadData : Msvm_EthernetSwitchData
{
  string  InstanceID;
  string  Caption = Ethernet Switch Offload Resource Status;
  string  Description = Represents the switch hardware offload status.;
  string  ElementName = Ethernet Switch Offload Resource Status;
  string  SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string  SystemName;
  string  CreationClassName = "Msvm_EthernetSwitchHardwareOffloadData";
  string  Name;
  uint32  IovVfCapacity = 0;
  uint32  IovVfUsage = 0;
  uint32  VmqCapacity = 0;
  uint32  VmqUsage = 0;
  uint32  IPsecSACapacity = 0;
  uint32  IPsecSAUsage = 0;
  uint32  IovQueuePairCapacity = 0;
  uint32  IovQueuePairUsage = 0;
  boolean PacketDirectInUse = FALSE;
  uint32  DefaultQueueVmmqQueuePairs = 0;
  boolean DefaultQueueVrssIndependentHostSpreading = TRUE;
  boolean DefaultQueueVrssExcludePrimaryProcessor = FALSE;
  uint32  DefaultQueueVrssQueueSchedulingMode = 0;
  uint32  DefaultQueueVrssMinQueuePairs = 0;
  boolean DefaultQueueVmmqEnabled = FALSE;
  boolean DefaultQueueVrssEnabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="93bf6-107">Membres</span><span class="sxs-lookup"><span data-stu-id="93bf6-107">Members</span></span>

<span data-ttu-id="93bf6-108">La classe **MSVM \_ EthernetSwitchHardwareOffloadData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="93bf6-108">The **Msvm\_EthernetSwitchHardwareOffloadData** class has these types of members:</span></span>

-   [<span data-ttu-id="93bf6-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="93bf6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="93bf6-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="93bf6-110">Properties</span></span>

<span data-ttu-id="93bf6-111">La classe **MSVM \_ EthernetSwitchHardwareOffloadData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="93bf6-111">The **Msvm\_EthernetSwitchHardwareOffloadData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="93bf6-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="93bf6-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bf6-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93bf6-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93bf6-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bf6-115">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="93bf6-115">A short description of the object.</span></span> <span data-ttu-id="93bf6-116">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="93bf6-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93bf6-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="93bf6-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bf6-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93bf6-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93bf6-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-120">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="93bf6-120">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="93bf6-121">Nom de la classe ou de la sous-classe utilisée dans la création de cette instance.</span><span class="sxs-lookup"><span data-stu-id="93bf6-121">The name of the class or subclass used in the creation of this instance.</span></span> <span data-ttu-id="93bf6-122">Cette propriété est héritée de [**MSVM \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="93bf6-122">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="93bf6-123">**DefaultQueueVmmqEnabled**</span><span class="sxs-lookup"><span data-stu-id="93bf6-123">**DefaultQueueVmmqEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bf6-124">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="93bf6-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93bf6-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-126">Qualificateurs : **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="93bf6-126">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="93bf6-127">Paramètre VMMQ actuel pour la file d’attente par défaut</span><span class="sxs-lookup"><span data-stu-id="93bf6-127">The current VMMQ setting for default queue</span></span>

> [!Note]  
> <span data-ttu-id="93bf6-128">Propriété ajoutée dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="93bf6-128">Property added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="93bf6-129">**DefaultQueueVmmqQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="93bf6-129">**DefaultQueueVmmqQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bf6-130">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93bf6-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93bf6-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-132">Qualificateurs : **WmiDataId** (12), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="93bf6-132">Qualifiers: **WmiDataId** (12), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="93bf6-133">Nombre actuel de files d’attente allouées à la file d’attente par défaut</span><span class="sxs-lookup"><span data-stu-id="93bf6-133">The current number of queues allocated for the default queue</span></span>

> [!Note]  
> <span data-ttu-id="93bf6-134">Propriété ajoutée dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="93bf6-134">Property added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="93bf6-135">**DefaultQueueVrssEnabled**</span><span class="sxs-lookup"><span data-stu-id="93bf6-135">**DefaultQueueVrssEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bf6-136">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="93bf6-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93bf6-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-138">Qualificateurs : **WmiDataId** (10), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="93bf6-138">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="93bf6-139">Paramètre VRss actuel pour la file d’attente par défaut</span><span class="sxs-lookup"><span data-stu-id="93bf6-139">The current VRss setting for default queue</span></span>

> [!Note]  
> <span data-ttu-id="93bf6-140">Propriété ajoutée dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="93bf6-140">Property added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="93bf6-141">**DefaultQueueVrssExcludePrimaryProcessor**</span><span class="sxs-lookup"><span data-stu-id="93bf6-141">**DefaultQueueVrssExcludePrimaryProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bf6-142">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="93bf6-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93bf6-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-144">Qualificateurs : **WmiDataId** (15), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="93bf6-144">Qualifiers: **WmiDataId** (15), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="93bf6-145">Indique si l’UC de l’unité centrale principale est exclue de la table d’indirection VRSS/VMMQ.</span><span class="sxs-lookup"><span data-stu-id="93bf6-145">Indicates whether the primary VMQ CPU is excluded from the VRSS/VMMQ indirection table.</span></span>

> [!Note]  
> <span data-ttu-id="93bf6-146">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="93bf6-146">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="93bf6-147">**DefaultQueueVrssIndependentHostSpreading**</span><span class="sxs-lookup"><span data-stu-id="93bf6-147">**DefaultQueueVrssIndependentHostSpreading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bf6-148">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="93bf6-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93bf6-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-150">Qualificateurs : **WmiDataId** (16), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="93bf6-150">Qualifiers: **WmiDataId** (16), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="93bf6-151">Indique s’il faut toujours effectuer la répartition VRSS pour la file d’attente par défaut, quel que soit l’État RSS du vPort externe.</span><span class="sxs-lookup"><span data-stu-id="93bf6-151">Indicates whether to always do VRSS spreading for default queue, regardless of the RSS state of the external vPort.</span></span>

> [!Note]  
> <span data-ttu-id="93bf6-152">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="93bf6-152">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="93bf6-153">**DefaultQueueVrssMinQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="93bf6-153">**DefaultQueueVrssMinQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bf6-154">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93bf6-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93bf6-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-156">Qualificateurs : **WmiDataId** (13), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="93bf6-156">Qualifiers: **WmiDataId** (13), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="93bf6-157">Indique le nombre minimal de files d’attente utilisées pour VRSS/VMMQ.</span><span class="sxs-lookup"><span data-stu-id="93bf6-157">Indicates minimum number of queues used for VRSS/VMMQ.</span></span>

> [!Note]  
> <span data-ttu-id="93bf6-158">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="93bf6-158">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="93bf6-159">**DefaultQueueVrssQueueSchedulingMode**</span><span class="sxs-lookup"><span data-stu-id="93bf6-159">**DefaultQueueVrssQueueSchedulingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bf6-160">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93bf6-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93bf6-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-162">Qualificateurs : **WmiDataId** (14), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="93bf6-162">Qualifiers: **WmiDataId** (14), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="93bf6-163">Indique comment les files d’attente VRSS/VMMQ sont directrices sur différents processeurs hôtes.</span><span class="sxs-lookup"><span data-stu-id="93bf6-163">Indicates how VRSS/VMMQ queues are steered to different host processors.</span></span>

> [!Note]  
> <span data-ttu-id="93bf6-164">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="93bf6-164">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="93bf6-165">**Description**</span><span class="sxs-lookup"><span data-stu-id="93bf6-165">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bf6-166">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93bf6-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93bf6-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bf6-168">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="93bf6-168">A description of the object.</span></span> <span data-ttu-id="93bf6-169">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="93bf6-169">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93bf6-170">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="93bf6-170">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bf6-171">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93bf6-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93bf6-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bf6-173">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="93bf6-173">A display name for the object.</span></span> <span data-ttu-id="93bf6-174">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="93bf6-174">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93bf6-175">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="93bf6-175">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bf6-176">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93bf6-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93bf6-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-178">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="93bf6-178">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="93bf6-179">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="93bf6-179">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="93bf6-180">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="93bf6-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93bf6-181">**IovQueuePairCapacity**</span><span class="sxs-lookup"><span data-stu-id="93bf6-181">**IovQueuePairCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bf6-182">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93bf6-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93bf6-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-184">Qualificateurs : **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="93bf6-184">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="93bf6-185">Nombre maximal de paires de files d’attente prises en charge par le commutateur.</span><span class="sxs-lookup"><span data-stu-id="93bf6-185">The maximum number of queue pairs supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="93bf6-186">**IovQueuePairUsage**</span><span class="sxs-lookup"><span data-stu-id="93bf6-186">**IovQueuePairUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bf6-187">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93bf6-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93bf6-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-189">Qualificateurs : **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="93bf6-189">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="93bf6-190">Nombre actuel de paires de files d’attente utilisées par le commutateur.</span><span class="sxs-lookup"><span data-stu-id="93bf6-190">The current number of queue pairs being used by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="93bf6-191">**IovVfCapacity**</span><span class="sxs-lookup"><span data-stu-id="93bf6-191">**IovVfCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bf6-192">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93bf6-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93bf6-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-194">Qualificateurs : **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="93bf6-194">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="93bf6-195">Nombre maximal de fonctions virtuelles prises en charge par le commutateur.</span><span class="sxs-lookup"><span data-stu-id="93bf6-195">The maximum number of virtual functions supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="93bf6-196">**IovVfUsage**</span><span class="sxs-lookup"><span data-stu-id="93bf6-196">**IovVfUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bf6-197">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93bf6-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93bf6-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-199">Qualificateurs : **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="93bf6-199">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="93bf6-200">Nombre actuel de fonctions virtuelles utilisées par le commutateur.</span><span class="sxs-lookup"><span data-stu-id="93bf6-200">The current number of virtual functions being used by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="93bf6-201">**IPsecSACapacity**</span><span class="sxs-lookup"><span data-stu-id="93bf6-201">**IPsecSACapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bf6-202">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93bf6-202">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93bf6-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-204">Qualificateurs : **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="93bf6-204">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="93bf6-205">Nombre maximal de déchargements d’associations de sécurité IPsec pris en charge par le commutateur.</span><span class="sxs-lookup"><span data-stu-id="93bf6-205">The maximum number of IPsec security association offloads supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="93bf6-206">**IPsecSAUsage**</span><span class="sxs-lookup"><span data-stu-id="93bf6-206">**IPsecSAUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bf6-207">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93bf6-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93bf6-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-209">Qualificateurs : **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="93bf6-209">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="93bf6-210">Nombre actuel de déchargements d’associations de sécurité IPsec utilisés par le commutateur.</span><span class="sxs-lookup"><span data-stu-id="93bf6-210">The current number of IPsec security association offloads being used by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="93bf6-211">**Nom**</span><span class="sxs-lookup"><span data-stu-id="93bf6-211">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bf6-212">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93bf6-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-213">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93bf6-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-214">Qualificateurs : **clé**, **remplacement**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="93bf6-214">Qualifiers: **Key**, **Override**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="93bf6-215">Nom unique de la ressource.</span><span class="sxs-lookup"><span data-stu-id="93bf6-215">The unique name of the resource.</span></span> <span data-ttu-id="93bf6-216">Cette propriété est héritée de [**MSVM \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="93bf6-216">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="93bf6-217">**PacketDirectInUse**</span><span class="sxs-lookup"><span data-stu-id="93bf6-217">**PacketDirectInUse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bf6-218">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="93bf6-218">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-219">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93bf6-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-220">Qualificateurs : **WmiDataId** (9), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="93bf6-220">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="93bf6-221">Indique si Packet direct est utilisé par le commutateur</span><span class="sxs-lookup"><span data-stu-id="93bf6-221">Indicates if packet direct is being used by the switch</span></span>

> [!Note]  
> <span data-ttu-id="93bf6-222">Propriété ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="93bf6-222">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="93bf6-223">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="93bf6-223">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bf6-224">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93bf6-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-225">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93bf6-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-226">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="93bf6-226">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="93bf6-227">Nom de la classe de création du système d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="93bf6-227">The hosting system's creation class name.</span></span> <span data-ttu-id="93bf6-228">Cette propriété est héritée de [**MSVM \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="93bf6-228">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="93bf6-229">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="93bf6-229">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bf6-230">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93bf6-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93bf6-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-232">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="93bf6-232">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="93bf6-233">Nom du commutateur virtuel auquel l’instance de ressource associée est liée.</span><span class="sxs-lookup"><span data-stu-id="93bf6-233">The name of the virtual switch to which the associated resource instance is bound.</span></span> <span data-ttu-id="93bf6-234">Cette propriété est héritée de [**MSVM \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="93bf6-234">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="93bf6-235">**VmqCapacity**</span><span class="sxs-lookup"><span data-stu-id="93bf6-235">**VmqCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bf6-236">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93bf6-236">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-237">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93bf6-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-238">Qualificateurs : **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="93bf6-238">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="93bf6-239">Nombre maximal de déchargements de files d’attente d’ordinateurs virtuels pris en charge par le commutateur.</span><span class="sxs-lookup"><span data-stu-id="93bf6-239">The maximum number of virtual machine queue offloads supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="93bf6-240">**VmqUsage**</span><span class="sxs-lookup"><span data-stu-id="93bf6-240">**VmqUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bf6-241">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93bf6-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-242">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93bf6-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93bf6-243">Qualificateurs : **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="93bf6-243">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="93bf6-244">Nombre actuel de déchargements de files d’attente d’ordinateurs virtuels utilisés par le commutateur.</span><span class="sxs-lookup"><span data-stu-id="93bf6-244">The current number of virtual machine queue offloads being used by the switch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="93bf6-245">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93bf6-245">Requirements</span></span>



| <span data-ttu-id="93bf6-246">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93bf6-246">Requirement</span></span> | <span data-ttu-id="93bf6-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="93bf6-247">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93bf6-248">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93bf6-248">Minimum supported client</span></span><br/> | <span data-ttu-id="93bf6-249">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93bf6-249">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="93bf6-250">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93bf6-250">Minimum supported server</span></span><br/> | <span data-ttu-id="93bf6-251">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93bf6-251">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="93bf6-252">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="93bf6-252">Namespace</span></span><br/>                | <span data-ttu-id="93bf6-253">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="93bf6-253">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="93bf6-254">MOF</span><span class="sxs-lookup"><span data-stu-id="93bf6-254">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93bf6-255"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93bf6-255"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="93bf6-256">DLL</span><span class="sxs-lookup"><span data-stu-id="93bf6-256">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93bf6-257"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="93bf6-257"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

