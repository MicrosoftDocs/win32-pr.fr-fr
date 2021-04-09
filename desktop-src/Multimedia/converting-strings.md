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
# <a name="converting-strings"></a><span data-ttu-id="1d477-104">Conversion de chaînes</span><span class="sxs-lookup"><span data-stu-id="1d477-104">Converting Strings</span></span>

<span data-ttu-id="1d477-105">Lorsque vous utilisez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) , toutes les valeurs transmises avec la commande et toutes les valeurs retournées sont des chaînes de texte. par conséquent, votre application a besoin de routines de conversion pour effectuer la conversion des variables en chaînes ou inversement.</span><span class="sxs-lookup"><span data-stu-id="1d477-105">When you use the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function, all values passed with the command and all return values are text strings, so your application needs conversion routines to translate from variables to strings or back again.</span></span> <span data-ttu-id="1d477-106">L’exemple suivant récupère le rectangle source et convertit la chaîne retournée en coordonnées de rectangle.</span><span class="sxs-lookup"><span data-stu-id="1d477-106">The following example retrieves the source rectangle and converts the returned string into rectangle coordinates.</span></span>


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
> <span data-ttu-id="1d477-107">Les structures **Rect** sont gérées différemment dans MCI et dans d’autres parties de Windows. dans MCI, le membre de **droite** contient la largeur du rectangle et le membre **inférieur** contient sa hauteur.</span><span class="sxs-lookup"><span data-stu-id="1d477-107">**RECT** structures are handled differently in MCI than in other parts of Windows; in MCI, the **right** member contains the width of the rectangle and the **bottom** member contains its height.</span></span> <span data-ttu-id="1d477-108">Dans l’interface de chaîne, un rectangle est spécifié sous la forme *x1*, *Y1*, *x2* et *Y2*.</span><span class="sxs-lookup"><span data-stu-id="1d477-108">In the string interface, a rectangle is specified as *X1*, *Y1*, *X2*, and *Y2*.</span></span> <span data-ttu-id="1d477-109">Les coordonnées *x1* et *Y1* spécifient l’angle supérieur gauche du rectangle, tandis que les coordonnées *x2* et *Y2* spécifient la largeur et la hauteur.</span><span class="sxs-lookup"><span data-stu-id="1d477-109">The coordinates *X1* and *Y1* specify the upper-left corner of the rectangle, and the coordinates *X2* and *Y2* specify the width and height.</span></span>

 

 

 