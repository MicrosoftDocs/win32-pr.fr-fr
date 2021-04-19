---
description: La fonction SetJob suspend, reprend, annule ou redémarre un travail d’impression sur une imprimante spécifiée. Vous pouvez également utiliser la fonction SetJob pour définir les paramètres du travail d’impression, tels que la priorité du travail d’impression et le nom du document.
ms.assetid: 21947c69-c517-4962-8eb7-b45ed4211d9a
title: SetJob, fonction (WinSpool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetJob
- SetJobA
- SetJobW
api_type:
- DllExport
api_location:
- WinSpool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 34dfc8c0239a10d7e7f036beed457d57329f4c67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543516"
---
# <a name="setjob-function"></a><span data-ttu-id="d95af-104">SetJob fonction)</span><span class="sxs-lookup"><span data-stu-id="d95af-104">SetJob function</span></span>

<span data-ttu-id="d95af-105">La fonction **SetJob** suspend, reprend, annule ou redémarre un travail d’impression sur une imprimante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d95af-105">The **SetJob** function pauses, resumes, cancels, or restarts a print job on a specified printer.</span></span> <span data-ttu-id="d95af-106">Vous pouvez également utiliser la fonction **SetJob** pour définir les paramètres du travail d’impression, tels que la priorité du travail d’impression et le nom du document.</span><span class="sxs-lookup"><span data-stu-id="d95af-106">You can also use the **SetJob** function to set print job parameters, such as the print job priority and the document name.</span></span>

<span data-ttu-id="d95af-107">Vous pouvez utiliser la fonction **SetJob** pour fournir une commande à un travail d’impression ou pour définir des paramètres de travail d’impression, ou pour effectuer les deux dans le même appel.</span><span class="sxs-lookup"><span data-stu-id="d95af-107">You can use the **SetJob** function to give a command to a print job, or to set print job parameters, or to do both in the same call.</span></span> <span data-ttu-id="d95af-108">La valeur du paramètre de *commande* n’affecte pas la manière dont la fonction utilise les paramètres *Level* et *pJob* .</span><span class="sxs-lookup"><span data-stu-id="d95af-108">The value of the *Command* parameter does not affect how the function uses the *Level* and *pJob* parameters.</span></span> <span data-ttu-id="d95af-109">En outre, vous pouvez utiliser **SetJob** avec les [**informations de travail \_ \_ 3**](job-info-3.md) pour lier ensemble un ensemble de travaux d’impression.</span><span class="sxs-lookup"><span data-stu-id="d95af-109">Also, you can use **SetJob** with [**JOB\_INFO\_3**](job-info-3.md) to link together a set of print jobs.</span></span> <span data-ttu-id="d95af-110">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="d95af-110">See Remarks for more information.</span></span>

## <a name="syntax"></a><span data-ttu-id="d95af-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d95af-111">Syntax</span></span>


```C++
BOOL SetJob(
  _In_ HANDLE hPrinter,
  _In_ DWORD  JobId,
  _In_ DWORD  Level,
  _In_ LPBYTE pJob,
  _In_ DWORD  Command
);
```



## <a name="parameters"></a><span data-ttu-id="d95af-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d95af-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d95af-113">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d95af-113">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d95af-114">Handle vers l’objet Printer qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="d95af-114">A handle to the printer object of interest.</span></span> <span data-ttu-id="d95af-115">Utilisez la fonction [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="d95af-115">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="d95af-116">*JobID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d95af-116">*JobId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d95af-117">Identificateur qui spécifie le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="d95af-117">Identifier that specifies the print job.</span></span> <span data-ttu-id="d95af-118">Vous obtenez un identificateur de travail d’impression en appelant la fonction [**AddJob**](addjob.md) ou la fonction [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) .</span><span class="sxs-lookup"><span data-stu-id="d95af-118">You obtain a print job identifier by calling the [**AddJob**](addjob.md) function or the [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) function.</span></span>

<span data-ttu-id="d95af-119">Si le paramètre *Level* a la valeur 3, le paramètre *JobID* doit correspondre au membre **JobID** de la structure [**Job \_ info \_ 3**](job-info-3.md) pointé par *pJob*</span><span class="sxs-lookup"><span data-stu-id="d95af-119">If the *Level* parameter is set to 3, the *JobId* parameter must match the **JobId** member of the [**JOB\_INFO\_3**](job-info-3.md) structure pointed to by *pJob*</span></span>

</dd> <dt>

<span data-ttu-id="d95af-120">De *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d95af-120">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d95af-121">Type de structure d’informations de travail vers lequel pointe le paramètre *pJob* .</span><span class="sxs-lookup"><span data-stu-id="d95af-121">The type of job information structure pointed to by the *pJob* parameter.</span></span>

<span data-ttu-id="d95af-122">**Toutes les versions de Windows**: vous pouvez définir le paramètre de *niveau* sur 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="d95af-122">**All versions of Windows**: You can set the *Level* parameter to 0, 1, or 2.</span></span> <span data-ttu-id="d95af-123">Lorsque vous définissez *Level* sur 0, *pJob* doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="d95af-123">When you set *Level* to 0, *pJob* should be **NULL**.</span></span> <span data-ttu-id="d95af-124">Utilisez ces valeurs lorsque vous ne définissez pas de paramètres de travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="d95af-124">Use these values when you are not setting any print job parameters.</span></span>

<span data-ttu-id="d95af-125">Vous pouvez également définir le paramètre de *niveau* sur 3.</span><span class="sxs-lookup"><span data-stu-id="d95af-125">You can also set the *Level* parameter to 3.</span></span>

<span data-ttu-id="d95af-126">À compter de **Windows Vista**: vous pouvez également définir le paramètre de *niveau* sur 4.</span><span class="sxs-lookup"><span data-stu-id="d95af-126">Starting with **Windows Vista**: You can also set the *Level* parameter to 4.</span></span>

</dd> <dt>

<span data-ttu-id="d95af-127">*pJob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d95af-127">*pJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d95af-128">Pointeur vers une structure qui définit les paramètres du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="d95af-128">A pointer to a structure that sets the print job parameters.</span></span>

<span data-ttu-id="d95af-129">**Toutes les versions de Windows**: *pJob* peut pointer vers une structure [**Job info \_ \_ 1**](job-info-1.md) ou [**Job \_ info \_ 2**](job-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="d95af-129">**All versions of Windows**: *pJob* can point to a [**JOB\_INFO\_1**](job-info-1.md) or [**JOB\_INFO\_2**](job-info-2.md) structure.</span></span>

<span data-ttu-id="d95af-130">*pJob* peut également pointer vers une structure d' [**informations de travail \_ \_ 3**](job-info-3.md) .</span><span class="sxs-lookup"><span data-stu-id="d95af-130">*pJob* can also point to a [**JOB\_INFO\_3**](job-info-3.md) structure.</span></span> <span data-ttu-id="d95af-131">Vous devez disposer de l’autorisation **\_ \_ administrer** l’accès au travail pour les travaux spécifiés par les membres **JobID** et **NextJobId** de la structure **Job \_ info \_ 3** .</span><span class="sxs-lookup"><span data-stu-id="d95af-131">You must have **JOB\_ACCESS\_ADMINISTER** access permission for the jobs specified by the **JobId** and **NextJobId** members of the **JOB\_INFO\_3** structure.</span></span>

<span data-ttu-id="d95af-132">À compter de **Windows Vista**: *pJob* peut également pointer vers une structure d' [**informations de travail \_ \_ 4**](job-info-4.md) .</span><span class="sxs-lookup"><span data-stu-id="d95af-132">Starting with **Windows Vista**: *pJob* can also point to a [**JOB\_INFO\_4**](job-info-4.md) structure.</span></span>

<span data-ttu-id="d95af-133">Si le paramètre *Level* est égal à 0, *pJob* doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="d95af-133">If the *Level* parameter is 0, *pJob* should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d95af-134">*Commande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d95af-134">*Command* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d95af-135">Opération de travail d’impression à effectuer.</span><span class="sxs-lookup"><span data-stu-id="d95af-135">The print job operation to perform.</span></span> <span data-ttu-id="d95af-136">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d95af-136">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="d95af-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="d95af-137">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="d95af-138">Signification</span><span class="sxs-lookup"><span data-stu-id="d95af-138">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="JOB_CONTROL_CANCEL"></span><span id="job_control_cancel"></span><dl> <span data-ttu-id="d95af-139"><dt>**\_annulation du contrôle de travail \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d95af-139"><dt>**JOB\_CONTROL\_CANCEL**</dt></span></span> </dl>                                    | <span data-ttu-id="d95af-140">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="d95af-140">Do not use.</span></span> <span data-ttu-id="d95af-141">Pour supprimer un travail d’impression, utilisez l' **opération de \_ \_ Suppression de contrôle de tâche**.</span><span class="sxs-lookup"><span data-stu-id="d95af-141">To delete a print job, use **JOB\_CONTROL\_DELETE**.</span></span><br/>        |
| <span id="JOB_CONTROL_PAUSE"></span><span id="job_control_pause"></span><dl> <span data-ttu-id="d95af-142"><dt>**\_pause du contrôle de travail \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d95af-142"><dt>**JOB\_CONTROL\_PAUSE**</dt></span></span> </dl>                                       | <span data-ttu-id="d95af-143">Suspendez le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="d95af-143">Pause the print job.</span></span><br/>                                                    |
| <span id="JOB_CONTROL_RESTART"></span><span id="job_control_restart"></span><dl> <span data-ttu-id="d95af-144"><dt>**redémarrage du contrôle de travail \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d95af-144"><dt>**JOB\_CONTROL\_RESTART**</dt></span></span> </dl>                                 | <span data-ttu-id="d95af-145">Redémarrez le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="d95af-145">Restart the print job.</span></span> <span data-ttu-id="d95af-146">Un travail ne peut être redémarré que s’il a été imprimé.</span><span class="sxs-lookup"><span data-stu-id="d95af-146">A job can only be restarted if it was printing.</span></span><br/>  |
| <span id="JOB_CONTROL_RESUME"></span><span id="job_control_resume"></span><dl> <span data-ttu-id="d95af-147"><dt>**\_reprise du contrôle de travail \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d95af-147"><dt>**JOB\_CONTROL\_RESUME**</dt></span></span> </dl>                                    | <span data-ttu-id="d95af-148">Reprendre un travail d’impression suspendu.</span><span class="sxs-lookup"><span data-stu-id="d95af-148">Resume a paused print job.</span></span><br/>                                              |
| <span id="JOB_CONTROL_DELETE"></span><span id="job_control_delete"></span><dl> <span data-ttu-id="d95af-149"><dt>**\_suppression du contrôle de travail \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d95af-149"><dt>**JOB\_CONTROL\_DELETE**</dt></span></span> </dl>                                    | <span data-ttu-id="d95af-150">Supprimez le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="d95af-150">Delete the print job.</span></span><br/>                                                   |
| <span id="JOB_CONTROL_SENT_TO_PRINTER"></span><span id="job_control_sent_to_printer"></span><dl> <span data-ttu-id="d95af-151"><dt>**\_contrôle \_ de travail envoyé à l' \_ \_ imprimante**</dt></span><span class="sxs-lookup"><span data-stu-id="d95af-151"><dt>**JOB\_CONTROL\_SENT\_TO\_PRINTER**</dt></span></span> </dl>       | <span data-ttu-id="d95af-152">Utilisé par les moniteurs de port pour mettre fin au travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="d95af-152">Used by port monitors to end the print job.</span></span><br/>                             |
| <span id="JOB_CONTROL_LAST_PAGE_EJECTED"></span><span id="job_control_last_page_ejected"></span><dl> <span data-ttu-id="d95af-153"><dt>**\_dernière page du contrôle des travaux \_ \_ \_ éjectée**</dt></span><span class="sxs-lookup"><span data-stu-id="d95af-153"><dt>**JOB\_CONTROL\_LAST\_PAGE\_EJECTED**</dt></span></span> </dl> | <span data-ttu-id="d95af-154">Utilisé par les moniteurs de langage pour mettre fin au travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="d95af-154">Used by language monitors to end the print job.</span></span><br/>                         |
| <span id="JOB_CONTROL_RETAIN"></span><span id="job_control_retain"></span><dl> <span data-ttu-id="d95af-155"><dt>**\_conservation du contrôle de travail \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d95af-155"><dt>**JOB\_CONTROL\_RETAIN**</dt></span></span> </dl>                                    | <span data-ttu-id="d95af-156">**Windows Vista et versions ultérieures**: conservez le travail dans la file d’attente après son impression.</span><span class="sxs-lookup"><span data-stu-id="d95af-156">**Windows Vista and later**: Keep the job in the queue after it prints.</span></span><br/> |
| <span id="JOB_CONTROL_RELEASE"></span><span id="job_control_release"></span><dl> <span data-ttu-id="d95af-157"><dt>**\_version de contrôle du travail \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d95af-157"><dt>**JOB\_CONTROL\_RELEASE**</dt></span></span> </dl>                                 | <span data-ttu-id="d95af-158">**Windows Vista et versions ultérieures**: Libérez le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="d95af-158">**Windows Vista and later**: Release the print job.</span></span><br/>                     |



 

<span data-ttu-id="d95af-159">Vous pouvez utiliser le même appel à la fonction **SetJob** pour définir les paramètres du travail d’impression et fournir une commande à un travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="d95af-159">You can use the same call to the **SetJob** function to set print job parameters and to give a command to a print job.</span></span> <span data-ttu-id="d95af-160">Par conséquent, la *commande* ne doit pas avoir la valeur 0 si vous définissez des paramètres de travail d’impression, bien que cela puisse être le cas.</span><span class="sxs-lookup"><span data-stu-id="d95af-160">Thus, *Command* does not need to be 0 if you are setting print job parameters, although it can be.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d95af-161">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d95af-161">Return value</span></span>

<span data-ttu-id="d95af-162">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="d95af-162">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="d95af-163">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="d95af-163">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d95af-164">Notes</span><span class="sxs-lookup"><span data-stu-id="d95af-164">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d95af-165">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="d95af-165">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="d95af-166">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="d95af-166">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="d95af-167">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="d95af-167">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="d95af-168">Vous pouvez utiliser la fonction **SetJob** pour définir différents paramètres de travail d’impression en fournissant un pointeur vers une structure [**Job information \_ \_ 1**](job-info-1.md), Job info [**\_ \_ 2**](job-info-2.md), [**Job \_ info \_ 3**](job-info-3.md)ou [**Job \_ info \_ 4**](job-info-4.md) qui contient les données nécessaires.</span><span class="sxs-lookup"><span data-stu-id="d95af-168">You can use the **SetJob** function to set various print job parameters by supplying a pointer to a [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), [**JOB\_INFO\_3**](job-info-3.md), or [**JOB\_INFO\_4**](job-info-4.md) structure that contains the necessary data.</span></span>

<span data-ttu-id="d95af-169">Pour supprimer ou supprimer tous les travaux d’impression pour une imprimante spécifique, appelez la fonction [**SetPrinter**](setprinter.md) avec son paramètre de *commande* défini **sur \_ \_ vidage du contrôle** de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="d95af-169">To remove or delete all of the print jobs for a particular printer, call the [**SetPrinter**](setprinter.md) function with its *Command* parameter set to **PRINTER\_CONTROL\_PURGE**.</span></span>

<span data-ttu-id="d95af-170">Les membres suivants d’une structure [**Job information \_ \_ 1**](job-info-1.md), [**Job \_ info \_ 2**](job-info-2.md)ou [**Job \_ info \_ 4**](job-info-4.md) sont ignorés lors d’un appel à **SetJob**: **JobID**, **pPrinterName**, **pMachineName**, **pUserName**, **pDrivername**, **Size**, **sent**, **Time** et **TotalPages**.</span><span class="sxs-lookup"><span data-stu-id="d95af-170">The following members of a [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), or [**JOB\_INFO\_4**](job-info-4.md) structure are ignored on a call to **SetJob**: **JobId**, **pPrinterName**, **pMachineName**, **pUserName**, **pDrivername**, **Size**, **Submitted**, **Time**, and **TotalPages**.</span></span>

<span data-ttu-id="d95af-171">Vous devez disposer de l’autorisation **\_ \_ administrer** l’accès à l’imprimante pour une imprimante afin de modifier la position d’un travail d’impression dans la file d’attente à l’impression.</span><span class="sxs-lookup"><span data-stu-id="d95af-171">You must have **PRINTER\_ACCESS\_ADMINISTER** access permission for a printer in order to change a print job's position in the print queue.</span></span>

<span data-ttu-id="d95af-172">Si vous ne souhaitez pas définir la position d’un travail d’impression dans la file d’attente à l’impression, vous devez définir le membre **position** de la structure Job information [**\_ \_ 1**](job-info-1.md), [**Job \_ info \_ 2**](job-info-2.md)ou [**Job \_ info \_ 4**](job-info-4.md) sur **Job \_ position \_ Unspecified**.</span><span class="sxs-lookup"><span data-stu-id="d95af-172">If you do not want to set a print job's position in the print queue, you should set the **Position** member of the [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), or [**JOB\_INFO\_4**](job-info-4.md) structure to **JOB\_POSITION\_UNSPECIFIED**.</span></span>

<span data-ttu-id="d95af-173">Utilisez la fonction **SetJob** avec la structure [**Job \_ info \_ 3**](job-info-3.md) pour lier ensemble un ensemble de travaux d’impression (également appelé chaîne).</span><span class="sxs-lookup"><span data-stu-id="d95af-173">Use the **SetJob** function with the [**JOB\_INFO\_3**](job-info-3.md) structure to link together a set of print jobs (also known as a chain).</span></span> <span data-ttu-id="d95af-174">Cela est utile dans les situations où un document unique est constitué de plusieurs parties que vous souhaitez restituer séparément.</span><span class="sxs-lookup"><span data-stu-id="d95af-174">This is useful in situations where a single document consists of several parts that you want to render separately.</span></span> <span data-ttu-id="d95af-175">Pour imprimer les travaux A, B, C et D dans l’ordre, appelez **SetJob** avec les [**informations de travail \_ \_ 4**](job-info-4.md) pour lier A à b, b à c et c à D.</span><span class="sxs-lookup"><span data-stu-id="d95af-175">To print jobs A, B, C, and D in order, call **SetJob** with [**JOB\_INFO\_4**](job-info-4.md) to link A to B, B to C, and C to D.</span></span>

<span data-ttu-id="d95af-176">Si vous liez des travaux d’impression, notez les points suivants :</span><span class="sxs-lookup"><span data-stu-id="d95af-176">If you link print jobs, note the following:</span></span>

-   <span data-ttu-id="d95af-177">Les travaux peuvent être ajoutés au début ou à la fin d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="d95af-177">Jobs can be added to the beginning or end of a chain.</span></span>
-   <span data-ttu-id="d95af-178">Tous les travaux de la chaîne doivent avoir le même type de données.</span><span class="sxs-lookup"><span data-stu-id="d95af-178">All jobs in the chain must have the same data type.</span></span>
-   <span data-ttu-id="d95af-179">La chaîne doit être entièrement liée avant le début de la mise en file d’attente ; sinon, le spouleur peut imprimer et supprimer les travaux mis en attente avant de les lier tous.</span><span class="sxs-lookup"><span data-stu-id="d95af-179">The chain must be completely linked before spooling begins, otherwise the spooler may print and delete spooled jobs before you link them all.</span></span> <span data-ttu-id="d95af-180">Il existe deux façons de garder la chaîne imprime prématurément :</span><span class="sxs-lookup"><span data-stu-id="d95af-180">There are two ways to keep the chain from printing prematurely:</span></span>

    -   <span data-ttu-id="d95af-181">Suspendez la première tâche de la chaîne jusqu’à ce que la chaîne soit entièrement liée.</span><span class="sxs-lookup"><span data-stu-id="d95af-181">Pause the first job in the chain until the chain is completely linked.</span></span> <span data-ttu-id="d95af-182">L’état suspendu de la première tâche régit l’état de tous les travaux de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="d95af-182">The paused state of the first job governs the state of all jobs in the chain.</span></span>
    -   <span data-ttu-id="d95af-183">Conservez la première tâche incomplète, autrement dit, n’appelez pas [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) ou [**ScheduleJob**](schedulejob.md) pour le premier travail.</span><span class="sxs-lookup"><span data-stu-id="d95af-183">Keep the first job incomplete, that is, do not call [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) or [**ScheduleJob**](schedulejob.md) for the first job.</span></span> <span data-ttu-id="d95af-184">Toutefois, si l’option « imprimer pendant la mise en file d’attente » est activée (valeur par défaut), cette méthode bloque le port pendant la génération de la chaîne, ce qui empêche également l’impression des travaux non liés.</span><span class="sxs-lookup"><span data-stu-id="d95af-184">However, if 'print while spooling' is enabled (the default), this method blocks the port while the chain is built, which also prevents the printing of non-related jobs.</span></span>

-   <span data-ttu-id="d95af-185">L’application doit gérer le cas où l’utilisateur supprime un travail dans la chaîne avant la fin de l’impression de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="d95af-185">The application must handle the case where the user deletes a job in the chain before the chain finishes printing.</span></span> <span data-ttu-id="d95af-186">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne **un \_ paramètre non valide** lorsqu’un JobID n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="d95af-186">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **INVALID\_PARAMETER** when a JobID does not exist.</span></span>

## <a name="requirements"></a><span data-ttu-id="d95af-187">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d95af-187">Requirements</span></span>



| <span data-ttu-id="d95af-188">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d95af-188">Requirement</span></span> | <span data-ttu-id="d95af-189">Valeur</span><span class="sxs-lookup"><span data-stu-id="d95af-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d95af-190">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d95af-190">Minimum supported client</span></span><br/> | <span data-ttu-id="d95af-191">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d95af-191">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d95af-192">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d95af-192">Minimum supported server</span></span><br/> | <span data-ttu-id="d95af-193">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d95af-193">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d95af-194">En-tête</span><span class="sxs-lookup"><span data-stu-id="d95af-194">Header</span></span><br/>                   | <dl> <span data-ttu-id="d95af-195"><dt>WinSpool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d95af-195"><dt>WinSpool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d95af-196">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d95af-196">Library</span></span><br/>                  | <dl> <span data-ttu-id="d95af-197"><dt>WinSpool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d95af-197"><dt>WinSpool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="d95af-198">DLL</span><span class="sxs-lookup"><span data-stu-id="d95af-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d95af-199"><dt>WinSpool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="d95af-199"><dt>WinSpool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="d95af-200">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="d95af-200">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d95af-201">**SetJobW** (Unicode) et **SetJobA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d95af-201">**SetJobW** (Unicode) and **SetJobA** (ANSI)</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="d95af-202">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d95af-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d95af-203">Impression</span><span class="sxs-lookup"><span data-stu-id="d95af-203">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d95af-204">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="d95af-204">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="d95af-205">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="d95af-205">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="d95af-206">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="d95af-206">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="d95af-207">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="d95af-207">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="d95af-208">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="d95af-208">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="d95af-209">**\_Informations sur le travail \_ 1**</span><span class="sxs-lookup"><span data-stu-id="d95af-209">**JOB\_INFO\_1**</span></span>](job-info-1.md)
</dt> <dt>

[<span data-ttu-id="d95af-210">**\_Informations sur le travail \_ 2**</span><span class="sxs-lookup"><span data-stu-id="d95af-210">**JOB\_INFO\_2**</span></span>](job-info-2.md)
</dt> <dt>

[<span data-ttu-id="d95af-211">**\_Informations sur le travail \_ 3**</span><span class="sxs-lookup"><span data-stu-id="d95af-211">**JOB\_INFO\_3**</span></span>](job-info-3.md)
</dt> <dt>

[<span data-ttu-id="d95af-212">**\_Informations sur le travail \_ 4**</span><span class="sxs-lookup"><span data-stu-id="d95af-212">**JOB\_INFO\_4**</span></span>](job-info-4.md)
</dt> </dl>

 

