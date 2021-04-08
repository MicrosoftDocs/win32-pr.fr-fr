---
title: Fonction type_free_inst
description: Les stubs appellent la \_ \_ fonction Free inst pour libérer de la mémoire associée au type présenté.
ms.assetid: 4ee2e6a6-b506-445f-adaf-3705228defa7
keywords:
- type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3754106cf8e0cc6e338f91d6c233181aa33038eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840049"
---
# <a name="the-type_free_inst-function"></a><span data-ttu-id="a5a58-104">Type \_ Free \_ inst, fonction</span><span class="sxs-lookup"><span data-stu-id="a5a58-104">The type\_free\_inst Function</span></span>

<span data-ttu-id="a5a58-105">Les stubs appellent la fonction **\_ Free \_ inst** pour libérer de la mémoire associée au type présenté.</span><span class="sxs-lookup"><span data-stu-id="a5a58-105">The stubs call the **type\_free\_inst** function to free memory associated with the presented type.</span></span> <span data-ttu-id="a5a58-106">La fonction est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="a5a58-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <type>_free_inst(<type> __RPC_FAR *)
```

<span data-ttu-id="a5a58-107">Le paramètre pointe vers l’instance de type présentée.</span><span class="sxs-lookup"><span data-stu-id="a5a58-107">The parameter points to the presented type instance.</span></span> <span data-ttu-id="a5a58-108">Cet objet ne doit pas être libéré.</span><span class="sxs-lookup"><span data-stu-id="a5a58-108">This object should not be freed.</span></span> <span data-ttu-id="a5a58-109">Pour plus d’informations sur l’appel de la fonction, consultez [l' \_ attribut transmit As](the-transmit-as-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="a5a58-109">For a discussion on when to call the function, see [The transmit\_as Attribute](the-transmit-as-attribute.md).</span></span>

<span data-ttu-id="a5a58-110">Dans l’exemple suivant, la liste à double liaison est libérée en parcourant la liste jusqu’à sa fin, puis en sauvegardant et en libérant chaque élément de la liste.</span><span class="sxs-lookup"><span data-stu-id="a5a58-110">In the following example, the double-linked list is freed by walking the list to its end, then backing up and freeing each element of the list.</span></span>


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



 

 




