---
description: La plage de travail d’un processus correspond à l’ensemble de pages dans l’espace d’adressage virtuel du processus qui résident actuellement dans la mémoire physique.
ms.assetid: ff05276a-1d40-4844-b649-10e32e3f1937
title: Plage de travail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0d5b773098769d5358956099e2c2ed994677e33138ff05ae5a14d1115f09e6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896309"
---
# <a name="working-set"></a>Plage de travail

La plage de travail d’un processus correspond à l’ensemble de pages dans l’espace d’adressage virtuel du processus qui résident actuellement dans la mémoire physique. La plage de travail contient uniquement des allocations de mémoire paginables ; les allocations de mémoire non paginables telles que AWE ( [Address Windowing Extensions](address-windowing-extensions.md) ) ou les [allocations de pages de grande taille](large-page-support.md) ne sont pas incluses dans la plage de travail.

Lorsqu’un processus fait référence à une mémoire paginable qui ne se trouve pas actuellement dans sa plage de travail, une *erreur de page* se produit. Le gestionnaire d’erreurs de page système tente de résoudre l’erreur de page et, si elle est réussie, la page est ajoutée à la plage de travail. (L’accès à AWE ou aux allocations de pages volumineuses ne provoque jamais d’erreur de page, car ces allocations ne sont pas paginables.)

Une *erreur de page matérielle* doit être résolue en lisant le contenu de la page à partir du *magasin* de stockage de la page, qui est le fichier de pagination système ou un fichier mappé en mémoire créé par le processus. Un *défaut de page conditionnelle* peut être résolu sans accéder au magasin de stockage. Une erreur de page conditionnelle se produit dans les cas suivants :

-   La page se trouve dans la plage de travail d’un autre processus. elle est donc déjà résidente en mémoire.
-   La page est en cours de transition, car elle a été supprimée des jeux de travail de tous les processus qui utilisaient la page et n’a pas encore été réaffectée, ou elle est déjà en train de se produire en raison d’une opération de prérécupération du gestionnaire de mémoire.
-   Un processus fait référence à une page virtuelle allouée pour la première fois (parfois appelée une *erreur de demande nulle*).

Les pages peuvent être supprimées d’une plage de travail de processus suite aux actions suivantes :

-   Le processus réduit ou vide la plage de travail en appelant la fonction [**SetProcessWorkingSetSize**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsize), [**SetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsizeex) ou [**EmptyWorkingSet**](/windows/win32/api/psapi/nf-psapi-emptyworkingset) .
-   Le processus appelle la fonction [**VirtualUnlock**](/windows/win32/api/memoryapi/nf-memoryapi-virtualunlock) sur une plage mémoire qui n’est pas verrouillée.
-   Le processus annule le mappage d’une vue mappée d’un fichier à l’aide de la fonction [**UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) .
-   Le gestionnaire de mémoire supprime les pages de la plage de travail pour créer plus de mémoire disponible.
-   Le gestionnaire de mémoire doit supprimer une page de la plage de travail pour faire de la place pour une nouvelle page (par exemple, parce que la plage de travail est à sa taille maximale).

Si plusieurs processus partagent une page, la suppression de la page de la plage de travail d’un processus n’affecte pas les autres processus. Une fois qu’une page est supprimée des jeux de travail de tous les processus qui l’utilisaient, la page devient une *page de transition*. Les pages de transition restent mises en cache dans la mémoire RAM jusqu’à ce que la page soit à nouveau référencée par un processus ou réaffectée (par exemple, remplie de zéros et donnée à un autre processus). Si une page de transition a été modifiée depuis sa dernière écriture sur le disque (autrement dit, si la page est « modifiée »), la page doit être écrite dans le magasin de stockage avant de pouvoir être réaffectée. Le système peut commencer à écrire des pages de transition erronées dans le magasin de stockage dès que ces pages sont disponibles.

Chaque processus a une taille de jeu de travail minimale et maximale qui affecte le comportement de pagination de la mémoire virtuelle du processus. Pour obtenir la taille actuelle de la plage de travail d’un processus spécifié, utilisez la fonction [**GetProcessMemoryInfo**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) . Pour obtenir ou modifier les tailles de plage de travail minimale et maximale, utilisez les fonctions [**GetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-getprocessworkingsetsizeex) et [**SetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsizeex) .

L’interface de programmation d’applications (PSAPI) process Status fournit un certain nombre de fonctions qui retournent des informations détaillées sur la plage de travail d’un processus. Pour plus d’informations, consultez [Working Set information](../psapi/working-set-information.md).

 

 
