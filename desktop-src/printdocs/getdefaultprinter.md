---
description: La fonction GetDefaultPrinter récupère le nom de l’imprimante par défaut de l’utilisateur actuel sur l’ordinateur local.
ms.assetid: 8ec06743-43ce-4fac-83c4-f09eac7ee333
title: GetDefaultPrinter, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDefaultPrinter
- GetDefaultPrinterA
- GetDefaultPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 8db5b2aef859ea5d8247fc203611af74c8daddd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517839"
---
# <a name="getdefaultprinter-function"></a><span data-ttu-id="7a550-103">GetDefaultPrinter fonction)</span><span class="sxs-lookup"><span data-stu-id="7a550-103">GetDefaultPrinter function</span></span>

<span data-ttu-id="7a550-104">La fonction **GetDefaultPrinter** récupère le nom de l’imprimante par défaut de l’utilisateur actuel sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="7a550-104">The **GetDefaultPrinter** function retrieves the printer name of the default printer for the current user on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a550-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a550-105">Syntax</span></span>


```C++
BOOL GetDefaultPrinter(
  _In_    LPTSTR  pszBuffer,
  _Inout_ LPDWORD pcchBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="7a550-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7a550-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a550-107">*pszBuffer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7a550-107">*pszBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a550-108">Pointeur vers une mémoire tampon qui reçoit une chaîne de caractères se terminant par null et contenant le nom par défaut de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="7a550-108">A pointer to a buffer that receives a null-terminated character string containing the default printer name.</span></span> <span data-ttu-id="7a550-109">Si ce paramètre a la **valeur null**, la fonction échoue et la variable vers laquelle pointe *pcchBuffer* retourne la taille de mémoire tampon requise, en caractères.</span><span class="sxs-lookup"><span data-stu-id="7a550-109">If this parameter is **NULL**, the function fails and the variable pointed to by *pcchBuffer* returns the required buffer size, in characters.</span></span>

</dd> <dt>

<span data-ttu-id="7a550-110">*pcchBuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7a550-110">*pcchBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a550-111">En entrée, spécifie la taille, en caractères, de la mémoire tampon *pszBuffer* .</span><span class="sxs-lookup"><span data-stu-id="7a550-111">On input, specifies the size, in characters, of the *pszBuffer* buffer.</span></span> <span data-ttu-id="7a550-112">Lors de la sortie, reçoit la taille, en caractères, de la chaîne du nom de l’imprimante, y compris le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="7a550-112">On output, receives the size, in characters, of the printer name string, including the terminating null character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a550-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7a550-113">Return value</span></span>

<span data-ttu-id="7a550-114">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro et la variable vers laquelle pointe *pcchBuffer* contient le nombre de caractères copiés dans la mémoire tampon *pszBuffer* , y compris le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="7a550-114">If the function succeeds, the return value is a nonzero value and the variable pointed to by *pcchBuffer* contains the number of characters copied to the *pszBuffer* buffer, including the terminating null character.</span></span>

<span data-ttu-id="7a550-115">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="7a550-115">If the function fails, the return value is zero.</span></span>



| <span data-ttu-id="7a550-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a550-116">Value</span></span>                       | <span data-ttu-id="7a550-117">Signification</span><span class="sxs-lookup"><span data-stu-id="7a550-117">Meaning</span></span>                                                                                                                        |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a550-118">ERREUR \_ de \_ mémoire tampon insuffisante</span><span class="sxs-lookup"><span data-stu-id="7a550-118">ERROR\_INSUFFICIENT\_BUFFER</span></span> | <span data-ttu-id="7a550-119">La mémoire tampon *pszBuffer* est trop petite.</span><span class="sxs-lookup"><span data-stu-id="7a550-119">The *pszBuffer* buffer is too small.</span></span> <span data-ttu-id="7a550-120">La variable vers laquelle pointe *pcchBuffer* contient la taille de mémoire tampon requise, en caractères.</span><span class="sxs-lookup"><span data-stu-id="7a550-120">The variable pointed to by *pcchBuffer* contains the required buffer size, in characters.</span></span> |
| <span data-ttu-id="7a550-121">\_fichier d' \_ erreur \_ introuvable</span><span class="sxs-lookup"><span data-stu-id="7a550-121">ERROR\_FILE\_NOT\_FOUND</span></span>     | <span data-ttu-id="7a550-122">Il n’y a pas d’imprimante par défaut.</span><span class="sxs-lookup"><span data-stu-id="7a550-122">There is no default printer.</span></span>                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="7a550-123">Notes</span><span class="sxs-lookup"><span data-stu-id="7a550-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7a550-124">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="7a550-124">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="7a550-125">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="7a550-125">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="7a550-126">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="7a550-126">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7a550-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a550-127">Requirements</span></span>



| <span data-ttu-id="7a550-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a550-128">Requirement</span></span> | <span data-ttu-id="7a550-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a550-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a550-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a550-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7a550-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7a550-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7a550-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a550-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7a550-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7a550-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7a550-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="7a550-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a550-135"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7a550-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="7a550-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7a550-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="7a550-137"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a550-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="7a550-138">DLL</span><span class="sxs-lookup"><span data-stu-id="7a550-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a550-139"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="7a550-139"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="7a550-140">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="7a550-140">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7a550-141">**GetDefaultPrinterW** (Unicode) et **GetDefaultPrinterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7a550-141">**GetDefaultPrinterW** (Unicode) and **GetDefaultPrinterA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="7a550-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a550-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a550-143">Impression</span><span class="sxs-lookup"><span data-stu-id="7a550-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="7a550-144">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="7a550-144">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="7a550-145">**SetDefaultPrinter**</span><span class="sxs-lookup"><span data-stu-id="7a550-145">**SetDefaultPrinter**</span></span>](setdefaultprinter.md)
</dt> </dl>

 

 




