---
description: La fonction ClosePrinter ferme l’objet Printer spécifié.
ms.assetid: 95cc3eca-e65c-4fa6-8975-479e8e728dca
title: ClosePrinter, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ClosePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: bd21268b86a07357065d4f33b60d1af4b05fa019
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210357"
---
# <a name="closeprinter-function"></a><span data-ttu-id="246c6-103">ClosePrinter fonction)</span><span class="sxs-lookup"><span data-stu-id="246c6-103">ClosePrinter function</span></span>

<span data-ttu-id="246c6-104">La fonction **ClosePrinter** ferme l’objet Printer spécifié.</span><span class="sxs-lookup"><span data-stu-id="246c6-104">The **ClosePrinter** function closes the specified printer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="246c6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="246c6-105">Syntax</span></span>


```C++
BOOL ClosePrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="246c6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="246c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="246c6-107">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="246c6-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="246c6-108">Handle de l’objet Printer à fermer.</span><span class="sxs-lookup"><span data-stu-id="246c6-108">A handle to the printer object to be closed.</span></span> <span data-ttu-id="246c6-109">Ce descripteur est retourné par la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="246c6-109">This handle is returned by the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="246c6-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="246c6-110">Return value</span></span>

<span data-ttu-id="246c6-111">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="246c6-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="246c6-112">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="246c6-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="246c6-113">Notes</span><span class="sxs-lookup"><span data-stu-id="246c6-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="246c6-114">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="246c6-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="246c6-115">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="246c6-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="246c6-116">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="246c6-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="246c6-117">Lorsque la fonction **ClosePrinter** retourne, le descripteur *hPrinter* n’est pas valide, que la fonction ait réussi ou échoué.</span><span class="sxs-lookup"><span data-stu-id="246c6-117">When the **ClosePrinter** function returns, the handle *hPrinter* is invalid, regardless of whether the function has succeeded or failed.</span></span>

## <a name="examples"></a><span data-ttu-id="246c6-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="246c6-118">Examples</span></span>

<span data-ttu-id="246c6-119">Pour obtenir un exemple de programme qui utilise cette fonction, consultez [Comment : imprimer à l’aide de l’API d’impression GDI](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="246c6-119">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="246c6-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="246c6-120">Requirements</span></span>



| <span data-ttu-id="246c6-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="246c6-121">Requirement</span></span> | <span data-ttu-id="246c6-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="246c6-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="246c6-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="246c6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="246c6-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="246c6-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="246c6-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="246c6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="246c6-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="246c6-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="246c6-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="246c6-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="246c6-128"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="246c6-128"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="246c6-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="246c6-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="246c6-130"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="246c6-130"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="246c6-131">DLL</span><span class="sxs-lookup"><span data-stu-id="246c6-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="246c6-132"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="246c6-132"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="246c6-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="246c6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="246c6-134">Impression</span><span class="sxs-lookup"><span data-stu-id="246c6-134">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="246c6-135">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="246c6-135">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="246c6-136">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="246c6-136">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="246c6-137">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="246c6-137">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




