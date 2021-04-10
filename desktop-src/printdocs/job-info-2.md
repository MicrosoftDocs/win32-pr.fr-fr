---
description: La \_ structure informations sur le travail \_ 2 décrit un jeu complet de valeurs associées à un travail.
ms.assetid: 0cc61e35-4ac9-47bd-bb0d-ff43854bdee5
title: Structure JOB_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_2
- _JOB_INFO_2A
- _JOB_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d6b582267afceb01fd7ced7d6d46144664bb9d2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210467"
---
# <a name="job_info_2-structure"></a><span data-ttu-id="4ef71-103">Structure des informations de travail \_ \_ 2</span><span class="sxs-lookup"><span data-stu-id="4ef71-103">JOB\_INFO\_2 structure</span></span>

<span data-ttu-id="4ef71-104">La **structure \_ informations \_ sur le travail 2** décrit un jeu complet de valeurs associées à un travail.</span><span class="sxs-lookup"><span data-stu-id="4ef71-104">The **JOB\_INFO\_2** structure describes a full set of values associated with a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ef71-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ef71-105">Syntax</span></span>


```C++
typedef struct _JOB_INFO_2 {
  DWORD                JobId;
  LPTSTR               pPrinterName;
  LPTSTR               pMachineName;
  LPTSTR               pUserName;
  LPTSTR               pDocument;
  LPTSTR               pNotifyName;
  LPTSTR               pDatatype;
  LPTSTR               pPrintProcessor;
  LPTSTR               pParameters;
  LPTSTR               pDriverName;
  LPDEVMODE            pDevMode;
  LPTSTR               pStatus;
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
  DWORD                Status;
  DWORD                Priority;
  DWORD                Position;
  DWORD                StartTime;
  DWORD                UntilTime;
  DWORD                TotalPages;
  DWORD                Size;
  SYSTEMTIME           Submitted;
  DWORD                Time;
  DWORD                PagesPrinted;
} JOB_INFO_2, *PJOB_INFO_2;
```



## <a name="members"></a><span data-ttu-id="4ef71-106">Membres</span><span class="sxs-lookup"><span data-stu-id="4ef71-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4ef71-107">**JobId**</span><span class="sxs-lookup"><span data-stu-id="4ef71-107">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="4ef71-108">Valeur d’identificateur de tâche.</span><span class="sxs-lookup"><span data-stu-id="4ef71-108">A job identifier value.</span></span>

</dd> <dt>

<span data-ttu-id="4ef71-109">**pPrinterName**</span><span class="sxs-lookup"><span data-stu-id="4ef71-109">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="4ef71-110">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’imprimante pour laquelle le travail est mis en attente.</span><span class="sxs-lookup"><span data-stu-id="4ef71-110">A pointer to a null-terminated string that specifies the name of the printer for which the job is spooled.</span></span>

</dd> <dt>

<span data-ttu-id="4ef71-111">**pMachineName**</span><span class="sxs-lookup"><span data-stu-id="4ef71-111">**pMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="4ef71-112">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’ordinateur qui a créé le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="4ef71-112">A pointer to a null-terminated string that specifies the name of the machine that created the print job.</span></span>

</dd> <dt>

<span data-ttu-id="4ef71-113">**pUserName**</span><span class="sxs-lookup"><span data-stu-id="4ef71-113">**pUserName**</span></span>
</dt> <dd>

<span data-ttu-id="4ef71-114">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’utilisateur propriétaire du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="4ef71-114">A pointer to a null-terminated string that specifies the name of the user who owns the print job.</span></span>

</dd> <dt>

<span data-ttu-id="4ef71-115">**pDocument**</span><span class="sxs-lookup"><span data-stu-id="4ef71-115">**pDocument**</span></span>
</dt> <dd>

<span data-ttu-id="4ef71-116">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du travail d’impression (par exemple, "MS-WORD : Review.doc").</span><span class="sxs-lookup"><span data-stu-id="4ef71-116">A pointer to a null-terminated string that specifies the name of the print job (for example, "MS-WORD: Review.doc").</span></span>

</dd> <dt>

<span data-ttu-id="4ef71-117">**pNotifyName**</span><span class="sxs-lookup"><span data-stu-id="4ef71-117">**pNotifyName**</span></span>
</dt> <dd>

<span data-ttu-id="4ef71-118">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’utilisateur qui doit être averti lorsque le travail a été imprimé ou lorsqu’une erreur se produit lors de l’impression du travail.</span><span class="sxs-lookup"><span data-stu-id="4ef71-118">A pointer to a null-terminated string that specifies the name of the user who should be notified when the job has been printed or when an error occurs while printing the job.</span></span>

</dd> <dt>

<span data-ttu-id="4ef71-119">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="4ef71-119">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="4ef71-120">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le type de données utilisé pour enregistrer le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="4ef71-120">A pointer to a null-terminated string that specifies the type of data used to record the print job.</span></span>

</dd> <dt>

<span data-ttu-id="4ef71-121">**pPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="4ef71-121">**pPrintProcessor**</span></span>
</dt> <dd>

<span data-ttu-id="4ef71-122">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du processeur d’impression qui doit être utilisé pour imprimer le travail.</span><span class="sxs-lookup"><span data-stu-id="4ef71-122">A pointer to a null-terminated string that specifies the name of the print processor that should be used to print the job.</span></span>

</dd> <dt>

<span data-ttu-id="4ef71-123">**pParameters**</span><span class="sxs-lookup"><span data-stu-id="4ef71-123">**pParameters**</span></span>
</dt> <dd>

<span data-ttu-id="4ef71-124">Pointeur vers une chaîne se terminant par un caractère null qui spécifie les paramètres du processeur d’impression.</span><span class="sxs-lookup"><span data-stu-id="4ef71-124">A pointer to a null-terminated string that specifies print-processor parameters.</span></span>

</dd> <dt>

<span data-ttu-id="4ef71-125">**pDriverName**</span><span class="sxs-lookup"><span data-stu-id="4ef71-125">**pDriverName**</span></span>
</dt> <dd>

<span data-ttu-id="4ef71-126">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du pilote d’imprimante qui doit être utilisé pour traiter le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="4ef71-126">A pointer to a null-terminated string that specifies the name of the printer driver that should be used to process the print job.</span></span>

</dd> <dt>

<span data-ttu-id="4ef71-127">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="4ef71-127">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="4ef71-128">Pointeur vers une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) qui contient les données d’initialisation et d’environnement de l’appareil pour le pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="4ef71-128">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that contains device-initialization and environment data for the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="4ef71-129">**pStatus**</span><span class="sxs-lookup"><span data-stu-id="4ef71-129">**pStatus**</span></span>
</dt> <dd>

<span data-ttu-id="4ef71-130">Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’état du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="4ef71-130">A pointer to a null-terminated string that specifies the status of the print job.</span></span> <span data-ttu-id="4ef71-131">Ce membre doit être vérifié avant l' **État** et, si **PStatus** a la **valeur null**, l’État est défini par le contenu du membre Status.</span><span class="sxs-lookup"><span data-stu-id="4ef71-131">This member should be checked prior to **Status** and, if **pStatus** is **NULL**, the status is defined by the contents of the Status member.</span></span>

</dd> <dt>

<span data-ttu-id="4ef71-132">**pSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="4ef71-132">**pSecurityDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="4ef71-133">La valeur de ce membre est **null**.</span><span class="sxs-lookup"><span data-stu-id="4ef71-133">The value of this member is **NULL**.</span></span> <span data-ttu-id="4ef71-134">La récupération et le paramétrage des descripteurs de sécurité de document ne sont pas pris en charge dans cette version.</span><span class="sxs-lookup"><span data-stu-id="4ef71-134">Retrieval and setting of document security descriptors is not supported in this release.</span></span>

</dd> <dt>

<span data-ttu-id="4ef71-135">**État**</span><span class="sxs-lookup"><span data-stu-id="4ef71-135">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="4ef71-136">État du travail.</span><span class="sxs-lookup"><span data-stu-id="4ef71-136">The job status.</span></span> <span data-ttu-id="4ef71-137">Ce membre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="4ef71-137">This member can be one or more of the following values.</span></span>

| <span data-ttu-id="4ef71-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ef71-138">Value</span></span>                           | <span data-ttu-id="4ef71-139">Signification</span><span class="sxs-lookup"><span data-stu-id="4ef71-139">Meaning</span></span>                                                      |
|---------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="4ef71-140">État du travail \_ \_ bloqué \_ DEVQ</span><span class="sxs-lookup"><span data-stu-id="4ef71-140">JOB\_STATUS\_BLOCKED\_DEVQ</span></span>      | <span data-ttu-id="4ef71-141">Le pilote ne peut pas imprimer le travail.</span><span class="sxs-lookup"><span data-stu-id="4ef71-141">The driver cannot print the job.</span></span>                             |
| <span data-ttu-id="4ef71-142">État du travail \_ \_ supprimé</span><span class="sxs-lookup"><span data-stu-id="4ef71-142">JOB\_STATUS\_DELETED</span></span>            | <span data-ttu-id="4ef71-143">La tâche a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="4ef71-143">Job has been deleted.</span></span>                                        |
| <span data-ttu-id="4ef71-144">suppression de l’état du travail \_ \_</span><span class="sxs-lookup"><span data-stu-id="4ef71-144">JOB\_STATUS\_DELETING</span></span>           | <span data-ttu-id="4ef71-145">Le travail est en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="4ef71-145">Job is being deleted.</span></span>                                        |
| <span data-ttu-id="4ef71-146">\_erreur d’état de la tâche \_</span><span class="sxs-lookup"><span data-stu-id="4ef71-146">JOB\_STATUS\_ERROR</span></span>              | <span data-ttu-id="4ef71-147">Une erreur est associée au travail.</span><span class="sxs-lookup"><span data-stu-id="4ef71-147">An error is associated with the job.</span></span>                         |
| <span data-ttu-id="4ef71-148">État du travail \_ \_ hors connexion</span><span class="sxs-lookup"><span data-stu-id="4ef71-148">JOB\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="4ef71-149">L’imprimante est hors connexion.</span><span class="sxs-lookup"><span data-stu-id="4ef71-149">Printer is offline.</span></span>                                          |
| <span data-ttu-id="4ef71-150">\_PAPEROUT État du travail \_</span><span class="sxs-lookup"><span data-stu-id="4ef71-150">JOB\_STATUS\_PAPEROUT</span></span>           | <span data-ttu-id="4ef71-151">L’imprimante n’est plus imprimée.</span><span class="sxs-lookup"><span data-stu-id="4ef71-151">Printer is out of paper.</span></span>                                     |
| <span data-ttu-id="4ef71-152">État du travail \_ \_ suspendu</span><span class="sxs-lookup"><span data-stu-id="4ef71-152">JOB\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="4ef71-153">Le travail est suspendu.</span><span class="sxs-lookup"><span data-stu-id="4ef71-153">Job is paused.</span></span>                                               |
| <span data-ttu-id="4ef71-154">État du travail \_ \_ imprimé</span><span class="sxs-lookup"><span data-stu-id="4ef71-154">JOB\_STATUS\_PRINTED</span></span>            | <span data-ttu-id="4ef71-155">Le travail a été imprimé.</span><span class="sxs-lookup"><span data-stu-id="4ef71-155">Job has printed.</span></span>                                             |
| <span data-ttu-id="4ef71-156">\_impression de l’état du travail \_</span><span class="sxs-lookup"><span data-stu-id="4ef71-156">JOB\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="4ef71-157">Le travail est en cours d’impression.</span><span class="sxs-lookup"><span data-stu-id="4ef71-157">Job is printing.</span></span>                                             |
| <span data-ttu-id="4ef71-158">redémarrage de l’état du travail \_ \_</span><span class="sxs-lookup"><span data-stu-id="4ef71-158">JOB\_STATUS\_RESTART</span></span>            | <span data-ttu-id="4ef71-159">Le travail a été redémarré.</span><span class="sxs-lookup"><span data-stu-id="4ef71-159">Job has been restarted.</span></span>                                      |
| <span data-ttu-id="4ef71-160">mise en file d’attente de l’état du travail \_ \_</span><span class="sxs-lookup"><span data-stu-id="4ef71-160">JOB\_STATUS\_SPOOLING</span></span>           | <span data-ttu-id="4ef71-161">Le travail est en attente.</span><span class="sxs-lookup"><span data-stu-id="4ef71-161">Job is spooling.</span></span>                                             |
| <span data-ttu-id="4ef71-162">INTERVENTION de l’utilisateur de l’état du travail \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="4ef71-162">JOB\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="4ef71-163">L’imprimante a une erreur qui nécessite que l’utilisateur effectue une action.</span><span class="sxs-lookup"><span data-stu-id="4ef71-163">Printer has an error that requires the user to do something.</span></span> |



 

<span data-ttu-id="4ef71-164">Dans Windows XP et les versions ultérieures de Windows, les valeurs suivantes peuvent également être utilisées :</span><span class="sxs-lookup"><span data-stu-id="4ef71-164">In Windows XP and later versions of Windows, the following values can also be used:</span></span>

| <span data-ttu-id="4ef71-165">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ef71-165">Value</span></span>                 | <span data-ttu-id="4ef71-166">Signification</span><span class="sxs-lookup"><span data-stu-id="4ef71-166">Meaning</span></span>                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ef71-167">État du travail \_ \_ terminé</span><span class="sxs-lookup"><span data-stu-id="4ef71-167">JOB\_STATUS\_COMPLETE</span></span> | <span data-ttu-id="4ef71-168">Le travail est envoyé à l’imprimante, mais il n’est peut-être pas encore imprimé.</span><span class="sxs-lookup"><span data-stu-id="4ef71-168">The job is sent to the printer, but may not be printed yet.</span></span> <span data-ttu-id="4ef71-169">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="4ef71-169">See Remarks for more information.</span></span> |
| <span data-ttu-id="4ef71-170">État du travail \_ \_ conservé</span><span class="sxs-lookup"><span data-stu-id="4ef71-170">JOB\_STATUS\_RETAINED</span></span> | <span data-ttu-id="4ef71-171">La tâche a été conservée dans la file d’attente à l’impression après l’impression.</span><span class="sxs-lookup"><span data-stu-id="4ef71-171">The job has been retained in the print queue following printing.</span></span>                              |



 

</dd> <dt>

<span data-ttu-id="4ef71-172">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="4ef71-172">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="4ef71-173">Priorité du travail.</span><span class="sxs-lookup"><span data-stu-id="4ef71-173">The job priority.</span></span> <span data-ttu-id="4ef71-174">Ce membre peut être l’une des valeurs suivantes ou se trouver dans la plage comprise entre 1 et 99 ( \_ Priorité minimale via \_ priorité maximale).</span><span class="sxs-lookup"><span data-stu-id="4ef71-174">This member can be one of the following values or in the range between 1 through 99 (MIN\_PRIORITY through MAX\_PRIORITY).</span></span>



| <span data-ttu-id="4ef71-175">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ef71-175">Value</span></span>         | <span data-ttu-id="4ef71-176">Signification</span><span class="sxs-lookup"><span data-stu-id="4ef71-176">Meaning</span></span>           |
|---------------|-------------------|
| <span data-ttu-id="4ef71-177">priorité MIN. \_</span><span class="sxs-lookup"><span data-stu-id="4ef71-177">MIN\_PRIORITY</span></span> | <span data-ttu-id="4ef71-178">Priorité minimale.</span><span class="sxs-lookup"><span data-stu-id="4ef71-178">Minimum priority.</span></span> |
| <span data-ttu-id="4ef71-179">priorité MAX. \_</span><span class="sxs-lookup"><span data-stu-id="4ef71-179">MAX\_PRIORITY</span></span> | <span data-ttu-id="4ef71-180">Priorité maximale.</span><span class="sxs-lookup"><span data-stu-id="4ef71-180">Maximum priority.</span></span> |
| <span data-ttu-id="4ef71-181">priorité de définition \_</span><span class="sxs-lookup"><span data-stu-id="4ef71-181">DEF\_PRIORITY</span></span> | <span data-ttu-id="4ef71-182">Priorité par défaut.</span><span class="sxs-lookup"><span data-stu-id="4ef71-182">Default priority.</span></span> |



 

</dd> <dt>

<span data-ttu-id="4ef71-183">**Position**</span><span class="sxs-lookup"><span data-stu-id="4ef71-183">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="4ef71-184">Position du travail dans la file d’attente à l’impression.</span><span class="sxs-lookup"><span data-stu-id="4ef71-184">The job's position in the print queue.</span></span>

</dd> <dt>

<span data-ttu-id="4ef71-185">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="4ef71-185">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="4ef71-186">Heure à laquelle le travail peut être imprimé au plus tôt.</span><span class="sxs-lookup"><span data-stu-id="4ef71-186">The earliest time that the job can be printed.</span></span>

</dd> <dt>

<span data-ttu-id="4ef71-187">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="4ef71-187">**UntilTime**</span></span>
</dt> <dd>

<span data-ttu-id="4ef71-188">Heure à laquelle le travail peut être imprimé au plus tard.</span><span class="sxs-lookup"><span data-stu-id="4ef71-188">The latest time that the job can be printed.</span></span>

</dd> <dt>

<span data-ttu-id="4ef71-189">**TotalPages**</span><span class="sxs-lookup"><span data-stu-id="4ef71-189">**TotalPages**</span></span>
</dt> <dd>

<span data-ttu-id="4ef71-190">Nombre de pages requises pour le travail.</span><span class="sxs-lookup"><span data-stu-id="4ef71-190">The number of pages required for the job.</span></span> <span data-ttu-id="4ef71-191">Cette valeur peut être égale à zéro si le travail d’impression ne contient pas d’informations de délimitation de page.</span><span class="sxs-lookup"><span data-stu-id="4ef71-191">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> <dt>

<span data-ttu-id="4ef71-192">**Taille**</span><span class="sxs-lookup"><span data-stu-id="4ef71-192">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="4ef71-193">Taille, en octets, du travail.</span><span class="sxs-lookup"><span data-stu-id="4ef71-193">The size, in bytes, of the job.</span></span>

</dd> <dt>

<span data-ttu-id="4ef71-194">**Envoyée**</span><span class="sxs-lookup"><span data-stu-id="4ef71-194">**Submitted**</span></span>
</dt> <dd>

<span data-ttu-id="4ef71-195">Structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) qui spécifie l’heure à laquelle le travail a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="4ef71-195">A [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that specifies the time when the job was submitted.</span></span>

<span data-ttu-id="4ef71-196">Cette valeur de date/heure est au format UTC (Universal Time Coordinate).</span><span class="sxs-lookup"><span data-stu-id="4ef71-196">This time value is in Universal Time Coordinate (UTC) format.</span></span> <span data-ttu-id="4ef71-197">Vous devez la convertir en une valeur d’heure locale avant de l’afficher.</span><span class="sxs-lookup"><span data-stu-id="4ef71-197">You should convert it to a local time value before displaying it.</span></span> <span data-ttu-id="4ef71-198">Vous pouvez utiliser la fonction [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) pour effectuer la conversion.</span><span class="sxs-lookup"><span data-stu-id="4ef71-198">You can use the [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) function to perform the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="4ef71-199">**Time**</span><span class="sxs-lookup"><span data-stu-id="4ef71-199">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="4ef71-200">Durée totale, en millisecondes, qui s’est écoulée depuis le début de l’impression du travail.</span><span class="sxs-lookup"><span data-stu-id="4ef71-200">The total time, in milliseconds, that has elapsed since the job began printing.</span></span>

</dd> <dt>

<span data-ttu-id="4ef71-201">**PagesPrinted**</span><span class="sxs-lookup"><span data-stu-id="4ef71-201">**PagesPrinted**</span></span>
</dt> <dd>

<span data-ttu-id="4ef71-202">Nombre de pages imprimées.</span><span class="sxs-lookup"><span data-stu-id="4ef71-202">The number of pages that have printed.</span></span> <span data-ttu-id="4ef71-203">Cette valeur peut être égale à zéro si le travail d’impression ne contient pas d’informations de délimitation de page.</span><span class="sxs-lookup"><span data-stu-id="4ef71-203">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ef71-204">Notes</span><span class="sxs-lookup"><span data-stu-id="4ef71-204">Remarks</span></span>

<span data-ttu-id="4ef71-205">Les moniteurs de port qui ne prennent pas en charge TrueEndOfJob définissent le travail en tant qu’État du travail \_ \_ imprimé juste après l’envoi du travail à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="4ef71-205">Port monitors that do not support TrueEndOfJob will set the job as JOB\_STATUS\_PRINTED right after the job is submitted to the printer.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ef71-206">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4ef71-206">Requirements</span></span>



| <span data-ttu-id="4ef71-207">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4ef71-207">Requirement</span></span> | <span data-ttu-id="4ef71-208">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ef71-208">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ef71-209">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4ef71-209">Minimum supported client</span></span><br/> | <span data-ttu-id="4ef71-210">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4ef71-210">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4ef71-211">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4ef71-211">Minimum supported server</span></span><br/> | <span data-ttu-id="4ef71-212">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4ef71-212">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4ef71-213">En-tête</span><span class="sxs-lookup"><span data-stu-id="4ef71-213">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ef71-214"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ef71-214"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4ef71-215">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="4ef71-215">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4ef71-216">**\_ \_ Informations sur \_ le travail 2S** (Unicode) et **\_ \_ informations sur les travaux \_ 2A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4ef71-216">**\_JOB\_INFO\_2W** (Unicode) and **\_JOB\_INFO\_2A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="4ef71-217">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ef71-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ef71-218">Impression</span><span class="sxs-lookup"><span data-stu-id="4ef71-218">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4ef71-219">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="4ef71-219">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="4ef71-220">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="4ef71-220">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="4ef71-221">**EnumJobs**</span><span class="sxs-lookup"><span data-stu-id="4ef71-221">**EnumJobs**</span></span>](enumjobs.md)
</dt> <dt>

[<span data-ttu-id="4ef71-222">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="4ef71-222">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="4ef71-223">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="4ef71-223">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

