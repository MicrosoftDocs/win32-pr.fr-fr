---
title: Structure CHANGE_LOG_ENTRY
description: Entrée du journal des modifications.
ms.assetid: adbdc6e6-895e-486d-a194-c74d2cbd0052
keywords:
- Restauration du système de la structure CHANGE_LOG_ENTRY
- PCHANGE_LOG_ENTRY de la restauration du système du pointeur de structure
topic_type:
- apiref
api_name:
- CHANGE_LOG_ENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a129b7c8368e6af1d259d6c19a9dde963d9deef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032502"
---
# <a name="change_log_entry-structure"></a><span data-ttu-id="dc52a-105">Structure de l’entrée du journal des modifications \_ \_</span><span class="sxs-lookup"><span data-stu-id="dc52a-105">CHANGE\_LOG\_ENTRY structure</span></span>

<span data-ttu-id="dc52a-106">\[Ces informations s’appliquent uniquement à Windows XP avec Service Pack 2 (SP2).\]</span><span class="sxs-lookup"><span data-stu-id="dc52a-106">\[This information applies only to Windows XP with Service Pack 2 (SP2).\]</span></span>

<span data-ttu-id="dc52a-107">Entrée du journal des modifications.</span><span class="sxs-lookup"><span data-stu-id="dc52a-107">A change log entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc52a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dc52a-108">Syntax</span></span>


```C++
typedef struct _CHANGE_LOG_ENTRY {
  RECORD_HEADER RecordHeader;
  DWORD         dwMagicNum;
  DWORD         dwEntryType;
  DWORD         dwEntryFlags;
  DWORD         dwAttributes;
  INT64         i64SequenceNum;
  WCHAR         szProcName[16];
} CHANGE_LOG_ENTRY, *PCHANGE_LOG_ENTRY;
```



## <a name="members"></a><span data-ttu-id="dc52a-109">Membres</span><span class="sxs-lookup"><span data-stu-id="dc52a-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="dc52a-110">**RecordHeader**</span><span class="sxs-lookup"><span data-stu-id="dc52a-110">**RecordHeader**</span></span>
</dt> <dd>

<span data-ttu-id="dc52a-111">Structure [**d' \_ en-tête d’enregistrement**](record-header.md) .</span><span class="sxs-lookup"><span data-stu-id="dc52a-111">A [**RECORD\_HEADER**](record-header.md) structure.</span></span> <span data-ttu-id="dc52a-112">Le membre **dwRecordType** doit être défini sur **RecordTypeLogEntry** (1).</span><span class="sxs-lookup"><span data-stu-id="dc52a-112">The **dwRecordType** member should be set to **RecordTypeLogEntry** (1).</span></span>

</dd> <dt>

<span data-ttu-id="dc52a-113">**dwMagicNum**</span><span class="sxs-lookup"><span data-stu-id="dc52a-113">**dwMagicNum**</span></span>
</dt> <dd>

<span data-ttu-id="dc52a-114">Ce membre doit être défini sur 0xabcdef12.</span><span class="sxs-lookup"><span data-stu-id="dc52a-114">This member should be set to 0xabcdef12.</span></span>

</dd> <dt>

<span data-ttu-id="dc52a-115">**dwEntryType**</span><span class="sxs-lookup"><span data-stu-id="dc52a-115">**dwEntryType**</span></span>
</dt> <dd>

<span data-ttu-id="dc52a-116">Ce membre peut prendre l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="dc52a-116">This member can be one of the following values:</span></span>

<dl><span id="CHANGE_LOG_ENTRYTYPES_ACLCHANGE__0x2_"></span><span id="change_log_entrytypes_aclchange__0x2_"></span><span id="CHANGE_LOG_ENTRYTYPES_ACLCHANGE__0X2_"></span><dt>

<span data-ttu-id="dc52a-117">Journal des modifications \_ \_ ENTRYTYPES \_ ACLCHANGE \* \* (0X2) \* \*</span><span class="sxs-lookup"><span data-stu-id="dc52a-117">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_ACLCHANGE\*\* (0x2)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_ATTRCHANGE__0x4_"></span><span id="change_log_entrytypes_attrchange__0x4_"></span><span id="CHANGE_LOG_ENTRYTYPES_ATTRCHANGE__0X4_"></span><dt>

<span data-ttu-id="dc52a-118">Journal des modifications \_ \_ ENTRYTYPES \_ ATTRCHANGE \* \* (0x4) \* \*</span><span class="sxs-lookup"><span data-stu-id="dc52a-118">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_ATTRCHANGE\*\* (0x4)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRCREATE__0x80_"></span><span id="change_log_entrytypes_dircreate__0x80_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRCREATE__0X80_"></span><dt>

<span data-ttu-id="dc52a-119">Journal des modifications \_ \_ ENTRYTYPES \_ DIRCREATE \* \* (0x80) \* \*</span><span class="sxs-lookup"><span data-stu-id="dc52a-119">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_DIRCREATE\*\* (0x80)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRRENAME__0x100_"></span><span id="change_log_entrytypes_dirrename__0x100_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRRENAME__0X100_"></span><dt>

<span data-ttu-id="dc52a-120">Journal des modifications \_ \_ ENTRYTYPES \_ DIRRENAME \* \* (0x100) \* \*</span><span class="sxs-lookup"><span data-stu-id="dc52a-120">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_DIRRENAME\*\* (0x100)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRDELETE__0x200_"></span><span id="change_log_entrytypes_dirdelete__0x200_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRDELETE__0X200_"></span><dt>

<span data-ttu-id="dc52a-121">Journal des modifications \_ \_ ENTRYTYPES \_ DIRDELETE \* \* (0x200) \* \*</span><span class="sxs-lookup"><span data-stu-id="dc52a-121">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_DIRDELETE\*\* (0x200)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILECREATE__0x20_"></span><span id="change_log_entrytypes_filecreate__0x20_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILECREATE__0X20_"></span><dt>

<span data-ttu-id="dc52a-122">Journal des modifications \_ \_ ENTRYTYPES \_ FILECREATE \* \* (0x20) \* \*</span><span class="sxs-lookup"><span data-stu-id="dc52a-122">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_FILECREATE\*\* (0x20)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILEDELETE__0x10_"></span><span id="change_log_entrytypes_filedelete__0x10_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILEDELETE__0X10_"></span><dt>

<span data-ttu-id="dc52a-123">Journal des modifications \_ \_ ENTRYTYPES \_ FILEDELETE \* \* (0x10) \* \*</span><span class="sxs-lookup"><span data-stu-id="dc52a-123">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_FILEDELETE\*\* (0x10)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILERENAME__0x40_"></span><span id="change_log_entrytypes_filerename__0x40_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILERENAME__0X40_"></span><dt>

<span data-ttu-id="dc52a-124">Journal des modifications \_ \_ ENTRYTYPES \_ FILERENAME \* \* (0x40) \* \*</span><span class="sxs-lookup"><span data-stu-id="dc52a-124">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_FILERENAME\*\* (0x40)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_INPRECREATE__0x100000_"></span><span id="change_log_entrytypes_inprecreate__0x100000_"></span><span id="CHANGE_LOG_ENTRYTYPES_INPRECREATE__0X100000_"></span><dt>

<span data-ttu-id="dc52a-125">Journal des modifications \_ \_ ENTRYTYPES \_ INPRECREATE \* \* (3 x) \* \*</span><span class="sxs-lookup"><span data-stu-id="dc52a-125">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_INPRECREATE\*\* (0x100000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_ISDIR__0x20000_"></span><span id="change_log_entrytypes_isdir__0x20000_"></span><span id="CHANGE_LOG_ENTRYTYPES_ISDIR__0X20000_"></span><dt>

<span data-ttu-id="dc52a-126">Journal des modifications \_ \_ ENTRYTYPES \_ ISDIR \* \* (0x20000) \* \*</span><span class="sxs-lookup"><span data-stu-id="dc52a-126">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_ISDIR\*\* (0x20000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_ISNOTDIR__0x40000_"></span><span id="change_log_entrytypes_isnotdir__0x40000_"></span><span id="CHANGE_LOG_ENTRYTYPES_ISNOTDIR__0X40000_"></span><dt>

<span data-ttu-id="dc52a-127">Journal des modifications \_ \_ ENTRYTYPES \_ ISNOTDIR \* \* (0x40000) \* \*</span><span class="sxs-lookup"><span data-stu-id="dc52a-127">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_ISNOTDIR\*\* (0x40000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_MOUNTCREATE__0x400_"></span><span id="change_log_entrytypes_mountcreate__0x400_"></span><span id="CHANGE_LOG_ENTRYTYPES_MOUNTCREATE__0X400_"></span><dt>

<span data-ttu-id="dc52a-128">Journal des modifications \_ \_ ENTRYTYPES \_ MOUNTCREATE \* \* (0x400) \* \*</span><span class="sxs-lookup"><span data-stu-id="dc52a-128">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_MOUNTCREATE\*\* (0x400)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_MOUNTDELETE__0x800_"></span><span id="change_log_entrytypes_mountdelete__0x800_"></span><span id="CHANGE_LOG_ENTRYTYPES_MOUNTDELETE__0X800_"></span><dt>

<span data-ttu-id="dc52a-129">Journal des modifications \_ \_ ENTRYTYPES \_ MOUNTDELETE \* \* (0x800) \* \*</span><span class="sxs-lookup"><span data-stu-id="dc52a-129">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_MOUNTDELETE\*\* (0x800)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_NOOPTIMIZE__0x10000_"></span><span id="change_log_entrytypes_nooptimize__0x10000_"></span><span id="CHANGE_LOG_ENTRYTYPES_NOOPTIMIZE__0X10000_"></span><dt>

<span data-ttu-id="dc52a-130">Journal des modifications \_ \_ ENTRYTYPES \_ nooptimise \* \* (0x10000) \* \*</span><span class="sxs-lookup"><span data-stu-id="dc52a-130">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_NOOPTIMIZE\*\* (0x10000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_OPENBYID__0x200000_"></span><span id="change_log_entrytypes_openbyid__0x200000_"></span><span id="CHANGE_LOG_ENTRYTYPES_OPENBYID__0X200000_"></span><dt>

<span data-ttu-id="dc52a-131">Journal des modifications \_ \_ ENTRYTYPES \_ OPENBYID \* \* (0x200000) \* \*</span><span class="sxs-lookup"><span data-stu-id="dc52a-131">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_OPENBYID\*\* (0x200000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_SIMULATEDELETE__0x80000_"></span><span id="change_log_entrytypes_simulatedelete__0x80000_"></span><span id="CHANGE_LOG_ENTRYTYPES_SIMULATEDELETE__0X80000_"></span><dt>

<span data-ttu-id="dc52a-132">Journal des modifications \_ \_ ENTRYTYPES \_ SIMULATEDELETE \* \* (0x80000) \* \*</span><span class="sxs-lookup"><span data-stu-id="dc52a-132">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_SIMULATEDELETE\*\* (0x80000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMCHANGE__0x1_"></span><span id="change_log_entrytypes_streamchange__0x1_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMCHANGE__0X1_"></span><dt>

<span data-ttu-id="dc52a-133">Journal des modifications \_ \_ ENTRYTYPES \_ STREAMCHANGE \* \* (0x1) \* \*</span><span class="sxs-lookup"><span data-stu-id="dc52a-133">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_STREAMCHANGE\*\* (0x1)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMCREATE__0x2000_"></span><span id="change_log_entrytypes_streamcreate__0x2000_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMCREATE__0X2000_"></span><dt>

<span data-ttu-id="dc52a-134">Journal des modifications \_ \_ ENTRYTYPES \_ STREAMCREATE \* \* (0x2000) \* \*</span><span class="sxs-lookup"><span data-stu-id="dc52a-134">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_STREAMCREATE\*\* (0x2000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMOVERWRITE__0x8_"></span><span id="change_log_entrytypes_streamoverwrite__0x8_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMOVERWRITE__0X8_"></span><dt>

<span data-ttu-id="dc52a-135">Journal des modifications \_ \_ ENTRYTYPES \_ STREAMOVERWRITE \* \* (0x8) \* \*</span><span class="sxs-lookup"><span data-stu-id="dc52a-135">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_STREAMOVERWRITE\*\* (0x8)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_VOLUMEERROR__0x1000_"></span><span id="change_log_entrytypes_volumeerror__0x1000_"></span><span id="CHANGE_LOG_ENTRYTYPES_VOLUMEERROR__0X1000_"></span><dt>

<span data-ttu-id="dc52a-136">Journal des modifications \_ \_ ENTRYTYPES \_ VOLUMEERROR \* \* (0x1000) \* \*</span><span class="sxs-lookup"><span data-stu-id="dc52a-136">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_VOLUMEERROR\*\* (0x1000)\*\*</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="dc52a-137">**dwEntryFlags**</span><span class="sxs-lookup"><span data-stu-id="dc52a-137">**dwEntryFlags**</span></span>
</dt> <dd>

<span data-ttu-id="dc52a-138">Ce membre peut prendre l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="dc52a-138">This member can be one of the following values:</span></span>

<dl><span id="CHANGE_LOG_ENTRYFLAGS_ACLINFO__0x4_"></span><span id="change_log_entryflags_aclinfo__0x4_"></span><span id="CHANGE_LOG_ENTRYFLAGS_ACLINFO__0X4_"></span><dt>

<span data-ttu-id="dc52a-139">**Journal des modifications \_ \_ ENTRYFLAGS \_ ACLINFO (0x4)**</span><span class="sxs-lookup"><span data-stu-id="dc52a-139">**CHANGE\_LOG\_ENTRYFLAGS\_ACLINFO (0x4)**</span></span>
</dt><span id="CHANGE_LOG_ENTRYFLAGS_DEBUGINFO__0x8_"></span><span id="change_log_entryflags_debuginfo__0x8_"></span><span id="CHANGE_LOG_ENTRYFLAGS_DEBUGINFO__0X8_"></span><dt>

<span data-ttu-id="dc52a-140">**Journal des modifications \_ \_ ENTRYFLAGS \_ DebugInfo (0x8)**</span><span class="sxs-lookup"><span data-stu-id="dc52a-140">**CHANGE\_LOG\_ENTRYFLAGS\_DEBUGINFO (0x8)**</span></span>
</dt><span id="CHANGE_LOG_ENTRYFLAGS_SECONDPATH__0x2_"></span><span id="change_log_entryflags_secondpath__0x2_"></span><span id="CHANGE_LOG_ENTRYFLAGS_SECONDPATH__0X2_"></span><dt>

<span data-ttu-id="dc52a-141">**Journal des modifications \_ \_ ENTRYFLAGS \_ SECONDPATH (0X2)**</span><span class="sxs-lookup"><span data-stu-id="dc52a-141">**CHANGE\_LOG\_ENTRYFLAGS\_SECONDPATH (0x2)**</span></span>
</dt><span id="CHANGE_LOG_ENTRYFLAGS_SHORTNAME__0x10_"></span><span id="change_log_entryflags_shortname__0x10_"></span><span id="CHANGE_LOG_ENTRYFLAGS_SHORTNAME__0X10_"></span><dt>

<span data-ttu-id="dc52a-142">**MODIFIER le \_ journal \_ ENTRYFLAGS \_ ShortName (0x10)**</span><span class="sxs-lookup"><span data-stu-id="dc52a-142">**CHANGE\_LOG\_ENTRYFLAGS\_SHORTNAME (0x10)**</span></span>
</dt><span id="CHANGE_LOG_ENTRYFLAGS_TEMPPATH__0x1_"></span><span id="change_log_entryflags_temppath__0x1_"></span><span id="CHANGE_LOG_ENTRYFLAGS_TEMPPATH__0X1_"></span><dt>

<span data-ttu-id="dc52a-143">**Journal des modifications \_ \_ ENTRYFLAGS \_ TempPath (0x1)**</span><span class="sxs-lookup"><span data-stu-id="dc52a-143">**CHANGE\_LOG\_ENTRYFLAGS\_TEMPPATH (0x1)**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="dc52a-144">**dwAttributes**</span><span class="sxs-lookup"><span data-stu-id="dc52a-144">**dwAttributes**</span></span>
</dt> <dd>

<span data-ttu-id="dc52a-145">Attributs de fichier du fichier journal de modification.</span><span class="sxs-lookup"><span data-stu-id="dc52a-145">The file attributes of the change log file.</span></span> <span data-ttu-id="dc52a-146">Si aucun attribut n’est spécifié, cette valeur doit être définie sur 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="dc52a-146">If no attributes are specified, this value should be set to 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="dc52a-147">**i64SequenceNum**</span><span class="sxs-lookup"><span data-stu-id="dc52a-147">**i64SequenceNum**</span></span>
</dt> <dd>

<span data-ttu-id="dc52a-148">Numéro de séquence assigné à l’entrée du journal des modifications.</span><span class="sxs-lookup"><span data-stu-id="dc52a-148">The sequence number assigned to the change log entry.</span></span>

</dd> <dt>

<span data-ttu-id="dc52a-149">**szProcName**</span><span class="sxs-lookup"><span data-stu-id="dc52a-149">**szProcName**</span></span>
</dt> <dd>

<span data-ttu-id="dc52a-150">Nom du processus qui effectue la modification.</span><span class="sxs-lookup"><span data-stu-id="dc52a-150">The name of the process making the change.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc52a-151">Notes</span><span class="sxs-lookup"><span data-stu-id="dc52a-151">Remarks</span></span>

<span data-ttu-id="dc52a-152">Cette structure est suivie d’un nombre variable d’enregistrements de données de longueur variable, ainsi que d’une valeur **DWORD** qui doit être identique à la valeur du membre **dwRecordSize** de **RecordHeader**.</span><span class="sxs-lookup"><span data-stu-id="dc52a-152">This structure is followed by a variable number of variable-length data records, plus a **DWORD** value that should be identical to the value of the **dwRecordSize** member of **RecordHeader**.</span></span>

<span data-ttu-id="dc52a-153">Les enregistrements de données de longueur variable se composent d’une structure d' [**\_ en-tête d’enregistrement**](record-header.md) et de données qui peuvent être utilisées pour restaurer l’entrée du journal des modifications.</span><span class="sxs-lookup"><span data-stu-id="dc52a-153">The variable-length data records consist of a [**RECORD\_HEADER**](record-header.md) structure plus data that can be used to restore the change log entry.</span></span> <span data-ttu-id="dc52a-154">Le format des données dépend de la valeur du membre **dwRecordType** de la structure d' **\_ en-tête d’enregistrement** .</span><span class="sxs-lookup"><span data-stu-id="dc52a-154">The format of the data depends on the value of the **dwRecordType** member of the **RECORD\_HEADER** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc52a-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc52a-155">Requirements</span></span>



| <span data-ttu-id="dc52a-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc52a-156">Requirement</span></span> | <span data-ttu-id="dc52a-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc52a-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dc52a-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc52a-158">Minimum supported client</span></span><br/> | <span data-ttu-id="dc52a-159">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc52a-159">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="dc52a-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc52a-160">Minimum supported server</span></span><br/> | <span data-ttu-id="dc52a-161">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc52a-161">None supported</span></span><br/>                            |
| <span data-ttu-id="dc52a-162">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="dc52a-162">End of client support</span></span><br/>    | <span data-ttu-id="dc52a-163">Windows XP SP2</span><span class="sxs-lookup"><span data-stu-id="dc52a-163">Windows XP with SP2</span></span><br/>                       |



 

 





