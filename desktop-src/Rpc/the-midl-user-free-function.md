---
title: Fonction midl_user_free
description: La \_ fonction gratuite de l’utilisateur MIDL \_ doit être fournie par les développeurs RPC.
ms.assetid: 5e940e93-bdd4-48cc-b84e-654637699719
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd6ca52635da5bedb60fdc7f94165ad9c888c030d5fe3340c53dfc970a90ff49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080819"
---
# <a name="the-midl_user_free-function"></a>Fonction d' \_ utilisateur \_ gratuit MIDL

La **fonction \_ \_ gratuite de l’utilisateur MIDL** doit être fournie par les développeurs RPC. Elle alloue de la mémoire pour les stubs RPC et les routines de bibliothèque. Votre fonction d' **\_ utilisateur \_ gratuit MIDL** doit correspondre au prototype suivant :

``` syntax
void __RPC_USER midl_user_free(void * pBuffer);
```

Le paramètre *pbuffer* spécifie un pointeur vers la mémoire qui doit être libérée. L’application cliente et l’application serveur doivent implémenter la fonction **\_ utilisateur \_ MIDL MIDL** , sauf si vous compilez en mode de compatibilité OSF ([**/OSF**](/windows/desktop/Midl/-osf)). La **fonction \_ \_ gratuite de l’utilisateur MIDL** doit pouvoir libérer tout le stockage alloué par l’allocation de l' [**\_ utilisateur \_ MIDL**](the-midl-user-allocate-function.md).

Les applications et les stubs appellent **MIDL \_ \_ sans utilisateur** lors du traitement des objets alloués :

-   L’application serveur doit appeler **l' \_ utilisateur MIDL \_ gratuit** pour libérer de la mémoire allouée par l’application, par exemple lors de la suppression d’un nœud de données alloué dynamiquement.
-   Le stub serveur appelle **l' \_ utilisateur MIDL \_ gratuit** pour libérer de la mémoire sur le serveur après avoir marshalé tous les \[ \] arguments out, les arguments out, les \[ \] \[ \] arguments out et la valeur de retour de la fonction.

par exemple, l’exemple de programme RPC Windows qui affiche « Hello, world » implémente l' **\_ utilisateur midl \_ gratuit** en termes de fonction C free :


```C++
void __RPC_USER midl_user_free(void __RPC_FAR * p)
{
    free(p);
}
```



> [!Note]  
> Si le package RpcSs est activé (par exemple, à la suite de l’utilisation de l' \[ attribut [**Enable \_ allocate**](/windows/desktop/Midl/enable-allocate) \] ), votre programme serveur doit utiliser [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) pour libérer de la mémoire. Pour plus d’informations, consultez package de gestion de la [mémoire RPCSS](rpcss-memory-management-package.md).

 

 

 