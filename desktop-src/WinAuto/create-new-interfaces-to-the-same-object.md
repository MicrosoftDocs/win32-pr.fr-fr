---
title: Créer des interfaces vers le même objet
description: Créer des interfaces vers le même objet
ms.assetid: 127c44b6-51a6-4fd6-9edc-9fbe0d08d458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aae1d6328b6d803e4d20207381fe596c5f584fee8281e1e6651ffc2325fb044
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998709"
---
# <a name="create-new-interfaces-to-the-same-object"></a>Créer des interfaces vers le même objet

Dans ce scénario, le serveur répond à chaque demande du [**\_ client objid**](object-identifiers.md) en obtenant un nouveau pointeur d’interface vers le même objet.

Dans l’exemple de code suivant, *m \_ pUIObj* est un pointeur vers un objet qui prend en charge plusieurs interfaces COM (Component Object Model). Bien qu’un objet existant soit réutilisé, un nouveau pointeur d’interface est créé chaque fois que l’objet est récupéré, de sorte que le décompte de références doit être décrémenté.


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



 

 




