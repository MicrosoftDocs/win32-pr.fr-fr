---
description: L’espace d’adressage virtuel d’un processus correspond à l’ensemble des adresses mémoire virtuelles qu’il peut utiliser. L’espace d’adressage de chaque processus est privé et n’est pas accessible par d’autres processus, sauf s’il est partagé.
ms.assetid: 747f9f53-a595-4f4b-8b81-3123d59edb2f
title: Espace d’adressage virtuel (gestion de la mémoire)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6584d0404799e6b0e5ab343c7d8b39d7f8d741a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094009"
---
# <a name="virtual-address-space-memory-management"></a>Espace d’adressage virtuel (gestion de la mémoire)

L’espace d’adressage virtuel d’un processus correspond à l’ensemble des adresses mémoire virtuelles qu’il peut utiliser. L’espace d’adressage de chaque processus est privé et n’est pas accessible par d’autres processus, sauf s’il est partagé.

Une adresse virtuelle ne représente pas l’emplacement physique réel d’un objet en mémoire ; au lieu de cela, le système gère une *table de pages* pour chaque processus, qui est une structure de données interne utilisée pour convertir des adresses virtuelles en adresses physiques correspondantes. Chaque fois qu’un thread fait référence à une adresse, le système convertit l’adresse virtuelle en adresse physique.

l’espace d’adressage virtuel pour la Windows 32 bits est de 4 gigaoctets (go) et est divisé en deux partitions : une pour une utilisation par le processus et l’autre réservée pour une utilisation par le système. pour plus d’informations sur l’espace d’adressage virtuel dans le Windows 64 bits, consultez [espace d’adressage virtuel dans 64 bits Windows](../winprog64/virtual-address-space.md).

Pour plus d’informations sur la mémoire virtuelle, consultez les rubriques suivantes :

-   [espace d’adressage virtuel et Stockage physique](virtual-address-space-and-physical-storage.md)
-   [Plage de travail](working-set.md)
-   [État de la page](page-state.md)
-   [Portée de la mémoire allouée](scope-of-allocated-memory.md)
-   [Prévention de l’exécution des données](data-execution-prevention.md)
-   [Protection de la mémoire](memory-protection.md)
-   [limites de mémoire pour les versions de Windows](memory-limits-for-windows-releases.md)

## <a name="default-virtual-address-space-for-32-bit-windows"></a>Espace d’adressage virtuel par défaut pour l’Windows 32 bits

Le tableau suivant indique la plage de mémoire par défaut pour chaque partition.



| Plage mémoire                             | Usage                |
|------------------------------------------|----------------------|
| 2 Go bas (0x00000000 à 0x7FFFFFFF)  | Utilisé par le processus. |
| 2 Go de poids fort (0x80000000 à 0xFFFFFFFF) | Utilisé par le système.  |



 

## <a name="virtual-address-space-for-32-bit-windows-with-4gt"></a>espace d’adressage virtuel pour l’Windows 32 bits avec 4gt

Si le [réglage à 4 gigaoctets](4-gigabyte-tuning.md) (4GT) est activé, la plage de mémoire pour chaque partition est la suivante.



| Plage mémoire                             | Usage                |
|------------------------------------------|----------------------|
| 3 Go bas (0x00000000 à 0xBFFFFFFF)  | Utilisé par le processus. |
| Haute de 1 Go (0xC0000000 à 0xFFFFFFFF) | Utilisé par le système.  |



 

Une fois 4GT activé, un processus dont l’en-tête de prise en [**\_ \_ \_ \_ charge d’adresse de fichier image**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) est défini dans son en-tête d’image aura accès aux 1 Go supplémentaires de mémoire au-dessus des 2 Go de basse.

## <a name="adjusting-the-virtual-address-space-for-32-bit-windows"></a>Ajustement de l’espace d’adressage virtuel pour la Windows 32 bits

Vous pouvez utiliser la commande suivante pour définir une option d’entrée de démarrage qui configure la taille de la partition qui peut être utilisée par le processus sur une valeur comprise entre 2048 (2 Go) et 3072 (3 Go) :

[Bcdedit/set](/windows-hardware/drivers/devtest/bcdedit--set) **increaseuserva** *mégaoctets*

Une fois l’option d’entrée de démarrage définie, la plage de mémoire pour chaque partition est la suivante.



| Plage mémoire                            | Usage                |
|-----------------------------------------|----------------------|
| Faible (0x00000000 à *mégaoctets*)    | Utilisé par le processus. |
| Élevé (*mégaoctets*+ 1 à 0xFFFFFFFF) | Utilisé par le système.  |



 

**Windows Server 2003 :** Définissez le commutateur **/USERVA** dans boot.ini sur une valeur comprise entre 2048 et 3072.

 

 
