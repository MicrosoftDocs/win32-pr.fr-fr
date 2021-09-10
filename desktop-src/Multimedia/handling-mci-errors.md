---
title: Gestion des erreurs MCI
description: Gestion des erreurs MCI
ms.assetid: 01a2ff95-34a2-434f-9c7e-d0cdac826c02
keywords:
- mciSendCommand fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab8412c74153d5ddfb03a3aff895f9f2e0e73798
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368287"
---
# <a name="handling-mci-errors"></a>Gestion des erreurs MCI

Vous devez toujours vérifier la valeur de retour de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) . S’il indique une erreur, vous pouvez utiliser [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) pour obtenir une description textuelle de l’erreur.

L’exemple suivant transmet le code d’erreur MCI spécifié par *dwError* à **mciGetErrorString**, puis affiche la description de l’erreur textuelle résultante à l’aide de la fonction [MessageBox](/windows/win32/api/winuser/nf-winuser-messagebox) .


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
> Pour interpréter vous-même une valeur de retour d’erreur [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) , masquez le mot de poids fort (le mot de poids faible contient le code d’erreur). Toutefois, si vous transmettez la valeur de retour d’erreur à [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)), vous devez passer la valeur de mot double entière.

 

 

 