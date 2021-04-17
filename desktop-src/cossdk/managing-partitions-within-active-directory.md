---
description: En guise d’alternative à la gestion des partitions de Active Directory par le biais de l’outil d’administration utilisateurs et ordinateurs Active Directory, vous pouvez gérer les partitions COM+ par programme à l’aide d’un ensemble d’objets COM+ au sein de l’interface système d’Active Directory (ADSI).
ms.assetid: 915b4643-cbda-433a-a383-65a6b0fd0874
title: Gestion des partitions dans Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6635e49b7d2833a1e6e177c25f9f2fb05ff0dff4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524175"
---
# <a name="managing-partitions-within-active-directory"></a>Gestion des partitions dans Active Directory

En guise d’alternative à la gestion des partitions de Active Directory par le biais de l’outil d’administration utilisateurs et ordinateurs Active Directory, vous pouvez gérer les partitions COM+ par programme à l’aide d’un ensemble d’objets COM+ au sein de l’interface système d’Active Directory (ADSI).

Quelle que soit la technique d’administration choisie pour la gestion des partitions COM+, les administrateurs doivent suivre une séquence générale d’étapes :

1.  Créez les nouvelles partitions COM+ dans Active Directory pour votre domaine.
2.  Créez des groupes de partitions COM+ dans Active Directory et mappez-les à vos partitions COM+ nouvellement créées.
3.  Configurez vos partitions Active Directory sur votre ordinateur local, à l’aide de l’objet COM+ approprié. Quand vous configurez une partition Active Directory sur un ordinateur local, un dossier **applications com+** est automatiquement créé dans ce dossier de partition.
4.  Installez vos applications COM+ dans les partitions COM+ appropriées.

Toutes les étapes précédentes peuvent être effectuées par programme, à l’aide d’un ensemble d’interfaces Active Directory appelées ADSI. Les objets disponibles pour la gestion des partitions disponibles dans ADSI sont les suivants :

-   nom de l' \_ USERPARTITIONSETLINK DS \_
-   nom de l' \_ PARTITIONLINK DS \_
-   nom de l' \_ ObjectID DS \_
-   nom de l' \_ DEFAULTPARTITIONLINK DS \_
-   nom de l' \_ USERLINK DS \_
-   nom de l' \_ PARTITIONSET DS \_
-   nom de la \_ partition DS \_

Pour plus d’informations sur la création et la gestion des partitions COM+ à l’aide des outils d’administration Active Directory utilisateurs et ordinateurs et services de composants, consultez l’aide en ligne disponible dans chaque outil.

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

[Définition des droits d’administration pour une partition](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



