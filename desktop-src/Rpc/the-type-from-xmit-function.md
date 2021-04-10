---
title: Fonction type_from_xmit
description: Les stubs appellent le type \_ à partir de la \_ fonction de transmission pour convertir les données de son type transmis vers le type présenté à l’application.
ms.assetid: 679a2738-a166-4e73-bca7-950f979ed97a
keywords:
- type_from_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e594e8586522dd3697f5ae62c95851917741f73c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029653"
---
# <a name="the-type_from_xmit-function"></a><span data-ttu-id="5ea6c-104">Le type \_ de la fonction de transmission \_</span><span class="sxs-lookup"><span data-stu-id="5ea6c-104">The type\_from\_xmit Function</span></span>

<span data-ttu-id="5ea6c-105">Les stubs appellent **le \_ type \_ à partir de** la fonction de transmission pour convertir les données de son type transmis vers le type présenté à l’application.</span><span class="sxs-lookup"><span data-stu-id="5ea6c-105">The stubs call the **type\_from\_xmit** function to convert data from its transmitted type to the type that is presented to the application.</span></span> <span data-ttu-id="5ea6c-106">La fonction est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="5ea6c-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <type>_from_xmit ( 
    <xmit_type> __RPC_FAR *, 
    <type> __RPC_FAR *);
```

<span data-ttu-id="5ea6c-107">Le premier paramètre est un pointeur vers les données transmises.</span><span class="sxs-lookup"><span data-stu-id="5ea6c-107">The first parameter is a pointer to the transmitted data.</span></span> <span data-ttu-id="5ea6c-108">La fonction définit le deuxième paramètre pour qu’il pointe vers les données présentées.</span><span class="sxs-lookup"><span data-stu-id="5ea6c-108">The function sets the second parameter to point to the presented data.</span></span>

<span data-ttu-id="5ea6c-109">Le **type \_ de \_** la fonction de transmission doit gérer la mémoire pour le type présenté.</span><span class="sxs-lookup"><span data-stu-id="5ea6c-109">The **type\_from\_xmit** function must manage memory for the presented type.</span></span> <span data-ttu-id="5ea6c-110">La fonction doit allouer de la mémoire pour l’ensemble de la structure de données qui commence à l’adresse indiquée par le deuxième paramètre, à l’exception du paramètre lui-même (le stub alloue de la mémoire pour le nœud racine et le transmet à la fonction).</span><span class="sxs-lookup"><span data-stu-id="5ea6c-110">The function must allocate memory for the entire data structure that starts at the address indicated by the second parameter, except for the parameter itself (the stub allocates memory for the root node and passes it to the function).</span></span> <span data-ttu-id="5ea6c-111">La valeur du deuxième paramètre ne peut pas changer pendant l’appel.</span><span class="sxs-lookup"><span data-stu-id="5ea6c-111">The value of the second parameter cannot change during the call.</span></span> <span data-ttu-id="5ea6c-112">La fonction peut modifier le contenu à cette adresse.</span><span class="sxs-lookup"><span data-stu-id="5ea6c-112">The function can change the contents at that address.</span></span>

<span data-ttu-id="5ea6c-113">Dans cet exemple, le \_ type de lien double de la fonction \_ de transmission \_ \_ convertit le tableau de taille en une liste à double liaison.</span><span class="sxs-lookup"><span data-stu-id="5ea6c-113">In this example, the function DOUBLE\_LINK\_TYPE\_from\_xmit converts the sized array to a double-linked list.</span></span> <span data-ttu-id="5ea6c-114">La fonction conserve le pointeur valide jusqu’au début de la liste, libère la mémoire associée au reste de la liste, puis crée une nouvelle liste qui démarre au même pointeur.</span><span class="sxs-lookup"><span data-stu-id="5ea6c-114">The function retains the valid pointer to the beginning of the list, frees memory associated with the rest of the list, then creates a new list that starts at the same pointer.</span></span> <span data-ttu-id="5ea6c-115">La fonction utilise une fonction utilitaire, **InsertNewNode**, pour ajouter un nœud de liste à la fin de la liste et assigner les pointeurs *pNext* et *pPrevious* aux valeurs appropriées.</span><span class="sxs-lookup"><span data-stu-id="5ea6c-115">The function uses a utility function, **InsertNewNode**, to append a list node to the end of the list and to assign the *pNext* and *pPrevious* pointers to appropriate values.</span></span>


```C++
void __RPC_USER DOUBLE_LINK_TYPE_from_xmit(
     DOUBLE_XMIT_TYPE __RPC_FAR * pArray,
     DOUBLE_LINK_TYPE __RPC_FAR * pList)
{
    DOUBLE_LINK_TYPE *pCurrent;
    int i;
 
    if (pArray->sSize <= 0) 
    {  
        // error checking
        return;
    }
 
    if (pList == NULL) // if invalid, create the list head
        pList = InsertNewNode(pArray->asNumber[0], NULL);             
    else 
    {    
        DOUBLE_LINK_TYPE_free_inst(pList);  // free all other nodes
        pList->sNumber = pArray->asNumber[0];
        pList->pNext = NULL; 
    }
 
    pCurrent = pList; 
    for (i = 1; i < pArray->sSize; i++)  
        pCurrent = InsertNewNode(pArray->asNumber[i], pCurrent);
    
    return;
}
```



 

 




