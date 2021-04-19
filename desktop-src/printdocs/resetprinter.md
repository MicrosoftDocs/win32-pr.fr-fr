---
description: La fonction ResetPrinter spécifie les valeurs du type de données et du mode de l’appareil à utiliser pour l’impression des documents soumis par la fonction StartDocPrinter. Ces valeurs peuvent être remplacées à l’aide de la fonction SetJob après le début de l’impression du document.
ms.assetid: 9efc6629-dbb7-4320-90b9-07c66f0add47
title: ResetPrinter, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResetPrinter
- ResetPrinterA
- ResetPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 8bdfef0229a646e802878a96370d27d49a6bfc2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527910"
---
# <a name="resetprinter-function"></a><span data-ttu-id="2e4b8-104">ResetPrinter fonction)</span><span class="sxs-lookup"><span data-stu-id="2e4b8-104">ResetPrinter function</span></span>

<span data-ttu-id="2e4b8-105">La fonction **ResetPrinter** spécifie les valeurs du type de données et du mode de l’appareil à utiliser pour l’impression des documents soumis par la fonction [**StartDocPrinter**](startdocprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="2e4b8-105">The **ResetPrinter** function specifies the data type and device mode values to be used for printing documents submitted by the [**StartDocPrinter**](startdocprinter.md) function.</span></span> <span data-ttu-id="2e4b8-106">Ces valeurs peuvent être remplacées à l’aide de la fonction [**SetJob**](setjob.md) après le début de l’impression du document.</span><span class="sxs-lookup"><span data-stu-id="2e4b8-106">These values can be overridden by using the [**SetJob**](setjob.md) function after document printing has started.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e4b8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e4b8-107">Syntax</span></span>


```C++
BOOL ResetPrinter(
  _In_ HANDLE             hPrinter,
  _In_ LPPRINTER_DEFAULTS pDefault
);
```



## <a name="parameters"></a><span data-ttu-id="2e4b8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2e4b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e4b8-109">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2e4b8-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e4b8-110">Handle vers l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="2e4b8-110">Handle to the printer.</span></span> <span data-ttu-id="2e4b8-111">Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="2e4b8-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="2e4b8-112">*pDefault* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2e4b8-112">*pDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e4b8-113">Pointeur vers une structure d' [**imprimante \_ par défaut**](printer-defaults.md) .</span><span class="sxs-lookup"><span data-stu-id="2e4b8-113">Pointer to a [**PRINTER\_DEFAULTS**](printer-defaults.md) structure.</span></span>

<span data-ttu-id="2e4b8-114">La fonction **ResetPrinter** ignore le membre **desiredAccess** de la [**structure \_ par défaut**](printer-defaults.md) de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="2e4b8-114">The **ResetPrinter** function ignores the **DesiredAccess** member of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure.</span></span> <span data-ttu-id="2e4b8-115">Définissez ce membre sur zéro.</span><span class="sxs-lookup"><span data-stu-id="2e4b8-115">Set that member to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e4b8-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2e4b8-116">Return value</span></span>

<span data-ttu-id="2e4b8-117">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="2e4b8-117">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="2e4b8-118">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="2e4b8-118">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e4b8-119">Notes</span><span class="sxs-lookup"><span data-stu-id="2e4b8-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2e4b8-120">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="2e4b8-120">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="2e4b8-121">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="2e4b8-121">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="2e4b8-122">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="2e4b8-122">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2e4b8-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e4b8-123">Requirements</span></span>



| <span data-ttu-id="2e4b8-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e4b8-124">Requirement</span></span> | <span data-ttu-id="2e4b8-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e4b8-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e4b8-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e4b8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2e4b8-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2e4b8-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2e4b8-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e4b8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2e4b8-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2e4b8-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2e4b8-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="2e4b8-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e4b8-131"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2e4b8-131"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="2e4b8-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2e4b8-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="2e4b8-133"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e4b8-133"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="2e4b8-134">DLL</span><span class="sxs-lookup"><span data-stu-id="2e4b8-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e4b8-135"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="2e4b8-135"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="2e4b8-136">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="2e4b8-136">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2e4b8-137">**ResetPrinterW** (Unicode) et **ResetPrinterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2e4b8-137">**ResetPrinterW** (Unicode) and **ResetPrinterA** (ANSI)</span></span><br/>                                       |



## <a name="see-also"></a><span data-ttu-id="2e4b8-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e4b8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e4b8-139">Impression</span><span class="sxs-lookup"><span data-stu-id="2e4b8-139">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="2e4b8-140">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="2e4b8-140">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="2e4b8-141">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="2e4b8-141">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="2e4b8-142">**\_valeurs par défaut de l’imprimante**</span><span class="sxs-lookup"><span data-stu-id="2e4b8-142">**PRINTER\_DEFAULTS**</span></span>](printer-defaults.md)
</dt> <dt>

[<span data-ttu-id="2e4b8-143">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="2e4b8-143">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="2e4b8-144">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="2e4b8-144">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

 




