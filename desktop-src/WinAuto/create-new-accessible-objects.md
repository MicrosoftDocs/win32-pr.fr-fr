---
title: Créer des objets accessibles
description: Créer des objets accessibles
ms.assetid: d34a52d1-1eb2-4bb4-989c-a1ca4b5d815f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaaa9ee8669199a9f4de938b4e1cb9e6dd24336bd86527a2cc528709e303543e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052817"
---
# <a name="create-new-accessible-objects"></a>Créer des objets accessibles

Dans ce scénario, le serveur crée un nouvel objet accessible en réponse à chaque demande du [**\_ client objid**](object-identifiers.md) .

Dans l’exemple de code suivant, un pointeur vers le contrôle est récupéré à partir des données de fenêtre supplémentaires. Cela et le handle de fenêtre sont passés au constructeur de l’objet AccServer (Custom Accessibility Server). Cet objet est créé à chaque fois que le [**\_ client objid**](object-identifiers.md) est reçu.

Lorsque l’objet est créé, le serveur obtient une référence, qui doit être libérée après l’appel de [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), afin que l’objet soit détruit dès que le client a terminé de l’utiliser. Notez que **LresultFromObject** incrémente le nombre de références plusieurs fois, mais qu’il est de la responsabilité des applications clientes, et du runtime Microsoft Active Accessibility, de publier ces références.


```C++
case WM_GETOBJECT:
{
    // Return the IAccessible object. 
    if ((DWORD)lParam == OBJID_CLIENT)
    {
        // Get the control.  
        CustomListControl* pCustomList = (CustomListControl*)(LONG_PTR)GetWindowLongPtr(hwnd, 0);
        AccServer* pAccServer = new AccServer(hwnd, pCustomList);
        if (pAccServer != NULL)  // NULL if out of memory. 
        {
            LRESULT Lresult = LresultFromObject(IID_IAccessible, wParam, pAccServer);
            pAccServer->Release();
            return Lresult;
        }
        else return 0;
    }
    break;
}
```



 

 




