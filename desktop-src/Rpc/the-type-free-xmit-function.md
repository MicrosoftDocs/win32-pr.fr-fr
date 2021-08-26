---
title: Fonction type_free_xmit
description: Les stubs appellent la \_ \_ fonction de transmission libre de type pour libérer de la mémoire associée aux données transmises.
ms.assetid: f15ce25b-d36c-4ee5-b796-f0aba1997047
keywords:
- type_free_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4c192e30ec4f18d70d6e694e6097cb77ee7a2338230868730dc37c1c3207010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016579"
---
# <a name="the-type_free_xmit-function"></a>Fonction de transmission libre du type \_ \_

Les stubs appellent la fonction de transmission **libre de type \_ \_** pour libérer de la mémoire associée aux données transmises. Une fois que le [type \_ de \_ ](the-type-from-xmit-function.md) la fonction de transmission convertit les données transmises en son type présenté, la mémoire n’est plus nécessaire. La fonction est définie comme suit :

``` syntax
void __RPC_USER <type>_free_xmit(<xmit_type> __RPC_FAR *);
```

Le paramètre est un pointeur vers la mémoire qui contient le type transmis.

Dans cet exemple, la mémoire contient un tableau qui se trouve dans une structure unique. La transmission libre du type de lien DOUBLE de la fonction \_ \_ \_ \_ utilise la fonction utilisateur MIDL de la fonction fournie par l’utilisateur \_ \_ libre pour libérer la mémoire :

``` syntax
void __RPC_USER DOUBLE_LINK_TYPE_free_xmit( 
     DOUBLE_XMIT_TYPE __RPC_FAR * pArray)
{
     midl_user_free(pArray);
}
```

 

 




