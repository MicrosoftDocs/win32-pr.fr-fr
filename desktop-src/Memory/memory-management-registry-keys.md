---
description: L’espace d’adressage virtuel du système (VA) sur les systèmes 32 bits peut devenir épuisé en raison de la fragmentation. Plusieurs clés de Registre peuvent être utilisées pour configurer les limites de mémoire sur les systèmes 32 bits qui rencontrent ce problème.
ms.assetid: ec2a8c6b-cd8e-4085-b337-02f78a210bb5
title: Clés de registre de gestion de la mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48e8c53bd54f8caeb82aad58ceed61cc5644c112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869065"
---
# <a name="memory-management-registry-keys"></a>Clés de registre de gestion de la mémoire

L’espace d’adressage virtuel du système (VA) sur les systèmes 32 bits peut devenir épuisé en raison de la fragmentation. Plusieurs clés de Registre peuvent être utilisées pour configurer les limites de mémoire sur les systèmes 32 bits qui rencontrent ce problème. L’espace système VA sur les systèmes 64 bits n’est pas soumis à l’épuisement par fragmentation ; par conséquent, ces clés n’ont aucun effet sur les systèmes 64 bits.

Pour les systèmes 32 bits, ces clés de registre de gestion de la mémoire doivent être créées explicitement sous la clé de Registre suivante :

**HKEY \_ \_** Contrôle actuel du jeu de \\  \\ **contrôle** de \\  \\ **session** \\  du système d’ordinateur local gestion de la mémoire

**Windows Server 2008 et Windows Vista :** Ces clés de Registre sont disponibles sur les systèmes 32 bits à partir de Windows Server 2008 et Windows Vista avec Service Pack 1 (SP1).

Pour les limites de mémoire et d’espace d’adressage par défaut sur les systèmes 32 bits et 64 bits, consultez [limites de mémoire pour les versions de Windows](memory-limits-for-windows-releases.md).

Le tableau suivant décrit les clés de registre de gestion de la mémoire qui peuvent être utilisées pour configurer les limites de mémoire sur les systèmes 32 bits. Toutes ces clés ont un \_ type DWORD reg et les valeurs possibles sont comprises entre 0 et 2 048 Mo. La valeur par défaut est 0, ce qui signifie qu’aucune limite n’est appliquée. Les valeurs sont automatiquement arrondies à la limite d’allocation de VA du système suivante, qui est de 2 Mo sur les systèmes 32 bits sur lesquels l' [extension d’adresse physique](physical-address-extension.md) (PAE) est activée et 4 Mo sur les systèmes 32 bits sur lesquels PAE n’est pas activé.



| Clé                   | Description                                                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **NonPagedPoolLimit** | Spécifie la quantité maximale d’espace de VA du système qui peut être utilisée par la réserve non paginée. Dans certaines conditions, cette limite peut être dépassée d’une petite quantité. |
| **PagedPoolLimit**    | Spécifie la quantité maximale d’espace de VA du système qui peut être utilisée par la réserve paginée.                                                                            |
| **SessionSpaceLimit** | Spécifie la quantité maximale d’espace de VA du système qui peut être utilisée par les allocations d’espace de session.                                                                 |
| **SystemCacheLimit**  | Spécifie la quantité maximale d’espace de VA du système qui peut être utilisée par le cache système. Dans certaines conditions, cette limite peut être dépassée d’une petite quantité.  |
| **SystemPtesLimit**   | Spécifie la quantité maximale d’espace de VA système qui peut être utilisée par les mappages d’e/s et d’autres ressources qui utilisent des entrées de table de pages système (PTE).            |



 

L’utilisation d’un débogueur de noyau permet de déterminer si l’espace du système VA être épuisé. Pour plus d'informations, consultez [Outils de débogage pour Windows](https://msdn.microsoft.com/library/cc267445.aspx).

 

 



