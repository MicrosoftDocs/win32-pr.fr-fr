---
title: Créer des objets accessibles
description: Créer des objets accessibles
ms.assetid: d34a52d1-1eb2-4bb4-989c-a1ca4b5d815f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5efa85e44d6d51105e6363d276ecb7e5f33d8378
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127124527"
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



 

 




