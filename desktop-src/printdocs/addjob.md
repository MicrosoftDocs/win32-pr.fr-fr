---
description: La fonction AddJob ajoute un travail d’impression à la liste des travaux d’impression qui peuvent être planifiés par le spouleur d’impression. La fonction récupère le nom du fichier que vous pouvez utiliser pour stocker le travail.
ms.assetid: cfafa874-6022-4bf4-bf3d-096213eb0c98
title: AddJob, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddJob
- AddJobA
- AddJobW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: ab21b98036975934c00e28d0be1d5670d4c0742c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756411"
---
# <a name="addjob-function"></a><span data-ttu-id="f1bda-104">AddJob fonction)</span><span class="sxs-lookup"><span data-stu-id="f1bda-104">AddJob function</span></span>

<span data-ttu-id="f1bda-105">La fonction **AddJob** ajoute un travail d’impression à la liste des travaux d’impression qui peuvent être planifiés par le spouleur d’impression.</span><span class="sxs-lookup"><span data-stu-id="f1bda-105">The **AddJob** function adds a print job to the list of print jobs that can be scheduled by the print spooler.</span></span> <span data-ttu-id="f1bda-106">La fonction récupère le nom du fichier que vous pouvez utiliser pour stocker le travail.</span><span class="sxs-lookup"><span data-stu-id="f1bda-106">The function retrieves the name of the file you can use to store the job.</span></span>

> [!NOTE]
> <span data-ttu-id="f1bda-107">Dans Windows 8 et les systèmes d’exploitation ultérieurs, nous ne recommandons pas l’utilisation directe de **AddJob** , car il existe des cas (par exemple, l’impression dans une file d’attente à l’aide de file : ou PORTPROMPT :) où **AddJob** échouera.</span><span class="sxs-lookup"><span data-stu-id="f1bda-107">In Windows 8 and later operating systems, we do not recommended using **AddJob** directly because there are cases (such as printing to a queue using File: or PORTPROMPT:) where **AddJob** will fail.</span></span> <span data-ttu-id="f1bda-108">Au lieu de cela, il est recommandé d’utiliser l' [API d’impression GDI](gdi-printing.md), l' [API d’impression XPS](xps-printing.md), [**StartDocPrinter**](startdocprinter.md)ou la méthode appropriée de l’espace de noms [**Windows. Graphics. Printing**](/uwp/api/Windows.Graphics.Printing) , en fonction du scénario d’impression.</span><span class="sxs-lookup"><span data-stu-id="f1bda-108">Instead, you are advised to use [GDI Print API](gdi-printing.md), [XPS Print API](xps-printing.md), [**StartDocPrinter**](startdocprinter.md), or the appropriate method from the [**Windows.Graphics.Printing**](/uwp/api/Windows.Graphics.Printing) namespace, depending on the print scenario.</span></span>
>
> <span data-ttu-id="f1bda-109">Si vous essayez d’imprimer dans une file d’attente à l’aide de **file :** ou **PORTPROMPT :**, **AddJob** retourne l' \_ erreur non prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f1bda-109">If you try to print to a queue using **File:** or **PORTPROMPT:**, **AddJob** will Return the NOT\_SUPPORTED error.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1bda-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1bda-110">Syntax</span></span>

```C++
BOOL AddJob(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pData,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```

## <a name="parameters"></a><span data-ttu-id="f1bda-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1bda-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1bda-112">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f1bda-112">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1bda-113">Handle qui spécifie l’imprimante pour le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="f1bda-113">A handle that specifies the printer for the print job.</span></span> <span data-ttu-id="f1bda-114">Il doit s’agir d’une imprimante locale configurée comme imprimante spoulée.</span><span class="sxs-lookup"><span data-stu-id="f1bda-114">This must be a local printer that is configured as a spooled printer.</span></span> <span data-ttu-id="f1bda-115">Si *hPrinter* est un handle vers une connexion d’imprimante distante, ou si l’imprimante est configurée pour l’impression directe, la fonction **AddJob** échoue.</span><span class="sxs-lookup"><span data-stu-id="f1bda-115">If *hPrinter* is a handle to a remote printer connection, or if the printer is configured for direct printing, the **AddJob** function fails.</span></span> <span data-ttu-id="f1bda-116">Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="f1bda-116">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="f1bda-117">De *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f1bda-117">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1bda-118">Version de la structure de données d’informations du travail d’impression que la fonction stocke dans la mémoire tampon vers laquelle pointe *pData*.</span><span class="sxs-lookup"><span data-stu-id="f1bda-118">The version of the print job information data structure that the function stores into the buffer pointed to by *pData*.</span></span> <span data-ttu-id="f1bda-119">Définissez ce paramètre sur un.</span><span class="sxs-lookup"><span data-stu-id="f1bda-119">Set this parameter to one.</span></span>

</dd> <dt>

<span data-ttu-id="f1bda-120">*pData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f1bda-120">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1bda-121">Pointeur vers une mémoire tampon qui reçoit une structure de données [**ADDJOB \_ information \_ 1**](addjob-info-1.md) et une chaîne de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="f1bda-121">A pointer to a buffer that receives an [**ADDJOB\_INFO\_1**](addjob-info-1.md) data structure and a path string.</span></span>

</dd> <dt>

<span data-ttu-id="f1bda-122">*cbBuf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f1bda-122">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1bda-123">Taille, en octets, de la mémoire tampon vers laquelle pointe *pData*.</span><span class="sxs-lookup"><span data-stu-id="f1bda-123">The size, in bytes, of the buffer pointed to by *pData*.</span></span> <span data-ttu-id="f1bda-124">La mémoire tampon doit être suffisamment grande pour contenir une structure [**ADDJOB \_ information \_ 1**](addjob-info-1.md) et une chaîne de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="f1bda-124">The buffer needs to be large enough to contain an [**ADDJOB\_INFO\_1**](addjob-info-1.md) structure and a path string.</span></span>

</dd> <dt>

<span data-ttu-id="f1bda-125">*pcbNeeded* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f1bda-125">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1bda-126">Pointeur vers une variable qui reçoit la taille totale, en octets, de la structure de données [**ADDJOB \_ info \_ 1**](addjob-info-1.md) plus la chaîne du chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="f1bda-126">A pointer to a variable that receives the total size, in bytes, of the [**ADDJOB\_INFO\_1**](addjob-info-1.md) data structure plus the path string.</span></span> <span data-ttu-id="f1bda-127">Si cette valeur est inférieure ou égale à *cbBuf* et que la fonction est réussie, il s’agit du nombre réel d’octets écrits dans la mémoire tampon pointée par *pData*.</span><span class="sxs-lookup"><span data-stu-id="f1bda-127">If this value is less than or equal to *cbBuf* and the function succeeds, this is the actual number of bytes written to the buffer pointed to by *pData*.</span></span> <span data-ttu-id="f1bda-128">Si ce nombre est supérieur à *cbBuf*, la mémoire tampon est insuffisante et vous devez appeler à nouveau la fonction avec une taille de mémoire tampon au moins aussi grande que \* *pcbNeeded*.</span><span class="sxs-lookup"><span data-stu-id="f1bda-128">If this number is greater than *cbBuf*, the buffer is too small, and you must call the function again with a buffer size at least as large as \**pcbNeeded*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1bda-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f1bda-129">Return value</span></span>

<span data-ttu-id="f1bda-130">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="f1bda-130">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="f1bda-131">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="f1bda-131">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1bda-132">Notes</span><span class="sxs-lookup"><span data-stu-id="f1bda-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f1bda-133">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="f1bda-133">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="f1bda-134">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="f1bda-134">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="f1bda-135">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="f1bda-135">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="f1bda-136">Vous pouvez appeler la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) pour ouvrir le fichier de mise en file d’attente spécifié par le membre **path** de la structure [**ADDJOB \_ info \_ 1**](addjob-info-1.md) , puis appeler la fonction [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) pour y écrire des données de travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="f1bda-136">You can call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open the spool file specified by the **Path** member of the [**ADDJOB\_INFO\_1**](addjob-info-1.md) structure, and then call the [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) function to write print job data to it.</span></span> <span data-ttu-id="f1bda-137">Après cela, appelez la fonction [**ScheduleJob**](schedulejob.md) pour notifier au spouleur d’impression que le travail d’impression peut désormais être planifié par le spouleur pour l’impression.</span><span class="sxs-lookup"><span data-stu-id="f1bda-137">After that is done, call the [**ScheduleJob**](schedulejob.md) function to notify the print spooler that the print job can now be scheduled by the spooler for printing.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1bda-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1bda-138">Requirements</span></span>



| <span data-ttu-id="f1bda-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1bda-139">Requirement</span></span> | <span data-ttu-id="f1bda-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1bda-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1bda-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1bda-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f1bda-142">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1bda-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f1bda-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1bda-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f1bda-144">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1bda-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f1bda-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="f1bda-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1bda-146"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1bda-146"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f1bda-147">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f1bda-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="f1bda-148"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1bda-148"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="f1bda-149">DLL</span><span class="sxs-lookup"><span data-stu-id="f1bda-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1bda-150"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="f1bda-150"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="f1bda-151">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="f1bda-151">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f1bda-152">**AddJobW** (Unicode) et **AddJobA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f1bda-152">**AddJobW** (Unicode) and **AddJobA** (ANSI)</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="f1bda-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1bda-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1bda-154">**\_Informations ADDJOB \_ 1**</span><span class="sxs-lookup"><span data-stu-id="f1bda-154">**ADDJOB\_INFO\_1**</span></span>](addjob-info-1.md)
</dt> <dt>

[<span data-ttu-id="f1bda-155">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="f1bda-155">**CreateFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="f1bda-156">API d’impression GDI</span><span class="sxs-lookup"><span data-stu-id="f1bda-156">GDI Print API</span></span>](gdi-printing.md)
</dt> <dt>

[<span data-ttu-id="f1bda-157">Impression</span><span class="sxs-lookup"><span data-stu-id="f1bda-157">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f1bda-158">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="f1bda-158">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="f1bda-159">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="f1bda-159">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="f1bda-160">**ScheduleJob**</span><span class="sxs-lookup"><span data-stu-id="f1bda-160">**ScheduleJob**</span></span>](schedulejob.md)
</dt> <dt>

[<span data-ttu-id="f1bda-161">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="f1bda-161">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="f1bda-162">**Windows. Graphics. Printing**</span><span class="sxs-lookup"><span data-stu-id="f1bda-162">**Windows.Graphics.Printing**</span></span>](/uwp/api/Windows.Graphics.Printing)
</dt> <dt>

[<span data-ttu-id="f1bda-163">**WriteFile**</span><span class="sxs-lookup"><span data-stu-id="f1bda-163">**WriteFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-writefile)
</dt> <dt>

[<span data-ttu-id="f1bda-164">API d’impression XPS</span><span class="sxs-lookup"><span data-stu-id="f1bda-164">XPS Print API</span></span>](xps-printing.md)
</dt> </dl>

 

