---
description: Représente les paramètres spécifiques au stockage pour un système virtuel.
ms.assetid: 0b3fcd78-7e9a-4a94-ad18-0ca72b3cfd73
title: Classe Msvm_StorageSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageSettingData
- Msvm_StorageSettingData.VirtualProcessorsPerChannel
- Msvm_StorageSettingData.DisableInterruptBatching
- Msvm_StorageSettingData.ThreadCountPerChannel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: db061d048ce45a4d6fa076a5b0367e794cdf16e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538390"
---
# <a name="msvm_storagesettingdata-class"></a><span data-ttu-id="ed1b9-103">MSVM \_ StorageSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="ed1b9-103">Msvm\_StorageSettingData class</span></span>

<span data-ttu-id="ed1b9-104">Représente les paramètres spécifiques au stockage pour un système virtuel.</span><span class="sxs-lookup"><span data-stu-id="ed1b9-104">Represents the storage-specific settings for a virtual system.</span></span>

<span data-ttu-id="ed1b9-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ed1b9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed1b9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed1b9-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageSettingData : Msvm_SystemComponentSettingData
{
  uint16  VirtualProcessorsPerChannel;
  boolean DisableInterruptBatching;
  uint16  ThreadCountPerChannel;
};
```

## <a name="members"></a><span data-ttu-id="ed1b9-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ed1b9-107">Members</span></span>

<span data-ttu-id="ed1b9-108">La classe **MSVM \_ StorageSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ed1b9-108">The **Msvm\_StorageSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="ed1b9-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ed1b9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ed1b9-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ed1b9-110">Properties</span></span>

<span data-ttu-id="ed1b9-111">La classe **MSVM \_ StorageSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ed1b9-111">The **Msvm\_StorageSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ed1b9-112">**DisableInterruptBatching**</span><span class="sxs-lookup"><span data-stu-id="ed1b9-112">**DisableInterruptBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed1b9-113">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ed1b9-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ed1b9-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ed1b9-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed1b9-115">Spécifie si le traitement par lots des interruptions doit être désactivé.</span><span class="sxs-lookup"><span data-stu-id="ed1b9-115">Specifies whether interrupt batching should be disabled.</span></span>

<span data-ttu-id="ed1b9-116">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) de la classe WMI [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="ed1b9-116">This is a read-only property, but it can be changed using the [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) method of the Wmi [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="ed1b9-117">**ThreadCountPerChannel**</span><span class="sxs-lookup"><span data-stu-id="ed1b9-117">**ThreadCountPerChannel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed1b9-118">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ed1b9-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ed1b9-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ed1b9-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed1b9-120">Nombre de threads par canal de stockage pour traiter les e/s.</span><span class="sxs-lookup"><span data-stu-id="ed1b9-120">The number of threads per storage channel to process IO.</span></span>

<span data-ttu-id="ed1b9-121">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="ed1b9-121">This is a read-only property, but it can be changed using the [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="ed1b9-122"><span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Valeur par défaut** (0)</span><span class="sxs-lookup"><span data-stu-id="ed1b9-122"><span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Default** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ed1b9-123">Comportement par défaut</span><span class="sxs-lookup"><span data-stu-id="ed1b9-123">Default behavior</span></span>

</dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="ed1b9-124"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Faible** (1)</span><span class="sxs-lookup"><span data-stu-id="ed1b9-124"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ed1b9-125">Nombre de threads faible par canal de stockage.</span><span class="sxs-lookup"><span data-stu-id="ed1b9-125">Low number of threads per storage channel.</span></span>

</dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="ed1b9-126"><span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Moyenne** (2)</span><span class="sxs-lookup"><span data-stu-id="ed1b9-126"><span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Medium** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ed1b9-127">Nombre moyen de threads par canal de stockage.</span><span class="sxs-lookup"><span data-stu-id="ed1b9-127">Medium number of threads per storage channel.</span></span>

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="ed1b9-128"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**Élevé** (3)</span><span class="sxs-lookup"><span data-stu-id="ed1b9-128"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**High** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ed1b9-129">Nombre élevé de threads par canal de stockage.</span><span class="sxs-lookup"><span data-stu-id="ed1b9-129">High number of threads per storage channel.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ed1b9-130">**VirtualProcessorsPerChannel**</span><span class="sxs-lookup"><span data-stu-id="ed1b9-130">**VirtualProcessorsPerChannel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed1b9-131">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ed1b9-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ed1b9-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ed1b9-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed1b9-133">Nombre de processeurs par canal de stockage.</span><span class="sxs-lookup"><span data-stu-id="ed1b9-133">The number of processors per storage channel.</span></span> <span data-ttu-id="ed1b9-134">Le nombre de canaux à ouvrir est donné par (nombre de processeurs logiques sur l’ordinateur hôte/**VirtualProcessorsPerChannel**).</span><span class="sxs-lookup"><span data-stu-id="ed1b9-134">The number of channels to be opened is given by (Count of logical processors on the host /**VirtualProcessorsPerChannel**).</span></span>

<span data-ttu-id="ed1b9-135">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="ed1b9-135">This is a read-only property, but it can be changed using the [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ed1b9-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ed1b9-136">Requirements</span></span>



| <span data-ttu-id="ed1b9-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ed1b9-137">Requirement</span></span> | <span data-ttu-id="ed1b9-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed1b9-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed1b9-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed1b9-139">Minimum supported client</span></span><br/> | <span data-ttu-id="ed1b9-140">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ed1b9-140">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ed1b9-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed1b9-141">Minimum supported server</span></span><br/> | <span data-ttu-id="ed1b9-142">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ed1b9-142">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ed1b9-143">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ed1b9-143">Namespace</span></span><br/>                | <span data-ttu-id="ed1b9-144">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ed1b9-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ed1b9-145">MOF</span><span class="sxs-lookup"><span data-stu-id="ed1b9-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed1b9-146"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed1b9-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed1b9-147">DLL</span><span class="sxs-lookup"><span data-stu-id="ed1b9-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed1b9-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ed1b9-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ed1b9-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed1b9-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed1b9-150">**MSVM \_ SystemComponentSettingData**</span><span class="sxs-lookup"><span data-stu-id="ed1b9-150">**Msvm\_SystemComponentSettingData**</span></span>](msvm-systemcomponentsettingdata.md)
</dt> </dl>

 

 




