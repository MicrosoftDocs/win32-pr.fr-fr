---
description: Chaque processus a un segment de mémoire par défaut fourni par le système. Les applications qui effectuent des allocations fréquentes à partir du tas peuvent améliorer les performances à l’aide de tas privés.
ms.assetid: cfb683fa-4f46-48b5-9a28-f4625a9cb8cd
title: Fonctions de tas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e591c1e349ed6806cbebe00a178a99e63bb412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864861"
---
# <a name="heap-functions"></a>Fonctions de tas

Chaque processus a un segment de mémoire par défaut fourni par le système. Les applications qui effectuent des allocations fréquentes à partir du tas peuvent améliorer les performances à l’aide de tas privés.

Un tas privé est un bloc d’une ou plusieurs pages dans l’espace d’adressage du processus appelant. Après avoir créé le tas privé, le processus utilise des fonctions telles que [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) et [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) pour gérer la mémoire dans ce tas.

Les fonctions de tas peuvent également être utilisées pour gérer la mémoire dans le tas par défaut du processus, à l’aide du handle retourné par la fonction [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) . Les nouvelles applications doivent utiliser les fonctions de tas au lieu des [fonctions globales et locales](global-and-local-functions.md) à cet effet.

Il n’existe aucune différence entre la mémoire allouée à partir d’un tas privé et celle allouée à l’aide des autres fonctions d’allocation de mémoire. Pour obtenir la liste complète des fonctions, consultez le tableau dans [fonctions de gestion](memory-management-functions.md)de la mémoire.

> [!Note]  
> Un thread doit appeler des fonctions de tas uniquement pour le tas par défaut du processus et les tas privés que le thread crée et gère, à l’aide de handles retournés par la fonction [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) ou [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) .

 

La fonction [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) crée un objet de tas privé à partir duquel le processus appelant peut allouer des blocs de mémoire à l’aide de la fonction [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) . **HeapCreate** spécifie à la fois une taille initiale et une taille maximale pour le tas. La taille initiale détermine le nombre de pages validées, en lecture/écriture initialement allouées pour le segment de mémoire. La taille maximale détermine le nombre total de pages réservées. Ces pages créent un bloc contigu dans l’espace d’adressage virtuel d’un processus dans lequel le tas peut croître. Les pages supplémentaires sont automatiquement validées à partir de cet espace réservé si les demandes par **HeapAlloc** dépassent la taille actuelle des pages validées, en supposant que le stockage physique correspondant est disponible. Une fois les pages validées, elles ne sont pas dévalidées tant que le processus n’est pas terminé ou que le segment de mémoire n’a pas été détruit en appelant la fonction [**HeapDestroy**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy) .

La mémoire d’un objet de tas privé est accessible uniquement au processus qui l’a créé. Si une bibliothèque de liens dynamiques (DLL) crée un tas privé, elle le fait dans l’espace d’adressage du processus qui a appelé la DLL. Il est uniquement accessible à ce processus.

La fonction [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) alloue un nombre spécifié d’octets à partir d’un tas privé et retourne un pointeur vers le bloc alloué. Ce pointeur peut être utilisé dans les fonctions [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree), [**HeapReAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heaprealloc), [**HEAPSIZE**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize)et [**HeapValidate**](/windows/desktop/api/HeapApi/nf-heapapi-heapvalidate) .

La mémoire allouée par [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) n’est pas déplaçable. L’adresse retournée par **HeapAlloc** est valide jusqu’à ce que le bloc de mémoire soit libéré ou réalloué ; le bloc de mémoire n’a pas besoin d’être verrouillé.

Étant donné que le système ne peut pas compacter un tas privé, il peut être fragmenté. Les applications qui allouent de grandes quantités de mémoire dans différentes tailles d’allocation peuvent utiliser le [tas de faible fragmentation](low-fragmentation-heap.md) pour réduire la fragmentation du tas.

Une utilisation possible pour les fonctions de tas consiste à créer un tas privé lorsqu’un processus démarre, en spécifiant une taille initiale suffisante pour répondre aux besoins en mémoire du processus. Si l’appel à la fonction [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) échoue, le processus peut se terminer ou informer l’utilisateur de l’insuffisance de mémoire. Toutefois, s’il y parvient, le processus est assuré de disposer de la mémoire dont il a besoin.

La mémoire demandée par [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) peut être ou ne pas être contiguë. La mémoire allouée dans un segment de mémoire par [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) est contiguë. Vous ne devez pas écrire ou lire à partir de la mémoire dans un tas à l’exception de celui alloué par **HeapAlloc**, et vous ne devez pas non plus supposer une relation entre deux zones de mémoire allouée par **HeapAlloc**.

Vous ne devez pas faire référence à la mémoire qui a été libérée par [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree). Une fois la mémoire libérée, toutes les informations qui y sont susceptibles de l’être sont infinies. Si vous avez besoin d’informations, ne libérez pas de mémoire contenant les informations. Les appels de fonction qui retournent des informations sur la mémoire (par exemple, [**HEAPSIZE**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize)) ne peuvent pas être utilisés avec la mémoire libérée, car ils peuvent retourner des données factices.

La fonction [**HeapDestroy**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy) détruit un objet de tas privé. Il annule la validation et libère toutes les pages de l’objet segment de mémoire, et invalide le descripteur du tas.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comparaison des méthodes d’allocation de mémoire](comparing-memory-allocation-methods.md)
</dt> </dl>

 

 



