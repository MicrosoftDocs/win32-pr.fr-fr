---
description: Décrit un disque dur, le partitionnement et l’enregistrement de démarrage principal.
ms.assetid: daf45180-2cc3-433d-823e-395e85ce3410
title: Périphériques de disque et partitions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e063b943d33118a45cb6ab4c304569094af2c32e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570276"
---
# <a name="disk-devices-and-partitions"></a>Périphériques de disque et partitions

Un disque dur se compose d’un ensemble de plateaux empilés, dont les données sont stockées de façon électromagnétique dans des cercles concentriques ou des *pistes*. Chaque plateau a deux têtes, une à chaque côté du plateau, qui lit ou écrit des données à mesure que le disque tourne. Un *lecteur de disque dur* contrôle la position, la lecture et l’écriture du disque dur. Notez que les têtes de tous les plateaux sont positionnés en tant qu’unité.

La plus petite unité adressable d’une piste est un *secteur*. Un *cylindre* est défini comme l’ensemble des pistes qui s’affichent au même emplacement sur chaque plateau. Par exemple, le schéma suivant montre un disque dur avec quatre plateaux. Le cylindre X comprend huit pistes (piste X de chaque côté de chaque plateau).

![disque dur, y compris les pistes, les secteurs et les plateaux](images/diskdevice.png)

Un disque dur peut contenir une ou plusieurs régions logiques appelées *partitions*. Les partitions sont créées lorsque l’utilisateur met en forme un disque dur en tant que *disque de base*. Windows prend également en charge les *disques dynamiques*, qui ne sont pas abordés dans cette rubrique. Pour plus d’informations sur les disques de base et les disques dynamiques, consultez [disques de base et dynamiques](basic-and-dynamic-disks.md).

La création de plusieurs partitions sur un disque permet l’apparition de disques durs distincts. Par exemple, un système avec un disque dur doté d’une partition contient un seul volume, désigné par le système en tant que lecteur C. Un système doté d’un disque dur avec deux partitions contient généralement les lecteurs C et D. Le fait de disposer de plusieurs partitions sur un disque dur peut faciliter la gestion du système, par exemple pour organiser des fichiers ou pour prendre en charge plusieurs utilisateurs.

Le premier secteur physique sur un disque de base contient une structure de données connue sous le nom d’enregistrement de démarrage principal (MBR). Le MBR contient les éléments suivants :

-   Un programme de démarrage (taille maximale de 442 octets)
-   Une signature de disque (nombre unique de 4 octets)
-   Une table de partition (jusqu’à quatre entrées);
-   Marqueur de fin de MBR (Always 0x55AA)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de la gestion des volumes](about-volume-management.md)
</dt> <dt>

[Disques de base et dynamiques](basic-and-dynamic-disks.md)
</dt> </dl>

 

 



