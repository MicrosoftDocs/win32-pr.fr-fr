---
description: La fonction PrinterProperties affiche une feuille de propriétés Printer-Properties pour l’imprimante spécifiée.
ms.assetid: 1d4c961b-178b-47af-b983-5b7327919f93
title: PrinterProperties, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrinterProperties
api_type:
- DllExport
api_location:
- plotui.dll
- winspool.drv
ms.openlocfilehash: e7e2c8586c06b2cb64a0e499bd05a6b6016de0a6
ms.sourcegitcommit: c77ed4d933c9f30af0ca0e095a75ad2bdd4d8bf8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/31/2021
ms.locfileid: "106541570"
---
# <a name="printerproperties-function"></a><span data-ttu-id="c2305-103">PrinterProperties fonction)</span><span class="sxs-lookup"><span data-stu-id="c2305-103">PrinterProperties function</span></span>

<span data-ttu-id="c2305-104">La fonction **PrinterProperties** affiche une feuille de propriétés Printer-Properties pour l’imprimante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c2305-104">The **PrinterProperties** function displays a printer-properties property sheet for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2305-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2305-105">Syntax</span></span>


```C++
BOOL PrinterProperties(
  _In_ HWND   hWnd,
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="c2305-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c2305-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2305-107">*HWND* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c2305-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2305-108">Handle de la fenêtre parente de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="c2305-108">A handle to the parent window of the property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="c2305-109">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c2305-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2305-110">Handle d’un objet Printer.</span><span class="sxs-lookup"><span data-stu-id="c2305-110">A handle to a printer object.</span></span> <span data-ttu-id="c2305-111">Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c2305-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2305-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c2305-112">Return value</span></span>

<span data-ttu-id="c2305-113">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="c2305-113">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="c2305-114">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="c2305-114">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2305-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c2305-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c2305-116">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="c2305-116">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="c2305-117">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="c2305-117">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="c2305-118">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="c2305-118">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c2305-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2305-119">Requirements</span></span>



| <span data-ttu-id="c2305-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2305-120">Requirement</span></span> | <span data-ttu-id="c2305-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2305-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2305-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2305-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c2305-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2305-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c2305-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2305-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c2305-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2305-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c2305-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="c2305-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2305-127"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2305-127"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c2305-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c2305-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="c2305-129"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2305-129"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="c2305-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c2305-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2305-131"><dt>winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="c2305-131"><dt>winspool.drv</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c2305-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2305-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2305-133">Impression</span><span class="sxs-lookup"><span data-stu-id="c2305-133">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c2305-134">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="c2305-134">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="c2305-135">**DocumentProperties**</span><span class="sxs-lookup"><span data-stu-id="c2305-135">**DocumentProperties**</span></span>](documentproperties.md)
</dt> <dt>

[<span data-ttu-id="c2305-136">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="c2305-136">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




