---
description: La fonction EnumJobs récupère des informations sur un ensemble spécifié de travaux d’impression pour une imprimante spécifiée.
ms.assetid: 1cf429ea-b40e-4063-b6de-c43b7b87f3d3
title: Fonction EnumJobs (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumJobs
- EnumJobsA
- EnumJobsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 174f58ba3fb1012e6ff46612fe312579969e6945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203857"
---
# <a name="enumjobs-function"></a><span data-ttu-id="bc8b6-103">EnumJobs, fonction</span><span class="sxs-lookup"><span data-stu-id="bc8b6-103">EnumJobs function</span></span>

<span data-ttu-id="bc8b6-104">La fonction **EnumJobs** récupère des informations sur un ensemble spécifié de travaux d’impression pour une imprimante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-104">The **EnumJobs** function retrieves information about a specified set of print jobs for a specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc8b6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc8b6-105">Syntax</span></span>


```C++
BOOL EnumJobs(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   FirstJob,
  _In_  DWORD   NoJobs,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pJob,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="bc8b6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc8b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc8b6-107">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bc8b6-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc8b6-108">Handle vers l’objet Printer dont les tâches d’impression sont énumérées par la fonction.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-108">A handle to the printer object whose print jobs the function enumerates.</span></span> <span data-ttu-id="bc8b6-109">Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="bc8b6-110">*FirstJob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bc8b6-110">*FirstJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc8b6-111">Position de base zéro dans la file d’attente à l’impression du premier travail d’impression à énumérer.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-111">The zero-based position within the print queue of the first print job to enumerate.</span></span> <span data-ttu-id="bc8b6-112">Par exemple, la valeur 0 spécifie que l’énumération doit commencer au premier travail d’impression dans la file d’attente à l’impression ; la valeur 9 spécifie que l’énumération doit commencer au dixième travail d’impression dans la file d’attente à l’impression.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-112">For example, a value of 0 specifies that enumeration should begin at the first print job in the print queue; a value of 9 specifies that enumeration should begin at the tenth print job in the print queue.</span></span>

</dd> <dt>

<span data-ttu-id="bc8b6-113">*Nojobs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bc8b6-113">*NoJobs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc8b6-114">Nombre total de travaux d’impression à énumérer.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-114">The total number of print jobs to enumerate.</span></span>

</dd> <dt>

<span data-ttu-id="bc8b6-115">De *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bc8b6-115">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc8b6-116">Type d’informations retournées dans la mémoire tampon *pJob* .</span><span class="sxs-lookup"><span data-stu-id="bc8b6-116">The type of information returned in the *pJob* buffer.</span></span>



| <span data-ttu-id="bc8b6-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc8b6-117">Value</span></span>                                                                                                | <span data-ttu-id="bc8b6-118">Signification</span><span class="sxs-lookup"><span data-stu-id="bc8b6-118">Meaning</span></span>                                                                              |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="bc8b6-119"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="bc8b6-119"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="bc8b6-120">*pJob* reçoit un tableau de structures [**Job \_ info \_ 1**](job-info-1.md)</span><span class="sxs-lookup"><span data-stu-id="bc8b6-120">*pJob* receives an array of [**JOB\_INFO\_1**](job-info-1.md) structures</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="bc8b6-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="bc8b6-121"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="bc8b6-122">*pJob* reçoit un tableau de structures [**Job \_ info \_ 2**](job-info-2.md)</span><span class="sxs-lookup"><span data-stu-id="bc8b6-122">*pJob* receives an array of [**JOB\_INFO\_2**](job-info-2.md) structures</span></span><br/> |
| <span id="3"></span><dl> <span data-ttu-id="bc8b6-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="bc8b6-123"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="bc8b6-124">*pJob* reçoit un tableau de structures [**Job \_ info \_ 3**](job-info-3.md)</span><span class="sxs-lookup"><span data-stu-id="bc8b6-124">*pJob* receives an array of [**JOB\_INFO\_3**](job-info-3.md) structures</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bc8b6-125">*pJob* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bc8b6-125">*pJob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc8b6-126">Pointeur vers une mémoire tampon qui reçoit un tableau d' [**informations sur le travail \_ \_ 1**](job-info-1.md), des [**\_ informations sur le travail \_ 2**](job-info-2.md)ou des structures [**Job \_ info \_ 3**](job-info-3.md) .</span><span class="sxs-lookup"><span data-stu-id="bc8b6-126">A pointer to a buffer that receives an array of [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), or [**JOB\_INFO\_3**](job-info-3.md) structures.</span></span> <span data-ttu-id="bc8b6-127">La mémoire tampon doit être suffisamment grande pour recevoir le tableau de structures et toutes les chaînes ou autres données auxquelles les membres de la structure pointent.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-127">The buffer must be large enough to receive the array of structures and any strings or other data to which the structure members point.</span></span>

<span data-ttu-id="bc8b6-128">Pour déterminer la taille de mémoire tampon requise, appelez **EnumJobs** avec *cbBuf* défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-128">To determine the required buffer size, call **EnumJobs** with *cbBuf* set to zero.</span></span> <span data-ttu-id="bc8b6-129">Échec de **EnumJobs** , [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une erreur \_ \_ de mémoire tampon insuffisante et le paramètre *pcbNeeded* retourne la taille, en octets, de la mémoire tampon nécessaire pour contenir le tableau de structures et leurs données.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-129">**EnumJobs** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="bc8b6-130">*cbBuf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bc8b6-130">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc8b6-131">Taille, en octets, de la mémoire tampon *pJob* .</span><span class="sxs-lookup"><span data-stu-id="bc8b6-131">The size, in bytes, of the *pJob* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="bc8b6-132">*pcbNeeded* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bc8b6-132">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc8b6-133">Pointeur vers une variable qui reçoit le nombre d’octets copiés si la fonction est réussie.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-133">A pointer to a variable that receives the number of bytes copied if the function succeeds.</span></span> <span data-ttu-id="bc8b6-134">Si la fonction échoue, la variable reçoit le nombre d’octets requis.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-134">If the function fails, the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="bc8b6-135">*pcReturned* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bc8b6-135">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc8b6-136">Pointeur vers une variable qui reçoit le nombre d' [**\_ informations sur le travail \_ 1**](job-info-1.md), les [**\_ informations sur le travail \_ 2**](job-info-2.md)ou les structures d' [**informations de travail \_ \_ 3**](job-info-3.md) retournées dans la mémoire tampon *pJob* .</span><span class="sxs-lookup"><span data-stu-id="bc8b6-136">A pointer to a variable that receives the number of [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), or [**JOB\_INFO\_3**](job-info-3.md) structures returned in the *pJob* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc8b6-137">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bc8b6-137">Return value</span></span>

<span data-ttu-id="bc8b6-138">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-138">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="bc8b6-139">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-139">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc8b6-140">Notes</span><span class="sxs-lookup"><span data-stu-id="bc8b6-140">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bc8b6-141">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-141">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="bc8b6-142">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-142">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="bc8b6-143">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-143">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="bc8b6-144">La [**structure \_ informations \_ sur le travail 1**](job-info-1.md) contient des informations générales sur le travail d’impression ; la structure des informations de [**travail \_ \_ 2**](job-info-2.md) présente des informations bien plus détaillées.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-144">The [**JOB\_INFO\_1**](job-info-1.md) structure contains general print-job information; the [**JOB\_INFO\_2**](job-info-2.md) structure has much more detailed information.</span></span> <span data-ttu-id="bc8b6-145">La structure [**Job \_ info \_ 3**](job-info-3.md) contient des informations sur la façon dont les tâches sont liées.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-145">The [**JOB\_INFO\_3**](job-info-3.md) structure contains information about how jobs are linked.</span></span>

<span data-ttu-id="bc8b6-146">Pour déterminer le nombre de travaux d’impression dans la file d’attente de l’imprimante, appelez la fonction [**GetPrinter**](getprinter.md) avec le paramètre de *niveau* défini sur 2.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-146">To determine the number of print jobs in the printer queue, call the [**GetPrinter**](getprinter.md) function with the *Level* parameter set to 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc8b6-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc8b6-147">Requirements</span></span>



| <span data-ttu-id="bc8b6-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc8b6-148">Requirement</span></span> | <span data-ttu-id="bc8b6-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc8b6-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc8b6-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc8b6-150">Minimum supported client</span></span><br/> | <span data-ttu-id="bc8b6-151">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc8b6-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bc8b6-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc8b6-152">Minimum supported server</span></span><br/> | <span data-ttu-id="bc8b6-153">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc8b6-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bc8b6-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="bc8b6-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc8b6-155"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bc8b6-155"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="bc8b6-156">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bc8b6-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="bc8b6-157"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc8b6-157"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="bc8b6-158">DLL</span><span class="sxs-lookup"><span data-stu-id="bc8b6-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc8b6-159"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="bc8b6-159"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="bc8b6-160">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="bc8b6-160">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bc8b6-161">**EnumJobsW** (Unicode) et **EnumJobsA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bc8b6-161">**EnumJobsW** (Unicode) and **EnumJobsA** (ANSI)</span></span><br/>                                               |



## <a name="see-also"></a><span data-ttu-id="bc8b6-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc8b6-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc8b6-163">Impression</span><span class="sxs-lookup"><span data-stu-id="bc8b6-163">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="bc8b6-164">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="bc8b6-164">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="bc8b6-165">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="bc8b6-165">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="bc8b6-166">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="bc8b6-166">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="bc8b6-167">**\_Informations sur le travail \_ 1**</span><span class="sxs-lookup"><span data-stu-id="bc8b6-167">**JOB\_INFO\_1**</span></span>](job-info-1.md)
</dt> <dt>

[<span data-ttu-id="bc8b6-168">**\_Informations sur le travail \_ 2**</span><span class="sxs-lookup"><span data-stu-id="bc8b6-168">**JOB\_INFO\_2**</span></span>](job-info-2.md)
</dt> <dt>

[<span data-ttu-id="bc8b6-169">**\_Informations sur le travail \_ 3**</span><span class="sxs-lookup"><span data-stu-id="bc8b6-169">**JOB\_INFO\_3**</span></span>](job-info-3.md)
</dt> <dt>

[<span data-ttu-id="bc8b6-170">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="bc8b6-170">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="bc8b6-171">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="bc8b6-171">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

