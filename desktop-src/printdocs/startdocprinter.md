---
description: La fonction StartDocPrinter informe le spouleur d’impression qu’un document doit être mis en file d’attente pour l’impression.
ms.assetid: caa2bd80-4af3-4968-a5b9-d12f16cac6fc
title: StartDocPrinter, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StartDocPrinter
- StartDocPrinterA
- StartDocPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: f8bdb0ae08c88e553dad3a91f0f1a578bed4ad39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868025"
---
# <a name="startdocprinter-function"></a><span data-ttu-id="b7706-103">StartDocPrinter fonction)</span><span class="sxs-lookup"><span data-stu-id="b7706-103">StartDocPrinter function</span></span>

<span data-ttu-id="b7706-104">La fonction **StartDocPrinter** informe le spouleur d’impression qu’un document doit être mis en file d’attente pour l’impression.</span><span class="sxs-lookup"><span data-stu-id="b7706-104">The **StartDocPrinter** function notifies the print spooler that a document is to be spooled for printing.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7706-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7706-105">Syntax</span></span>


```C++
DWORD StartDocPrinter(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pDocInfo
);
```



## <a name="parameters"></a><span data-ttu-id="b7706-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7706-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7706-107">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b7706-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7706-108">Handle vers l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="b7706-108">A handle to the printer.</span></span> <span data-ttu-id="b7706-109">Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="b7706-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="b7706-110">De *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b7706-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7706-111">Version de la structure vers laquelle *pDocInfo* pointe.</span><span class="sxs-lookup"><span data-stu-id="b7706-111">The version of the structure to which *pDocInfo* points.</span></span> <span data-ttu-id="b7706-112">Cette valeur doit être 1.</span><span class="sxs-lookup"><span data-stu-id="b7706-112">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="b7706-113">*pDocInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b7706-113">*pDocInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7706-114">Pointeur vers une structure [**\_ infos doc \_ 1**](doc-info-1.md) qui décrit le document à imprimer.</span><span class="sxs-lookup"><span data-stu-id="b7706-114">A pointer to a [**DOC\_INFO\_1**](doc-info-1.md) structure that describes the document to print.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7706-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b7706-115">Return value</span></span>

<span data-ttu-id="b7706-116">Si la fonction est réussie, la valeur de retour identifie le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="b7706-116">If the function succeeds, the return value identifies the print job.</span></span>

<span data-ttu-id="b7706-117">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="b7706-117">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7706-118">Notes</span><span class="sxs-lookup"><span data-stu-id="b7706-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b7706-119">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="b7706-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="b7706-120">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="b7706-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="b7706-121">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="b7706-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="b7706-122">La séquence classique d’un travail d’impression est la suivante :</span><span class="sxs-lookup"><span data-stu-id="b7706-122">The typical sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="b7706-123">Pour commencer un travail d’impression, appelez **StartDocPrinter**.</span><span class="sxs-lookup"><span data-stu-id="b7706-123">To begin a print job, call **StartDocPrinter**.</span></span>
2.  <span data-ttu-id="b7706-124">Pour commencer chaque page, appelez [**StartPagePrinter**](startpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="b7706-124">To begin each page, call [**StartPagePrinter**](startpageprinter.md).</span></span>
3.  <span data-ttu-id="b7706-125">Pour écrire des données dans une page, appelez [**WritePrinter**](writeprinter.md).</span><span class="sxs-lookup"><span data-stu-id="b7706-125">To write data to a page, call [**WritePrinter**](writeprinter.md).</span></span>
4.  <span data-ttu-id="b7706-126">Pour terminer chaque page, appelez [**EndPagePrinter**](endpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="b7706-126">To end each page, call [**EndPagePrinter**](endpageprinter.md).</span></span>
5.  <span data-ttu-id="b7706-127">Répétez les étapes 2, 3 et 4 pour autant de pages que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b7706-127">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="b7706-128">Pour mettre fin au travail d’impression, appelez [**EndDocPrinter**](enddocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="b7706-128">To end the print job, call [**EndDocPrinter**](enddocprinter.md).</span></span>

<span data-ttu-id="b7706-129">Notez que l’appel de [**StartPagePrinter**](startpageprinter.md) et de [**EndPagePrinter**](endpageprinter.md) peut ne pas être nécessaire, par exemple si le type de données d’impression comprend les informations de page.</span><span class="sxs-lookup"><span data-stu-id="b7706-129">Note that calling [**StartPagePrinter**](startpageprinter.md) and [**EndPagePrinter**](endpageprinter.md) may not be necessary, such as if the print data type includes the page information.</span></span>

<span data-ttu-id="b7706-130">Quand une page dans un fichier mis en file d’attente dépasse environ 350 Mo, elle peut échouer et ne pas envoyer de message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b7706-130">When a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message.</span></span> <span data-ttu-id="b7706-131">Par exemple, cela peut se produire lors de l’impression de fichiers EMF volumineux.</span><span class="sxs-lookup"><span data-stu-id="b7706-131">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="b7706-132">La limite de taille de page dépend de nombreux facteurs, notamment de la quantité de mémoire virtuelle disponible, de la quantité de mémoire allouée par les processus d’appel et de la quantité de fragmentation dans le segment de mémoire de processus.</span><span class="sxs-lookup"><span data-stu-id="b7706-132">The page size limit depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span>

## <a name="examples"></a><span data-ttu-id="b7706-133">Exemples</span><span class="sxs-lookup"><span data-stu-id="b7706-133">Examples</span></span>

<span data-ttu-id="b7706-134">Pour obtenir un exemple de programme qui utilise cette fonction, consultez [Comment : imprimer à l’aide de l’API d’impression GDI](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="b7706-134">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b7706-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7706-135">Requirements</span></span>



| <span data-ttu-id="b7706-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7706-136">Requirement</span></span> | <span data-ttu-id="b7706-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7706-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7706-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7706-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b7706-139">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7706-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b7706-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7706-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b7706-141">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7706-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b7706-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="b7706-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7706-143"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b7706-143"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b7706-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b7706-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="b7706-145"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7706-145"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="b7706-146">DLL</span><span class="sxs-lookup"><span data-stu-id="b7706-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7706-147"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="b7706-147"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="b7706-148">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="b7706-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b7706-149">**StartDocPrinterW** (Unicode) et **StartDocPrinterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b7706-149">**StartDocPrinterW** (Unicode) and **StartDocPrinterA** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="b7706-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7706-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7706-151">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="b7706-151">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="b7706-152">**\_Infos doc \_ 1**</span><span class="sxs-lookup"><span data-stu-id="b7706-152">**DOC\_INFO\_1**</span></span>](doc-info-1.md)
</dt> <dt>

[<span data-ttu-id="b7706-153">**\_Infos doc \_ 2**</span><span class="sxs-lookup"><span data-stu-id="b7706-153">**DOC\_INFO\_2**</span></span>](doc-info-2.md)
</dt> <dt>

[<span data-ttu-id="b7706-154">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="b7706-154">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="b7706-155">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="b7706-155">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="b7706-156">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="b7706-156">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="b7706-157">Impression</span><span class="sxs-lookup"><span data-stu-id="b7706-157">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b7706-158">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="b7706-158">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="b7706-159">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="b7706-159">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="b7706-160">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="b7706-160">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="b7706-161">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="b7706-161">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




