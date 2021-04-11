---
description: La fonction GetJob récupère des informations sur un travail d’impression spécifié.
ms.assetid: 57e59f84-d2a0-4722-b0fc-6673f7bb5c57
title: GetJob, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetJob
- GetJobA
- GetJobW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 73ae36ebab4530bf21eb86918fdbbbe941ed0741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202811"
---
# <a name="getjob-function"></a><span data-ttu-id="31f5d-103">GetJob fonction)</span><span class="sxs-lookup"><span data-stu-id="31f5d-103">GetJob function</span></span>

<span data-ttu-id="31f5d-104">La fonction **GetJob** récupère des informations sur un travail d’impression spécifié.</span><span class="sxs-lookup"><span data-stu-id="31f5d-104">The **GetJob** function retrieves information about a specified print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="31f5d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31f5d-105">Syntax</span></span>


```C++
BOOL GetJob(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   JobId,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pJob,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="31f5d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="31f5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31f5d-107">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="31f5d-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31f5d-108">Handle vers l’imprimante pour laquelle les données du travail d’impression sont récupérées.</span><span class="sxs-lookup"><span data-stu-id="31f5d-108">A handle to the printer for which the print-job data is retrieved.</span></span> <span data-ttu-id="31f5d-109">Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="31f5d-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="31f5d-110">*JobID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="31f5d-110">*JobId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31f5d-111">Identifie le travail d’impression dont les données doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="31f5d-111">Identifies the print job for which to retrieve data.</span></span> <span data-ttu-id="31f5d-112">Utilisez la fonction [**AddJob**](addjob.md) ou la fonction [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) pour obtenir un identificateur de travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="31f5d-112">Use the [**AddJob**](addjob.md) function or [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) function to get a print job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="31f5d-113">De *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="31f5d-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31f5d-114">Type d’informations retournées dans la mémoire tampon *pJob* .</span><span class="sxs-lookup"><span data-stu-id="31f5d-114">The type of information returned in the *pJob* buffer.</span></span> <span data-ttu-id="31f5d-115">Si le *niveau* est 1, *pJob* reçoit une structure [**\_ informations sur le travail \_ 1**](job-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="31f5d-115">If *Level* is 1, *pJob* receives a [**JOB\_INFO\_1**](job-info-1.md) structure.</span></span> <span data-ttu-id="31f5d-116">Si le *niveau* est 2, *pJob* reçoit une structure d' [**informations de travail \_ \_ 2**](job-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="31f5d-116">If *Level* is 2, *pJob* receives a [**JOB\_INFO\_2**](job-info-2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="31f5d-117">*pJob* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="31f5d-117">*pJob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31f5d-118">Pointeur vers une mémoire tampon qui reçoit un [**Job \_ information \_ 1**](job-info-1.md) ou une structure [**Job \_ information \_ 2**](job-info-2.md) contenant des informations sur le travail.</span><span class="sxs-lookup"><span data-stu-id="31f5d-118">A pointer to a buffer that receives a [**JOB\_INFO\_1**](job-info-1.md) or a [**JOB\_INFO\_2**](job-info-2.md) structure containing information about the job.</span></span> <span data-ttu-id="31f5d-119">La mémoire tampon doit être suffisamment grande pour stocker les chaînes pointées par les membres de la structure.</span><span class="sxs-lookup"><span data-stu-id="31f5d-119">The buffer must be large enough to store the strings pointed to by the structure members.</span></span>

<span data-ttu-id="31f5d-120">Pour déterminer la taille de mémoire tampon requise, appelez **GetJob** avec *cbBuf* défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="31f5d-120">To determine the required buffer size, call **GetJob** with *cbBuf* set to zero.</span></span> <span data-ttu-id="31f5d-121">**GetJob** échoue, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une \_ erreur \_ de mémoire tampon insuffisante et le paramètre *pcbNeeded* retourne la taille, en octets, de la mémoire tampon nécessaire pour contenir le tableau de structures et leurs données.</span><span class="sxs-lookup"><span data-stu-id="31f5d-121">**GetJob** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="31f5d-122">*cbBuf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="31f5d-122">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31f5d-123">Taille, en octets, du tableau.</span><span class="sxs-lookup"><span data-stu-id="31f5d-123">The size, in bytes, of the array.</span></span>

</dd> <dt>

<span data-ttu-id="31f5d-124">*pcbNeeded* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="31f5d-124">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31f5d-125">Pointeur vers une valeur qui spécifie le nombre d’octets copiés si la fonction est réussie ou le nombre d’octets requis si *cbBuf* est trop petit.</span><span class="sxs-lookup"><span data-stu-id="31f5d-125">A pointer to a value that specifies the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31f5d-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="31f5d-126">Return value</span></span>

<span data-ttu-id="31f5d-127">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="31f5d-127">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="31f5d-128">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="31f5d-128">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="31f5d-129">Notes</span><span class="sxs-lookup"><span data-stu-id="31f5d-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="31f5d-130">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="31f5d-130">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="31f5d-131">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="31f5d-131">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="31f5d-132">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="31f5d-132">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="31f5d-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31f5d-133">Requirements</span></span>



| <span data-ttu-id="31f5d-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31f5d-134">Requirement</span></span> | <span data-ttu-id="31f5d-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="31f5d-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31f5d-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31f5d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="31f5d-137">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="31f5d-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="31f5d-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31f5d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="31f5d-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="31f5d-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="31f5d-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="31f5d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="31f5d-141"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="31f5d-141"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="31f5d-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="31f5d-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="31f5d-143"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31f5d-143"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="31f5d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="31f5d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31f5d-145"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="31f5d-145"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="31f5d-146">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="31f5d-146">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="31f5d-147">**GetJobW** (Unicode) et **GetJobA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="31f5d-147">**GetJobW** (Unicode) and **GetJobA** (ANSI)</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="31f5d-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31f5d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31f5d-149">Impression</span><span class="sxs-lookup"><span data-stu-id="31f5d-149">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="31f5d-150">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="31f5d-150">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="31f5d-151">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="31f5d-151">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="31f5d-152">**\_Informations sur le travail \_ 1**</span><span class="sxs-lookup"><span data-stu-id="31f5d-152">**JOB\_INFO\_1**</span></span>](job-info-1.md)
</dt> <dt>

[<span data-ttu-id="31f5d-153">**\_Informations sur le travail \_ 2**</span><span class="sxs-lookup"><span data-stu-id="31f5d-153">**JOB\_INFO\_2**</span></span>](job-info-2.md)
</dt> <dt>

[<span data-ttu-id="31f5d-154">**ScheduleJob**</span><span class="sxs-lookup"><span data-stu-id="31f5d-154">**ScheduleJob**</span></span>](schedulejob.md)
</dt> <dt>

[<span data-ttu-id="31f5d-155">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="31f5d-155">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

