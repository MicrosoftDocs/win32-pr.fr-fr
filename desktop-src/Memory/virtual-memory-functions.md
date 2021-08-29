---
description: Les fonctions de mémoire virtuelle permettent à un processus de manipuler ou de déterminer l’état des pages dans son espace d’adressage virtuel.
ms.assetid: 9488a854-1ef0-488f-b3d1-57c1acb82a88
title: Fonctions de mémoire virtuelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bee6839a00c573a3724cd22b3d304fef4276db29507c89802b42602120180bd5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105709"
---
# <a name="virtual-memory-functions"></a>Fonctions de mémoire virtuelle

Les fonctions de mémoire virtuelle permettent à un processus de manipuler ou de déterminer l’état des pages dans son espace d’adressage virtuel. Ils peuvent effectuer les opérations suivantes :

-   Réserver une plage de l’espace d’adressage virtuel d’un processus. La réservation de l’espace d’adressage n’alloue pas de stockage physique, mais empêche d’autres opérations d’allocation d’utiliser la plage spécifiée. Il n’affecte pas les espaces d’adressage virtuel d’autres processus. La réservation de pages empêche toute consommation inutile de stockage physique, tout en permettant à un processus de réserver une plage de son espace d’adressage dans laquelle une structure de données dynamique peut croître. Le processus peut allouer du stockage physique pour cet espace, si nécessaire.
-   Validez une plage de pages réservées dans l’espace d’adressage virtuel d’un processus afin que le stockage physique (en RAM ou sur disque) soit accessible uniquement au processus d’allocation.
-   Spécifiez lecture/écriture, lecture seule ou aucun accès pour une plage de pages validées. Cela diffère des fonctions d’allocation standard qui allouent toujours des pages avec un accès en lecture/écriture.
-   Libérez une plage de pages réservées, en rendant la plage d’adresses virtuelles disponible pour les opérations d’allocation suivantes par le processus appelant.
-   Annulez la validation d’une plage de pages validées, libérez son stockage physique et rendez-la disponible pour une allocation ultérieure par n’importe quel processus.
-   Verrouille une ou plusieurs pages de la mémoire allouée dans la mémoire physique (RAM) afin que le système ne puisse pas échanger les pages dans le fichier d’échange.
-   Obtenir des informations sur une plage de pages dans l’espace d’adressage virtuel du processus appelant ou un processus spécifié.
-   Modifiez la protection d’accès pour une plage spécifiée de pages validées dans l’espace d’adressage virtuel du processus appelant ou un processus spécifié.

Pour plus d’informations, voir les rubriques suivantes :

-   [Allocation de mémoire virtuelle](allocating-virtual-memory.md)
-   [Comparaison des méthodes d’allocation de mémoire](comparing-memory-allocation-methods.md)
-   [Libération de la mémoire virtuelle](freeing-virtual-memory.md)
-   [Utilisation des pages](working-with-pages.md)
-   [Fonctions de gestion de la mémoire](memory-management-functions.md)

 

 



