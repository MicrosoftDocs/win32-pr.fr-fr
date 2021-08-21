---
title: Nommage des contextes et des partitions d’annuaire
description: Chaque contrôleur de domaine dans une forêt de domaine contrôlée par Active Directory Domain Services comprend des partitions d’annuaire.
ms.assetid: 77ac171c-2031-46d7-b81e-dd9ae0c70ccb
ms.tgt_platform: multiple
keywords:
- Nommage des contextes et des partitions d’annuaire Active Directory
- Nommage des contextes Active Directory, à propos de
- Partitions d’annuaire Active Directory, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d309b76b50270f093b3a4930680b343d517976e269e731082696b89bf6a58c46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025707"
---
# <a name="naming-contexts-and-directory-partitions"></a>Nommage des contextes et des partitions d’annuaire

Chaque contrôleur de domaine dans une forêt de domaine contrôlée par Active Directory Domain Services comprend des [*partitions d’annuaire*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)). Les partitions d’annuaire sont également appelées [*contextes d’attribution de noms*](/previous-versions/windows/desktop/legacy/ms681918(v=vs.85)). Une partition d’annuaire est une partie contiguë de l’annuaire global qui a une étendue de réplication indépendante et des données de planification. Par défaut, le service domaine Active Directory pour une entreprise contient les partitions suivantes :

-   [*Partition de schéma*](/previous-versions/windows/desktop/legacy/ms681936(v=vs.85)): la partition de schéma contient les objets **classSchema** et **attributeSchema** qui définissent les types d’objets qui peuvent exister dans la forêt. Chaque contrôleur de domaine de la forêt a un réplica de la même partition de schéma.
-   [*Partition de configuration*](/previous-versions/windows/desktop/legacy/ms681898(v=vs.85)): la partition de configuration contient une topologie de réplication et d’autres données de configuration qui doivent être répliquées dans toute la forêt. Chaque contrôleur de domaine de la forêt a un réplica de la même partition de configuration.
-   [*Partition de domaine*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)): la partition de domaine contient les objets d’annuaire, tels que les utilisateurs et les ordinateurs, associés au domaine local. Un domaine peut avoir plusieurs contrôleurs de domaine et une forêt peut avoir plusieurs domaines. Chaque contrôleur de domaine stocke un réplica complet de la partition de domaine pour son domaine local, mais il ne stocke pas les réplicas des partitions de domaine pour les autres domaines.

Windows Le serveur 2003 introduit la partition de l' *Annuaire d’applications*, qui permet de contrôler l’étendue de la réplication et d’autoriser le placement des réplicas de manière plus appropriée pour les données dynamiques. Pour plus d’informations sur les partitions de l’annuaire d’applications, consultez [à propos des partitions de l’annuaire d’applications](about-application-directory-partitions.md).

Pour plus d’informations sur la façon dont Active Directory Domain Services maintenir la cohérence entre les différents réplicas d’une partition d’annuaire, consultez [réplication et intégrité des données](replication-and-data-integrity.md).

 

 