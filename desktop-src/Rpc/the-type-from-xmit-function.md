---
title: Fonction type_from_xmit
description: Les stubs appellent le type \_ à partir de la \_ fonction de transmission pour convertir les données de son type transmis vers le type présenté à l’application.
ms.assetid: 679a2738-a166-4e73-bca7-950f979ed97a
keywords:
- type_from_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e594e8586522dd3697f5ae62c95851917741f73c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218228"
---
# <a name="the-type_from_xmit-function"></a>Le type \_ de la fonction de transmission \_

Les stubs appellent **le \_ type \_ à partir de** la fonction de transmission pour convertir les données de son type transmis vers le type présenté à l’application. La fonction est définie comme suit :

``` syntax
void __RPC_USER <type>_from_xmit ( 
    <xmit_type> __RPC_FAR *, 
    <type> __RPC_FAR *);
```

Le premier paramètre est un pointeur vers les données transmises. La fonction définit le deuxième paramètre pour qu’il pointe vers les données présentées.

Le **type \_ de \_** la fonction de transmission doit gérer la mémoire pour le type présenté. La fonction doit allouer de la mémoire pour l’ensemble de la structure de données qui commence à l’adresse indiquée par le deuxième paramètre, à l’exception du paramètre lui-même (le stub alloue de la mémoire pour le nœud racine et le transmet à la fonction). La valeur du deuxième paramètre ne peut pas changer pendant l’appel. La fonction peut modifier le contenu à cette adresse.

Dans cet exemple, le \_ type de lien double de la fonction \_ de transmission \_ \_ convertit le tableau de taille en une liste à double liaison. La fonction conserve le pointeur valide jusqu’au début de la liste, libère la mémoire associée au reste de la liste, puis crée une nouvelle liste qui démarre au même pointeur. La fonction utilise une fonction utilitaire, **InsertNewNode**, pour ajouter un nœud de liste à la fin de la liste et assigner les pointeurs *pNext* et *pPrevious* aux valeurs appropriées.


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



 

 




