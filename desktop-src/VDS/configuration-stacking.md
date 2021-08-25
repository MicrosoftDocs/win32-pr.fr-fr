---
description: Empilement de configurations
ms.assetid: 1f0f75d6-3553-4ee1-8ee6-bd617da4a109
title: Empilement de configurations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9018a2484ce4e5b9121d08abffee54911531b7f421cfef75643594e827fe350e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905557"
---
# <a name="configuration-stacking"></a>Empilement de configurations

\[à partir de Windows 8 et Windows Server 2012, l’interface COM du [Service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion des Stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

L’empilement implique la concaténation d’un ensemble de mappages de blocs logiques. Vous pouvez empiler plusieurs numéros d’unités logiques à partir du même sous-système sous un même numéro d’unité logique. Vous pouvez empiler un numéro d’unité logique avec des volumes à partir du même Pack sous un seul volume. En outre, vous pouvez empiler plusieurs numéros d’unités logiques qui sont exposés par des sous-systèmes hétérogènes sous un seul volume.

Comme le montre l’illustration suivante, la création d’un volume ne change pas la liaison existante d’un numéro d’unité logique contributeur. De même, l’annulation de la liaison d’un volume ne dissocie pas un LUN contributeur. L’illustration représente la configuration RAID 0 1 (0 + 1). Cette configuration connue combine l’entrelacement (RAID 0) et la mise en miroir (RAID 1), qui associe l’accès rapide aux données de RAID 0 à la fiabilité de RAID 1.

![Diagramme illustrant une configuration RAID 0 1 (0 + 1).](images/vdsstacklunvolzeroplusone.png)

La contribution des numéros d’unités logiques peut avoir des types de liaison différents. De nombreuses configurations sont possibles avec VDS, mais sont très peu probables, comme dans l’illustration suivante. Dans cet exemple, un plex de volume est un numéro d’unité logique agrégé par bandes et l’autre est un numéro d’unité logique (LUN) en miroir triple.

![Diagramme illustrant une configuration VDS dans laquelle un plex de volume est un LUN agrégé par bandes et l’autre est un numéro d’unité logique (LUN) en miroir 3 voies.](images/vdsstacklunvol.png)

Bien qu’il ne soit pas pratique, cet exemple illustre un aspect important de l’empilement. Étant donné que l’empilement concatène les plex, VDS ajoute les trois Plex LUN aux deux plex de volume pour un total de cinq Plex.

 

 
