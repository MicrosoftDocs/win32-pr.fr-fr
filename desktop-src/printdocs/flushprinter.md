---
description: La fonction FlushPrinter envoie une mémoire tampon à l’imprimante afin de l’effacer d’un état transitoire.
ms.assetid: 08e54175-da68-4ebd-91ec-8f4525f49d30
title: FlushPrinter, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FlushPrinter
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d46a4a8d7143e10fc13722d278ca21a0602b7f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528996"
---
# <a name="flushprinter-function"></a><span data-ttu-id="d4304-103">FlushPrinter fonction)</span><span class="sxs-lookup"><span data-stu-id="d4304-103">FlushPrinter function</span></span>

<span data-ttu-id="d4304-104">La fonction **FlushPrinter** envoie une mémoire tampon à l’imprimante afin de l’effacer d’un état transitoire.</span><span class="sxs-lookup"><span data-stu-id="d4304-104">The **FlushPrinter** function sends a buffer to the printer in order to clear it from a transient state.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4304-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4304-105">Syntax</span></span>


```C++
BOOL FlushPrinter(
  _In_  HANDLE  hPrinter,
  _In_  LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcWritten,
  _In_  DWORD   cSleep
);
```



## <a name="parameters"></a><span data-ttu-id="d4304-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4304-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4304-107">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d4304-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4304-108">Handle de l’objet Printer.</span><span class="sxs-lookup"><span data-stu-id="d4304-108">A handle to the printer object.</span></span> <span data-ttu-id="d4304-109">Il doit s’agir du même handle que celui qui a été utilisé dans un appel antérieur à [**WritePrinter**](writeprinter.md) , par le pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="d4304-109">This should be the same handle that was used, in a prior [**WritePrinter**](writeprinter.md) call, by the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="d4304-110">*pBuf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d4304-110">*pBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4304-111">Pointeur vers un tableau d’octets qui contient les données à écrire sur l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="d4304-111">A pointer to an array of bytes that contains the data to be written to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="d4304-112">*cbBuf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d4304-112">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4304-113">Taille, en octets, du tableau pointé par *pBuf*.</span><span class="sxs-lookup"><span data-stu-id="d4304-113">The size, in bytes, of the array pointed to by *pBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="d4304-114">*pcWritten* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d4304-114">*pcWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4304-115">Pointeur vers une valeur qui reçoit le nombre d’octets de données qui ont été écrits sur l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="d4304-115">A pointer to a value that receives the number of bytes of data that were written to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="d4304-116">*cSleep* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d4304-116">*cSleep* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4304-117">Durée, en millisecondes, pendant laquelle la ligne d’e/s du port de l’imprimante doit rester inactive.</span><span class="sxs-lookup"><span data-stu-id="d4304-117">The time, in milliseconds, for which the I/O line to the printer port should be kept idle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4304-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d4304-118">Return value</span></span>

<span data-ttu-id="d4304-119">Si la fonction réussit, la valeur de retour est différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="d4304-119">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="d4304-120">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="d4304-120">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4304-121">Notes</span><span class="sxs-lookup"><span data-stu-id="d4304-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d4304-122">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="d4304-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="d4304-123">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="d4304-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="d4304-124">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="d4304-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="d4304-125">**FlushPrinter** doit être appelé uniquement si [**WritePrinter**](writeprinter.md) a échoué, laissant l’imprimante dans un état transitoire.</span><span class="sxs-lookup"><span data-stu-id="d4304-125">**FlushPrinter** should be called only if [**WritePrinter**](writeprinter.md) failed, leaving the printer in a transient state.</span></span> <span data-ttu-id="d4304-126">Par exemple, l’imprimante peut passer à l’état transitoire lorsque le travail est abandonné et que le pilote d’imprimante a partiellement envoyé des données brutes à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="d4304-126">For example, the printer could get into a transient state when the job gets aborted and the printer driver has partially sent some raw data to the printer.</span></span>

<span data-ttu-id="d4304-127">**FlushPrinter** peut également spécifier une période d’inactivité pendant laquelle le spouleur d’impression ne planifie aucun travail sur le port d’imprimante correspondant.</span><span class="sxs-lookup"><span data-stu-id="d4304-127">**FlushPrinter** also can specify an idle period during which the print spooler does not schedule any jobs to the corresponding printer port.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4304-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4304-128">Requirements</span></span>



| <span data-ttu-id="d4304-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4304-129">Requirement</span></span> | <span data-ttu-id="d4304-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4304-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4304-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4304-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d4304-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d4304-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d4304-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4304-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d4304-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d4304-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d4304-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4304-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4304-136"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d4304-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d4304-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d4304-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="d4304-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4304-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="d4304-139">DLL</span><span class="sxs-lookup"><span data-stu-id="d4304-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4304-140"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="d4304-140"><dt>Winspool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="d4304-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4304-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4304-142">Impression</span><span class="sxs-lookup"><span data-stu-id="d4304-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d4304-143">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="d4304-143">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="d4304-144">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="d4304-144">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




