---
title: Conversion de chaînes
description: Conversion de chaînes
ms.assetid: 40621c71-4264-40bc-b6c3-6b639d2f28fa
keywords:
- mciSendString fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d1db4cb4b3d02a93adecc82d6ce95de436fb2e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940862"
---
# <a name="converting-strings"></a>Conversion de chaînes

Lorsque vous utilisez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) , toutes les valeurs transmises avec la commande et toutes les valeurs retournées sont des chaînes de texte. par conséquent, votre application a besoin de routines de conversion pour effectuer la conversion des variables en chaînes ou inversement. L’exemple suivant récupère le rectangle source et convertit la chaîne retournée en coordonnées de rectangle.


```C++
BOOL GetSourceRect(LPTSTR lpstrAlias, LPRECT lprc) 
{ 
    TCHAR achRetBuff[128]; 
    TCHAR achCommandBuff[128]; 

    int result;
    MCIERROR err;
 
    // Build the command string. 
    result = _stprintf_s(
        achCommandBuff, 
        TEXT("where %s source"), 
        lpstrAlias); 

    if (result == -1)
    {
        return FALSE;
    }
    
    // Clear the RECT.
    SetRectEmpty(lprc);
 
    // Send the MCI command. 
    err = mciSendString(
        achCommandBuff, 
        achRetBuff, 
        sizeof(achRetBuff), 
        NULL);

    if (err != 0)
    {
        return FALSE;
    }
        
    // The rectangle is returned as "x y dx dy". 
    // Translate the string into the RECT structure. 

    // Warning: This example omits error checking
    // for the _tcstok_s and _tstoi functions.
    TCHAR *p; 
    TCHAR *context;

    // Left.
    p = _tcstok_s(achRetBuff, TEXT(" "), &context);
    lprc->left = _tstoi(p);

    // Top.
    p = _tcstok_s(NULL, TEXT(" "), &context);
    lprc->top = _tstoi(p);

    // Right.
    p = _tcstok_s(NULL, TEXT(" "), &context);
    lprc->right = _tstoi(p);
    
    // Bottom.
    p = _tcstok_s(NULL, TEXT(" "), &context);
    lprc->bottom = _tstoi(p);

    return TRUE;
}
 
```



> [!Note]  
> Les structures **Rect** sont gérées différemment dans MCI et dans d’autres parties de Windows. dans MCI, le membre de **droite** contient la largeur du rectangle et le membre **inférieur** contient sa hauteur. Dans l’interface de chaîne, un rectangle est spécifié sous la forme *x1*, *Y1*, *x2* et *Y2*. Les coordonnées *x1* et *Y1* spécifient l’angle supérieur gauche du rectangle, tandis que les coordonnées *x2* et *Y2* spécifient la largeur et la hauteur.

 

 

 