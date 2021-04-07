---
description: Signale au service spouleur d’impression si un travail d’impression XPS se trouve dans la phase de mise en file d’attente ou de rendu et quelle partie du traitement est actuellement en cours.
ms.assetid: 66f7483d-be98-410d-b0c7-430743397de2
title: ReportJobProcessingProgress, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReportJobProcessingProgress
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 327d2f7cffe2f90a5719de38cef4cd3fde17e086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952437"
---
# <a name="reportjobprocessingprogress-function"></a><span data-ttu-id="6050c-103">ReportJobProcessingProgress fonction)</span><span class="sxs-lookup"><span data-stu-id="6050c-103">ReportJobProcessingProgress function</span></span>

<span data-ttu-id="6050c-104">Signale au service spouleur d’impression si un travail d’impression XPS se trouve dans la phase de mise en file d’attente ou de rendu et quelle partie du traitement est actuellement en cours.</span><span class="sxs-lookup"><span data-stu-id="6050c-104">Reports to the Print Spooler service whether an XPS print job is in the spooling or the rendering phase and what part of the processing is currently underway.</span></span>

## <a name="syntax"></a><span data-ttu-id="6050c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6050c-105">Syntax</span></span>


```C++
HRESULT ReportJobProcessingProgress(
  _In_ HANDLE                printerHandle,
  _In_ ULONG                 jobId,
       EPrintXPSJobOperation jobOperation,
       EPrintXPSJobProgress  jobProgress
);
```



## <a name="parameters"></a><span data-ttu-id="6050c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6050c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6050c-107">*printerHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6050c-107">*printerHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6050c-108">Handle d’imprimante pour lequel la fonction doit récupérer des informations.</span><span class="sxs-lookup"><span data-stu-id="6050c-108">A printer handle for which the function is to retrieve information.</span></span> <span data-ttu-id="6050c-109">Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="6050c-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="6050c-110">*JobID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6050c-110">*jobId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6050c-111">Identifie le travail d’impression dont les données doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="6050c-111">Identifies the print job for which to retrieve data.</span></span> <span data-ttu-id="6050c-112">Utilisez la fonction [**AddJob**](addjob.md) ou la fonction [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) pour obtenir un identificateur de travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="6050c-112">Use the [**AddJob**](addjob.md) function or [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) function to get a print job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="6050c-113">*jobOperation*</span><span class="sxs-lookup"><span data-stu-id="6050c-113">*jobOperation*</span></span> 
</dt> <dd>

<span data-ttu-id="6050c-114">Spécifie si le travail se trouve dans la phase de mise en file d’attente ou dans la phase de rendu.</span><span class="sxs-lookup"><span data-stu-id="6050c-114">Specifies whether the job is in the spooling phase or the rendering phase.</span></span>

</dd> <dt>

<span data-ttu-id="6050c-115">*jobProgress*</span><span class="sxs-lookup"><span data-stu-id="6050c-115">*jobProgress*</span></span> 
</dt> <dd>

<span data-ttu-id="6050c-116">Spécifie quelle partie du traitement est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="6050c-116">Specifies what part of the processing is currently underway.</span></span> <span data-ttu-id="6050c-117">Cette valeur fait référence aux événements de la phase de mise en file d’attente ou de rendu en fonction de la valeur de *jobOperation*.</span><span class="sxs-lookup"><span data-stu-id="6050c-117">This value refers to events in either the spooling or rendering phase depending on the value of *jobOperation*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6050c-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6050c-118">Return value</span></span>

<span data-ttu-id="6050c-119">Si l’opération a échoué, la valeur de retour est S \_ OK, sinon le **HRESULT** contient un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="6050c-119">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="6050c-120">Pour plus d’informations sur les codes d’erreur COM, consultez [gestion des erreurs](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="6050c-120">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6050c-121">Notes</span><span class="sxs-lookup"><span data-stu-id="6050c-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6050c-122">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="6050c-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="6050c-123">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="6050c-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="6050c-124">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="6050c-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

> [!Note]  
> <span data-ttu-id="6050c-125">**ReportJobProcessingProgress** indique uniquement la progression du travail d’impression XPS si le travail d’impression est en phase de mise en file d’attente ou de rendu.</span><span class="sxs-lookup"><span data-stu-id="6050c-125">**ReportJobProcessingProgress** will only report the progress of the XPS print job if the print job is in the spooling or rendering phase.</span></span> <span data-ttu-id="6050c-126">**ReportJobProcessingProgress** échoue si elle est appelée lorsque le travail d’impression XPS n’est pas dans la phase de mise en file d’attente ou de rendu.</span><span class="sxs-lookup"><span data-stu-id="6050c-126">**ReportJobProcessingProgress** will fail if it is called when the XPS print job is not in the spooling or rendering phase.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6050c-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6050c-127">Requirements</span></span>



| <span data-ttu-id="6050c-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6050c-128">Requirement</span></span> | <span data-ttu-id="6050c-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="6050c-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6050c-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6050c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6050c-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6050c-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="6050c-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6050c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6050c-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6050c-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6050c-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="6050c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="6050c-135"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6050c-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="6050c-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6050c-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="6050c-137"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6050c-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="6050c-138">DLL</span><span class="sxs-lookup"><span data-stu-id="6050c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6050c-139"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6050c-139"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="6050c-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6050c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6050c-141">Impression</span><span class="sxs-lookup"><span data-stu-id="6050c-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="6050c-142">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="6050c-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="6050c-143">**EPrintXPSJobOperation**</span><span class="sxs-lookup"><span data-stu-id="6050c-143">**EPrintXPSJobOperation**</span></span>](eprintxpsjoboperation.md)
</dt> <dt>

[<span data-ttu-id="6050c-144">**EPrintXPSJobProgress**</span><span class="sxs-lookup"><span data-stu-id="6050c-144">**EPrintXPSJobProgress**</span></span>](eprintxpsjobprogress.md)
</dt> </dl>

 

