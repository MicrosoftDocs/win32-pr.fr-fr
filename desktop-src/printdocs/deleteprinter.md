---
description: La fonction DeletePrinter supprime l’objet Printer spécifié.
ms.assetid: 04d9c073-b795-4307-ba89-d4984bc5b354
title: DeletePrinter, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 16d82a263b09c87f5c9b9725db48dd6634404ad3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517058"
---
# <a name="deleteprinter-function"></a><span data-ttu-id="074ce-103">DeletePrinter fonction)</span><span class="sxs-lookup"><span data-stu-id="074ce-103">DeletePrinter function</span></span>

<span data-ttu-id="074ce-104">La fonction **DeletePrinter** supprime l’objet Printer spécifié.</span><span class="sxs-lookup"><span data-stu-id="074ce-104">The **DeletePrinter** function deletes the specified printer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="074ce-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="074ce-105">Syntax</span></span>


```C++
BOOL DeletePrinter(
  _Inout_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="074ce-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="074ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="074ce-107">*hPrinter* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="074ce-107">*hPrinter* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="074ce-108">Handle vers un objet Printer qui sera supprimé.</span><span class="sxs-lookup"><span data-stu-id="074ce-108">Handle to a printer object that will be deleted.</span></span> <span data-ttu-id="074ce-109">Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="074ce-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="074ce-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="074ce-110">Return value</span></span>

<span data-ttu-id="074ce-111">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="074ce-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="074ce-112">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="074ce-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="074ce-113">Notes</span><span class="sxs-lookup"><span data-stu-id="074ce-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="074ce-114">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="074ce-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="074ce-115">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="074ce-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="074ce-116">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="074ce-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="074ce-117">S’il reste des travaux d’impression à traiter pour l’imprimante spécifiée, **DeletePrinter** marque l’imprimante comme étant en attente de suppression, puis la supprime une fois que tous les travaux d’impression ont été imprimés.</span><span class="sxs-lookup"><span data-stu-id="074ce-117">If there are print jobs remaining to be processed for the specified printer, **DeletePrinter** marks the printer for pending deletion, and then deletes it when all the print jobs have been printed.</span></span> <span data-ttu-id="074ce-118">Aucun travail d’impression ne peut être ajouté à une imprimante marquée pour une suppression en attente.</span><span class="sxs-lookup"><span data-stu-id="074ce-118">No print jobs can be added to a printer that is marked for pending deletion.</span></span>

<span data-ttu-id="074ce-119">Une imprimante marquée pour une suppression en attente ne peut pas être maintenue, mais ses travaux d’impression peuvent être conservés, repris et redémarrés.</span><span class="sxs-lookup"><span data-stu-id="074ce-119">A printer marked for pending deletion cannot be held, but its print jobs can be held, resumed, and restarted.</span></span> <span data-ttu-id="074ce-120">Si l’imprimante est maintenue et qu’il y a des travaux pour l’imprimante, **DeletePrinter** échoue avec l’erreur \_ accès \_ refusé.</span><span class="sxs-lookup"><span data-stu-id="074ce-120">If the printer is held and there are jobs for the printer, **DeletePrinter** fails with ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="074ce-121">Notez que **DeletePrinter** ne ferme pas le handle qui lui est passé.</span><span class="sxs-lookup"><span data-stu-id="074ce-121">Note that **DeletePrinter** does not close the handle that is passed to it.</span></span> <span data-ttu-id="074ce-122">Ainsi, l’application doit toujours appeler [**ClosePrinter**](closeprinter.md).</span><span class="sxs-lookup"><span data-stu-id="074ce-122">Thus, the application must still call [**ClosePrinter**](closeprinter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="074ce-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="074ce-123">Requirements</span></span>



| <span data-ttu-id="074ce-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="074ce-124">Requirement</span></span> | <span data-ttu-id="074ce-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="074ce-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="074ce-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="074ce-126">Minimum supported client</span></span><br/> | <span data-ttu-id="074ce-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="074ce-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="074ce-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="074ce-128">Minimum supported server</span></span><br/> | <span data-ttu-id="074ce-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="074ce-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="074ce-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="074ce-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="074ce-131"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="074ce-131"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="074ce-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="074ce-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="074ce-133"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="074ce-133"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="074ce-134">DLL</span><span class="sxs-lookup"><span data-stu-id="074ce-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="074ce-135"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="074ce-135"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="074ce-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="074ce-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="074ce-137">Impression</span><span class="sxs-lookup"><span data-stu-id="074ce-137">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="074ce-138">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="074ce-138">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="074ce-139">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="074ce-139">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="074ce-140">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="074ce-140">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="074ce-141">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="074ce-141">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




