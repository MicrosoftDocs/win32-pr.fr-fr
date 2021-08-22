---
title: Informations sur l’utilisation de la mémoire du processus
description: La fonction GetProcessMemoryInfo prend un handle de processus comme entrée et remplit une structure de compteurs de mémoire de processus \_ \_ avec des informations sur les statistiques de mémoire pour le processus.
ms.assetid: 683c899e-a7e8-4440-8f13-2a713c1618bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac85a62853cf95dcf42380c76b914f23045152b32499870182a47ee2449e8ed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094701"
---
# <a name="process-memory-usage-information"></a>Informations sur l’utilisation de la mémoire du processus

La fonction [**GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) prend un handle de processus comme entrée et remplit une structure de [**\_ \_ compteurs de mémoire de processus**](/windows/desktop/api/Psapi/ns-psapi-process_memory_counters) avec des informations sur les statistiques de mémoire pour le processus. Le membre **CB** reçoit la taille de la structure. Le membre **PageFaultCount** reçoit le nombre de défauts de page. Les membres restants reçoivent l’utilisation actuelle et maximale de la mémoire dans les catégories suivantes :

-   Plage de travail
-   pool paginé
-   pool non paginé
-   fichier

La *plage de travail* correspond à la quantité de mémoire physiquement mappée au contexte de processus à un moment donné. La mémoire de la *réserve paginée* est la mémoire système qui peut être transférée vers le fichier d’échange sur le disque (paginée) lorsqu’elle n’est pas utilisée. La mémoire dans la *réserve non paginée* est une mémoire système qui ne peut pas être paginée sur le disque tant que les objets correspondants sont alloués. L' *utilisation du fichier d’échange représente* la quantité de mémoire réservée pour le processus dans le fichier de pagination système. Lorsque l’utilisation de la mémoire est trop élevée, les pages du gestionnaire de mémoire virtuelle ont sélectionné la mémoire sur le disque. Quand un thread a besoin d’une page qui n’est pas dans la mémoire, le gestionnaire de mémoire le recharge à partir du fichier d’échange.

 

 




