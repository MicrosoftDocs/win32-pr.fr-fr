---
title: Créer des interfaces vers le même objet
description: Créer des interfaces vers le même objet
ms.assetid: 127c44b6-51a6-4fd6-9edc-9fbe0d08d458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b641eed3918af3acbf399427ad5f7427112f399
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510207"
---
# <a name="create-new-interfaces-to-the-same-object"></a><span data-ttu-id="4223f-103">Créer des interfaces vers le même objet</span><span class="sxs-lookup"><span data-stu-id="4223f-103">Create New Interfaces to the Same Object</span></span>

<span data-ttu-id="4223f-104">Dans ce scénario, le serveur répond à chaque demande du [**\_ client objid**](object-identifiers.md) en obtenant un nouveau pointeur d’interface vers le même objet.</span><span class="sxs-lookup"><span data-stu-id="4223f-104">In this scenario, the server responds to each [**OBJID\_CLIENT**](object-identifiers.md) request by obtaining a new interface pointer to the same object.</span></span>

<span data-ttu-id="4223f-105">Dans l’exemple de code suivant, *m \_ pUIObj* est un pointeur vers un objet qui prend en charge plusieurs interfaces COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="4223f-105">In the following example code, *m\_pUIObj* is a pointer to an object that supports more than one Component Object Model (COM) interface.</span></span> <span data-ttu-id="4223f-106">Bien qu’un objet existant soit réutilisé, un nouveau pointeur d’interface est créé chaque fois que l’objet est récupéré, de sorte que le décompte de références doit être décrémenté.</span><span class="sxs-lookup"><span data-stu-id="4223f-106">Even though an existing object is reused, a new interface pointer is created each time the object is retrieved, so the reference count must be decremented.</span></span>


```C++
case WM_GETOBJECT:
   if ((DWORD)lParam == OBJID_CLIENT)
   {
      // Get a new interface to the same object. 
      IAccessible *pAcc = NULL;
      // The following increments the reference count. 
      m_pUIObj->QueryInterface(IID_IAccessible, (LPVOID*)&pAcc); 
      LRESULT lAcc = LresultFromObject(IID_IAccessible, wParam, 
            (LPUNKNOWN) &pAcc); 
      // Release our reference to the object.             
      pAcc->Release();               
      return lAcc;
   }
   break;  // Fall through to DefWindowProc. 
   
```



 

 




