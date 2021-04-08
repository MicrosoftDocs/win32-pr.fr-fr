---
title: Créer des objets accessibles
description: Créer des objets accessibles
ms.assetid: d34a52d1-1eb2-4bb4-989c-a1ca4b5d815f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5efa85e44d6d51105e6363d276ecb7e5f33d8378
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673594"
---
# <a name="create-new-accessible-objects"></a><span data-ttu-id="5111b-103">Créer des objets accessibles</span><span class="sxs-lookup"><span data-stu-id="5111b-103">Create New Accessible Objects</span></span>

<span data-ttu-id="5111b-104">Dans ce scénario, le serveur crée un nouvel objet accessible en réponse à chaque demande du [**\_ client objid**](object-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="5111b-104">In this scenario, the server creates a new accessible object in response to each [**OBJID\_CLIENT**](object-identifiers.md) request.</span></span>

<span data-ttu-id="5111b-105">Dans l’exemple de code suivant, un pointeur vers le contrôle est récupéré à partir des données de fenêtre supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="5111b-105">In the following example code, a pointer to the control is retrieved from the extra window data.</span></span> <span data-ttu-id="5111b-106">Cela et le handle de fenêtre sont passés au constructeur de l’objet AccServer (Custom Accessibility Server).</span><span class="sxs-lookup"><span data-stu-id="5111b-106">This and the window handle are passed to the constructor of the custom accessibility server (AccServer) object.</span></span> <span data-ttu-id="5111b-107">Cet objet est créé à chaque fois que le [**\_ client objid**](object-identifiers.md) est reçu.</span><span class="sxs-lookup"><span data-stu-id="5111b-107">This object is created whenever [**OBJID\_CLIENT**](object-identifiers.md) is received.</span></span>

<span data-ttu-id="5111b-108">Lorsque l’objet est créé, le serveur obtient une référence, qui doit être libérée après l’appel de [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), afin que l’objet soit détruit dès que le client a terminé de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="5111b-108">When the object is created, the server obtains a reference, which must be released after calling [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), so that the object is destroyed as soon as the client is finished with it.</span></span> <span data-ttu-id="5111b-109">Notez que **LresultFromObject** incrémente le nombre de références plusieurs fois, mais qu’il est de la responsabilité des applications clientes, et du runtime Microsoft Active Accessibility, de publier ces références.</span><span class="sxs-lookup"><span data-stu-id="5111b-109">Note that **LresultFromObject** increments the reference count several times, but it is the responsibility of client applications, and the Microsoft Active Accessibility runtime, to release these references.</span></span>


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



 

 




