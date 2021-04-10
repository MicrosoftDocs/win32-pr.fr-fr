---
description: La fonction EndPagePrinter informe le spouleur d’impression que l’application se trouve à la fin d’une page dans un travail d’impression.
ms.assetid: aceb88b9-375b-4cd2-996a-c369f590154e
title: EndPagePrinter, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndPagePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 45e8ce005953e07f10ec621660ed38e68d50c62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115482"
---
# <a name="endpageprinter-function"></a><span data-ttu-id="bdfac-103">EndPagePrinter fonction)</span><span class="sxs-lookup"><span data-stu-id="bdfac-103">EndPagePrinter function</span></span>

<span data-ttu-id="bdfac-104">La fonction **EndPagePrinter** informe le spouleur d’impression que l’application se trouve à la fin d’une page dans un travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="bdfac-104">The **EndPagePrinter** function notifies the print spooler that the application is at the end of a page in a print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdfac-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bdfac-105">Syntax</span></span>


```C++
BOOL EndPagePrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="bdfac-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bdfac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdfac-107">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bdfac-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdfac-108">Handle vers l’imprimante pour laquelle la page sera concluante.</span><span class="sxs-lookup"><span data-stu-id="bdfac-108">Handle to the printer for which the page will be concluded.</span></span> <span data-ttu-id="bdfac-109">Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="bdfac-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdfac-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bdfac-110">Return value</span></span>

<span data-ttu-id="bdfac-111">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="bdfac-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="bdfac-112">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="bdfac-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdfac-113">Notes</span><span class="sxs-lookup"><span data-stu-id="bdfac-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bdfac-114">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="bdfac-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="bdfac-115">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="bdfac-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="bdfac-116">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="bdfac-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="bdfac-117">La séquence d’un travail d’impression se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="bdfac-117">The sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="bdfac-118">Pour commencer un travail d’impression, appelez [**StartDocPrinter**](startdocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="bdfac-118">To begin a print job, call [**StartDocPrinter**](startdocprinter.md).</span></span>
2.  <span data-ttu-id="bdfac-119">Pour commencer chaque page, appelez [**StartPagePrinter**](startpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="bdfac-119">To begin each page, call [**StartPagePrinter**](startpageprinter.md).</span></span>
3.  <span data-ttu-id="bdfac-120">Pour écrire des données dans une page, appelez [**WritePrinter**](writeprinter.md).</span><span class="sxs-lookup"><span data-stu-id="bdfac-120">To write data to a page, call [**WritePrinter**](writeprinter.md).</span></span>
4.  <span data-ttu-id="bdfac-121">Pour terminer chaque page, appelez **EndPagePrinter**.</span><span class="sxs-lookup"><span data-stu-id="bdfac-121">To end each page, call **EndPagePrinter**.</span></span>
5.  <span data-ttu-id="bdfac-122">Répétez les étapes 2, 3 et 4 pour autant de pages que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="bdfac-122">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="bdfac-123">Pour mettre fin au travail d’impression, appelez [**EndDocPrinter**](enddocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="bdfac-123">To end the print job, call [**EndDocPrinter**](enddocprinter.md).</span></span>

<span data-ttu-id="bdfac-124">Quand une page dans un fichier mis en file d’attente dépasse environ 350 Mo, elle peut échouer et ne pas envoyer de message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="bdfac-124">When a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message.</span></span> <span data-ttu-id="bdfac-125">Par exemple, cela peut se produire lors de l’impression de fichiers EMF volumineux.</span><span class="sxs-lookup"><span data-stu-id="bdfac-125">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="bdfac-126">La limite de taille de page dépend de nombreux facteurs, notamment de la quantité de mémoire virtuelle disponible, de la quantité de mémoire allouée par les processus d’appel et de la quantité de fragmentation dans le segment de mémoire de processus.</span><span class="sxs-lookup"><span data-stu-id="bdfac-126">The page size limit depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdfac-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bdfac-127">Requirements</span></span>



| <span data-ttu-id="bdfac-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bdfac-128">Requirement</span></span> | <span data-ttu-id="bdfac-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="bdfac-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdfac-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bdfac-130">Minimum supported client</span></span><br/> | <span data-ttu-id="bdfac-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bdfac-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bdfac-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bdfac-132">Minimum supported server</span></span><br/> | <span data-ttu-id="bdfac-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bdfac-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bdfac-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="bdfac-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdfac-135"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bdfac-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="bdfac-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bdfac-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="bdfac-137"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bdfac-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="bdfac-138">DLL</span><span class="sxs-lookup"><span data-stu-id="bdfac-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bdfac-139"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdfac-139"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="bdfac-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bdfac-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdfac-141">Impression</span><span class="sxs-lookup"><span data-stu-id="bdfac-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="bdfac-142">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="bdfac-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="bdfac-143">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="bdfac-143">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="bdfac-144">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="bdfac-144">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="bdfac-145">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="bdfac-145">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="bdfac-146">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="bdfac-146">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="bdfac-147">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="bdfac-147">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="bdfac-148">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="bdfac-148">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




