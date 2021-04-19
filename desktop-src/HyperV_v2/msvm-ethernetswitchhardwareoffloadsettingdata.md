---
description: Représente les paramètres de déchargement du commutateur.
ms.assetid: 4e00544e-a8db-4337-af3f-f651bfcf6b05
title: Classe Msvm_EthernetSwitchHardwareOffloadSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchHardwareOffloadSettingData
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssEnabled
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVmmqEnabled
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVmmqQueuePairs
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssIndependentHostSpreading
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssExcludePrimaryProcessor
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssQueueSchedulingMode
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssMinQueuePairs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86ef0e22143ffd424ee3acee616504e45d8125bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543140"
---
# <a name="msvm_ethernetswitchhardwareoffloadsettingdata-class"></a><span data-ttu-id="0cb84-103">MSVM \_ EthernetSwitchHardwareOffloadSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="0cb84-103">Msvm\_EthernetSwitchHardwareOffloadSettingData class</span></span>

<span data-ttu-id="0cb84-104">Représente les paramètres de déchargement du commutateur.</span><span class="sxs-lookup"><span data-stu-id="0cb84-104">Represents the switch offload settings.</span></span>

<span data-ttu-id="0cb84-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0cb84-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cb84-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0cb84-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("1550e863-4337-4917-a040-5a27dbc58b59"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("2"), InterfaceRevision("0"), DisplayName("Ethernet Switch Hardware Offload Settings"), AMENDMENT]
class Msvm_EthernetSwitchHardwareOffloadSettingData : Msvm_EthernetSwitchFeatureSettingData
{
  boolean DefaultQueueVrssEnabled = TRUE;
  boolean DefaultQueueVmmqEnabled = FALSE;
  uint32  DefaultQueueVmmqQueuePairs = 16;
  boolean DefaultQueueVrssIndependentHostSpreading = TRUE;
  boolean DefaultQueueVrssExcludePrimaryProcessor = FALSE;
  uint32  DefaultQueueVrssQueueSchedulingMode = 2;
  uint32  DefaultQueueVrssMinQueuePairs = 1;
};
```

## <a name="members"></a><span data-ttu-id="0cb84-107">Membres</span><span class="sxs-lookup"><span data-stu-id="0cb84-107">Members</span></span>

<span data-ttu-id="0cb84-108">La classe **MSVM \_ EthernetSwitchHardwareOffloadSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0cb84-108">The **Msvm\_EthernetSwitchHardwareOffloadSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="0cb84-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0cb84-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0cb84-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0cb84-110">Properties</span></span>

<span data-ttu-id="0cb84-111">La classe **MSVM \_ EthernetSwitchHardwareOffloadSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="0cb84-111">The **Msvm\_EthernetSwitchHardwareOffloadSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0cb84-112">**DefaultQueueVmmqEnabled**</span><span class="sxs-lookup"><span data-stu-id="0cb84-112">**DefaultQueueVmmqEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb84-113">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0cb84-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0cb84-114">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0cb84-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0cb84-115">Qualificateurs : **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0cb84-115">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0cb84-116">Spécifie les paramètres VMMQ pour la file d’attente par défaut du vswitch.</span><span class="sxs-lookup"><span data-stu-id="0cb84-116">Specifies the VMMQ settings for the default queue of the vswitch.</span></span>

</dd> <dt>

<span data-ttu-id="0cb84-117">**DefaultQueueVmmqQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="0cb84-117">**DefaultQueueVmmqQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb84-118">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0cb84-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0cb84-119">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0cb84-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0cb84-120">Qualificateurs : **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0cb84-120">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0cb84-121">Spécifie le nombre de files d’attente pour la file d’attente par défaut.</span><span class="sxs-lookup"><span data-stu-id="0cb84-121">Specifies the number of queues for the default queue.</span></span>

</dd> <dt>

<span data-ttu-id="0cb84-122">**DefaultQueueVrssEnabled**</span><span class="sxs-lookup"><span data-stu-id="0cb84-122">**DefaultQueueVrssEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb84-123">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0cb84-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0cb84-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0cb84-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0cb84-125">Qualificateurs : **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0cb84-125">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0cb84-126">Spécifie les paramètres VRss pour la file d’attente par défaut du vswitch.</span><span class="sxs-lookup"><span data-stu-id="0cb84-126">Specifies the VRss settings for the default queue of the vswitch.</span></span>

</dd> <dt>

<span data-ttu-id="0cb84-127">**DefaultQueueVrssExcludePrimaryProcessor**</span><span class="sxs-lookup"><span data-stu-id="0cb84-127">**DefaultQueueVrssExcludePrimaryProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb84-128">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0cb84-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0cb84-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0cb84-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cb84-130">Qualificateurs : **WmiDataId** (6), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0cb84-130">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0cb84-131">Indique si l’UC de l’unité centrale principale est exclue de la table d’indirection VRSS/VMMQ.</span><span class="sxs-lookup"><span data-stu-id="0cb84-131">Indicates whether the primary VMQ CPU is excluded from the VRSS/VMMQ indirection table.</span></span>

> [!Note]  
> <span data-ttu-id="0cb84-132">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="0cb84-132">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="0cb84-133">**DefaultQueueVrssIndependentHostSpreading**</span><span class="sxs-lookup"><span data-stu-id="0cb84-133">**DefaultQueueVrssIndependentHostSpreading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb84-134">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0cb84-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0cb84-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0cb84-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cb84-136">Qualificateurs : **WmiDataId** (7), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0cb84-136">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0cb84-137">Indique s’il faut toujours effectuer la répartition VRSS pour la file d’attente par défaut, quel que soit l’État RSS du vPort externe.</span><span class="sxs-lookup"><span data-stu-id="0cb84-137">Indicates whether to always do VRSS spreading for default queue, regardless of the RSS state of the external vPort.</span></span>

> [!Note]  
> <span data-ttu-id="0cb84-138">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="0cb84-138">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="0cb84-139">**DefaultQueueVrssMinQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="0cb84-139">**DefaultQueueVrssMinQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb84-140">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0cb84-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0cb84-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0cb84-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cb84-142">Qualificateurs : **WmiDataId** (4), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0cb84-142">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0cb84-143">Indique le nombre minimal de files d’attente utilisées pour VRSS/VMMQ.</span><span class="sxs-lookup"><span data-stu-id="0cb84-143">Indicates minimum number of queues used for VRSS/VMMQ.</span></span>

> [!Note]  
> <span data-ttu-id="0cb84-144">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="0cb84-144">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="0cb84-145">**DefaultQueueVrssQueueSchedulingMode**</span><span class="sxs-lookup"><span data-stu-id="0cb84-145">**DefaultQueueVrssQueueSchedulingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb84-146">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0cb84-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0cb84-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0cb84-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cb84-148">Qualificateurs : **WmiDataId** (5), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0cb84-148">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0cb84-149">Indique comment les files d’attente VRSS/VMMQ sont directrices sur différents processeurs hôtes.</span><span class="sxs-lookup"><span data-stu-id="0cb84-149">Indicates how VRSS/VMMQ queues are steered to different host processors.</span></span>

> [!Note]  
> <span data-ttu-id="0cb84-150">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="0cb84-150">Added in Windows 10, version 1709.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0cb84-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0cb84-151">Requirements</span></span>



| <span data-ttu-id="0cb84-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0cb84-152">Requirement</span></span> | <span data-ttu-id="0cb84-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="0cb84-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cb84-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0cb84-154">Minimum supported client</span></span><br/> | <span data-ttu-id="0cb84-155">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0cb84-155">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0cb84-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0cb84-156">Minimum supported server</span></span><br/> | <span data-ttu-id="0cb84-157">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0cb84-157">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="0cb84-158">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0cb84-158">Namespace</span></span><br/>                | <span data-ttu-id="0cb84-159">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="0cb84-159">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0cb84-160">MOF</span><span class="sxs-lookup"><span data-stu-id="0cb84-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0cb84-161"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0cb84-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0cb84-162">DLL</span><span class="sxs-lookup"><span data-stu-id="0cb84-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cb84-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0cb84-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0cb84-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0cb84-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cb84-165">**MSVM \_ EthernetSwitchFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="0cb84-165">**Msvm\_EthernetSwitchFeatureSettingData**</span></span>](msvm-ethernetswitchfeaturesettingdata.md)
</dt> </dl>

 

 




