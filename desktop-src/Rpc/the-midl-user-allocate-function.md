---
title: Fonction midl_user_allocate
description: La \_ \_ fonction Allocate de l’utilisateur MIDL est une procédure qui doit être fournie par les développeurs d’applications RPC.
ms.assetid: 3def405c-da05-4cce-9dc4-499864a0de6e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12b2e3196de79992f5856b7117b25f05ad782d26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102005"
---
# <a name="the-midl_user_allocate-function"></a>La fonction d’allocation de l' \_ utilisateur MIDL \_

La **fonction \_ \_ allocate de l’utilisateur MIDL** est une procédure qui doit être fournie par les développeurs d’applications RPC. Elle alloue de la mémoire pour les stubs RPC et les routines de bibliothèque. La fonction d' **\_ \_ allocation de votre utilisateur MIDL** doit correspondre au prototype suivant :

``` syntax
void __RPC_FAR * __RPC_USER midl_user_allocate (size_t cBytes);
```

Le paramètre *cBytes* spécifie le nombre d’octets à allouer. Les applications clientes et les applications serveur doivent implémenter la fonction d' **\_ \_ allocation utilisateur MIDL** , sauf si vous compilez en mode de compatibilité OSF (/OSF). Les applications et les stubs générés appellent l' **\_ \_ allocation** directe ou indirecte de l’utilisateur MIDL pour gérer les objets alloués. Par exemple :

-   Les applications clientes et serveur appellent **MIDL \_ User \_ allocate** pour allouer de la mémoire pour l’application, par exemple lors de la création d’un nœud dans une arborescence ou une liste liée.
-   Le stub serveur appelle **l' \_ \_ allocation d’utilisateur MIDL** lors du démarshaling de données dans l’espace d’adressage du serveur.
-   Le stub client appelle **l' \_ \_ allocation d’utilisateur MIDL** lors du démarshaling de données à partir du serveur qui est référencé par un \[ pointeur de sortie \] . Notez que pour \[ les \] \[ pointeurs in, out \] et \[ unique \] , le stub client appelle **l' \_ \_ allocation de l’utilisateur MIDL** uniquement si la \[ \] valeur de pointeur unique était null en entrée et que les modifications apportées à une valeur non null au cours de l’appel. Si le \[ \] pointeur unique n’était pas null en entrée, le stub client écrit les données associées dans la mémoire existante.

Si **l' \_ \_ allocation d’utilisateur MIDL** échoue pour allouer de la mémoire, elle doit retourner un pointeur null.

La fonction d' **\_ \_ allocation de l’utilisateur MIDL** doit retourner un pointeur aligné sur 8 octets.

Par exemple, les exemples de programmes fournis avec le kit de développement logiciel (SDK) de la plateforme implémentent **MIDL \_ User \_ allocate** en termes de la fonction C [**malloc**](pointers-and-memory-allocation.md):


```C++
void __RPC_FAR * __RPC_USER midl_user_allocate(size_t cBytes)
{
    return((void __RPC_FAR *) malloc(cBytes));
}
```



> [!Note]  
> Si le package RpcSs est activé (par exemple, à la suite de l’utilisation de l' \[ attribut [**Enable \_ allocate**](/windows/desktop/Midl/enable-allocate) \] ), utilisez [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) pour allouer de la mémoire côté serveur. Pour plus d’informations sur \[ **Enable \_ allocate** \] , consultez [référence MIDL](/windows/desktop/Midl/midl-language-reference).

 

 

 