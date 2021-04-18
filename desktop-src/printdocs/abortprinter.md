---
description: La fonction AbortPrinter supprime un fichier de mise en file d’attente d’imprimantes si l’imprimante est configurée pour la mise en file d’attente.
ms.assetid: b361fba5-e4e7-4c9e-ab32-b8ab88dcb1dc
title: AbortPrinter, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AbortPrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: f28e0c921db8fd075b6cad0e1df07401faaaffb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536364"
---
# <a name="abortprinter-function"></a><span data-ttu-id="63f0a-103">AbortPrinter fonction)</span><span class="sxs-lookup"><span data-stu-id="63f0a-103">AbortPrinter function</span></span>

<span data-ttu-id="63f0a-104">La fonction **AbortPrinter** supprime le fichier de mise en file d’attente de l’imprimante si celle-ci est configurée pour la mise en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="63f0a-104">The **AbortPrinter** function deletes a printer's spool file if the printer is configured for spooling.</span></span>

## <a name="syntax"></a><span data-ttu-id="63f0a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63f0a-105">Syntax</span></span>


```C++
BOOL AbortPrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="63f0a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63f0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63f0a-107">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="63f0a-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63f0a-108">Handle vers l’imprimante à partir de laquelle le fichier de mise en file d’attente est supprimé.</span><span class="sxs-lookup"><span data-stu-id="63f0a-108">Handle to the printer from which the spool file is deleted.</span></span> <span data-ttu-id="63f0a-109">Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="63f0a-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63f0a-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="63f0a-110">Return value</span></span>

<span data-ttu-id="63f0a-111">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="63f0a-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="63f0a-112">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="63f0a-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="63f0a-113">Notes</span><span class="sxs-lookup"><span data-stu-id="63f0a-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="63f0a-114">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="63f0a-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="63f0a-115">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="63f0a-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="63f0a-116">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="63f0a-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="63f0a-117">Si l’imprimante n’est pas configurée pour la mise en file d’attente, la fonction **AbortPrinter** n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="63f0a-117">If the printer is not configured for spooling, the **AbortPrinter** function has no effect.</span></span>

<span data-ttu-id="63f0a-118">La séquence d’un travail d’impression se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="63f0a-118">The sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="63f0a-119">Pour commencer un travail d’impression, appelez [**StartDocPrinter**](startdocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="63f0a-119">To begin a print job, call [**StartDocPrinter**](startdocprinter.md).</span></span>
2.  <span data-ttu-id="63f0a-120">Pour commencer chaque page, appelez [**StartPagePrinter**](startpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="63f0a-120">To begin each page, call [**StartPagePrinter**](startpageprinter.md).</span></span>
3.  <span data-ttu-id="63f0a-121">Pour écrire des données dans une page, appelez [**WritePrinter**](writeprinter.md).</span><span class="sxs-lookup"><span data-stu-id="63f0a-121">To write data to a page, call [**WritePrinter**](writeprinter.md).</span></span>
4.  <span data-ttu-id="63f0a-122">Pour terminer chaque page, appelez [**EndPagePrinter**](endpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="63f0a-122">To end each page, call [**EndPagePrinter**](endpageprinter.md).</span></span>
5.  <span data-ttu-id="63f0a-123">Répétez les étapes 2, 3 et 4 pour autant de pages que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="63f0a-123">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="63f0a-124">Pour mettre fin au travail d’impression, appelez [**EndDocPrinter**](enddocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="63f0a-124">To end the print job, call [**EndDocPrinter**](enddocprinter.md).</span></span>

<span data-ttu-id="63f0a-125">Quand une page dans un fichier mis en file d’attente dépasse environ 350 Mo, elle peut échouer et ne pas envoyer de message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="63f0a-125">When a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message.</span></span> <span data-ttu-id="63f0a-126">Par exemple, cela peut se produire lors de l’impression de fichiers EMF volumineux.</span><span class="sxs-lookup"><span data-stu-id="63f0a-126">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="63f0a-127">La limite de taille de page dépend de nombreux facteurs, notamment de la quantité de mémoire virtuelle disponible, de la quantité de mémoire allouée par les processus d’appel et de la quantité de fragmentation dans le segment de mémoire de processus.</span><span class="sxs-lookup"><span data-stu-id="63f0a-127">The page size limit depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span>

## <a name="requirements"></a><span data-ttu-id="63f0a-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63f0a-128">Requirements</span></span>



| <span data-ttu-id="63f0a-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63f0a-129">Requirement</span></span> | <span data-ttu-id="63f0a-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="63f0a-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63f0a-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63f0a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="63f0a-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63f0a-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="63f0a-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63f0a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="63f0a-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63f0a-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="63f0a-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="63f0a-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="63f0a-136"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63f0a-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="63f0a-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="63f0a-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="63f0a-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63f0a-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="63f0a-139">DLL</span><span class="sxs-lookup"><span data-stu-id="63f0a-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63f0a-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63f0a-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="63f0a-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63f0a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63f0a-142">Impression</span><span class="sxs-lookup"><span data-stu-id="63f0a-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="63f0a-143">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="63f0a-143">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="63f0a-144">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="63f0a-144">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="63f0a-145">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="63f0a-145">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="63f0a-146">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="63f0a-146">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="63f0a-147">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="63f0a-147">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="63f0a-148">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="63f0a-148">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="63f0a-149">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="63f0a-149">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




