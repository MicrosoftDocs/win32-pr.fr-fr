---
description: La fonction ScheduleJob demande que le spouleur d’impression planifie l’impression d’un travail d’impression spécifié.
ms.assetid: a103a29c-be4d-491e-9b04-84571fe969a5
title: ScheduleJob, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ScheduleJob
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 1ef938cc2a9b1893a4825255325457d5c210842a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528233"
---
# <a name="schedulejob-function"></a><span data-ttu-id="ea465-103">ScheduleJob fonction)</span><span class="sxs-lookup"><span data-stu-id="ea465-103">ScheduleJob function</span></span>

<span data-ttu-id="ea465-104">La fonction **ScheduleJob** demande que le spouleur d’impression planifie l’impression d’un travail d’impression spécifié.</span><span class="sxs-lookup"><span data-stu-id="ea465-104">The **ScheduleJob** function requests that the print spooler schedule a specified print job for printing.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea465-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea465-105">Syntax</span></span>


```C++
BOOL ScheduleJob(
  _In_ HANDLE hPrinter,
  _In_ DWORD  dwJobID
);
```



## <a name="parameters"></a><span data-ttu-id="ea465-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea465-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea465-107">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ea465-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea465-108">Handle vers l’imprimante pour le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="ea465-108">A handle to the printer for the print job.</span></span> <span data-ttu-id="ea465-109">Il doit s’agir d’une imprimante locale configurée comme imprimante spoulée.</span><span class="sxs-lookup"><span data-stu-id="ea465-109">This must be a local printer that is configured as a spooled printer.</span></span> <span data-ttu-id="ea465-110">Si *hPrinter* est un handle vers une connexion d’imprimante distante, ou si l’imprimante est configurée pour l’impression directe, la fonction **ScheduleJob** échoue.</span><span class="sxs-lookup"><span data-stu-id="ea465-110">If *hPrinter* is a handle to a remote printer connection, or if the printer is configured for direct printing, the **ScheduleJob** function fails.</span></span> <span data-ttu-id="ea465-111">Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ea465-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

<span data-ttu-id="ea465-112">*hPrinter* doit être le même handle d’imprimante que celui spécifié dans l’appel à [**AddJob**](addjob.md) qui a obtenu l’identificateur de travail d’impression *dwJobID* .</span><span class="sxs-lookup"><span data-stu-id="ea465-112">*hPrinter* must be the same printer handle specified in the call to [**AddJob**](addjob.md) that obtained the *dwJobID* print job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="ea465-113">*dwJobID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ea465-113">*dwJobID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea465-114">Travail d’impression à planifier.</span><span class="sxs-lookup"><span data-stu-id="ea465-114">The print job to be scheduled.</span></span> <span data-ttu-id="ea465-115">Vous obtenez cet identificateur de travail d’impression en appelant la fonction [**AddJob**](addjob.md) .</span><span class="sxs-lookup"><span data-stu-id="ea465-115">You obtain this print job identifier by calling the [**AddJob**](addjob.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea465-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ea465-116">Return value</span></span>

<span data-ttu-id="ea465-117">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="ea465-117">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="ea465-118">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="ea465-118">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea465-119">Notes</span><span class="sxs-lookup"><span data-stu-id="ea465-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ea465-120">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="ea465-120">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="ea465-121">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="ea465-121">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="ea465-122">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="ea465-122">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="ea465-123">Vous devez appeler la fonction [**AddJob**](addjob.md) avant d’appeler la fonction **ScheduleJob** .</span><span class="sxs-lookup"><span data-stu-id="ea465-123">You must successfully call the [**AddJob**](addjob.md) function before calling the **ScheduleJob** function.</span></span> <span data-ttu-id="ea465-124">**AddJob** obtient l’identificateur du travail d’impression que vous transmettez à **ScheduleJob** en tant que *dwJobID*.</span><span class="sxs-lookup"><span data-stu-id="ea465-124">**AddJob** obtains the print job identifier that you pass to **ScheduleJob** as *dwJobID*.</span></span> <span data-ttu-id="ea465-125">Les deux appels doivent utiliser la même valeur pour *hPrinter*.</span><span class="sxs-lookup"><span data-stu-id="ea465-125">Both calls must use the same value for *hPrinter*.</span></span>

<span data-ttu-id="ea465-126">La fonction **ScheduleJob** vérifie si un fichier spouleur est valide.</span><span class="sxs-lookup"><span data-stu-id="ea465-126">The **ScheduleJob** function checks for a valid spool file.</span></span> <span data-ttu-id="ea465-127">Si un fichier de mise en file d’attente n’est pas valide ou s’il est vide, **ScheduleJob** supprime à la fois le fichier spouleur et l’entrée correspondante dans le spouleur d’impression.</span><span class="sxs-lookup"><span data-stu-id="ea465-127">If there is an invalid spool file, or if it is empty, **ScheduleJob** deletes both the spool file and the corresponding print job entry in the print spooler.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea465-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea465-128">Requirements</span></span>



| <span data-ttu-id="ea465-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea465-129">Requirement</span></span> | <span data-ttu-id="ea465-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea465-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea465-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea465-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ea465-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea465-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ea465-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea465-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ea465-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea465-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ea465-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea465-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea465-136"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea465-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ea465-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ea465-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="ea465-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea465-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="ea465-139">DLL</span><span class="sxs-lookup"><span data-stu-id="ea465-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea465-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea465-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="ea465-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea465-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea465-142">Impression</span><span class="sxs-lookup"><span data-stu-id="ea465-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ea465-143">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="ea465-143">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="ea465-144">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="ea465-144">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="ea465-145">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="ea465-145">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




