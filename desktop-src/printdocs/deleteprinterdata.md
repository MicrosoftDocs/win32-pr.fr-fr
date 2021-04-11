---
description: La fonction DeletePrinterData supprime les données de configuration spécifiées pour une imprimante. Les données de configuration des imprimantes consistent en un ensemble de valeurs nommées et typées. La fonction DeletePrinterData supprime l’une de ces valeurs, spécifiée par son nom de valeur.
ms.assetid: 03c0bd75-d6de-46e3-b8e9-5a55df5135ea
title: DeletePrinterData, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterData
- DeletePrinterDataA
- DeletePrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: a88df8484d367ae2cc50f4a465b5db1dcd53c355
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319101"
---
# <a name="deleteprinterdata-function"></a><span data-ttu-id="fd92b-105">DeletePrinterData fonction)</span><span class="sxs-lookup"><span data-stu-id="fd92b-105">DeletePrinterData function</span></span>

<span data-ttu-id="fd92b-106">La fonction **DeletePrinterData** supprime les données de configuration spécifiées pour une imprimante.</span><span class="sxs-lookup"><span data-stu-id="fd92b-106">The **DeletePrinterData** function deletes specified configuration data for a printer.</span></span> <span data-ttu-id="fd92b-107">Les données de configuration d’une imprimante consistent en un ensemble de valeurs nommées et typées.</span><span class="sxs-lookup"><span data-stu-id="fd92b-107">A printer's configuration data consists of a set of named and typed values.</span></span> <span data-ttu-id="fd92b-108">La fonction **DeletePrinterData** supprime l’une de ces valeurs, spécifiée par son nom de valeur.</span><span class="sxs-lookup"><span data-stu-id="fd92b-108">The **DeletePrinterData** function deletes one of these values, specified by its value name.</span></span>

<span data-ttu-id="fd92b-109">L’appel de **DeletePrinterData** équivaut à appeler la fonction [**DeletePrinterDataEx**](deleteprinterdataex.md) avec le paramètre *pKeyName* défini sur « PrinterDriverData ».</span><span class="sxs-lookup"><span data-stu-id="fd92b-109">Calling **DeletePrinterData** is equivalent to calling the [**DeletePrinterDataEx**](deleteprinterdataex.md) function with the *pKeyName* parameter set to "PrinterDriverData".</span></span>

## <a name="syntax"></a><span data-ttu-id="fd92b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd92b-110">Syntax</span></span>


```C++
DWORD DeletePrinterData(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pValueName
);
```



## <a name="parameters"></a><span data-ttu-id="fd92b-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd92b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd92b-112">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd92b-112">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd92b-113">Handle vers l’imprimante dont les données de configuration doivent être supprimées.</span><span class="sxs-lookup"><span data-stu-id="fd92b-113">A handle to the printer whose configuration data is to be deleted.</span></span> <span data-ttu-id="fd92b-114">Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="fd92b-114">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="fd92b-115">*pValueName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd92b-115">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd92b-116">Pointeur vers le nom se terminant par null de la valeur de données de configuration à supprimer.</span><span class="sxs-lookup"><span data-stu-id="fd92b-116">A pointer to the null-terminated name of the configuration data value to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd92b-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fd92b-117">Return value</span></span>

<span data-ttu-id="fd92b-118">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="fd92b-118">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="fd92b-119">Si la fonction échoue, la valeur de retour est un code d’erreur système.</span><span class="sxs-lookup"><span data-stu-id="fd92b-119">If the function fails, the return value is a system error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd92b-120">Notes</span><span class="sxs-lookup"><span data-stu-id="fd92b-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fd92b-121">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="fd92b-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="fd92b-122">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="fd92b-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="fd92b-123">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="fd92b-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fd92b-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd92b-124">Requirements</span></span>



| <span data-ttu-id="fd92b-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd92b-125">Requirement</span></span> | <span data-ttu-id="fd92b-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd92b-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd92b-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd92b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fd92b-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd92b-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fd92b-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd92b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fd92b-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd92b-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fd92b-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd92b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd92b-132"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fd92b-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="fd92b-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fd92b-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="fd92b-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd92b-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="fd92b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="fd92b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd92b-136"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="fd92b-136"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="fd92b-137">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="fd92b-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fd92b-138">**DeletePrinterDataW** (Unicode) et **DeletePrinterDataA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fd92b-138">**DeletePrinterDataW** (Unicode) and **DeletePrinterDataA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="fd92b-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd92b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd92b-140">Impression</span><span class="sxs-lookup"><span data-stu-id="fd92b-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="fd92b-141">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="fd92b-141">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="fd92b-142">**EnumPrinterData**</span><span class="sxs-lookup"><span data-stu-id="fd92b-142">**EnumPrinterData**</span></span>](enumprinterdata.md)
</dt> <dt>

[<span data-ttu-id="fd92b-143">**GetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="fd92b-143">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> <dt>

[<span data-ttu-id="fd92b-144">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="fd92b-144">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="fd92b-145">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="fd92b-145">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="fd92b-146">**SetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="fd92b-146">**SetPrinterData**</span></span>](setprinterdata.md)
</dt> </dl>

 

 




