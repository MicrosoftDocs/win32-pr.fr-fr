---
description: Les administrateurs peuvent utiliser COM+ pour créer et configurer des partitions COM+ par programmation.
ms.assetid: 15f0cd9a-cd40-49df-85b8-15c4e626f8ee
title: Création et configuration de partitions COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3cc9623272d4aba345cc666deb5c63965584af94f42dbf869b00cf7d52a2f30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858989"
---
# <a name="creating-and-configuring-com-partitions"></a>Création et configuration de partitions COM+

Les administrateurs peuvent utiliser COM+ pour créer et configurer des partitions COM+ par programmation. En fait, toutes les tâches de création et de configuration qu’un administrateur peut effectuer à partir des services de composants ou les outils d’administration utilisateurs et ordinateurs Active Directory peuvent être effectuées à l’aide de regroupements, d’objets et d’interfaces COM+ ou par le biais de l’interface de système Active Directory (ADSI).

**Windows XP :** La possibilité de créer, de configurer ou de déléguer des partitions COM+ n’est pas disponible. La partition globale est la seule partition COM+ disponible.

* * Windows 2000 : * * le service partitions COM+ n’est pas disponible dans Windows 2000.

> [!Note]  
> Le service partitions COM+ n’est pas activé par défaut. Pour utiliser le service partitions COM+, vous devez l’activer par le biais de l’outil d’administration Services de composants ou en modifiant la propriété PartitionsEnabled de la collection [**LocalComputer**](localcomputer.md) sur true.

 

Pour accomplir des tâches liées aux partitions, COM+ fournit les éléments de programmation suivants :

-   Méthodes et propriétés de l’interface [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) sur la classe [**COMAdminCatalog**](comadmincatalog.md) :
    -   Propriété [**CurrentPartition**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-put_currentpartition) .
    -   Propriété [**CurrentPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionid) .
    -   Propriété [**CurrentPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionname) .
    -   Méthode [**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) .
    -   Méthode [**GetPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionid) .
    -   Méthode [**GetPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionname) .
    -   Propriété [**GlobalPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_globalpartitionid) .
-   Ensemble d’objets COM+ pour créer et gérer des partitions dans Active Directory.
-   Une clé de registre COM+, **PartitionCache**, pour la modification de la taille du cache de partition.
-   Ensemble de [regroupements d’administration com+](com--administration-collections.md)liés aux partitions :
    -   Collection [**partitions**](partitions.md) .
    -   Collection [**PartitionUsers**](partitionusers.md) .
    -   Collection [**RolesForPartition**](rolesforpartition.md) .
    -   Collection [**UsersInPartitionRole**](usersinpartitionrole.md) .
-   Propriétés d’autres [regroupements d’administration com+](com--administration-collections.md):
    -   Propriété PartitionID sur la collection [**ApplicationInstances**](applicationinstances.md) .
    -   Propriété AppPartitionID sur la collection d' [**applications**](applications.md) .
    -   Propriétés PartitionDescription, PartitionID et PartitionName sur la collection [**FilesForImport**](filesforimport.md) .
    -   Propriétés DSPartitionLookupEnabled, LocalPartitionLookupEnabled et PartitionsEnabled sur la collection [**LocalComputer**](localcomputer.md) .
    -   Propriétés EventClassPartitionID et SubscriberPartitionID sur la collection [**SubscriptionsForComponent**](subscriptionsforcomponent.md) .
    -   Propriétés EventClassPartitionID et SubscriberPartitionID sur la collection [**TransientSubscriptions**](transientsubscriptions.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Collecte des métriques de partition](collecting-partition-metrics.md)
</dt> <dt>

[Configuration du cache de partition](configuring-the-partition-cache.md)
</dt> <dt>

[Regroupement d’applications en partitions](grouping-applications-into-partitions.md)
</dt> <dt>

[Gestion des partitions locales](managing-local-partitions.md)
</dt> <dt>

[Gestion des partitions dans Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Définition des droits d’administration pour une partition](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



