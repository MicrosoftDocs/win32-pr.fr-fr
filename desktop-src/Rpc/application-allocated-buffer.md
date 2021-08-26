---
title: Mémoire tampon de Application-Allocated
description: L’attribut ACF \ Byte \_ Count \ indique aux stubs d’utiliser une mémoire tampon préallouée qui n’est pas allouée ou libérée par les routines de prise en charge du client.
ms.assetid: 1b370f74-394e-4e57-9749-83334be50f28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb87390637cba57cbdf4021a43f4ec98ea64c3828c67dfdb615ffcd62dc8c16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024179"
---
# <a name="application-allocated-buffer"></a>Mémoire tampon de Application-Allocated

Le \[ [**\_ nombre d’octets**](/windows/desktop/Midl/byte-count) de l’attribut ACF \] indique aux stubs d’utiliser une mémoire tampon préallouée qui n’est pas allouée ou libérée par les routines de prise en charge du client. L' \[ **attribut \_ nombre** \] d’octets est appliqué à un pointeur ou à un paramètre de tableau qui pointe vers la mémoire tampon. Elle nécessite un paramètre qui spécifie la taille de la mémoire tampon en octets.

La zone mémoire allouée par le client peut contenir des structures de données complexes avec plusieurs pointeurs. Étant donné que la zone mémoire est contiguë, l’application n’a pas besoin d’effectuer plusieurs appels pour libérer individuellement chaque pointeur et toute structure. Comme lorsque vous utilisez l' \[ attribut [**allocate (tous les \_ nœuds)**](/windows/desktop/Midl/allocate) \] , la zone de mémoire peut être allouée ou libérée à l’aide d’un appel à la routine d’allocation de mémoire ou à la routine libre. Toutefois, contrairement à l’utilisation de l' \[ attribut **allocate (tous les \_ nœuds)** \] , le paramètre buffer n’est pas géré par le stub client, mais par l’application cliente.

La mémoire tampon doit être un \[ [](/windows/desktop/Midl/out-idl) \] paramètre en sortie seule et la longueur de la mémoire tampon en octets doit être un \[ [](/windows/desktop/Midl/in) \] paramètre en uniquement. L' \[ [**attribut \_ nombre**](/windows/desktop/Midl/byte-count) \] d’octets ne peut être appliqué qu’aux types pointeur. L' \[ attribut ACF du **\_ nombre d’octets** \] est une extension Microsoft de l’IDL DCE et, par conséquent, n’est pas disponible si vous compilez à l’aide du commutateur [**/OSF**](/windows/desktop/Midl/-osf) MIDL.

Dans l’exemple suivant, le paramètre *pRoot* utilise le nombre d’octets :

``` syntax
/* function prototype in IDL file (fragment) */
void SortNames(
    [in] short cNames,
    [in, size_is(cNames)] STRINGTYPE pszArray[],
    [in] short cBytes,
    [out, ref] P_TREE_TYPE pRoot  /* tree with sorted data */
);
```

L' \[ [**attribut \_ nombre**](/windows/desktop/Midl/byte-count) \] d’octets apparaît dans le CCP en tant que :

``` syntax
/* ACF file (fragment) */
SortNames([byte_count(cBytes)] pRoot);
```

Le stub client généré à partir de ces fichiers IDL et ACF n’alloue pas ou ne libère pas la mémoire pour cette mémoire tampon. Le stub serveur alloue et libère la mémoire tampon dans un appel unique à l’aide du paramètre de taille fourni. Si les données sont trop volumineuses pour la taille de la mémoire tampon spécifiée, une exception est levée.

 

 