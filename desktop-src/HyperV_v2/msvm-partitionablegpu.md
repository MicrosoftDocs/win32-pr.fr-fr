---
description: Représente un GPU partitionné. Chaque GPU peut être divisé en plusieurs partitions GPU, qui peuvent être attribuées à un ordinateur virtuel en tant que processeur graphique virtuel.
ms.assetid: a32dfc03-6967-4fa3-ae32-bf074137740b
title: Classe Msvm_PartitionableGpu
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PartitionableGpu
- Msvm_PartitionableGpu.ValidPartitionCounts
- Msvm_PartitionableGpu.PartitionCount
- Msvm_PartitionableGpu.TotalVRAM
- Msvm_PartitionableGpu.AvailableVRAM
- Msvm_PartitionableGpu.MinPartitionVRAM
- Msvm_PartitionableGpu.MaxPartitionVRAM
- Msvm_PartitionableGpu.OptimalPartitionVRAM
- Msvm_PartitionableGpu.TotalEncode
- Msvm_PartitionableGpu.AvailableEncode
- Msvm_PartitionableGpu.MinPartitionEncode
- Msvm_PartitionableGpu.MaxPartitionEncode
- Msvm_PartitionableGpu.OptimalPartitionEncode
- Msvm_PartitionableGpu.TotalDecode
- Msvm_PartitionableGpu.AvailableDecode
- Msvm_PartitionableGpu.MinPartitionDecode
- Msvm_PartitionableGpu.MaxPartitionDecode
- Msvm_PartitionableGpu.OptimalPartitionDecode
- Msvm_PartitionableGpu.TotalCompute
- Msvm_PartitionableGpu.AvailableCompute
- Msvm_PartitionableGpu.MinPartitionCompute
- Msvm_PartitionableGpu.MaxPartitionCompute
- Msvm_PartitionableGpu.OptimalPartitionCompute
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7f82904608a8e2ee4dfa13942066d57d35d511f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868494"
---
# <a name="msvm_partitionablegpu-class"></a><span data-ttu-id="52980-104">MSVM \_ PartitionableGpu, classe</span><span class="sxs-lookup"><span data-stu-id="52980-104">Msvm\_PartitionableGpu class</span></span>

<span data-ttu-id="52980-105">Représente un GPU partitionné.</span><span class="sxs-lookup"><span data-stu-id="52980-105">Represents a partitionable GPU.</span></span> <span data-ttu-id="52980-106">Chaque GPU peut être divisé en plusieurs partitions GPU, qui peuvent être attribuées à un ordinateur virtuel en tant que processeur graphique virtuel.</span><span class="sxs-lookup"><span data-stu-id="52980-106">Each GPU can be sliced into a number of GPU partitions, which can be assigned to a virtual machine as a vGPU.</span></span>

<span data-ttu-id="52980-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="52980-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="52980-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52980-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PartitionableGpu : CIM_ComputerSystem
{
  uint16 ValidPartitionCounts[];
  uint16 PartitionCount;
  uint64 TotalVRAM;
  uint64 AvailableVRAM;
  uint64 MinPartitionVRAM;
  uint64 MaxPartitionVRAM;
  uint64 OptimalPartitionVRAM;
  uint64 TotalEncode;
  uint64 AvailableEncode;
  uint64 MinPartitionEncode;
  uint64 MaxPartitionEncode;
  uint64 OptimalPartitionEncode;
  uint64 TotalDecode;
  uint64 AvailableDecode;
  uint64 MinPartitionDecode;
  uint64 MaxPartitionDecode;
  uint64 OptimalPartitionDecode;
  uint64 TotalCompute;
  uint64 AvailableCompute;
  uint64 MinPartitionCompute;
  uint64 MaxPartitionCompute;
  uint64 OptimalPartitionCompute;
};
```

## <a name="members"></a><span data-ttu-id="52980-109">Membres</span><span class="sxs-lookup"><span data-stu-id="52980-109">Members</span></span>

<span data-ttu-id="52980-110">La classe **MSVM \_ PartitionableGpu** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="52980-110">The **Msvm\_PartitionableGpu** class has these types of members:</span></span>

-   [<span data-ttu-id="52980-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="52980-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="52980-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="52980-112">Properties</span></span>

<span data-ttu-id="52980-113">La classe **MSVM \_ PartitionableGpu** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="52980-113">The **Msvm\_PartitionableGpu** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="52980-114">**AvailableCompute**</span><span class="sxs-lookup"><span data-stu-id="52980-114">**AvailableCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52980-115">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52980-115">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52980-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52980-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52980-117">Quantité de moteurs de calcul disponibles qui s’affiche dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="52980-117">The available amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="52980-118">**AvailableDecode**</span><span class="sxs-lookup"><span data-stu-id="52980-118">**AvailableDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52980-119">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52980-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52980-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52980-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52980-121">Quantité de moteurs de décodage disponibles qui apparaîtra dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="52980-121">The available amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="52980-122">**AvailableEncode**</span><span class="sxs-lookup"><span data-stu-id="52980-122">**AvailableEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52980-123">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52980-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52980-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52980-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52980-125">Quantité de moteurs d’encodage disponibles qui s’affiche dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="52980-125">The available amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="52980-126">**AvailableVRAM**</span><span class="sxs-lookup"><span data-stu-id="52980-126">**AvailableVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52980-127">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52980-127">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52980-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52980-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52980-129">Quantité de VRAM disponible qui s’affiche dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="52980-129">The available amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="52980-130">**MaxPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="52980-130">**MaxPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52980-131">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52980-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52980-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52980-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52980-133">Quantité maximale de moteurs de calcul qui s’affichera dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="52980-133">The maximum amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="52980-134">**MaxPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="52980-134">**MaxPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52980-135">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52980-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52980-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52980-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52980-137">Quantité maximale de moteurs de décodage qui s’affichent dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="52980-137">The maximum amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="52980-138">**MaxPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="52980-138">**MaxPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52980-139">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52980-139">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52980-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52980-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52980-141">Quantité maximale de moteurs d’encodage qui s’affiche dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="52980-141">The maximum amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="52980-142">**MaxPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="52980-142">**MaxPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52980-143">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52980-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52980-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52980-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52980-145">Quantité maximale de VRAM qui s’affichera dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="52980-145">The maximum amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="52980-146">**MinPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="52980-146">**MinPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52980-147">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52980-147">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52980-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52980-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52980-149">Quantité minimale de moteurs de calcul qui s’affichera dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="52980-149">The minumum amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="52980-150">**MinPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="52980-150">**MinPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52980-151">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52980-151">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52980-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52980-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52980-153">Quantité minimale de moteurs de décodage qui s’affichent dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="52980-153">The minimum amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="52980-154">**MinPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="52980-154">**MinPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52980-155">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52980-155">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52980-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52980-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52980-157">Quantité minimale de moteurs d’encodage qui s’affiche dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="52980-157">The minumum amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="52980-158">**MinPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="52980-158">**MinPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52980-159">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52980-159">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52980-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52980-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52980-161">Quantité minimale de VRAM qui apparaîtra dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="52980-161">The minimum amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="52980-162">**OptimalPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="52980-162">**OptimalPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52980-163">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52980-163">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52980-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52980-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52980-165">Quantité optimale de moteurs de calcul qui s’affichera dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="52980-165">The optimal amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="52980-166">**OptimalPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="52980-166">**OptimalPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52980-167">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52980-167">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52980-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52980-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52980-169">Quantité optimale de moteurs de décodage qui s’affichent dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="52980-169">The optimal amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="52980-170">**OptimalPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="52980-170">**OptimalPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52980-171">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52980-171">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52980-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52980-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52980-173">Quantité optimale de moteurs d’encodage qui s’affiche dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="52980-173">The optimal amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="52980-174">**OptimalPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="52980-174">**OptimalPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52980-175">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52980-175">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52980-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52980-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52980-177">Quantité optimale de VRAM qui apparaîtra dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="52980-177">The optimal amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="52980-178">**PartitionCount**</span><span class="sxs-lookup"><span data-stu-id="52980-178">**PartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52980-179">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52980-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="52980-180">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52980-180">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="52980-181">Quantité de partitions GPU dans laquelle le GPU physique est découpé.</span><span class="sxs-lookup"><span data-stu-id="52980-181">The amount of GPU partitions the physical GPU is sliced into.</span></span>

</dd> <dt>

<span data-ttu-id="52980-182">**TotalCompute**</span><span class="sxs-lookup"><span data-stu-id="52980-182">**TotalCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52980-183">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52980-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52980-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52980-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52980-185">Quantité totale de moteurs de calcul qui s’affichera dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="52980-185">The total amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="52980-186">**TotalDecode**</span><span class="sxs-lookup"><span data-stu-id="52980-186">**TotalDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52980-187">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52980-187">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52980-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52980-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52980-189">Quantité totale de moteurs de décodage qui s’affichent dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="52980-189">The total amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="52980-190">**TotalEncode**</span><span class="sxs-lookup"><span data-stu-id="52980-190">**TotalEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52980-191">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52980-191">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52980-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52980-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52980-193">Quantité totale de moteurs d’encodage qui s’affiche dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="52980-193">The total amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="52980-194">**TotalVRAM**</span><span class="sxs-lookup"><span data-stu-id="52980-194">**TotalVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52980-195">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52980-195">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52980-196">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52980-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52980-197">Quantité totale de VRAM qui s’affichera dans la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="52980-197">The total amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="52980-198">**ValidPartitionCounts**</span><span class="sxs-lookup"><span data-stu-id="52980-198">**ValidPartitionCounts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52980-199">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52980-199">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="52980-200">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52980-200">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="52980-201">Tableau des options de partition GPU valides dans lesquelles le GPU physique peut être découpé.</span><span class="sxs-lookup"><span data-stu-id="52980-201">An array of valid GPU partition options the physical GPU can be sliced into.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="52980-202">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52980-202">Requirements</span></span>



| <span data-ttu-id="52980-203">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52980-203">Requirement</span></span> | <span data-ttu-id="52980-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="52980-204">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52980-205">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52980-205">Minimum supported client</span></span><br/> | <span data-ttu-id="52980-206">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52980-206">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="52980-207">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52980-207">Minimum supported server</span></span><br/> | <span data-ttu-id="52980-208">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="52980-208">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="52980-209">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="52980-209">Namespace</span></span><br/>                | <span data-ttu-id="52980-210">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="52980-210">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="52980-211">MOF</span><span class="sxs-lookup"><span data-stu-id="52980-211">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52980-212"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="52980-212"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="52980-213">DLL</span><span class="sxs-lookup"><span data-stu-id="52980-213">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52980-214"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="52980-214"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="52980-215">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52980-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52980-216">**\_ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="52980-216">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> </dl>

 

 




