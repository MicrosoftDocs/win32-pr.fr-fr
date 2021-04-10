---
title: Fonction type_to_xmit
description: Les stubs appellent le type pour transmettre la \_ \_ fonction pour convertir le type présenté par l’application en type transmis.
ms.assetid: fb5b3760-d660-4e4e-b5c5-768e8e598e23
keywords:
- type_to_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd6a6b250d661fc19b0ee8fb68d21f171960e512
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940182"
---
# <a name="the-type_to_xmit-function"></a><span data-ttu-id="852bb-104">Type \_ vers la \_ fonction de transmission</span><span class="sxs-lookup"><span data-stu-id="852bb-104">The type\_to\_xmit Function</span></span>

<span data-ttu-id="852bb-105">Les stubs appellent le **type \_ pour \_** transmettre la fonction pour convertir le type présenté par l’application en type transmis.</span><span class="sxs-lookup"><span data-stu-id="852bb-105">The stubs call the **type\_to\_xmit** function to convert the type that is presented by the application into the transmitted type.</span></span> <span data-ttu-id="852bb-106">La fonction est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="852bb-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <type>_to_xmit ( 
     <type> __RPC_FAR *, <xmit_type> __RPC_FAR *     __RPC_FAR *);
```

<span data-ttu-id="852bb-107">Le premier paramètre est un pointeur vers les données d’application.</span><span class="sxs-lookup"><span data-stu-id="852bb-107">The first parameter is a pointer to the application data.</span></span> <span data-ttu-id="852bb-108">Le deuxième paramètre est défini par la fonction pour pointer vers les données transmises.</span><span class="sxs-lookup"><span data-stu-id="852bb-108">The second parameter is set by the function to point to the transmitted data.</span></span> <span data-ttu-id="852bb-109">La fonction doit allouer de la mémoire pour le type transmis.</span><span class="sxs-lookup"><span data-stu-id="852bb-109">The function must allocate memory for the transmitted type.</span></span>

<span data-ttu-id="852bb-110">Dans l’exemple suivant, le client appelle la procédure distante qui a un paramètre **\[ in, out \]** de type double \_ Link \_ type.</span><span class="sxs-lookup"><span data-stu-id="852bb-110">In the following example, the client calls the remote procedure that has an **\[in, out\]** parameter of type DOUBLE\_LINK\_TYPE.</span></span> <span data-ttu-id="852bb-111">Le stub client appelle le **type \_ pour \_** la transmission de la fonction, ici nommé double \_ \_ type \_ de lien vers transmission \_ , pour convertir des données de liste à double liaison en tableau de taille.</span><span class="sxs-lookup"><span data-stu-id="852bb-111">The client stub calls the **type\_to\_xmit** function, here named DOUBLE\_LINK\_TYPE\_to\_xmit, to convert double-linked list data into a sized array.</span></span>

<span data-ttu-id="852bb-112">La fonction détermine le nombre d’éléments dans la liste, alloue un tableau suffisamment grand pour contenir ces éléments, puis copie les éléments de la liste dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="852bb-112">The function determines the number of elements in the list, allocates an array large enough to hold those elements, then copies the list elements into the array.</span></span> <span data-ttu-id="852bb-113">Avant le retour de la fonction, le deuxième paramètre, *ppArray*, est défini pour pointer vers la structure de données qui vient d’être allouée.</span><span class="sxs-lookup"><span data-stu-id="852bb-113">Before the function returns, the second parameter, *ppArray*, is set to point to the newly allocated data structure.</span></span>


```C++
void __RPC_USER DOUBLE_LINK_TYPE_to_xmit ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList, 
    DOUBLE_XMIT_TYPE __RPC_FAR * __RPC_FAR * ppArray)
{
    short cCount = 0;
    DOUBLE_LINK_TYPE * pHead = pList;  // save pointer to start 
    DOUBLE_XMIT_TYPE * pArray;
 
    /* count the number of elements to allocate memory */
    for (; pList != NULL; pList = pList->pNext)
        cCount++;
 
    /* allocate the memory for the array */
    pArray = (DOUBLE_XMIT_TYPE *) MIDL_user_allocate 
         (sizeof(DOUBLE_XMIT_TYPE) + (cCount * sizeof(short)));
    pArray->sSize = cCount;
 
    /* copy the linked list contents into the array */
    cCount = 0;
    for (i = 0, pList = pHead; pList != NULL; pList = pList->pNext)
        pArray->asNumber[cCount++] = pList->sNumber;
 
    /* return the address of the pointer to the array */
    *ppArray = pArray;
}
```



 

 




