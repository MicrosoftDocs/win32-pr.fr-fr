---
title: ApiBuffer, fonctions
description: Les fonctions de ApiBuffer de gestion de réseau sont utilisées pour gérer l’allocation de mémoire utilisée par une application avec des fonctions de gestion de réseau.
ms.assetid: bf2fe8aa-dda6-4f6b-9c52-d7a96b96da18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b0778c216860fe16a673e1bdcc2ac470cbb52a128f0e08d4d32d98df929bc7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912478"
---
# <a name="apibuffer-functions"></a>ApiBuffer, fonctions

Les fonctions de ApiBuffer de gestion de réseau sont utilisées pour gérer l’allocation de mémoire utilisée par une application avec des fonctions de gestion de réseau. Toutefois, en général, pour toute autre mémoire utilisée par une application, vous devez utiliser les [fonctions de gestion](/windows/desktop/Memory/memory-management-functions) de la mémoire au lieu de ces fonctions ApiBuffer.

Les fonctions ApiBuffer sont répertoriées ci-dessous.



| Fonction                                                 | Description                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**NetApiBufferAllocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferallocate)     | Alloue de la mémoire à partir du tas. Appelez cette fonction lorsque vous avez besoin d’une compatibilité avec la fonction **NetApiBufferFree** . |
| [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree)             | Libère de la mémoire allouée par la fonction **NetApiBufferAllocate** et d’autres fonctions de gestion de réseau.                   |
| [**NetApiBufferReallocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferreallocate) | Modifie la taille d’une mémoire tampon allouée par un appel à la fonction **NetApiBufferAllocate** .                                |
| [**NetApiBufferSize**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibuffersize)             | Retourne la taille, en octets, d’une mémoire tampon allouée par un appel à la fonction **NetApiBufferAllocate** .                     |



 

Pour les fonctions accessibles à distance qui retournent des informations à l’appelant, la bibliothèque Runtime RPC alloue la mémoire tampon contenant les informations de retour. Lorsque l’appelant a fini de traiter les informations, il doit appeler la fonction [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) pour libérer la mémoire tampon allouée.

 

 