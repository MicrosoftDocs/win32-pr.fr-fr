---
description: La fonction DeleteForm supprime un nom de formulaire de la liste des formulaires pris en charge.
ms.assetid: a2d0345f-2469-46ab-935f-777f2b33b621
title: DeleteForm, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteForm
- DeleteFormA
- DeleteFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 70ead5026c3b5cf21b28d230f79819bf71eeaf10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034500"
---
# <a name="deleteform-function"></a><span data-ttu-id="be04a-103">DeleteForm fonction)</span><span class="sxs-lookup"><span data-stu-id="be04a-103">DeleteForm function</span></span>

<span data-ttu-id="be04a-104">La fonction **DeleteForm** supprime un nom de formulaire de la liste des formulaires pris en charge.</span><span class="sxs-lookup"><span data-stu-id="be04a-104">The **DeleteForm** function removes a form name from the list of supported forms.</span></span>

## <a name="syntax"></a><span data-ttu-id="be04a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be04a-105">Syntax</span></span>


```C++
BOOL DeleteForm(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pFormName
);
```



## <a name="parameters"></a><span data-ttu-id="be04a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be04a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be04a-107">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be04a-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be04a-108">Indique le descripteur d’imprimante ouvert sur lequel cette fonction doit être exécutée.</span><span class="sxs-lookup"><span data-stu-id="be04a-108">Indicates the open printer handle that this function is to be performed upon.</span></span> <span data-ttu-id="be04a-109">Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="be04a-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="be04a-110">*pFormName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be04a-110">*pFormName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be04a-111">Pointeur vers le nom du formulaire à supprimer.</span><span class="sxs-lookup"><span data-stu-id="be04a-111">Pointer to the form name to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be04a-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="be04a-112">Return value</span></span>

<span data-ttu-id="be04a-113">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="be04a-113">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="be04a-114">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="be04a-114">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="be04a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="be04a-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="be04a-116">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="be04a-116">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="be04a-117">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="be04a-117">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="be04a-118">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="be04a-118">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="be04a-119">**DeleteForm** peut uniquement supprimer les noms de formulaire qui ont été ajoutés à l’aide de la fonction [**AddForm**](addform.md) .</span><span class="sxs-lookup"><span data-stu-id="be04a-119">**DeleteForm** can only delete form names that were added by using the [**AddForm**](addform.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="be04a-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be04a-120">Requirements</span></span>



| <span data-ttu-id="be04a-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be04a-121">Requirement</span></span> | <span data-ttu-id="be04a-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="be04a-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be04a-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be04a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="be04a-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be04a-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="be04a-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be04a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="be04a-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be04a-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="be04a-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="be04a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="be04a-128"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be04a-128"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="be04a-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="be04a-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="be04a-130"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be04a-130"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="be04a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="be04a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be04a-132"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="be04a-132"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="be04a-133">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="be04a-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="be04a-134">**DeleteFormW** (Unicode) et **DeleteFormA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="be04a-134">**DeleteFormW** (Unicode) and **DeleteFormA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="be04a-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be04a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be04a-136">Impression</span><span class="sxs-lookup"><span data-stu-id="be04a-136">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="be04a-137">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="be04a-137">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="be04a-138">**AddForm**</span><span class="sxs-lookup"><span data-stu-id="be04a-138">**AddForm**</span></span>](addform.md)
</dt> <dt>

[<span data-ttu-id="be04a-139">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="be04a-139">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




