---
description: La fonction SetDefaultPrinter définit le nom de l’imprimante par défaut de l’utilisateur actuel sur l’ordinateur local.
ms.assetid: 55eec548-577f-422b-80e3-8b23aa4d2159
title: SetDefaultPrinter, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetDefaultPrinter
- SetDefaultPrinterA
- SetDefaultPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 346d356aea3d806284823541aa219699e51c2187
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541873"
---
# <a name="setdefaultprinter-function"></a><span data-ttu-id="7a803-103">SetDefaultPrinter fonction)</span><span class="sxs-lookup"><span data-stu-id="7a803-103">SetDefaultPrinter function</span></span>

<span data-ttu-id="7a803-104">La fonction **SetDefaultPrinter** définit le nom de l’imprimante par défaut de l’utilisateur actuel sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="7a803-104">The **SetDefaultPrinter** function sets the printer name of the default printer for the current user on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a803-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a803-105">Syntax</span></span>


```C++
BOOL SetDefaultPrinter(
  _In_ LPCTSTR pszPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="7a803-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7a803-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a803-107">*pszPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7a803-107">*pszPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a803-108">Pointeur vers une chaîne se terminant par null et contenant le nom par défaut de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="7a803-108">A pointer to a null-terminated string containing the default printer name.</span></span> <span data-ttu-id="7a803-109">Pour une connexion d’imprimante distante, le format du nom est **\\\\** _serveur_ *_\\_* _nom_imprimante_.</span><span class="sxs-lookup"><span data-stu-id="7a803-109">For a remote printer connection, the name format is **\\\\**_server_*_\\_*_printername_.</span></span> <span data-ttu-id="7a803-110">Pour une imprimante locale, le format du nom est *nom_imprimante*.</span><span class="sxs-lookup"><span data-stu-id="7a803-110">For a local printer, the name format is *printername*.</span></span>

<span data-ttu-id="7a803-111">Si ce paramètre a la **valeur null** ou est une chaîne vide, autrement dit, «», **SetDefaultPrinter** sélectionne une imprimante par défaut à partir de l’une des imprimantes installées.</span><span class="sxs-lookup"><span data-stu-id="7a803-111">If this parameter is **NULL** or an empty string, that is, "", **SetDefaultPrinter** will select a default printer from one of the installed printers.</span></span> <span data-ttu-id="7a803-112">Si une imprimante par défaut existe déjà, l’appel de **SetDefaultPrinter** avec une chaîne **null** ou vide dans ce paramètre peut modifier l’imprimante par défaut.</span><span class="sxs-lookup"><span data-stu-id="7a803-112">If a default printer already exists, calling **SetDefaultPrinter** with a **NULL** or an empty string in this parameter might change the default printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a803-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7a803-113">Return value</span></span>

<span data-ttu-id="7a803-114">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="7a803-114">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="7a803-115">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="7a803-115">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a803-116">Notes</span><span class="sxs-lookup"><span data-stu-id="7a803-116">Remarks</span></span>

<span data-ttu-id="7a803-117">Lorsque vous utilisez cette méthode, vous devez spécifier une imprimante, un pilote et un port valides.</span><span class="sxs-lookup"><span data-stu-id="7a803-117">When using this method, you must specify a valid printer, driver, and port.</span></span> <span data-ttu-id="7a803-118">Si elles ne sont pas valides, les API n’échouent pas, mais le résultat n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="7a803-118">If they are invalid, the APIs do not fail but the result is not defined.</span></span> <span data-ttu-id="7a803-119">Cela peut permettre à d’autres programmes de remettre l’imprimante à l’imprimante valide précédente.</span><span class="sxs-lookup"><span data-stu-id="7a803-119">This could cause other programs to set the printer back to the previous valid printer.</span></span> <span data-ttu-id="7a803-120">Vous pouvez utiliser [**EnumPrinters**](enumprinters.md) pour récupérer le nom de l’imprimante, le nom du pilote et le nom de port de toutes les imprimantes disponibles.</span><span class="sxs-lookup"><span data-stu-id="7a803-120">You can use [**EnumPrinters**](enumprinters.md) to retrieve the printer name, driver name, and port name of all available printers.</span></span>

> [!Note]  
> <span data-ttu-id="7a803-121">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="7a803-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="7a803-122">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="7a803-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="7a803-123">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="7a803-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7a803-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a803-124">Requirements</span></span>



| <span data-ttu-id="7a803-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a803-125">Requirement</span></span> | <span data-ttu-id="7a803-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a803-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a803-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a803-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7a803-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7a803-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7a803-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a803-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7a803-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7a803-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7a803-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="7a803-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a803-132"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7a803-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="7a803-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7a803-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="7a803-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a803-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="7a803-135">DLL</span><span class="sxs-lookup"><span data-stu-id="7a803-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a803-136"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="7a803-136"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="7a803-137">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="7a803-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7a803-138">**SetDefaultPrinterW** (Unicode) et **SetDefaultPrinterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7a803-138">**SetDefaultPrinterW** (Unicode) and **SetDefaultPrinterA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="7a803-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a803-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a803-140">Impression</span><span class="sxs-lookup"><span data-stu-id="7a803-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="7a803-141">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="7a803-141">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="7a803-142">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="7a803-142">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="7a803-143">**GetDefaultPrinter**</span><span class="sxs-lookup"><span data-stu-id="7a803-143">**GetDefaultPrinter**</span></span>](getdefaultprinter.md)
</dt> </dl>

 

 




