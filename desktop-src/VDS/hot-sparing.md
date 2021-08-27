---
description: Remplacement à chaud
ms.assetid: 2faf2f3f-f459-4e41-9c8e-042c7b72281b
title: Remplacement à chaud
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61b8df9bc27e303277c869901872a9b879cb2d7df32764589501b9d33a51c3fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125949"
---
# <a name="hot-sparing"></a>Remplacement à chaud

\[à partir de Windows 8 et Windows Server 2012, l’interface COM du [Service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion des Stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Le remplacement à chaud est la substitution d’un disque ou d’un lecteur pour un disque ou un lecteur défaillant ou défaillant. (Les fournisseurs de matériel agissent sur les lecteurs ; les fournisseurs de logiciels agissent sur les disques.) Vous pouvez partager un disque de rechange à chaud entre tous les numéros d’unités logiques du sous-système ou l’associer à un numéro d’unité logique spécifique. De même, vous pouvez associer un disque de rechange à chaud à un seul fournisseur de volume, de Pack et de logiciel, ou le partager entre tous les ordinateurs hôtes d’un réseau SAN.

Si le volume ou le numéro d’unité logique associé est à tolérance de panne, vous pouvez remplacer le disque ou le disque défaillant par un disque d’échange à chaud, puis reconstruire les miroirs ou les RAID de parité affectés. Vous pouvez remplacer un disque défaillant par un disque défectueux, même si le volume ou le numéro d’unité logique associé n’est pas tolérant aux pannes. En supposant que vous puissiez déterminer la défaillance imminente avant la perte catastrophique de données, vous pouvez temporairement mettre en miroir le disque de secours à chaud sur le disque ou le lecteur défaillant, puis supprimer le disque ou le lecteur défaillant.

Le remplacement à chaud peut être automatique ou manuel. Si un fournisseur implémente le remplacement à chaud automatique, il effectue la substitution de manière dynamique. Le remplacement à chaud manuel nécessite une intervention de l’opérateur ou de l’application. Un disque d’échange à chaud peut contenir des données partielles ou une mise en forme d’une utilisation précédente. VDS remplace le disque d’échange à chaud lorsque la substitution se produit.

Vous ne pouvez pas utiliser un disque d’échange à chaud pour les opérations de liaison ordinaires. Si le disque de secours est plus grand que le disque ou le disque défectueux, tout espace excédentaire reste inutilisé tant qu’il n’est pas explicitement déclaré disponible pour la liaison. Une fois que le disque de rechange à chaud a été utilisé pour la récupération, le disque ou le lecteur n’est plus un disque de rechange à chaud. En d’autres termes, l’axe de 1 16 Go ne peut pas agir en tant que disques d’échange à chaud de 2 8 gigaoctets.

 

 
