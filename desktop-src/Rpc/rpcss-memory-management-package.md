---
title: Package de gestion de mémoire RpcSs
description: La paire d’allocateur/annulateur par défaut utilisée par les stubs et le moment de l’exécution lors de l’allocation de mémoire pour le compte de l’application est MIDL User aslocate \_ \_ /MIDL \_ User \_ Free.
ms.assetid: 9477e677-59cb-45d5-b485-ab0171ac17ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93648b56ed47eb98a83b27a39b606fa2a51de9bf5791ad1b732e7169ef5dfa63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018179"
---
# <a name="rpcss-memory-management-package"></a>Package de gestion de mémoire RpcSs

La paire d’allocateur/annulateur par défaut utilisée par les stubs et le moment de l’exécution lors de l’allocation de mémoire pour le compte de l’application est **MIDL utilisateur \_ \_ allouez** un / **\_ utilisateur MIDL \_ gratuit** à l’utilisateur. Toutefois, vous pouvez choisir le package RpcSs au lieu de la valeur par défaut en utilisant l’attribut ACF **\[ Enable \_ allocate \]**. Le package RpcSs se compose de fonctions RPC qui commencent par le préfixe **RPCSS** ou **RpcSm**. le package RpcSs n’est pas recommandé pour les applications Windows.

> [!Note]  
> Le package de gestion de la mémoire RPCSS est obsolète. Il est recommandé que [**l' \_ \_ allocation d’utilisateur MIDL**](/windows/desktop/Midl/midl-user-allocate-1) et l' [**\_ utilisateur MIDL \_ gratuit**](/windows/desktop/Midl/midl-user-free-1) soient utilisés à la place.

 

En mode **/OSF** , le package RPCSS est activé automatiquement pour les stubs générés par MIDL lorsque des pointeurs complets sont utilisés, lorsque les arguments nécessitent une allocation de mémoire ou à la suite de l’utilisation de l’attribut **\[ Enable \_ allocate \]** . Dans le mode par défaut (Microsoft étendu), le package RpcSs est activé uniquement lorsque l’attribut **\[ activer l' \_ allocation \]** est utilisé. L’attribut **\[ Enable \_ allocate \]** active l’environnement RPCSS par les stubs côté serveur. Le côté client est averti de la possibilité que le package RpcSs soit activé. En mode **/OSF** , le côté client n’est pas affecté.

Lorsque le package RpcSs est activé, l’allocation de mémoire côté serveur s’effectue à l’aide de la paire annulateur et de la paire de gestion de mémoire RpcSs privée. Vous pouvez allouer de la mémoire à l’aide du même mécanisme en appelant [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) (ou [**RpcSsAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssallocate)). Lors du retour du stub serveur, toute la mémoire allouée par le package RpcSs est automatiquement libérée. L’exemple suivant montre comment activer le package RpcSs :

``` syntax
/* ACF file fragment */

[ 
    implicit_handle(handle_t GlobalHandle),
    enable_allocate
]
interface iface
{
}

/*Server management routine fragment. Replaces p=midl_user_allocate(size); */

    p=RpcSsAllocate(size);                /*raises exception */
    p=RpcSmAllocate(size, &status);       /*returns error code */
```

Votre application peut libérer explicitement la mémoire en appelant la fonction [**RpcSsFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssfree) ou [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) . Notez que ces fonctions ne libèrent pas réellement de la mémoire. Ils le marquent pour suppression. La bibliothèque RPC libère la mémoire lorsque votre programme appelle [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate) ou [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate).

Vous pouvez également activer l’environnement de gestion de la mémoire de votre application en appelant la routine [**RpcSmEnableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmenableallocate) (et vous pouvez la désactiver en appelant la routine [**RpcSmDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmdisableallocate) ). Une fois activée, le code d’application peut allouer et libérer de la mémoire en appelant des fonctions à partir du package RpcSs.

 

 