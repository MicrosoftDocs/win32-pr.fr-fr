---
title: Fonction type_free_inst
description: Les stubs appellent la \_ \_ fonction Free inst pour libérer de la mémoire associée au type présenté.
ms.assetid: 4ee2e6a6-b506-445f-adaf-3705228defa7
keywords:
- type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3754106cf8e0cc6e338f91d6c233181aa33038eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096486"
---
# <a name="the-type_free_inst-function"></a>Type \_ Free \_ inst, fonction

Les stubs appellent la fonction **\_ Free \_ inst** pour libérer de la mémoire associée au type présenté. La fonction est définie comme suit :

``` syntax
void __RPC_USER <type>_free_inst(<type> __RPC_FAR *)
```

Le paramètre pointe vers l’instance de type présentée. Cet objet ne doit pas être libéré. Pour plus d’informations sur l’appel de la fonction, consultez [l' \_ attribut transmit As](the-transmit-as-attribute.md).

Dans l’exemple suivant, la liste à double liaison est libérée en parcourant la liste jusqu’à sa fin, puis en sauvegardant et en libérant chaque élément de la liste.


```C++
void __RPC_USER DOUBLE_LINK_TYPE_free_inst(
     DOUBLE_LINK_TYPE __RPC_FAR * pList)
{
    while (pList->pNext != NULL)  // go to end of the list
        pList = pList->pNext;

    pList = pList->pPrevious;
    while (pList != NULL) 
    {  
        // back through the list
        midl_user_free(pList->pNext);
        pList = pList->pPrevious;
    }
} 
```



 

 




