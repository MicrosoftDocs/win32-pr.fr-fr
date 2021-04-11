---
description: La \_ structure d’informations sur le travail \_ 1 spécifie les informations de travail d’impression, telles que la valeur de l’identificateur du travail, le nom de l’imprimante pour laquelle le travail est mis en attente, le nom de l’ordinateur qui a créé le travail d’impression, le nom de l’utilisateur propriétaire du travail d’impression, et ainsi de suite.
ms.assetid: d42ada89-6bc7-4006-81d9-dbcc0347edd3
title: Structure JOB_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_1
- _JOB_INFO_1A
- _JOB_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d56d4d6bce15a661ce141d8e22d27a15837a9f6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320609"
---
# <a name="job_info_1-structure"></a><span data-ttu-id="7d92f-103">\_Structure informations sur le travail \_ 1</span><span class="sxs-lookup"><span data-stu-id="7d92f-103">JOB\_INFO\_1 structure</span></span>

<span data-ttu-id="7d92f-104">La structure d’informations **sur le travail \_ \_ 1** spécifie les informations de travail d’impression, telles que la valeur de l’identificateur du travail, le nom de l’imprimante pour laquelle le travail est mis en attente, le nom de l’ordinateur qui a créé le travail d’impression, le nom de l’utilisateur propriétaire du travail d’impression, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="7d92f-104">The **JOB\_INFO\_1** structure specifies print-job information such as the job-identifier value, the name of the printer for which the job is spooled, the name of the machine that created the print job, the name of the user that owns the print job, and so on.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d92f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7d92f-105">Syntax</span></span>


```C++
typedef struct _JOB_INFO_1 {
  DWORD      JobId;
  LPTSTR     pPrinterName;
  LPTSTR     pMachineName;
  LPTSTR     pUserName;
  LPTSTR     pDocument;
  LPTSTR     pDatatype;
  LPTSTR     pStatus;
  DWORD      Status;
  DWORD      Priority;
  DWORD      Position;
  DWORD      TotalPages;
  DWORD      PagesPrinted;
  SYSTEMTIME Submitted;
} JOB_INFO_1, *PJOB_INFO_1;
```



## <a name="members"></a><span data-ttu-id="7d92f-106">Membres</span><span class="sxs-lookup"><span data-stu-id="7d92f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7d92f-107">**JobId**</span><span class="sxs-lookup"><span data-stu-id="7d92f-107">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="7d92f-108">Identificateur de tâche.</span><span class="sxs-lookup"><span data-stu-id="7d92f-108">A job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="7d92f-109">**pPrinterName**</span><span class="sxs-lookup"><span data-stu-id="7d92f-109">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="7d92f-110">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’imprimante pour laquelle le travail est mis en attente.</span><span class="sxs-lookup"><span data-stu-id="7d92f-110">A pointer to a null-terminated string that specifies the name of the printer for which the job is spooled.</span></span>

</dd> <dt>

<span data-ttu-id="7d92f-111">**pMachineName**</span><span class="sxs-lookup"><span data-stu-id="7d92f-111">**pMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="7d92f-112">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’ordinateur qui a créé le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="7d92f-112">A pointer to a null-terminated string that specifies the name of the machine that created the print job.</span></span>

</dd> <dt>

<span data-ttu-id="7d92f-113">**pUserName**</span><span class="sxs-lookup"><span data-stu-id="7d92f-113">**pUserName**</span></span>
</dt> <dd>

<span data-ttu-id="7d92f-114">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’utilisateur propriétaire du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="7d92f-114">A pointer to a null-terminated string that specifies the name of the user that owns the print job.</span></span>

</dd> <dt>

<span data-ttu-id="7d92f-115">**pDocument**</span><span class="sxs-lookup"><span data-stu-id="7d92f-115">**pDocument**</span></span>
</dt> <dd>

<span data-ttu-id="7d92f-116">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du travail d’impression (par exemple, "MS-WORD : Review.doc").</span><span class="sxs-lookup"><span data-stu-id="7d92f-116">A pointer to a null-terminated string that specifies the name of the print job (for example, "MS-WORD: Review.doc").</span></span>

</dd> <dt>

<span data-ttu-id="7d92f-117">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="7d92f-117">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="7d92f-118">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le type de données utilisé pour enregistrer le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="7d92f-118">A pointer to a null-terminated string that specifies the type of data used to record the print job.</span></span>

</dd> <dt>

<span data-ttu-id="7d92f-119">**pStatus**</span><span class="sxs-lookup"><span data-stu-id="7d92f-119">**pStatus**</span></span>
</dt> <dd>

<span data-ttu-id="7d92f-120">Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’état du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="7d92f-120">A pointer to a null-terminated string that specifies the status of the print job.</span></span> <span data-ttu-id="7d92f-121">Ce membre doit être vérifié avant l' *État* et, si *PStatus* a la **valeur null**, l’État est défini par le contenu du membre Status.</span><span class="sxs-lookup"><span data-stu-id="7d92f-121">This member should be checked prior to *Status* and, if *pStatus* is **NULL**, the status is defined by the contents of the Status member.</span></span>

</dd> <dt>

<span data-ttu-id="7d92f-122">**État**</span><span class="sxs-lookup"><span data-stu-id="7d92f-122">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="7d92f-123">État du travail.</span><span class="sxs-lookup"><span data-stu-id="7d92f-123">The job status.</span></span> <span data-ttu-id="7d92f-124">La valeur de ce membre peut être zéro ou une combinaison d’une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="7d92f-124">The value of this member can be zero or a combination of one or more of the following values.</span></span> <span data-ttu-id="7d92f-125">La valeur zéro indique que la file d’attente à l’impression a été suspendue après la fin de la mise en attente du document.</span><span class="sxs-lookup"><span data-stu-id="7d92f-125">A value of zero indicates that the print queue was paused after the document finished spooling.</span></span>



| <span data-ttu-id="7d92f-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d92f-126">Value</span></span>                           | <span data-ttu-id="7d92f-127">Signification</span><span class="sxs-lookup"><span data-stu-id="7d92f-127">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d92f-128">État du travail \_ \_ bloqué \_ DEVQ</span><span class="sxs-lookup"><span data-stu-id="7d92f-128">JOB\_STATUS\_BLOCKED\_DEVQ</span></span>      | <span data-ttu-id="7d92f-129">Le pilote ne peut pas imprimer le travail.</span><span class="sxs-lookup"><span data-stu-id="7d92f-129">The driver cannot print the job.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="7d92f-130">État du travail \_ \_ terminé</span><span class="sxs-lookup"><span data-stu-id="7d92f-130">JOB\_STATUS\_COMPLETE</span></span>           | <span data-ttu-id="7d92f-131">**Windows XP et versions ultérieures :** Le travail est envoyé à l’imprimante, mais le travail n’est peut-être pas encore imprimé.</span><span class="sxs-lookup"><span data-stu-id="7d92f-131">**Windows XP and later:** Job is sent to the printer, but the job may not be printed yet.</span></span><br/> <span data-ttu-id="7d92f-132">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="7d92f-132">See Remarks for more information.</span></span><br/>                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="7d92f-133">État du travail \_ \_ supprimé</span><span class="sxs-lookup"><span data-stu-id="7d92f-133">JOB\_STATUS\_DELETED</span></span>            | <span data-ttu-id="7d92f-134">La tâche a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="7d92f-134">Job has been deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="7d92f-135">suppression de l’état du travail \_ \_</span><span class="sxs-lookup"><span data-stu-id="7d92f-135">JOB\_STATUS\_DELETING</span></span>           | <span data-ttu-id="7d92f-136">Le travail est en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="7d92f-136">Job is being deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="7d92f-137">\_erreur d’état de la tâche \_</span><span class="sxs-lookup"><span data-stu-id="7d92f-137">JOB\_STATUS\_ERROR</span></span>              | <span data-ttu-id="7d92f-138">Une erreur est associée au travail.</span><span class="sxs-lookup"><span data-stu-id="7d92f-138">An error is associated with the job.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="7d92f-139">État du travail \_ \_ hors connexion</span><span class="sxs-lookup"><span data-stu-id="7d92f-139">JOB\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="7d92f-140">L’imprimante est hors connexion.</span><span class="sxs-lookup"><span data-stu-id="7d92f-140">Printer is offline.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="7d92f-141">\_PAPEROUT État du travail \_</span><span class="sxs-lookup"><span data-stu-id="7d92f-141">JOB\_STATUS\_PAPEROUT</span></span>           | <span data-ttu-id="7d92f-142">L’imprimante n’est plus imprimée.</span><span class="sxs-lookup"><span data-stu-id="7d92f-142">Printer is out of paper.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="7d92f-143">État du travail \_ \_ suspendu</span><span class="sxs-lookup"><span data-stu-id="7d92f-143">JOB\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="7d92f-144">Le travail est suspendu.</span><span class="sxs-lookup"><span data-stu-id="7d92f-144">Job is paused.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="7d92f-145">État du travail \_ \_ imprimé</span><span class="sxs-lookup"><span data-stu-id="7d92f-145">JOB\_STATUS\_PRINTED</span></span>            | <span data-ttu-id="7d92f-146">Le travail a été imprimé.</span><span class="sxs-lookup"><span data-stu-id="7d92f-146">Job has printed.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="7d92f-147">\_impression de l’état du travail \_</span><span class="sxs-lookup"><span data-stu-id="7d92f-147">JOB\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="7d92f-148">Le travail est en cours d’impression.</span><span class="sxs-lookup"><span data-stu-id="7d92f-148">Job is printing.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="7d92f-149">redémarrage de l’état du travail \_ \_</span><span class="sxs-lookup"><span data-stu-id="7d92f-149">JOB\_STATUS\_RESTART</span></span>            | <span data-ttu-id="7d92f-150">Le travail a été redémarré.</span><span class="sxs-lookup"><span data-stu-id="7d92f-150">Job has been restarted.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="7d92f-151">État du travail \_ \_ conservé</span><span class="sxs-lookup"><span data-stu-id="7d92f-151">JOB\_STATUS\_RETAINED</span></span>           | <span data-ttu-id="7d92f-152">**Windows Vista et versions ultérieures :** La tâche a été conservée dans la file d’attente à l’impression et ne peut pas être supprimée.</span><span class="sxs-lookup"><span data-stu-id="7d92f-152">**Windows Vista and later:** Job has been retained in the print queue and cannot be deleted.</span></span> <span data-ttu-id="7d92f-153">Ceci peut être lié aux problèmes suivants :</span><span class="sxs-lookup"><span data-stu-id="7d92f-153">This can be caused by the following:</span></span><br/> <span data-ttu-id="7d92f-154">1) la tâche a été conservée manuellement par un appel à SetJob et le spouleur attend que la tâche soit libérée.</span><span class="sxs-lookup"><span data-stu-id="7d92f-154">1) The job was manually retained by a call to SetJob and the spooler is waiting for the job to be released.</span></span><br/> <span data-ttu-id="7d92f-155">2) le travail n’a pas terminé l’impression et doit terminer l’impression avant de pouvoir être supprimé automatiquement.</span><span class="sxs-lookup"><span data-stu-id="7d92f-155">2) The job has not finished printing and must finish printing before it can be automatically deleted.</span></span><br/> <span data-ttu-id="7d92f-156">Pour plus d’informations sur les commandes de travail d’impression, consultez [**SetJob**](setjob.md) .</span><span class="sxs-lookup"><span data-stu-id="7d92f-156">See [**SetJob**](setjob.md) for more information about print job commands.</span></span><br/> |
| <span data-ttu-id="7d92f-157">mise en file d’attente de l’état du travail \_ \_</span><span class="sxs-lookup"><span data-stu-id="7d92f-157">JOB\_STATUS\_SPOOLING</span></span>           | <span data-ttu-id="7d92f-158">Le travail est en attente.</span><span class="sxs-lookup"><span data-stu-id="7d92f-158">Job is spooling.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="7d92f-159">INTERVENTION de l’utilisateur de l’état du travail \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="7d92f-159">JOB\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="7d92f-160">L’imprimante a une erreur qui nécessite que l’utilisateur effectue une action.</span><span class="sxs-lookup"><span data-stu-id="7d92f-160">Printer has an error that requires the user to do something.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="7d92f-161">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="7d92f-161">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="7d92f-162">Priorité du travail.</span><span class="sxs-lookup"><span data-stu-id="7d92f-162">The job priority.</span></span> <span data-ttu-id="7d92f-163">Ce membre peut être l’une des valeurs suivantes ou se trouver dans la plage comprise entre 1 et 99 ( \_ Priorité minimale via \_ priorité maximale).</span><span class="sxs-lookup"><span data-stu-id="7d92f-163">This member can be one of the following values or in the range between 1 through 99 (MIN\_PRIORITY through MAX\_PRIORITY).</span></span>



| <span data-ttu-id="7d92f-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d92f-164">Value</span></span>         | <span data-ttu-id="7d92f-165">Signification</span><span class="sxs-lookup"><span data-stu-id="7d92f-165">Meaning</span></span>           |
|---------------|-------------------|
| <span data-ttu-id="7d92f-166">priorité MIN. \_</span><span class="sxs-lookup"><span data-stu-id="7d92f-166">MIN\_PRIORITY</span></span> | <span data-ttu-id="7d92f-167">Priorité minimale.</span><span class="sxs-lookup"><span data-stu-id="7d92f-167">Minimum priority.</span></span> |
| <span data-ttu-id="7d92f-168">priorité MAX. \_</span><span class="sxs-lookup"><span data-stu-id="7d92f-168">MAX\_PRIORITY</span></span> | <span data-ttu-id="7d92f-169">Priorité maximale.</span><span class="sxs-lookup"><span data-stu-id="7d92f-169">Maximum priority.</span></span> |
| <span data-ttu-id="7d92f-170">priorité de définition \_</span><span class="sxs-lookup"><span data-stu-id="7d92f-170">DEF\_PRIORITY</span></span> | <span data-ttu-id="7d92f-171">Priorité par défaut.</span><span class="sxs-lookup"><span data-stu-id="7d92f-171">Default priority.</span></span> |



 

</dd> <dt>

<span data-ttu-id="7d92f-172">**Position**</span><span class="sxs-lookup"><span data-stu-id="7d92f-172">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="7d92f-173">Position du travail dans la file d’attente à l’impression.</span><span class="sxs-lookup"><span data-stu-id="7d92f-173">The job's position in the print queue.</span></span>

</dd> <dt>

<span data-ttu-id="7d92f-174">**TotalPages**</span><span class="sxs-lookup"><span data-stu-id="7d92f-174">**TotalPages**</span></span>
</dt> <dd>

<span data-ttu-id="7d92f-175">Nombre total de pages contenues dans le document.</span><span class="sxs-lookup"><span data-stu-id="7d92f-175">The total number of pages that the document contains.</span></span> <span data-ttu-id="7d92f-176">Cette valeur peut être égale à zéro si le travail d’impression ne contient pas d’informations de délimitation de page.</span><span class="sxs-lookup"><span data-stu-id="7d92f-176">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> <dt>

<span data-ttu-id="7d92f-177">**PagesPrinted**</span><span class="sxs-lookup"><span data-stu-id="7d92f-177">**PagesPrinted**</span></span>
</dt> <dd>

<span data-ttu-id="7d92f-178">Nombre de pages imprimées.</span><span class="sxs-lookup"><span data-stu-id="7d92f-178">The number of pages that have printed.</span></span> <span data-ttu-id="7d92f-179">Cette valeur peut être égale à zéro si le travail d’impression ne contient pas d’informations de délimitation de page.</span><span class="sxs-lookup"><span data-stu-id="7d92f-179">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> <dt>

<span data-ttu-id="7d92f-180">**Envoyée**</span><span class="sxs-lookup"><span data-stu-id="7d92f-180">**Submitted**</span></span>
</dt> <dd>

<span data-ttu-id="7d92f-181">Structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) qui spécifie l’heure à laquelle ce document a été mis en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="7d92f-181">A [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that specifies the time that this document was spooled.</span></span>

<span data-ttu-id="7d92f-182">Cette valeur de date/heure est au format UTC (Universal Time Coordinate).</span><span class="sxs-lookup"><span data-stu-id="7d92f-182">This time value is in Universal Time Coordinate (UTC) format.</span></span> <span data-ttu-id="7d92f-183">Vous devez la convertir en une valeur d’heure locale avant de l’afficher.</span><span class="sxs-lookup"><span data-stu-id="7d92f-183">You should convert it to a local time value before displaying it.</span></span> <span data-ttu-id="7d92f-184">Vous pouvez utiliser la fonction [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) pour effectuer la conversion.</span><span class="sxs-lookup"><span data-stu-id="7d92f-184">You can use the [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) function to perform the conversion.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d92f-185">Notes</span><span class="sxs-lookup"><span data-stu-id="7d92f-185">Remarks</span></span>

<span data-ttu-id="7d92f-186">Les moniteurs de port qui ne prennent pas en charge TrueEndOfJob définissent le travail en tant qu’État du travail \_ \_ imprimé juste après l’envoi du travail à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="7d92f-186">Port monitors that do not support TrueEndOfJob will set the job as JOB\_STATUS\_PRINTED right after the job is submitted to the printer.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d92f-187">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7d92f-187">Requirements</span></span>



| <span data-ttu-id="7d92f-188">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d92f-188">Requirement</span></span> | <span data-ttu-id="7d92f-189">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d92f-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d92f-190">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d92f-190">Minimum supported client</span></span><br/> | <span data-ttu-id="7d92f-191">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d92f-191">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7d92f-192">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d92f-192">Minimum supported server</span></span><br/> | <span data-ttu-id="7d92f-193">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d92f-193">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7d92f-194">En-tête</span><span class="sxs-lookup"><span data-stu-id="7d92f-194">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d92f-195"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7d92f-195"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="7d92f-196">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="7d92f-196">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7d92f-197">**\_ \_ Informations sur \_ les travaux 1s** (Unicode) et **\_ \_ informations sur les travaux \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7d92f-197">**\_JOB\_INFO\_1W** (Unicode) and **\_JOB\_INFO\_1A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="7d92f-198">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d92f-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d92f-199">Impression</span><span class="sxs-lookup"><span data-stu-id="7d92f-199">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="7d92f-200">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="7d92f-200">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="7d92f-201">**EnumJobs**</span><span class="sxs-lookup"><span data-stu-id="7d92f-201">**EnumJobs**</span></span>](enumjobs.md)
</dt> <dt>

[<span data-ttu-id="7d92f-202">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="7d92f-202">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="7d92f-203">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="7d92f-203">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

