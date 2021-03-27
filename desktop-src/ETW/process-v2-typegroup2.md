---
description: Cette classe est la classe de type d’événement pour les événements de compteur de processus. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 7f1fa1c4-a2ff-4a1c-ac9d-e922a13c99a1
title: Classe Process_V2_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V2_TypeGroup2
- Process_V2_TypeGroup2.ProcessId
- Process_V2_TypeGroup2.PageFaultCount
- Process_V2_TypeGroup2.HandleCount
- Process_V2_TypeGroup2.Reserved
- Process_V2_TypeGroup2.PeakVirtualSize
- Process_V2_TypeGroup2.PeakWorkingSetSize
- Process_V2_TypeGroup2.PeakPagefileUsage
- Process_V2_TypeGroup2.QuotaPeakPagedPoolUsage
- Process_V2_TypeGroup2.QuotaPeakNonPagedPoolUsage
- Process_V2_TypeGroup2.VirtualSize
- Process_V2_TypeGroup2.WorkingSetSize
- Process_V2_TypeGroup2.PagefileUsage
- Process_V2_TypeGroup2.QuotaPagedPoolUsage
- Process_V2_TypeGroup2.QuotaNonPagedPoolUsage
- Process_V2_TypeGroup2.PrivatePageCount
api_type:
- NA
api_location: ''
ms.openlocfilehash: 284b77da03b53f9c2662c8729a7bf6606c45630a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867706"
---
# <a name="process_v2_typegroup2-class"></a><span data-ttu-id="aeef9-104">Traiter \_ la \_ classe TypeGroup2 v2</span><span class="sxs-lookup"><span data-stu-id="aeef9-104">Process\_V2\_TypeGroup2 class</span></span>

<span data-ttu-id="aeef9-105">Cette classe est la classe de type d’événement pour les événements de compteur de processus.</span><span class="sxs-lookup"><span data-stu-id="aeef9-105">This class is the event type class for process counter events.</span></span>

<span data-ttu-id="aeef9-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="aeef9-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="aeef9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aeef9-107">Syntax</span></span>

``` syntax
[EventType{32, 33}, EventTypeName{"PerfCtr", PerfCtrRundown"}]
class Process_V2_TypeGroup2 : Process_V2
{
  uint32 ProcessId;
  uint32 PageFaultCount;
  uint32 HandleCount;
  uint32 Reserved;
  object PeakVirtualSize;
  object PeakWorkingSetSize;
  object PeakPagefileUsage;
  object QuotaPeakPagedPoolUsage;
  object QuotaPeakNonPagedPoolUsage;
  object VirtualSize;
  object WorkingSetSize;
  object PagefileUsage;
  object QuotaPagedPoolUsage;
  object QuotaNonPagedPoolUsage;
  object PrivatePageCount;
};
```

## <a name="members"></a><span data-ttu-id="aeef9-108">Membres</span><span class="sxs-lookup"><span data-stu-id="aeef9-108">Members</span></span>

<span data-ttu-id="aeef9-109">La classe **process \_ v2 \_ TypeGroup2** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="aeef9-109">The **Process\_V2\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="aeef9-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="aeef9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aeef9-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="aeef9-111">Properties</span></span>

<span data-ttu-id="aeef9-112">La classe **process \_ v2 \_ TypeGroup2** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="aeef9-112">The **Process\_V2\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aeef9-113">**HandleCount**</span><span class="sxs-lookup"><span data-stu-id="aeef9-113">**HandleCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeef9-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aeef9-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aeef9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-116">Qualificateurs : WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="aeef9-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="aeef9-117">Nombre de handles utilisés.</span><span class="sxs-lookup"><span data-stu-id="aeef9-117">Count of used handles.</span></span>

</dd> <dt>

<span data-ttu-id="aeef9-118">**PageFaultCount**</span><span class="sxs-lookup"><span data-stu-id="aeef9-118">**PageFaultCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeef9-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aeef9-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aeef9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-121">Qualificateurs : WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="aeef9-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="aeef9-122">Nombre de défauts de page.</span><span class="sxs-lookup"><span data-stu-id="aeef9-122">Count of page faults.</span></span>

</dd> <dt>

<span data-ttu-id="aeef9-123">**PagefileUsage**</span><span class="sxs-lookup"><span data-stu-id="aeef9-123">**PagefileUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeef9-124">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="aeef9-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aeef9-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-126">Qualificateurs : WmiDataId (12), extension ("Sizet")</span><span class="sxs-lookup"><span data-stu-id="aeef9-126">Qualifiers: WmiDataId(12), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="aeef9-127">Utilisation du fichier d’échange actuel.</span><span class="sxs-lookup"><span data-stu-id="aeef9-127">Current page file usage.</span></span>

</dd> <dt>

<span data-ttu-id="aeef9-128">**PeakPagefileUsage**</span><span class="sxs-lookup"><span data-stu-id="aeef9-128">**PeakPagefileUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeef9-129">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="aeef9-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aeef9-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-131">Qualificateurs : WmiDataId (7), extension ("Sizet")</span><span class="sxs-lookup"><span data-stu-id="aeef9-131">Qualifiers: WmiDataId(7), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="aeef9-132">Taille de fichier d’échange la plus grande utilisée.</span><span class="sxs-lookup"><span data-stu-id="aeef9-132">Largest page file size used.</span></span>

</dd> <dt>

<span data-ttu-id="aeef9-133">**PeakVirtualSize**</span><span class="sxs-lookup"><span data-stu-id="aeef9-133">**PeakVirtualSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeef9-134">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="aeef9-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aeef9-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-136">Qualificateurs : WmiDataId (5), extension ("Sizet")</span><span class="sxs-lookup"><span data-stu-id="aeef9-136">Qualifiers: WmiDataId(5), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="aeef9-137">Taille de page virtuelle la plus grande utilisée.</span><span class="sxs-lookup"><span data-stu-id="aeef9-137">Largest virtual page size used.</span></span>

</dd> <dt>

<span data-ttu-id="aeef9-138">**PeakWorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="aeef9-138">**PeakWorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeef9-139">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="aeef9-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aeef9-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-141">Qualificateurs : WmiDataId (6), extension ("Sizet")</span><span class="sxs-lookup"><span data-stu-id="aeef9-141">Qualifiers: WmiDataId(6), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="aeef9-142">Taille de la plus grande plage de travail utilisée.</span><span class="sxs-lookup"><span data-stu-id="aeef9-142">Largest working set size used.</span></span>

</dd> <dt>

<span data-ttu-id="aeef9-143">**PrivatePageCount**</span><span class="sxs-lookup"><span data-stu-id="aeef9-143">**PrivatePageCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeef9-144">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="aeef9-144">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aeef9-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-146">Qualificateurs : WmiDataId (15), extension ("Sizet")</span><span class="sxs-lookup"><span data-stu-id="aeef9-146">Qualifiers: WmiDataId(15), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="aeef9-147">Nombre de pages physiques privées actuelles.</span><span class="sxs-lookup"><span data-stu-id="aeef9-147">Current private physical page count.</span></span>

</dd> <dt>

<span data-ttu-id="aeef9-148">ProcessId</span><span class="sxs-lookup"><span data-stu-id="aeef9-148">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeef9-149">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aeef9-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aeef9-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-151">Qualificateurs : WmiDataId (1), format ("x")</span><span class="sxs-lookup"><span data-stu-id="aeef9-151">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="aeef9-152">Identificateur de processus global que vous pouvez utiliser pour identifier un processus.</span><span class="sxs-lookup"><span data-stu-id="aeef9-152">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="aeef9-153">La valeur est valide à partir du moment où un processus est créé jusqu’à ce qu’il soit terminé.</span><span class="sxs-lookup"><span data-stu-id="aeef9-153">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="aeef9-154">**QuotaNonPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="aeef9-154">**QuotaNonPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeef9-155">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="aeef9-155">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aeef9-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-157">Qualificateurs : WmiDataId (14), extension ("Sizet")</span><span class="sxs-lookup"><span data-stu-id="aeef9-157">Qualifiers: WmiDataId(14), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="aeef9-158">Utilisation de la mémoire non paginée actuellement validée.</span><span class="sxs-lookup"><span data-stu-id="aeef9-158">Current committed non-paged memory usage.</span></span>

</dd> <dt>

<span data-ttu-id="aeef9-159">**QuotaPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="aeef9-159">**QuotaPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeef9-160">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="aeef9-160">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aeef9-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-162">Qualificateurs : WmiDataId (13), extension ("Sizet")</span><span class="sxs-lookup"><span data-stu-id="aeef9-162">Qualifiers: WmiDataId(13), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="aeef9-163">Utilisation de la mémoire paginée actuellement validée.</span><span class="sxs-lookup"><span data-stu-id="aeef9-163">Current committed paged memory usage.</span></span>

</dd> <dt>

<span data-ttu-id="aeef9-164">**QuotaPeakNonPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="aeef9-164">**QuotaPeakNonPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeef9-165">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="aeef9-165">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aeef9-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-167">Qualificateurs : WmiDataId (9), extension ("Sizet")</span><span class="sxs-lookup"><span data-stu-id="aeef9-167">Qualifiers: WmiDataId(9), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="aeef9-168">Mémoire non paginée validée la plus grande utilisée.</span><span class="sxs-lookup"><span data-stu-id="aeef9-168">Largest committed non-paged memory used.</span></span>

</dd> <dt>

<span data-ttu-id="aeef9-169">**QuotaPeakPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="aeef9-169">**QuotaPeakPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeef9-170">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="aeef9-170">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aeef9-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-172">Qualificateurs : WmiDataId (8), extension ("Sizet")</span><span class="sxs-lookup"><span data-stu-id="aeef9-172">Qualifiers: WmiDataId(8), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="aeef9-173">Mémoire paginée allouée la plus grande utilisée.</span><span class="sxs-lookup"><span data-stu-id="aeef9-173">Largest committed paged memory used.</span></span>

</dd> <dt>

<span data-ttu-id="aeef9-174">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="aeef9-174">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeef9-175">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aeef9-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aeef9-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-177">Qualificateurs : WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="aeef9-177">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="aeef9-178">Réservé.</span><span class="sxs-lookup"><span data-stu-id="aeef9-178">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="aeef9-179">**VirtualSize**</span><span class="sxs-lookup"><span data-stu-id="aeef9-179">**VirtualSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeef9-180">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="aeef9-180">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aeef9-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-182">Qualificateurs : WmiDataId (10), extension ("Sizet")</span><span class="sxs-lookup"><span data-stu-id="aeef9-182">Qualifiers: WmiDataId(10), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="aeef9-183">Taille de page virtuelle actuelle.</span><span class="sxs-lookup"><span data-stu-id="aeef9-183">Current virtual page size.</span></span>

</dd> <dt>

<span data-ttu-id="aeef9-184">**WorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="aeef9-184">**WorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeef9-185">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="aeef9-185">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aeef9-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeef9-187">Qualificateurs : WmiDataId (11), extension ("Sizet")</span><span class="sxs-lookup"><span data-stu-id="aeef9-187">Qualifiers: WmiDataId(11), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="aeef9-188">Taille actuelle de la plage de travail.</span><span class="sxs-lookup"><span data-stu-id="aeef9-188">Current working set size.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aeef9-189">Notes</span><span class="sxs-lookup"><span data-stu-id="aeef9-189">Remarks</span></span>

<span data-ttu-id="aeef9-190">Ces événements sont enregistrés lorsque le processus se termine.</span><span class="sxs-lookup"><span data-stu-id="aeef9-190">These events are logged when the process ends.</span></span> <span data-ttu-id="aeef9-191">L’événement indique comment un processus a traité l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="aeef9-191">The event indicates how a process handled memory usage.</span></span>

## <a name="requirements"></a><span data-ttu-id="aeef9-192">Spécifications</span><span class="sxs-lookup"><span data-stu-id="aeef9-192">Requirements</span></span>



| <span data-ttu-id="aeef9-193">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aeef9-193">Requirement</span></span> | <span data-ttu-id="aeef9-194">Valeur</span><span class="sxs-lookup"><span data-stu-id="aeef9-194">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="aeef9-195">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aeef9-195">Minimum supported client</span></span><br/> | <span data-ttu-id="aeef9-196">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aeef9-196">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="aeef9-197">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aeef9-197">Minimum supported server</span></span><br/> | <span data-ttu-id="aeef9-198">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aeef9-198">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aeef9-199">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aeef9-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeef9-200">**Traitement \_ v2**</span><span class="sxs-lookup"><span data-stu-id="aeef9-200">**Process\_V2**</span></span>](process-v2.md)
</dt> </dl>

 

 




