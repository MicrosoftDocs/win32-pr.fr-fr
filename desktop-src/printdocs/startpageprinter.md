---
description: La fonction StartPagePrinter informe le spouleur qu’une page va être imprimée sur l’imprimante spécifiée.
ms.assetid: 8ac7c47b-b3a7-4642-bfb7-54e014139fbf
title: StartPagePrinter, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StartPagePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: f8d1c5cc296fae1b166b891fc881a6abcdb6b2af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951871"
---
# <a name="startpageprinter-function"></a><span data-ttu-id="99ce9-103">StartPagePrinter fonction)</span><span class="sxs-lookup"><span data-stu-id="99ce9-103">StartPagePrinter function</span></span>

<span data-ttu-id="99ce9-104">La fonction **StartPagePrinter** informe le spouleur qu’une page va être imprimée sur l’imprimante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="99ce9-104">The **StartPagePrinter** function notifies the spooler that a page is about to be printed on the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="99ce9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99ce9-105">Syntax</span></span>


```C++
BOOL StartPagePrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="99ce9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99ce9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99ce9-107">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="99ce9-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99ce9-108">Handle vers une imprimante.</span><span class="sxs-lookup"><span data-stu-id="99ce9-108">Handle to a printer.</span></span> <span data-ttu-id="99ce9-109">Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="99ce9-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99ce9-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="99ce9-110">Return value</span></span>

<span data-ttu-id="99ce9-111">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="99ce9-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="99ce9-112">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="99ce9-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="99ce9-113">Notes</span><span class="sxs-lookup"><span data-stu-id="99ce9-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="99ce9-114">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="99ce9-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="99ce9-115">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="99ce9-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="99ce9-116">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="99ce9-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="99ce9-117">La séquence d’un travail d’impression se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="99ce9-117">The sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="99ce9-118">Pour commencer un travail d’impression, appelez [**StartDocPrinter**](startdocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="99ce9-118">To begin a print job, call [**StartDocPrinter**](startdocprinter.md).</span></span>
2.  <span data-ttu-id="99ce9-119">Pour commencer chaque page, appelez **StartPagePrinter**.</span><span class="sxs-lookup"><span data-stu-id="99ce9-119">To begin each page, call **StartPagePrinter**.</span></span>
3.  <span data-ttu-id="99ce9-120">Pour écrire des données dans une page, appelez [**WritePrinter**](writeprinter.md).</span><span class="sxs-lookup"><span data-stu-id="99ce9-120">To write data to a page, call [**WritePrinter**](writeprinter.md).</span></span>
4.  <span data-ttu-id="99ce9-121">Pour terminer chaque page, appelez [**EndPagePrinter**](endpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="99ce9-121">To end each page, call [**EndPagePrinter**](endpageprinter.md).</span></span>
5.  <span data-ttu-id="99ce9-122">Répétez les étapes 2, 3 et 4 pour autant de pages que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="99ce9-122">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="99ce9-123">Pour mettre fin au travail d’impression, appelez [**EndDocPrinter**](enddocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="99ce9-123">To end the print job, call [**EndDocPrinter**](enddocprinter.md).</span></span>

<span data-ttu-id="99ce9-124">Quand une page dans un fichier mis en file d’attente dépasse environ 350 Mo, elle peut échouer et ne pas envoyer de message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="99ce9-124">When a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message.</span></span> <span data-ttu-id="99ce9-125">Par exemple, cela peut se produire lors de l’impression de fichiers EMF volumineux.</span><span class="sxs-lookup"><span data-stu-id="99ce9-125">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="99ce9-126">La limite de taille de page dépend de nombreux facteurs, notamment de la quantité de mémoire virtuelle disponible, de la quantité de mémoire allouée par les processus d’appel et de la quantité de fragmentation dans le segment de mémoire de processus.</span><span class="sxs-lookup"><span data-stu-id="99ce9-126">The page size limit depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span>

## <a name="examples"></a><span data-ttu-id="99ce9-127">Exemples</span><span class="sxs-lookup"><span data-stu-id="99ce9-127">Examples</span></span>

<span data-ttu-id="99ce9-128">Pour obtenir un exemple de programme qui utilise cette fonction, consultez [Comment : imprimer à l’aide de l’API d’impression GDI](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="99ce9-128">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="99ce9-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99ce9-129">Requirements</span></span>



| <span data-ttu-id="99ce9-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99ce9-130">Requirement</span></span> | <span data-ttu-id="99ce9-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="99ce9-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99ce9-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99ce9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="99ce9-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="99ce9-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="99ce9-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99ce9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="99ce9-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="99ce9-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="99ce9-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="99ce9-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="99ce9-137"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99ce9-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="99ce9-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="99ce9-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="99ce9-139"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99ce9-139"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="99ce9-140">DLL</span><span class="sxs-lookup"><span data-stu-id="99ce9-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99ce9-141"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99ce9-141"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="99ce9-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99ce9-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99ce9-143">Impression</span><span class="sxs-lookup"><span data-stu-id="99ce9-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="99ce9-144">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="99ce9-144">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="99ce9-145">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="99ce9-145">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="99ce9-146">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="99ce9-146">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="99ce9-147">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="99ce9-147">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="99ce9-148">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="99ce9-148">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="99ce9-149">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="99ce9-149">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="99ce9-150">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="99ce9-150">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




