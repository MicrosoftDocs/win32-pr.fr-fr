---
title: Réutiliser des pointeurs existants vers des objets
description: Réutiliser des pointeurs existants vers des objets
ms.assetid: 7e1610c6-89b2-4e7e-aee5-94a6cab87a22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c151b8d957fb82718721ad81b452a81a2c71ec84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512027"
---
# <a name="reuse-existing-pointers-to-objects"></a><span data-ttu-id="e7a73-103">Réutiliser des pointeurs existants vers des objets</span><span class="sxs-lookup"><span data-stu-id="e7a73-103">Reuse Existing Pointers to Objects</span></span>

<span data-ttu-id="e7a73-104">Dans ce scénario, le serveur répond à une demande du [**\_ client objid**](object-identifiers.md) à l’aide du même pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) à chaque fois.</span><span class="sxs-lookup"><span data-stu-id="e7a73-104">In this scenario, the server responds to an [**OBJID\_CLIENT**](object-identifiers.md) request using the same [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer each time.</span></span>

<span data-ttu-id="e7a73-105">Dans l’exemple de code suivant, l’objet de contrôle est récupéré à partir des données de fenêtre supplémentaires, et une méthode du contrôle est appelée pour récupérer l’objet de serveur d’accessibilité (la classe AccServer définie par l’application), le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="e7a73-105">In the following example code, the control object is retrieved from the extra window data, and a method of the control is called to retrieve the accessibility server object (the application-defined AccServer class), if any.</span></span> <span data-ttu-id="e7a73-106">Si le serveur d’accessibilité n’existe pas encore, il est créé.</span><span class="sxs-lookup"><span data-stu-id="e7a73-106">If the accessibility server does not yet exist, it is created.</span></span>

<span data-ttu-id="e7a73-107">Lorsque l’objet de serveur d’accessibilité est créé, il a un nombre de références de 1.</span><span class="sxs-lookup"><span data-stu-id="e7a73-107">When the accessibility server object is created, it has a reference count of 1.</span></span> <span data-ttu-id="e7a73-108">[**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) incrémente le nombre de références plusieurs fois, mais ces références sont libérées lorsque le client a terminé avec l’objet.</span><span class="sxs-lookup"><span data-stu-id="e7a73-108">[**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) increments the reference count several times, but these references will be released when the client is finished with the object.</span></span> <span data-ttu-id="e7a73-109">Le serveur libère sa référence lorsque la fenêtre de contrôle est détruite.</span><span class="sxs-lookup"><span data-stu-id="e7a73-109">The server releases its reference when the control window is destroyed.</span></span>


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



 

 




