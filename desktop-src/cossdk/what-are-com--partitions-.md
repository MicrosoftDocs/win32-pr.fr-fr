---
description: Une partition COM+ est un conteneur logique qui permet aux applications de s’exécuter indépendamment des autres configurations de ces applications.
ms.assetid: c1290d10-968f-44f0-8099-d69c9e706c9e
title: Que sont les partitions COM+ ?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69acdae724bb0c9211d147a985f7571c5e7c052f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922864"
---
# <a name="what-are-com-partitions"></a>Que sont les partitions COM+ ?

Une partition COM+ est un conteneur logique qui permet aux applications de s’exécuter indépendamment des autres configurations de ces applications. Chaque configuration d’une application est installée dans une partition distincte et peut être gérée séparément, en fonction des besoins spécifiques de ses utilisateurs.

Au cours de l’activation d’un composant COM+, le service partitions détermine la configuration du composant à activer, en fonction de l’identité de l’utilisateur qui demande l’activation du composant. Par exemple, une organisation unique qui possède deux groupes, production et formation distincts, peut implémenter des partitions COM+ pour permettre aux deux groupes d’utiliser différentes configurations d’une application COM+ sur le même ordinateur.

**Windows XP :** La possibilité de créer, de configurer ou de déléguer des partitions COM+ n’est pas disponible. La partition globale est la seule partition COM+ disponible.

**Windows 2000 :** le service partitions COM+ n’est pas disponible dans Windows 2000.

## <a name="benefits-of-using-com-partitions"></a>Avantages de l’utilisation des partitions COM+

L’utilisation de partitions COM+ offre plusieurs avantages, notamment les suivants :

-   Les organisations peuvent réduire le coût total de possession (TCO) en utilisant moins de serveurs d’applications physiques pour prendre en charge les utilisateurs qui ont besoin de plusieurs configurations d’applications.
-   La surcharge administrative est réduite. Au lieu de devoir configurer et gérer plusieurs ordinateurs, les administrateurs doivent uniquement configurer et gérer plusieurs partitions sur le même ordinateur. En outre, les partitions peuvent être gérées par programme par le biais de l’ajout d’une nouvelle interface de programmation COM+.
-   La sécurité peut être implémentée et gérée sur la base d’une partition par partition pour les utilisateurs locaux, les utilisateurs de domaine et les unités d’organisation (UO).
-   les programmeurs et les administrateurs peuvent utiliser les outils de développement et d’administration de Microsoft, tels que les SDK Windows, Active Directory les utilisateurs et les ordinateurs, ainsi que l’outil d’administration Services de composants, pour gérer les partitions COM+. La fonctionnalité partitions est entièrement intégrée à ces outils.

## <a name="primary-usage-scenario"></a>Scénario d’utilisation principale

La principale raison pour laquelle les clients peuvent déployer la fonctionnalité partitions COM+ consiste à héberger des applications Web. Supposons, par exemple, qu’une petite entreprise de logiciels développe une application COM+ pour une utilisation par le personnel hospitalier. l’application, qui est une application Web distribuée, offre aux hôpitaux un moyen de stocker et de récupérer les dossiers médicaux des patients à l’aide d’une base de données SQL Server.

Supposons que l’entreprise logicielle a trois clients : hôpital A, hôpital B et hôpital C. Tandis que chaque client exécute le côté client de l’application COM+ localement sur ses ordinateurs de bureau, le côté serveur de l’application COM+ réside sur le serveur Web interne de l’éditeur de logiciels et est accessible par ses clients via le Web.

Étant donné que chaque hôpital a son propre ensemble d’exigences de stockage et de récupération et son propre ensemble de données de patients personnalisées, l’entreprise logicielle doit fournir un moyen de plusieurs configurations de la partie serveur de l’application à exécuter simultanément sur le serveur Web. Les partitions COM+ offrent une solution à ce problème.

L’illustration suivante montre le scénario des partitions pour l’application COM+ de l’éditeur de logiciels.

![diagramme illustrant un scénario de partitions pour une application COM+, avec une application cliente pour l’application serveur à la base de données du serveur de SQL.](images/c4a96ff9-9afd-43c7-807c-4593cb77f51b.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Restrictions relatives à la conception d’applications](application-design-restrictions.md)
</dt> <dt>

[Composants et partitions COM+ en file d’attente](com--queued-components-and-partitions.md)
</dt> <dt>

[Implémentation de la partition](partition-implementation.md)
</dt> <dt>

[Inscription et activation de composants dans des partitions](registering-and-activating-components-in-partitions.md)
</dt> </dl>

 

 



