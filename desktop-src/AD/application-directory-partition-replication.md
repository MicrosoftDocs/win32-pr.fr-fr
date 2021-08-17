---
title: Réplication de la partition de l’annuaire d’applications
description: Les partitions d’annuaire d’applications sont le plus souvent utilisées pour stocker des données dynamiques.
ms.assetid: b5fbec54-ee1a-4fe6-b4b7-67fc4e77d043
ms.tgt_platform: multiple
keywords:
- Active Directory de réplication de la partition d’annuaire d’applications
- Partitions de l’annuaire d’applications Active Directory, réplication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed7df6c50653fe1660bbf95f0f6ca580404d38c366c1045bc3d1b712ca771d3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024409"
---
# <a name="application-directory-partition-replication"></a>Réplication de la partition de l’annuaire d’applications

Les partitions d’annuaire d’applications sont le plus souvent utilisées pour stocker des données dynamiques. Étant donné que les données changent plus souvent que les données de configuration d’une forêt, l’étendue et la fréquence de réplication d’une partition d’annuaire d’applications peuvent être définies pour chaque partition. Les fonctionnalités de réplication de Active Directory Domain Services peuvent être utilisées, mais les données de réplication peuvent être ajustées pour s’adapter au type de données stockées sur la partition.

Le système d’exploitation n’impose pas un nombre maximal de réplicas, mais le nombre de réplicas doit être réduit au minimum pour réduire l’impact sur les performances de la réplication des données de la partition de l’annuaire d’applications dynamiques.

Le KCC génère et gère la topologie de réplication pour une partition d’annuaire d’applications.

## <a name="application-directory-partition-replication-within-a-site"></a>Réplication de la partition de l’annuaire d’applications au sein d’un site

Les intervalles de réplication qui contrôlent la réplication intra-site d’une partition d’annuaire d’applications peuvent être configurés. Cela permet de synchroniser plus rapidement les données dynamiques dans une partition d’annuaire d’application que les données plus statiques dans une partition de domaine. Pour plus d’informations sur la configuration par programme d’une partition d’annuaire d’applications, consultez Modification de la configuration de la [partition d’annuaire d’applications](modifying-application-directory-partition-configuration.md).

deux attributs sur l’objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) de la partition de l’annuaire d’applications et deux valeurs de registre sur chaque Windows 2000 et un contrôleur de domaine ultérieur contrôlent la latence de l’initiation d’une notification de modification d’origine aux partenaires de réplication au sein d’un site.

-   L’attribut [**MSDS-Replication-Notify-First-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-first-dsa-delay) d’un objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) spécifie le délai, en secondes, après la modification d’un objet d’origine avant que le premier partenaire de réplication soit notifié. Une valeur de Registre sur chaque contrôleur de domaine peut spécifier une valeur similaire. dans une forêt Windows Server 2003, le premier délai par défaut est de 15 secondes. Dans une forêt en mode mixte, le premier délai par défaut est de cinq minutes.
-   L’attribut [**MSDS-Replication-Notify-subséquente-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-subsequent-dsa-delay) d’un objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) spécifie le délai, en secondes, entre les notifications ultérieures aux deuxième, troisième, et ainsi de suite sur les partenaires de réplication. Une valeur de Registre sur chaque contrôleur de domaine peut spécifier une valeur similaire. dans une forêt Windows Server 2003, le délai suivant par défaut est de 3 secondes. Dans une forêt en mode mixte, le délai par défaut est de 30 secondes.

Les attributs [**crossRef**](/windows/desktop/ADSchema/c-crossref) s’appliquent à tous les contrôleurs de domaine qui hébergent un réplica de la partition de l’annuaire d’applications et affectent uniquement la réplication de la partition d’annuaire d’applications identifiée par l’objet **crossRef** . Les valeurs de registre s’appliquent uniquement au contrôleur de domaine sur lequel elles sont définies et affectent la réplication intra-site pour toutes les partitions hébergées par le contrôleur de domaine. Si les attributs **crossRef** et leurs valeurs de registre ne sont pas définis, un contrôleur de domaine utilise les valeurs par défaut. Si les valeurs de Registre sont définies, elles remplacent toutes les valeurs définies dans l’objet **crossRef** . Par défaut, les valeurs de Registre et **crossRef** ne sont pas définies. par conséquent, les valeurs par défaut sont utilisées. Cela permet à un administrateur d’accélérer la réplication de tous les réplicas d’une partition de l’annuaire d’applications en définissant les valeurs **crossRef** , tout en permettant un réglage plus fin avec les paramètres du Registre sur chaque contrôleur de domaine.

à partir de Windows Server 2003, les partitions de domaine utilisent également ces attributs de l’objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) pour contrôler la latence de réplication intra-site. Il s’agit d’une modification par rapport aux versions précédentes du serveur, dans lesquelles les intervalles de délai étaient contrôlés par les valeurs de Registre sur chaque contrôleur de domaine. lorsque la forêt est mise à niveau vers Windows Server 2003, les valeurs de registre existantes sont conservées uniquement si elles ont été modifiées à partir des valeurs par défaut. Les intervalles de notification des contrôleurs de domaine dans le registre remplacent les intervalles de notification stockés sur l’objet **crossRef** de la partition.

## <a name="application-directory-partition-replication-across-sites"></a>Réplication de la partition de l’annuaire d’applications entre les sites

Les réplicas d’une partition de l’annuaire d’applications qui se trouvent sur plusieurs sites observent la planification de la réplication intersite comme pour la réplication de la partition de domaine et du catalogue global. Toutefois, les réplicas d’une partition d’annuaire d’applications sont plus souvent situés au sein d’un site lors de l’hébergement de données réellement volatiles, car la latence de réplication intersite peut ne pas être acceptable pour que les réplicas soient cohérents entre eux.

## <a name="application-directory-partitions-are-not-replicated-to-global-catalogs"></a>Les partitions d’annuaire d’applications ne sont pas répliquées sur les catalogues globaux

Les objets d’une partition d’annuaire d’applications ne sont pas répliqués dans le catalogue global. La partition de l’annuaire d’applications est mise en place en hébergeant des données dynamiques et des objets pour lesquels elle ne peut pas être rationnelle, ni être susceptible de répliquer largement les objets. C’est la raison pour laquelle la partition d’annuaire d’applications offre une étendue contrôlée et une fréquence de réplication. Pour cette raison, il n’y a aucune raison de permettre à ces objets d’être répliqués sur le catalogue global et donc de les distribuer sur l’ensemble de la forêt où se trouve un serveur de catalogue global. Cela ne limite pas les objets d’une partition d’annuaire d’applications à l’aide d’attributs dans le schéma marqué comme [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset). Comme pour n’importe quel contrôleur de domaine, un serveur de catalogue global peut toujours être configuré pour être un réplica complet d’une partition d’annuaire d’applications.

 

 