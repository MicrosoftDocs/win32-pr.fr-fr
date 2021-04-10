---
description: Représente l’état configuré d’un périphérique de partition GPU.
ms.assetid: 33ec4ea2-4e79-4c84-8abe-da8308ad6702
title: Classe Msvm_GpuPartitionSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GpuPartitionSettingData
- Msvm_GpuPartitionSettingData.MinPartitionVRAM
- Msvm_GpuPartitionSettingData.MaxPartitionVRAM
- Msvm_GpuPartitionSettingData.OptimalPartitionVRAM
- Msvm_GpuPartitionSettingData.MinPartitionEncode
- Msvm_GpuPartitionSettingData.MaxPartitionEncode
- Msvm_GpuPartitionSettingData.OptimalPartitionEncode
- Msvm_GpuPartitionSettingData.MinPartitionDecode
- Msvm_GpuPartitionSettingData.MaxPartitionDecode
- Msvm_GpuPartitionSettingData.OptimalPartitionDecode
- Msvm_GpuPartitionSettingData.MinPartitionCompute
- Msvm_GpuPartitionSettingData.MaxPartitionCompute
- Msvm_GpuPartitionSettingData.OptimalPartitionCompute
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7d8c9809b3a062654eaf0fb7a73b75b0188f7284
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951288"
---
# <a name="msvm_gpupartitionsettingdata-class"></a><span data-ttu-id="0489b-103">MSVM \_ GpuPartitionSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="0489b-103">Msvm\_GpuPartitionSettingData class</span></span>

<span data-ttu-id="0489b-104">Représente l’état configuré d’un périphérique de partition GPU.</span><span class="sxs-lookup"><span data-stu-id="0489b-104">Represents the configured state of a GPU partition device.</span></span>

<span data-ttu-id="0489b-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0489b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0489b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0489b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GpuPartitionSettingData : CIM_ResourceAllocationSettingData
{
  uint64 MinPartitionVRAM;
  uint64 MaxPartitionVRAM;
  uint64 OptimalPartitionVRAM;
  uint64 MinPartitionEncode;
  uint64 MaxPartitionEncode;
  uint64 OptimalPartitionEncode;
  uint64 MinPartitionDecode;
  uint64 MaxPartitionDecode;
  uint64 OptimalPartitionDecode;
  uint64 MinPartitionCompute;
  uint64 MaxPartitionCompute;
  uint64 OptimalPartitionCompute;
};
```

## <a name="members"></a><span data-ttu-id="0489b-107">Membres</span><span class="sxs-lookup"><span data-stu-id="0489b-107">Members</span></span>

<span data-ttu-id="0489b-108">La classe **MSVM \_ GpuPartitionSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0489b-108">The **Msvm\_GpuPartitionSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="0489b-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0489b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0489b-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0489b-110">Properties</span></span>

<span data-ttu-id="0489b-111">La classe **MSVM \_ GpuPartitionSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="0489b-111">The **Msvm\_GpuPartitionSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0489b-112">**MaxPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="0489b-112">**MaxPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0489b-113">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0489b-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0489b-114">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0489b-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0489b-115">Quantité maximale de moteurs de calcul qui s’affichera dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="0489b-115">The maximum amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="0489b-116">**MaxPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="0489b-116">**MaxPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0489b-117">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0489b-117">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0489b-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0489b-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0489b-119">Quantité maximale de moteurs de décodage qui s’affichent dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="0489b-119">The maximum amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="0489b-120">**MaxPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="0489b-120">**MaxPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0489b-121">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0489b-121">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0489b-122">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0489b-122">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0489b-123">Quantité maximale de moteurs d’encodage qui s’affiche dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="0489b-123">The maximum amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="0489b-124">**MaxPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="0489b-124">**MaxPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0489b-125">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0489b-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0489b-126">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0489b-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0489b-127">Quantité maximale de VRAM qui s’affichera dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="0489b-127">The maximum amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="0489b-128">**MinPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="0489b-128">**MinPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0489b-129">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0489b-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0489b-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0489b-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0489b-131">Quantité minimale de moteurs de calcul qui s’affichera dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="0489b-131">The minumum amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="0489b-132">**MinPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="0489b-132">**MinPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0489b-133">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0489b-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0489b-134">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0489b-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0489b-135">Quantité minimale de moteurs de décodage qui s’affichent dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="0489b-135">The minimum amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="0489b-136">**MinPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="0489b-136">**MinPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0489b-137">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0489b-137">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0489b-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0489b-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0489b-139">Quantité minimale de moteurs d’encodage qui s’affiche dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="0489b-139">The minimum amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="0489b-140">**MinPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="0489b-140">**MinPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0489b-141">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0489b-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0489b-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0489b-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0489b-143">Quantité minimale de VRAM qui apparaîtra dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="0489b-143">The minimum amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="0489b-144">**OptimalPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="0489b-144">**OptimalPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0489b-145">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0489b-145">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0489b-146">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0489b-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0489b-147">Quantité optimale de moteurs de calcul qui s’affichera dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="0489b-147">The optimal amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="0489b-148">**OptimalPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="0489b-148">**OptimalPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0489b-149">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0489b-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0489b-150">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0489b-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0489b-151">Quantité optimale de moteurs de décodage qui s’affichent dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="0489b-151">The optimal amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="0489b-152">**OptimalPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="0489b-152">**OptimalPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0489b-153">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0489b-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0489b-154">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0489b-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0489b-155">Quantité optimale de moteurs d’encodage qui s’affiche dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="0489b-155">The optimal amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="0489b-156">**OptimalPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="0489b-156">**OptimalPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0489b-157">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0489b-157">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0489b-158">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0489b-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0489b-159">Quantité optimale de VRAM qui apparaîtra dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="0489b-159">The optimal amount of VRAM which will appear in the GPU partition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0489b-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0489b-160">Requirements</span></span>



| <span data-ttu-id="0489b-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0489b-161">Requirement</span></span> | <span data-ttu-id="0489b-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="0489b-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0489b-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0489b-163">Minimum supported client</span></span><br/> | <span data-ttu-id="0489b-164">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0489b-164">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0489b-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0489b-165">Minimum supported server</span></span><br/> | <span data-ttu-id="0489b-166">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0489b-166">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="0489b-167">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0489b-167">Namespace</span></span><br/>                | <span data-ttu-id="0489b-168">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="0489b-168">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0489b-169">MOF</span><span class="sxs-lookup"><span data-stu-id="0489b-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0489b-170"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0489b-170"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0489b-171">DLL</span><span class="sxs-lookup"><span data-stu-id="0489b-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0489b-172"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0489b-172"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0489b-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0489b-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0489b-174">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="0489b-174">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




