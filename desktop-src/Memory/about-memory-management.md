---
description: chaque processus sur un Windows Microsoft 32 bits possède son propre espace d’adressage virtuel qui permet d’adresser jusqu’à 4 gigaoctets de mémoire.
ms.assetid: f259f3cb-81c0-4b5f-b6fa-9681a278019a
title: À propos de la gestion de la mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b2cc91b2a907fa5f9db24f42393be51bb8795200357eff0b612f8241219361
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869969"
---
# <a name="about-memory-management"></a>À propos de la gestion de la mémoire

chaque processus sur un Windows Microsoft 32 bits possède son propre espace d’adressage virtuel qui permet d’adresser jusqu’à 4 gigaoctets de mémoire. chaque processus sur l’Windows 64 bits a un espace d’adressage virtuel de 8 téraoctets. Tous les threads d’un processus peuvent accéder à son espace d’adressage virtuel. Toutefois, les threads ne peuvent pas accéder à la mémoire qui appartient à un autre processus, ce qui empêche la corruption d’un processus par un autre processus.

Pour plus d’informations sur l’espace d’adressage virtuel et les fonctions de gestion de la mémoire, consultez les rubriques suivantes.

-   [Espace d’adressage virtuel](virtual-address-space.md)
-   [Pools de mémoire](memory-pools.md)
-   [Informations sur les performances de la mémoire](memory-performance-information.md)
-   [Fonctions de mémoire virtuelle](virtual-memory-functions.md)
-   [Fonctions de tas](heap-functions.md)
-   [Mappage de fichiers](file-mapping.md)
-   [Prise en charge de mémoire importante](large-memory-support.md)
-   [Fonctions globales et locales](global-and-local-functions.md)
-   [Fonctions de la bibliothèque C standard](standard-c-library-functions.md)
-   [Comparaison des méthodes d’allocation de mémoire](comparing-memory-allocation-methods.md)

 

 



