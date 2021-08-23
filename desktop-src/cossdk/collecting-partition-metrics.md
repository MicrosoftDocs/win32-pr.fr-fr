---
description: Collecte des métriques de partition
ms.assetid: 2dc35011-24fa-49df-9cf8-96db2de39efa
title: Collecte des métriques de partition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8168972a0bac0b4eb79c5adde3530d1a0673469adff6b66b4c1b31cc6446bca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047686"
---
# <a name="collecting-partition-metrics"></a>Collecte des métriques de partition

Dans certains cas, une organisation peut souhaiter collecter des informations sur l’utilisation des applications COM+ dans le cadre de la surveillance, de la planification de la capacité et de la gestion des ressources.

Par exemple, un fournisseur de services d’application (ASP) peut vouloir payer un client pour son utilisation des ressources. Pour ce faire, COM+ vous permet de collecter des informations sur les événements et les métriques sur une base par partition.

Pour collecter ces informations pour une partition spécifique, vous pouvez spécifier, pour chaque interface COM+ instrumentation, le membre ID de partition dans la structure d’événement standard. La structure d’événement est la première valeur d’une interface d’instrumentation COM+. Pour plus d’informations, consultez [interfaces d’instrumentation com+](com--instrumentation-interfaces.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

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

 

 



