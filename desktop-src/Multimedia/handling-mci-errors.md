---
title: Gestion des erreurs MCI
description: Gestion des erreurs MCI
ms.assetid: 01a2ff95-34a2-434f-9c7e-d0cdac826c02
keywords:
- mciSendCommand fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab8412c74153d5ddfb03a3aff895f9f2e0e73798
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106511680"
---
# <a name="handling-mci-errors"></a><span data-ttu-id="17367-104">Gestion des erreurs MCI</span><span class="sxs-lookup"><span data-stu-id="17367-104">Handling MCI Errors</span></span>

<span data-ttu-id="17367-105">Vous devez toujours vérifier la valeur de retour de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="17367-105">You should always check the return value of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span> <span data-ttu-id="17367-106">S’il indique une erreur, vous pouvez utiliser [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) pour obtenir une description textuelle de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="17367-106">If it indicates an error, you can use [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) to get a textual description of the error.</span></span>

<span data-ttu-id="17367-107">L’exemple suivant transmet le code d’erreur MCI spécifié par *dwError* à **mciGetErrorString**, puis affiche la description de l’erreur textuelle résultante à l’aide de la fonction [MessageBox](/windows/win32/api/winuser/nf-winuser-messagebox) .</span><span class="sxs-lookup"><span data-stu-id="17367-107">The following example passes the MCI error code specified by *dwError* to **mciGetErrorString**, and then displays the resulting textual error description using the [MessageBox](/windows/win32/api/winuser/nf-winuser-messagebox) function.</span></span>


```C++
// Use mciGetErrorString to get a textual description of an MCI error.
// Display the error description using MessageBox.

void showError(DWORD dwError)
{
    char szErrorBuf[MAXERRORLENGTH];
    MessageBeep(MB_ICONEXCLAMATION);
    if(mciGetErrorString(dwError, (LPSTR) szErrorBuf, MAXERRORLENGTH))
    {
        MessageBox(hMainWnd, szErrorBuf, "MCI Error",
        MB_ICONEXCLAMATION);
    }
    else
    {
        MessageBox(hMainWnd, "Unknown Error", "MCI Error",
            MB_ICONEXCLAMATION);
    }
}
 
```



> [!Note]  
> <span data-ttu-id="17367-108">Pour interpréter vous-même une valeur de retour d’erreur [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) , masquez le mot de poids fort (le mot de poids faible contient le code d’erreur).</span><span class="sxs-lookup"><span data-stu-id="17367-108">To interpret an [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) error return value yourself, mask the high-order word (the low-order word contains the error code).</span></span> <span data-ttu-id="17367-109">Toutefois, si vous transmettez la valeur de retour d’erreur à [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)), vous devez passer la valeur de mot double entière.</span><span class="sxs-lookup"><span data-stu-id="17367-109">If you pass the error return value to [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)), however, you must pass the entire doubleword value.</span></span>

 

 

 