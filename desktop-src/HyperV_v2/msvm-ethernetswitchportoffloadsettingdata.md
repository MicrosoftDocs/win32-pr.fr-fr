---
description: Représente les données de paramètre de la fonctionnalité de déchargement de port.
ms.assetid: 7b8d8bee-86f3-4c55-bb32-987bf840d995
title: Classe Msvm_EthernetSwitchPortOffloadSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortOffloadSettingData
- Msvm_EthernetSwitchPortOffloadSettingData.InstanceID
- Msvm_EthernetSwitchPortOffloadSettingData.Caption
- Msvm_EthernetSwitchPortOffloadSettingData.Description
- Msvm_EthernetSwitchPortOffloadSettingData.ElementName
- Msvm_EthernetSwitchPortOffloadSettingData.IPSecOffloadLimit
- Msvm_EthernetSwitchPortOffloadSettingData.VMQOffloadWeight
- Msvm_EthernetSwitchPortOffloadSettingData.IOVOffloadWeight
- Msvm_EthernetSwitchPortOffloadSettingData.IOVQueuePairsRequested
- Msvm_EthernetSwitchPortOffloadSettingData.IOVInterruptModeration
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectModerationInterval
- Msvm_EthernetSwitchPortOffloadSettingData.VmmqQueuePairs
- Msvm_EthernetSwitchPortOffloadSettingData.VrssVmbusChannelAffinityPolicy
- Msvm_EthernetSwitchPortOffloadSettingData.VrssIndependentHostSpreading
- Msvm_EthernetSwitchPortOffloadSettingData.VrssExcludePrimaryProcessor
- Msvm_EthernetSwitchPortOffloadSettingData.VrssQueueSchedulingMode
- Msvm_EthernetSwitchPortOffloadSettingData.VrssMinQueuePairs
- Msvm_EthernetSwitchPortOffloadSettingData.VmmqEnabled
- Msvm_EthernetSwitchPortOffloadSettingData.VrssEnabled
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectModerationCount
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectNumProcs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 150a7b5e54e371c11741dd7c763b0ae145354b09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522856"
---
# <a name="msvm_ethernetswitchportoffloadsettingdata-class"></a><span data-ttu-id="f2102-103">MSVM \_ EthernetSwitchPortOffloadSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="f2102-103">Msvm\_EthernetSwitchPortOffloadSettingData class</span></span>

<span data-ttu-id="f2102-104">Représente les données de paramètre de la fonctionnalité de déchargement de port.</span><span class="sxs-lookup"><span data-stu-id="f2102-104">Represents the port offload feature setting data.</span></span>

<span data-ttu-id="f2102-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="f2102-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2102-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2102-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("C885BFD1-ABB7-418F-8163-9F379C9F7166"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("4"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Offload Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortOffloadSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Offload Settings";
  string  Description = "Represents the port offload feature setting data.";
  string  ElementName = "Ethernet Switch Port Offload Settings";
  uint32  IPSecOffloadLimit = 512;
  uint32  VMQOffloadWeight = 100;
  uint32  IOVOffloadWeight = 0;
  uint32  IOVQueuePairsRequested = 1;
  uint32  IOVInterruptModeration = 0;
  uint32  PacketDirectModerationInterval = 0;
  uint32  VmmqQueuePairs = 16;
  uint32  VrssVmbusChannelAffinityPolicy = 3;
  boolean VrssIndependentHostSpreading = FALSE;
  boolean VrssExcludePrimaryProcessor = FALSE;
  uint32  VrssQueueSchedulingMode = 2;
  uint32  VrssMinQueuePairs = 1;
  boolean VmmqEnabled = FALSE;
  boolean VrssEnabled = TRUE;
  uint32  PacketDirectModerationCount = 0;
  uint32  PacketDirectNumProcs = 1;
};
```

## <a name="members"></a><span data-ttu-id="f2102-107">Membres</span><span class="sxs-lookup"><span data-stu-id="f2102-107">Members</span></span>

<span data-ttu-id="f2102-108">La classe **MSVM \_ EthernetSwitchPortOffloadSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f2102-108">The **Msvm\_EthernetSwitchPortOffloadSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="f2102-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f2102-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f2102-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f2102-110">Properties</span></span>

<span data-ttu-id="f2102-111">La classe **MSVM \_ EthernetSwitchPortOffloadSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="f2102-111">The **Msvm\_EthernetSwitchPortOffloadSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f2102-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f2102-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2102-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f2102-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2102-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f2102-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2102-115">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f2102-115">A short description of the object.</span></span> <span data-ttu-id="f2102-116">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et elle est toujours définie sur « paramètres de déchargement de port de commutateur Ethernet ».</span><span class="sxs-lookup"><span data-stu-id="f2102-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Offload Settings".</span></span>

</dd> <dt>

<span data-ttu-id="f2102-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="f2102-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2102-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f2102-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2102-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f2102-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2102-120">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="f2102-120">A description of the object.</span></span> <span data-ttu-id="f2102-121">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et elle est toujours définie sur « représente le paramètre de fonctionnalité de déchargement de port données. ».</span><span class="sxs-lookup"><span data-stu-id="f2102-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port offload feature setting data.".</span></span>

</dd> <dt>

<span data-ttu-id="f2102-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f2102-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2102-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f2102-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2102-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f2102-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2102-125">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f2102-125">A display name for the object.</span></span> <span data-ttu-id="f2102-126">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et elle est toujours définie sur « paramètres de déchargement de port de commutateur Ethernet ».</span><span class="sxs-lookup"><span data-stu-id="f2102-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Offload Settings".</span></span>

</dd> <dt>

<span data-ttu-id="f2102-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f2102-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2102-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f2102-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2102-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f2102-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2102-130">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="f2102-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f2102-131">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="f2102-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f2102-132">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f2102-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f2102-133">**IOVInterruptModeration**</span><span class="sxs-lookup"><span data-stu-id="f2102-133">**IOVInterruptModeration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2102-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f2102-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2102-135">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f2102-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f2102-136">Qualificateurs : **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f2102-136">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f2102-137">Valeur de modération de l’interruption pour le déchargement des e/s (IOV).</span><span class="sxs-lookup"><span data-stu-id="f2102-137">The interrupt moderation value for I/O virtualization (IOV) offloading.</span></span> <span data-ttu-id="f2102-138">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="f2102-138">The default is 0.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="f2102-139">**Valeur par défaut** (0)</span><span class="sxs-lookup"><span data-stu-id="f2102-139">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Adaptive"></span><span id="adaptive"></span><span id="ADAPTIVE"></span>

<span data-ttu-id="f2102-140">**Adaptative** (1)</span><span class="sxs-lookup"><span data-stu-id="f2102-140">**Adaptive** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="f2102-141">**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="f2102-141">**Off** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="f2102-142">**Faible** (100)</span><span class="sxs-lookup"><span data-stu-id="f2102-142">**Low** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="f2102-143">**Moyenne** (200)</span><span class="sxs-lookup"><span data-stu-id="f2102-143">**Medium** (200)</span></span>


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="f2102-144">**Élevé** (300)</span><span class="sxs-lookup"><span data-stu-id="f2102-144">**High** (300)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f2102-145">**IOVOffloadWeight**</span><span class="sxs-lookup"><span data-stu-id="f2102-145">**IOVOffloadWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2102-146">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f2102-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2102-147">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f2102-147">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f2102-148">Qualificateurs : **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f2102-148">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f2102-149">Poids affecté à ce port pour le déchargement des e/s de virtualisation (IOV).</span><span class="sxs-lookup"><span data-stu-id="f2102-149">The weight assigned to this port for I/O virtualization (IOV) offloading.</span></span> <span data-ttu-id="f2102-150">Le poids est l’importance relative lors de l’affectation de ressources IOV.</span><span class="sxs-lookup"><span data-stu-id="f2102-150">The weight is the relative importance when assigning IOV resources.</span></span> <span data-ttu-id="f2102-151">L’affectation de la valeur 0 à la propriété **IOVOffloadWeight** désactive le déchargement IOV sur le port.</span><span class="sxs-lookup"><span data-stu-id="f2102-151">Setting the **IOVOffloadWeight** property to 0 disables IOV offloading on the port.</span></span> <span data-ttu-id="f2102-152">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="f2102-152">The default is 0.</span></span>

</dd> <dt>

<span data-ttu-id="f2102-153">**IOVQueuePairsRequested**</span><span class="sxs-lookup"><span data-stu-id="f2102-153">**IOVQueuePairsRequested**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2102-154">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f2102-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2102-155">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f2102-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f2102-156">Qualificateurs : **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f2102-156">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f2102-157">Nombre de paires de files d’attente demandées pour ce port pour le déchargement des e/s (IOV).</span><span class="sxs-lookup"><span data-stu-id="f2102-157">The number of queue pairs requested for this port for I/O virtualization (IOV) offloading.</span></span> <span data-ttu-id="f2102-158">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="f2102-158">The default is 1.</span></span>

</dd> <dt>

<span data-ttu-id="f2102-159">**IPSecOffloadLimit**</span><span class="sxs-lookup"><span data-stu-id="f2102-159">**IPSecOffloadLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2102-160">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f2102-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2102-161">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f2102-161">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f2102-162">Qualificateurs : **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f2102-162">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f2102-163">Nombre maximal d’emplacements de déchargement d’association de sécurité (SA) autorisés à partir du port.</span><span class="sxs-lookup"><span data-stu-id="f2102-163">The maximum number of security association (SA) offload slots allowed from the port.</span></span>

</dd> <dt>

<span data-ttu-id="f2102-164">**PacketDirectModerationCount**</span><span class="sxs-lookup"><span data-stu-id="f2102-164">**PacketDirectModerationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2102-165">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f2102-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2102-166">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f2102-166">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f2102-167">Qualificateurs : **WmiDataId** (7), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f2102-167">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f2102-168">Valeur du nombre de modération des interruptions pour Packet direct (PD). La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="f2102-168">The interrupt moderation count value for Packet Direct (PD).The default is 0.</span></span>

> [!Note]  
> <span data-ttu-id="f2102-169">Propriété ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f2102-169">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="f2102-170">**PacketDirectModerationInterval**</span><span class="sxs-lookup"><span data-stu-id="f2102-170">**PacketDirectModerationInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2102-171">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f2102-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2102-172">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f2102-172">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f2102-173">Qualificateurs : **WmiDataId** (8), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f2102-173">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f2102-174">Valeur de l’intervalle de modération des interruptions pour Packet direct (PD). La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="f2102-174">The interrupt moderation interval value for Packet Direct (PD).The default is 0.</span></span>

> [!Note]  
> <span data-ttu-id="f2102-175">Propriété ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f2102-175">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="f2102-176">**PacketDirectNumProcs**</span><span class="sxs-lookup"><span data-stu-id="f2102-176">**PacketDirectNumProcs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2102-177">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f2102-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2102-178">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f2102-178">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f2102-179">Qualificateurs : **WmiDataId** (6), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f2102-179">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f2102-180">Nombre de processeurs utilisés par l’hôte pour traiter les paquets envoyés à partir de ce port en mode paquet direct.</span><span class="sxs-lookup"><span data-stu-id="f2102-180">The number of processors used by the host for processing packets sent from this port in Packet Direct mode.</span></span> <span data-ttu-id="f2102-181">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="f2102-181">The default is 1.</span></span>

> [!Note]  
> <span data-ttu-id="f2102-182">Propriété ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f2102-182">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="f2102-183">**VmmqEnabled**</span><span class="sxs-lookup"><span data-stu-id="f2102-183">**VmmqEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2102-184">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="f2102-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f2102-185">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f2102-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f2102-186">Qualificateurs : **WmiDataId** (10), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f2102-186">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f2102-187">Activez le déchargement VMMQ s’il est pris en charge par le matériel. La valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="f2102-187">Enable VMMQ offload if supported by hardware.The default is False.</span></span>

> [!Note]  
> <span data-ttu-id="f2102-188">Cette propriété a été ajoutée dans Windows 10, version 1703 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="f2102-188">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="f2102-189">**VmmqQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="f2102-189">**VmmqQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2102-190">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f2102-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2102-191">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f2102-191">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f2102-192">Qualificateurs : **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f2102-192">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f2102-193">Nombre de files d’attente à allouer lorsque VRSS est activé.</span><span class="sxs-lookup"><span data-stu-id="f2102-193">The number of queues to allocate when VRSS is enabled.</span></span> <span data-ttu-id="f2102-194">La valeur par défaut est 16.</span><span class="sxs-lookup"><span data-stu-id="f2102-194">The default is 16.</span></span>

> [!Note]  
> <span data-ttu-id="f2102-195">Cette propriété a été ajoutée dans Windows 10, version 1703 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="f2102-195">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="f2102-196">**VMQOffloadWeight**</span><span class="sxs-lookup"><span data-stu-id="f2102-196">**VMQOffloadWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2102-197">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f2102-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2102-198">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f2102-198">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f2102-199">Qualificateurs : **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f2102-199">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f2102-200">Poids attribué à ce port pour le déchargement de la file d’attente d’ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="f2102-200">The weight assigned to this port for virtual machine queue (VMQ) offloading.</span></span> <span data-ttu-id="f2102-201">Le poids est l’importance relative lors de l’affectation de ressources d’ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="f2102-201">The weight is the relative importance when assigning VMQ resources.</span></span> <span data-ttu-id="f2102-202">Si vous affectez la valeur 0 à la propriété **VMQOffloadWeight** , la valeur de la propriété de l’ordinateurs virtuels est désactivée</span><span class="sxs-lookup"><span data-stu-id="f2102-202">Setting the **VMQOffloadWeight** property to 0 disables VMQ on the port.</span></span> <span data-ttu-id="f2102-203">La valeur par défaut est 100.</span><span class="sxs-lookup"><span data-stu-id="f2102-203">The default is 100.</span></span>

</dd> <dt>

<span data-ttu-id="f2102-204">**VrssEnabled**</span><span class="sxs-lookup"><span data-stu-id="f2102-204">**VrssEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2102-205">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="f2102-205">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f2102-206">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f2102-206">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f2102-207">Qualificateurs : **WmiDataId** (9), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f2102-207">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f2102-208">Activez VRSS.</span><span class="sxs-lookup"><span data-stu-id="f2102-208">Enable VRSS.</span></span> <span data-ttu-id="f2102-209">La valeur par défaut est true.</span><span class="sxs-lookup"><span data-stu-id="f2102-209">The default is true.</span></span>

> [!Note]  
> <span data-ttu-id="f2102-210">Cette propriété a été ajoutée dans Windows 10, version 1703 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="f2102-210">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="f2102-211">**VrssExcludePrimaryProcessor**</span><span class="sxs-lookup"><span data-stu-id="f2102-211">**VrssExcludePrimaryProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2102-212">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="f2102-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f2102-213">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f2102-213">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f2102-214">Qualificateurs : **WmiDataId** (14), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f2102-214">Qualifiers: **WmiDataId** (14), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f2102-215">Indique s’il faut exclure le processeur d’ordinateurs virtuels principal de la table d’indirection VRSS lorsque VRSS est activé. La valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="f2102-215">Whether to exclude primary VMQ processor from the VRSS indirection table when VRSS is enabled.The default is false.</span></span>

> [!Note]  
> <span data-ttu-id="f2102-216">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="f2102-216">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="f2102-217">**VrssIndependentHostSpreading**</span><span class="sxs-lookup"><span data-stu-id="f2102-217">**VrssIndependentHostSpreading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2102-218">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="f2102-218">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f2102-219">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f2102-219">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f2102-220">Qualificateurs : **WmiDataId** (15), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f2102-220">Qualifiers: **WmiDataId** (15), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f2102-221">Indique s’il faut toujours exécuter VRSS côté hôte lorsque VRSS est activé, quel que soit le paramètre RSS de la carte réseau virtuelle. La valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="f2102-221">Whether to always do host-side VRSS when VRSS is enabled, regardless of RSS setting of the virtual NIC.The default is false.</span></span>

> [!Note]  
> <span data-ttu-id="f2102-222">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="f2102-222">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="f2102-223">**VrssMinQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="f2102-223">**VrssMinQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2102-224">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f2102-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2102-225">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f2102-225">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f2102-226">Qualificateurs : **WmiDataId** (12), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f2102-226">Qualifiers: **WmiDataId** (12), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f2102-227">Nombre minimal de files d’attente à allouer lorsque VRSS est activé. La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="f2102-227">The minimum number of queues to allocate when VRSS is enabled.The default is 1.</span></span>

> [!Note]  
> <span data-ttu-id="f2102-228">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="f2102-228">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="f2102-229">**VrssQueueSchedulingMode**</span><span class="sxs-lookup"><span data-stu-id="f2102-229">**VrssQueueSchedulingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2102-230">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f2102-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2102-231">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f2102-231">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f2102-232">Qualificateurs : **WmiDataId** (13), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f2102-232">Qualifiers: **WmiDataId** (13), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f2102-233">Mode de planification de la file d’attente à utiliser lorsque le VRSS est activé. La valeur par défaut est la planification statique.</span><span class="sxs-lookup"><span data-stu-id="f2102-233">The queue scheduling mode to use when VRSS is enabled.The default is static scheduling.</span></span>

> [!Note]  
> <span data-ttu-id="f2102-234">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="f2102-234">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="f2102-235">**VrssVmbusChannelAffinityPolicy**</span><span class="sxs-lookup"><span data-stu-id="f2102-235">**VrssVmbusChannelAffinityPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2102-236">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f2102-236">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2102-237">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f2102-237">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f2102-238">Qualificateurs : **WmiDataId** (16), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f2102-238">Qualifiers: **WmiDataId** (16), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f2102-239">Stratégie d’affinité du canal VMBus à utiliser lorsque le paramètre VRSS est activé. La valeur par défaut est Strong.</span><span class="sxs-lookup"><span data-stu-id="f2102-239">The vmbus channel affinity policy to use when VRSS is enabled.The default is strong.</span></span>

> [!Note]  
> <span data-ttu-id="f2102-240">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="f2102-240">Added in Windows 10, version 1709.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f2102-241">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2102-241">Requirements</span></span>



| <span data-ttu-id="f2102-242">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2102-242">Requirement</span></span> | <span data-ttu-id="f2102-243">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2102-243">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2102-244">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2102-244">Minimum supported client</span></span><br/> | <span data-ttu-id="f2102-245">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2102-245">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f2102-246">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2102-246">Minimum supported server</span></span><br/> | <span data-ttu-id="f2102-247">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2102-247">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f2102-248">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f2102-248">Namespace</span></span><br/>                | <span data-ttu-id="f2102-249">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="f2102-249">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f2102-250">MOF</span><span class="sxs-lookup"><span data-stu-id="f2102-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2102-251"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2102-251"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2102-252">DLL</span><span class="sxs-lookup"><span data-stu-id="f2102-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2102-253"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f2102-253"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

