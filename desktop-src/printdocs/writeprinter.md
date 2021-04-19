---
description: La fonction WritePrinter informe le spouleur d’impression que les données doivent être écrites sur l’imprimante spécifiée.
ms.assetid: 9411b71f-d686-44ed-9051-d410e5ab228e
title: WritePrinter, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WritePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 490221b15ed1e3c7dad3a4cb523c15e9ec484b13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527492"
---
# <a name="writeprinter-function"></a><span data-ttu-id="eb882-103">WritePrinter fonction)</span><span class="sxs-lookup"><span data-stu-id="eb882-103">WritePrinter function</span></span>

<span data-ttu-id="eb882-104">La fonction **WritePrinter** informe le spouleur d’impression que les données doivent être écrites sur l’imprimante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="eb882-104">The **WritePrinter** function notifies the print spooler that data should be written to the specified printer.</span></span>

> [!Note]  
> <span data-ttu-id="eb882-105">**WritePrinter** prend uniquement en charge l’impression GDI et ne doit pas être utilisé pour l’impression XPS.</span><span class="sxs-lookup"><span data-stu-id="eb882-105">**WritePrinter** only supports GDI printing and must not be used for XPS printing.</span></span> <span data-ttu-id="eb882-106">Si votre travail d’impression utilise le chemin d’impression XPS ou OpenXPS, utilisez l' [API d’impression XPS](/windows/desktop/printdocs/xps-printing).</span><span class="sxs-lookup"><span data-stu-id="eb882-106">If your print job uses the XPS or the OpenXPS print path, then use the [XPS Print API](/windows/desktop/printdocs/xps-printing).</span></span> <span data-ttu-id="eb882-107">L’envoi de travaux d’impression XPS ou OpenXPS au spouleur à l’aide de **WritePrinter** n’est pas pris en charge et peut entraîner des résultats indéterminés.</span><span class="sxs-lookup"><span data-stu-id="eb882-107">Sending XPS or OpenXPS print jobs to the spooler using **WritePrinter** is not supported and can result in undetermined results.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="eb882-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb882-108">Syntax</span></span>


```C++
BOOL WritePrinter(
  _In_  HANDLE  hPrinter,
  _In_  LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcWritten
);
```



## <a name="parameters"></a><span data-ttu-id="eb882-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb882-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb882-110">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb882-110">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb882-111">Handle vers l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="eb882-111">A handle to the printer.</span></span> <span data-ttu-id="eb882-112">Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="eb882-112">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="eb882-113">*pBuf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb882-113">*pBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb882-114">Pointeur vers un tableau d’octets qui contient les données qui doivent être écrites sur l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="eb882-114">A pointer to an array of bytes that contains the data that should be written to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="eb882-115">*cbBuf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb882-115">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb882-116">Taille, en octets, du tableau.</span><span class="sxs-lookup"><span data-stu-id="eb882-116">The size, in bytes, of the array.</span></span>

</dd> <dt>

<span data-ttu-id="eb882-117">*pcWritten* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="eb882-117">*pcWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb882-118">Pointeur vers une valeur qui reçoit le nombre d’octets de données qui ont été écrits sur l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="eb882-118">A pointer to a value that receives the number of bytes of data that were written to the printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb882-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb882-119">Return value</span></span>

<span data-ttu-id="eb882-120">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="eb882-120">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="eb882-121">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="eb882-121">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb882-122">Notes</span><span class="sxs-lookup"><span data-stu-id="eb882-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="eb882-123">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="eb882-123">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="eb882-124">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="eb882-124">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="eb882-125">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="eb882-125">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="eb882-126">La séquence d’un travail d’impression se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="eb882-126">The sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="eb882-127">Pour commencer un travail d’impression, appelez [**StartDocPrinter**](startdocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="eb882-127">To begin a print job, call [**StartDocPrinter**](startdocprinter.md).</span></span>
2.  <span data-ttu-id="eb882-128">Pour commencer chaque page, appelez [**StartPagePrinter**](startpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="eb882-128">To begin each page, call [**StartPagePrinter**](startpageprinter.md).</span></span>
3.  <span data-ttu-id="eb882-129">Pour écrire des données dans une page, appelez **WritePrinter**.</span><span class="sxs-lookup"><span data-stu-id="eb882-129">To write data to a page, call **WritePrinter**.</span></span>
4.  <span data-ttu-id="eb882-130">Pour terminer chaque page, appelez [**EndPagePrinter**](endpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="eb882-130">To end each page, call [**EndPagePrinter**](endpageprinter.md).</span></span>
5.  <span data-ttu-id="eb882-131">Répétez les étapes 2, 3 et 4 pour autant de pages que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="eb882-131">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="eb882-132">Pour mettre fin au travail d’impression, appelez [**EndDocPrinter**](enddocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="eb882-132">To end the print job, call [**EndDocPrinter**](enddocprinter.md).</span></span>

<span data-ttu-id="eb882-133">Lorsqu’un document de niveau supérieur (par exemple, un fichier Adobe PDF ou Microsoft Word) ou d’autres données d’imprimante (par exemple, PCL, PS ou HPGL) sont envoyés directement à une imprimante, les paramètres d’impression définis dans le document ont priorité sur les paramètres d’impression Windows.</span><span class="sxs-lookup"><span data-stu-id="eb882-133">When a high-level document (such as an Adobe PDF or Microsoft Word file) or other printer data (such PCL, PS, or HPGL) is sent directly to a printer, the print settings defined in the document take precedent over Windows print settings.</span></span> <span data-ttu-id="eb882-134">Les documents sont générés lorsque la valeur du membre *pDatatype* de la structure [**\_ infos doc \_ 1**](doc-info-1.md) qui a été transmise dans le paramètre *PDOCINFO* de l’appel [**StartDocPrinter**](startdocprinter.md) est « RAW » doit décrire entièrement les paramètres du travail d’impression de style [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)dans la langue comprise par le matériel.</span><span class="sxs-lookup"><span data-stu-id="eb882-134">Documents output when the value of the *pDatatype* member of the [**DOC\_INFO\_1**](doc-info-1.md) structure that was passed in the *pDocInfo* parameter of the [**StartDocPrinter**](startdocprinter.md) call is "RAW" must fully describe the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)-style print job settings in the language understood by the hardware.</span></span>

<span data-ttu-id="eb882-135">Dans les versions de Windows antérieures à Windows XP, quand une page dans un fichier mis en file d’attente dépasse environ 350 Mo, elle peut échouer et ne pas envoyer de message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="eb882-135">In versions of Windows prior to Windows XP, when a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message.</span></span> <span data-ttu-id="eb882-136">Par exemple, cela peut se produire lors de l’impression de fichiers EMF volumineux.</span><span class="sxs-lookup"><span data-stu-id="eb882-136">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="eb882-137">La limite de taille de page dans les versions de Windows antérieures à Windows XP dépend de nombreux facteurs, notamment la quantité de mémoire virtuelle disponible, la quantité de mémoire allouée par les processus appelant et la quantité de fragmentation dans le segment de mémoire de processus.</span><span class="sxs-lookup"><span data-stu-id="eb882-137">The page size limit in versions of Windows prior to Windows XP depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span> <span data-ttu-id="eb882-138">Dans Windows XP et les versions ultérieures de Windows, les fichiers EMF doivent avoir une taille inférieure ou égale à 2 Go.</span><span class="sxs-lookup"><span data-stu-id="eb882-138">In Windows XP and later versions of Windows, EMF files must be 2GB or less in size.</span></span> <span data-ttu-id="eb882-139">Si **WritePrinter** est utilisé pour écrire des données non EMF, telles que le PDL prêt pour l’impression, la taille du fichier est limitée uniquement par l’espace disque disponible.</span><span class="sxs-lookup"><span data-stu-id="eb882-139">If **WritePrinter** is used to write non EMF data, such as printer-ready PDL, the size of the file is limited only by the available disk space.</span></span>

## <a name="examples"></a><span data-ttu-id="eb882-140">Exemples</span><span class="sxs-lookup"><span data-stu-id="eb882-140">Examples</span></span>

<span data-ttu-id="eb882-141">Pour obtenir un exemple de programme qui utilise cette fonction, consultez [Comment : imprimer à l’aide de l’API d’impression GDI](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="eb882-141">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb882-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb882-142">Requirements</span></span>



| <span data-ttu-id="eb882-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb882-143">Requirement</span></span> | <span data-ttu-id="eb882-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb882-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb882-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb882-145">Minimum supported client</span></span><br/> | <span data-ttu-id="eb882-146">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb882-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="eb882-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb882-147">Minimum supported server</span></span><br/> | <span data-ttu-id="eb882-148">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb882-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="eb882-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="eb882-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb882-150"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb882-150"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="eb882-151">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eb882-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="eb882-152"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb882-152"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="eb882-153">DLL</span><span class="sxs-lookup"><span data-stu-id="eb882-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb882-154"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb882-154"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="eb882-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb882-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb882-156">Impression</span><span class="sxs-lookup"><span data-stu-id="eb882-156">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="eb882-157">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="eb882-157">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="eb882-158">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="eb882-158">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="eb882-159">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="eb882-159">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="eb882-160">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="eb882-160">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="eb882-161">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="eb882-161">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="eb882-162">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="eb882-162">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="eb882-163">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="eb882-163">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

