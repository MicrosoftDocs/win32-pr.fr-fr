---
description: La fonction DeletePrinterKey supprime une clé spécifiée et toutes ses sous-clés pour une imprimante spécifiée.
ms.assetid: 0bd81b43-5c1e-4989-8350-2ec0dc215f28
title: DeletePrinterKey, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterKey
- DeletePrinterKeyA
- DeletePrinterKeyW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 4be073f7832f647e156dbd3b5e12d23ffe6acc06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757749"
---
# <a name="deleteprinterkey-function"></a><span data-ttu-id="2692e-103">DeletePrinterKey fonction)</span><span class="sxs-lookup"><span data-stu-id="2692e-103">DeletePrinterKey function</span></span>

<span data-ttu-id="2692e-104">La fonction **DeletePrinterKey** supprime une clé spécifiée et toutes ses sous-clés pour une imprimante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2692e-104">The **DeletePrinterKey** function deletes a specified key and all its subkeys for a specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="2692e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2692e-105">Syntax</span></span>


```C++
DWORD DeletePrinterKey(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName
);
```



## <a name="parameters"></a><span data-ttu-id="2692e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2692e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2692e-107">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2692e-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2692e-108">Handle vers l’imprimante pour laquelle la fonction supprime une clé.</span><span class="sxs-lookup"><span data-stu-id="2692e-108">A handle to the printer for which the function deletes a key.</span></span> <span data-ttu-id="2692e-109">Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="2692e-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="2692e-110">*pKeyName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2692e-110">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2692e-111">Pointeur vers une chaîne se terminant par un caractère null qui spécifie la clé à supprimer.</span><span class="sxs-lookup"><span data-stu-id="2692e-111">A pointer to a null-terminated string that specifies the key to delete.</span></span> <span data-ttu-id="2692e-112">Utilisez la barre oblique inverse ( \\ ) comme séparateur pour spécifier un chemin d’accès avec une ou plusieurs sous-clés.</span><span class="sxs-lookup"><span data-stu-id="2692e-112">Use the backslash ( \\ ) character as a delimiter to specify a path with one or more subkeys.</span></span>

<span data-ttu-id="2692e-113">Si *pKeyName* est une chaîne vide (""), **DeletePrinterKey** supprime toutes les clés situées sous la clé de niveau supérieur pour l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="2692e-113">If *pKeyName* is an empty string (""), **DeletePrinterKey** deletes all keys below the top-level key for the printer.</span></span> <span data-ttu-id="2692e-114">Si *pKeyName* a la **valeur null**, **DELETEPRINTERKEY** retourne un paramètre d’erreur \_ non valide \_ .</span><span class="sxs-lookup"><span data-stu-id="2692e-114">If *pKeyName* is **NULL**, **DeletePrinterKey** returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2692e-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2692e-115">Return value</span></span>

<span data-ttu-id="2692e-116">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="2692e-116">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="2692e-117">Si la fonction échoue, la valeur de retour est un code d’erreur système.</span><span class="sxs-lookup"><span data-stu-id="2692e-117">If the function fails, the return value is a system error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2692e-118">Notes</span><span class="sxs-lookup"><span data-stu-id="2692e-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2692e-119">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="2692e-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="2692e-120">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="2692e-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="2692e-121">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="2692e-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2692e-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2692e-122">Requirements</span></span>



| <span data-ttu-id="2692e-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2692e-123">Requirement</span></span> | <span data-ttu-id="2692e-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="2692e-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2692e-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2692e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2692e-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2692e-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2692e-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2692e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2692e-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2692e-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2692e-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="2692e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2692e-130"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2692e-130"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="2692e-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2692e-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="2692e-132"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2692e-132"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="2692e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2692e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2692e-134"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="2692e-134"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="2692e-135">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="2692e-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2692e-136">**DeletePrinterKeyW** (Unicode) et **DeletePrinterKeyA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2692e-136">**DeletePrinterKeyW** (Unicode) and **DeletePrinterKeyA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="2692e-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2692e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2692e-138">Impression</span><span class="sxs-lookup"><span data-stu-id="2692e-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="2692e-139">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="2692e-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="2692e-140">**DeletePrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="2692e-140">**DeletePrinterDataEx**</span></span>](deleteprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="2692e-141">**EnumPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="2692e-141">**EnumPrinterDataEx**</span></span>](enumprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="2692e-142">**EnumPrinterKey**</span><span class="sxs-lookup"><span data-stu-id="2692e-142">**EnumPrinterKey**</span></span>](enumprinterkey.md)
</dt> <dt>

[<span data-ttu-id="2692e-143">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="2692e-143">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="2692e-144">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="2692e-144">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="2692e-145">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="2692e-145">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




