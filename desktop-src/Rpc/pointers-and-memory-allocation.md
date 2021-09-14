---
title: Pointeurs et allocation de mémoire
description: La possibilité de modifier la mémoire par le biais de pointeurs requiert souvent que le serveur et le client allouent suffisamment de mémoire pour les éléments du tableau.
ms.assetid: 8a49582a-9ae4-4f26-a172-bc8fe2aab65a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdd4c51207de093dfe2d32ec0c275aa7a05a317
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096494"
---
# <a name="pointers-and-memory-allocation"></a>Pointeurs et allocation de mémoire

La possibilité de modifier la mémoire par le biais de pointeurs requiert souvent que le serveur et le client allouent suffisamment de mémoire pour les éléments du tableau.

Quand un stub doit allouer ou libérer de la mémoire, il appelle des fonctions de la bibliothèque Runtime qui, à leur tour, appellent les fonctions [**MIDL \_ User \_ allocate**](/windows/desktop/Midl/midl-user-allocate-1) et [**MIDL \_ User \_ Free**](/windows/desktop/Midl/midl-user-free-1). Ces fonctions ne sont pas incluses dans la bibliothèque Runtime. Vous devez écrire vos propres versions de ces fonctions et les lier à votre application. De cette façon, vous pouvez décider comment gérer la mémoire. Lors de la compilation de votre fichier IDL en mode compatibilité OSF (**/OSF**), il n’est pas nécessaire d’implémenter ces fonctions. Vous devez écrire ces fonctions dans les prototypes suivants :

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate(size_t len)

void __RPC_API midl_user_free(void __RPC_FAR * ptr)
```

Par exemple, les versions de ces fonctions pour une application peuvent simplement appeler des fonctions de bibliothèque standard :


```C++
void __RPC_FAR * __RPC_API midl_user_allocate(size_t len)
{
    return(malloc(len));
}

void __RPC_API midl_user_free(void __RPC_FAR * ptr)
{
    free(ptr);
}
```



 

 