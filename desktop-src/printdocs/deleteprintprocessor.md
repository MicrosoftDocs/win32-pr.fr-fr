---
description: La fonction DeletePrintProcessor supprime un processeur d’impression ajouté par la fonction AddPrintProcessor.
ms.assetid: 65c77874-aa2c-4b4c-b218-fad361270a3e
title: DeletePrintProcessor, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrintProcessor
- DeletePrintProcessorA
- DeletePrintProcessorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 241efaad91e1587209f2ef2a905bc0e095c6b40c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202699"
---
# <a name="deleteprintprocessor-function"></a><span data-ttu-id="e1c02-103">DeletePrintProcessor fonction)</span><span class="sxs-lookup"><span data-stu-id="e1c02-103">DeletePrintProcessor function</span></span>

<span data-ttu-id="e1c02-104">La fonction **DeletePrintProcessor** supprime un processeur d’impression ajouté par la fonction [**AddPrintProcessor**](addprintprocessor.md) .</span><span class="sxs-lookup"><span data-stu-id="e1c02-104">The **DeletePrintProcessor** function removes a print processor added by the [**AddPrintProcessor**](addprintprocessor.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1c02-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1c02-105">Syntax</span></span>


```C++
BOOL DeletePrintProcessor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPrintProcessorName
);
```



## <a name="parameters"></a><span data-ttu-id="e1c02-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1c02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1c02-107">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e1c02-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1c02-108">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur à partir duquel le processeur doit être supprimé.</span><span class="sxs-lookup"><span data-stu-id="e1c02-108">A pointer to a null-terminated string that specifies the name of the server from which the processor is to be removed.</span></span> <span data-ttu-id="e1c02-109">Si ce paramètre a la **valeur null**, le processeur de l’imprimante est supprimé localement.</span><span class="sxs-lookup"><span data-stu-id="e1c02-109">If this parameter is **NULL**, the printer processor is removed locally.</span></span>

</dd> <dt>

<span data-ttu-id="e1c02-110">*pEnvironment* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e1c02-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1c02-111">Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement à partir duquel le processeur doit être supprimé (par exemple, Windows NT x86, Windows IA64 ou Windows x64).</span><span class="sxs-lookup"><span data-stu-id="e1c02-111">A pointer to a null-terminated string that specifies the environment from which the processor is to be removed (for example, Windows NT x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="e1c02-112">Si ce paramètre a la **valeur null**, le processeur est supprimé de l’environnement actuel de l’application appelante et de l’ordinateur client (pas du serveur d’impression et de l’application de destination).</span><span class="sxs-lookup"><span data-stu-id="e1c02-112">If this parameter is **NULL**, the processor is removed from the current environment of the calling application and client machine (not of the destination application and print server).</span></span> <span data-ttu-id="e1c02-113">La valeur **null** est recommandée, car elle offre une portabilité maximale.</span><span class="sxs-lookup"><span data-stu-id="e1c02-113">**NULL** is the recommended value, as it provides maximum portability.</span></span>

</dd> <dt>

<span data-ttu-id="e1c02-114">*pPrintProcessorName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e1c02-114">*pPrintProcessorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1c02-115">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du processeur à supprimer.</span><span class="sxs-lookup"><span data-stu-id="e1c02-115">A pointer to a null-terminated string that specifies the name of the processor to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1c02-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e1c02-116">Return value</span></span>

<span data-ttu-id="e1c02-117">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="e1c02-117">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="e1c02-118">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="e1c02-118">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1c02-119">Notes</span><span class="sxs-lookup"><span data-stu-id="e1c02-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e1c02-120">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="e1c02-120">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e1c02-121">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="e1c02-121">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e1c02-122">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="e1c02-122">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="e1c02-123">L’appelant doit avoir le [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="e1c02-123">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1c02-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1c02-124">Requirements</span></span>



| <span data-ttu-id="e1c02-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1c02-125">Requirement</span></span> | <span data-ttu-id="e1c02-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1c02-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1c02-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1c02-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e1c02-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1c02-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e1c02-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1c02-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e1c02-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1c02-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e1c02-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="e1c02-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1c02-132"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e1c02-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e1c02-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e1c02-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="e1c02-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1c02-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e1c02-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e1c02-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1c02-136"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="e1c02-136"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="e1c02-137">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="e1c02-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e1c02-138">**DeletePrintProcessorW** (Unicode) et **DeletePrintProcessorA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e1c02-138">**DeletePrintProcessorW** (Unicode) and **DeletePrintProcessorA** (ANSI)</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="e1c02-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1c02-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1c02-140">Impression</span><span class="sxs-lookup"><span data-stu-id="e1c02-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e1c02-141">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="e1c02-141">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e1c02-142">**AddPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="e1c02-142">**AddPrintProcessor**</span></span>](addprintprocessor.md)
</dt> </dl>

 

