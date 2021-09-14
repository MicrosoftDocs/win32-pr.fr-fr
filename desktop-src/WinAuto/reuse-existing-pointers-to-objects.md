---
title: Réutiliser des pointeurs existants vers des objets
description: Réutiliser des pointeurs existants vers des objets
ms.assetid: 7e1610c6-89b2-4e7e-aee5-94a6cab87a22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c151b8d957fb82718721ad81b452a81a2c71ec84
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010647"
---
# <a name="reuse-existing-pointers-to-objects"></a>Réutiliser des pointeurs existants vers des objets

Dans ce scénario, le serveur répond à une demande du [**\_ client objid**](object-identifiers.md) à l’aide du même pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) à chaque fois.

Dans l’exemple de code suivant, l’objet de contrôle est récupéré à partir des données de fenêtre supplémentaires, et une méthode du contrôle est appelée pour récupérer l’objet de serveur d’accessibilité (la classe AccServer définie par l’application), le cas échéant. Si le serveur d’accessibilité n’existe pas encore, il est créé.

Lorsque l’objet de serveur d’accessibilité est créé, il a un nombre de références de 1. [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) incrémente le nombre de références plusieurs fois, mais ces références sont libérées lorsque le client a terminé avec l’objet. Le serveur libère sa référence lorsque la fenêtre de contrôle est détruite.


```C++
case WM_GETOBJECT:
    {
        // Return the IAccessible object. 
        if ((DWORD)lParam == (DWORD)OBJID_CLIENT)
        {
            // Get the control.  
            CustomListControl* pCustomList = (CustomListControl*)(LONG_PTR)GetWindowLongPtr(hwnd, 0);
            // Create the accessible object. 
            AccServer* pAccServer = pCustomList->GetAccServer();
            if (pAccServer == NULL)
            {
                pAccServer = new AccServer(hwnd, pCustomList);
                pCustomList->SetAccServer(pAccServer);
            }
            if (pAccServer != NULL)  // NULL if out of memory. 
            {
                LRESULT Lresult = LresultFromObject(IID_IAccessible, wParam, pAccServer);
                return Lresult;
            }
            else return 0;
        }
        break;
    }

    
case WM_DESTROY:
    {
    CustomListControl* pCustomList = (CustomListControl*)(LONG_PTR)GetWindowLongPtr(hwnd, 0);
    AccServer* pAccServer = pCustomList->GetAccServer();
    if (pAccServer!= NULL)
    {
        // Notify the accessibility object that the control no longer exists. 
        pAccServer->SetControlIsAlive(false);
        // Release the reference created in WM_GETOBJECT. 
        pAccServer->Release(); 
    }   
    // Destroy the control. 
    delete pCustomList;
     break;
    }
```



 

 




