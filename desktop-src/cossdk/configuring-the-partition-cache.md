---
description: La fonctionnalité partitions COM+ comprend un cache de partition. Ce cache stocke les mappages d’utilisateur à partition et est conçu pour éviter un accès Active Directory répétitif.
ms.assetid: 8c3a269d-1933-4df6-aefb-f1f5587f1f42
title: Configuration du cache de partition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1389cc2685861e06d1b5c86baf2ad7b5fa9bd038
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916831"
---
# <a name="configuring-the-partition-cache"></a>Configuration du cache de partition

La fonctionnalité partitions COM+ comprend un cache de partition. Ce cache stocke les mappages d’utilisateur à partition et est conçu pour éviter un accès Active Directory répétitif.

## <a name="changing-cache-size"></a>Modification de la taille du cache

Le cache de partition est constitué de trois tables, dont la taille peut être modifiée pour améliorer les performances. Ces tables comportent le nombre d’entrées de SID dans le cache, le nombre d’entrées d’UO dans le cache et le nombre d’entrées de partition dans le cache.

Pour modifier ces tailles de table, les administrateurs peuvent modifier les valeurs d’une clé de registre. La clé de Registre et ses valeurs sont les suivantes :

**HKLM \\ Software \\ Microsoft \\ COM3 \\ PartitionCache**



| Valeurs de clé                         | Description                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **NumSidEntries**<br/>       | Contient la \_ valeur reg DWORD pour le nombre d’entrées sid dans le cache (valeur par défaut = 512). Cette valeur doit être définie sur une valeur supérieure au nombre d’identités uniques qu’un ordinateur traitera dans la fenêtre de temps d’invalidation du cache.<br/>                                                                                                                                                  |
| **NumNameEntries**<br/>      | Contient la \_ valeur reg DWORD pour le nombre d’entrées de nom d’unité d’organisation dans le cache (valeur par défaut = 64). Cette valeur doit être définie sur une valeur supérieure au nombre de noms d’UO uniques qu’un ordinateur traitera dans la fenêtre de temps d’invalidation du cache.<br/>                                                                                                                                                 |
| **NumPartitionEntries**<br/> | Contient la \_ valeur reg DWORD pour le nombre d’entrées de partition dans le cache (valeur par défaut = 1 024).<br/> Dans la fenêtre de temps d’invalidation du cache, la valeur DWORD doit être définie sur un nombre supérieur au nombre de partitions uniques qu’un ordinateur doit traiter. Cela est dû au fait que le contexte d’un composant peut inclure un ID de partition pour une partition qui ne réside pas sur cet ordinateur. <br/> |
| **EntryExpiration**<br/>     | Contient la \_ valeur reg DWORD pour le nombre de cycles (chaque graduation = ~ 7 minutes) jusqu’à ce qu’une entrée de cache devienne non valide (valeur par défaut = 4 (environ 28 minutes)).<br/>                                                                                                                                                                                                                                                          |



 

## <a name="flushing-the-cache"></a>Vidage du cache

Étant donné que COM+ met en cache la partition par défaut pour les utilisateurs, vous souhaiterez peut-être appeler cette méthode après avoir modifié la partition par défaut d’un utilisateur dans la Active Directory. Les administrateurs peuvent effectuer cette opération par programme en appelant la méthode [**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Collecte des métriques de partition](collecting-partition-metrics.md)
</dt> <dt>

[Regroupement d’applications en partitions](grouping-applications-into-partitions.md)
</dt> <dt>

[Gestion des partitions locales](managing-local-partitions.md)
</dt> <dt>

[Gestion des partitions dans Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Définition des droits d’administration pour une partition](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




