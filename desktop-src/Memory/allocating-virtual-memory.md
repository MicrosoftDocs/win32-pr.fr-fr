---
description: Les fonctions de mémoire virtuelle manipulent les pages de la mémoire. Les fonctions utilisent la taille d’une page sur l’ordinateur actuel pour arrondir les tailles et les adresses spécifiées.
ms.assetid: 509cd529-ff79-4b07-9e09-3c5ae65f6cba
title: Allocation de mémoire virtuelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f42b4f7eb9d5de3c8c5e9339c9e5931a89e371
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319125"
---
# <a name="allocating-virtual-memory"></a>Allocation de mémoire virtuelle

Les fonctions de mémoire virtuelle manipulent les pages de la mémoire. Les fonctions utilisent la taille d’une page sur l’ordinateur actuel pour arrondir les tailles et les adresses spécifiées.

La fonction [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) effectue l’une des opérations suivantes :

-   Réserve une ou plusieurs pages gratuites.
-   Valide une ou plusieurs pages réservées.
-   Réserve et valide une ou plusieurs pages gratuites.

Vous pouvez spécifier l’adresse de départ des pages réservées ou validées, ou vous pouvez autoriser le système à déterminer l’adresse. La fonction arrondit l’adresse spécifiée à la limite de page appropriée. Les pages réservées ne sont pas accessibles, mais les pages validées peuvent être allouées avec l’accès à la **page \_ ReadWrite**, **page \_ ReadOnly** ou **page \_ NoAccess** . Lorsque les pages sont validées, les frais de mémoire sont alloués à partir de la taille globale de la RAM et des fichiers d’échange sur le disque, mais chaque page est initialisée et chargée dans la mémoire physique uniquement lors de la première tentative de lecture ou d’écriture dans cette page. Vous pouvez utiliser des références de pointeur normales pour accéder à la mémoire validée par la fonction [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) .

 

 
