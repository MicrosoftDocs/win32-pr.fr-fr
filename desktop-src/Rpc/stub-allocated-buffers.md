---
title: Mémoires tampons de Stub-Allocated
description: Plutôt que de forcer un appel distinct pour chaque nœud de l’arborescence ou du graphique, vous pouvez demander aux stubs de calculer la taille des données et d’allouer et libérer de la mémoire en faisant un appel unique à l' \_ allocation utilisateur MIDL ou à l' \_ \_ utilisateur MIDL \_ gratuit.
ms.assetid: 9911649d-00e8-47d8-b512-7d9b185d1e09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956acf6452c1a4e7d04afcd1da263439436e3bad
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031584"
---
# <a name="stub-allocated-buffers"></a>Mémoires tampons de Stub-Allocated

Plutôt que de forcer un appel distinct pour chaque nœud de l’arborescence ou du graphique, vous pouvez demander aux stubs de calculer la taille des données et d’allouer et libérer de la mémoire en faisant un appel unique à l' [ \_ \_ allocation utilisateur MIDL](/windows/desktop/Midl/midl-user-allocate-1) ou à l' [ \_ utilisateur MIDL \_ gratuit](/windows/desktop/Midl/midl-user-free-1). L’attribut ACF **\[ allocate (tous les \_ nœuds) \]** indique aux stubs d’allouer ou de libérer tous les nœuds dans un appel unique aux fonctions de gestion de la mémoire fournies par l’utilisateur.

Par exemple, une application RPC peut utiliser la structure de données de l’arborescence binaire suivante :

``` syntax
/* IDL file fragment */
typedef struct _TREE_TYPE 
{
    short sNumber;
    struct _TREE_TYPE * pLeft;
    struct _TREE_TYPE * pRight;
} TREE_TYPE;

typedef TREE_TYPE * P_TREE_TYPE;
```

L’attribut ACF **\[ allocate (tous les \_ nœuds) \]** appliqué à ce type de données apparaît dans la Déclaration **typedef** dans le CCP en tant que :

``` syntax
/* ACF file fragment */
typedef [allocate(all_nodes)] P_TREE_TYPE;
```

L’attribut **\[ allocate \]** peut uniquement être appliqué aux types pointeur. L’attribut **\[ allocate \]** ACF est une extension Microsoft de l’IDL DCE et, par conséquent, n’est pas disponible si vous compilez avec le commutateur MIDL **/OSF** . Lorsque **\[ allocate (tous les \_ nœuds) \]** est appliqué à un type pointeur, les stubs générés par le compilateur MIDL traversent la structure de données spécifiée pour déterminer la taille d’allocation. Les stubs effectuent alors un appel unique pour allouer la quantité totale de mémoire requise par le graphique ou l’arborescence. Une application cliente peut libérer de la mémoire plus efficacement en effectuant un appel unique à l' **\_ utilisateur MIDL \_ gratuit**. Toutefois, les performances du stub serveur sont généralement augmentées lors de l’utilisation de la mémoire nœud par nœud, car les stubs de serveur peuvent souvent utiliser la mémoire privée qui ne nécessite aucune allocation.

Pour plus d’informations, consultez [allocation et désallocation de nœuds par nœud](node-by-node-allocation-and-deallocation.md).

 

 