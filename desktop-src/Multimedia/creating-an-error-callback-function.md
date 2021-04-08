---
title: Création d’une fonction de rappel d’erreur
description: Création d’une fonction de rappel d’erreur
ms.assetid: a489ec94-c566-44b1-aa93-9b43f23de744
keywords:
- capSetCallbackOnError macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac37c0e12b8f92520c4445c4c5ba3361974d836
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673173"
---
# <a name="creating-an-error-callback-function"></a><span data-ttu-id="d75d7-104">Création d’une fonction de rappel d’erreur</span><span class="sxs-lookup"><span data-stu-id="d75d7-104">Creating an Error Callback Function</span></span>

<span data-ttu-id="d75d7-105">L’exemple suivant est une fonction de rappel d’erreur simple.</span><span class="sxs-lookup"><span data-stu-id="d75d7-105">The following example is a simple error callback function.</span></span> <span data-ttu-id="d75d7-106">Inscrivez ce rappel à l’aide de la macro [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) .</span><span class="sxs-lookup"><span data-stu-id="d75d7-106">Register this callback by using the [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) macro.</span></span>


```
TCHAR gachBuffer[100]; // Global buffer.

// ErrorCallbackProc: error callback function. 
// hWnd:              capture window handle. 
// nErrID:            error code for the encountered error. 
// lpErrorText:       error text string for the encountered error. 
// 
LRESULT PASCAL ErrorCallbackProc(HWND hWnd, int nErrID,
    LPTSTR lpErrorText) 
{ 
 
    if (!hWnd) 
        return FALSE; 
 
    if (nErrID == 0)            // Starting a new major function. 
        return TRUE;            // Clear out old errors. 
 
    // Show the error identifier and text. 
    _stprintf_s(gachBuffer, TEXT("Error# %d"), nErrID); 
 
    MessageBox(hWnd, lpErrorText, gachBuffer, 
        MB_OK | MB_ICONEXCLAMATION); 
 
    return (LRESULT) TRUE; 
} 
```



## <a name="related-topics"></a><span data-ttu-id="d75d7-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d75d7-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d75d7-108">Utilisation de la capture vidéo</span><span class="sxs-lookup"><span data-stu-id="d75d7-108">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




