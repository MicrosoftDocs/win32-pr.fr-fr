---
description: Déploiement pour une communication plus rapide
ms.assetid: 9099f9df-b620-4623-826e-c541202ebc4a
title: Déploiement pour une communication plus rapide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2594a7dbd34813013257350e2deb9d93db6bae5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516801"
---
# <a name="deploying-for-faster-communication"></a>Déploiement pour une communication plus rapide

Les performances sont un élément clé à prendre en compte lors du déploiement d’une application COM+, et l’emplacement des composants est la clé pour obtenir les meilleures performances d’une application bien conçue.

Une fois largement détenues, avec les architectures d’applications évolutives, les performances peuvent être résolues en déplaçant simplement les composants principaux de l’application sur du matériel plus rapide. Cela a prouvé que cela ne soit pas vrai. Les problèmes de performances ne proviennent pas des performances des composants individuels, mais des liens reliant les composants.

Le principal facteur de réussite est l’emplacement. La proximité ou l’emplacement physique, le temps, la capacité et l’objectif sont des aspects distincts de l’emplacement qui s’appliquent au déploiement d’une application COM+, qui ont tous une incidence sur les performances.

Les meilleures performances sont fournies lorsque les composants et les ressources de l’application sont conçus et déployés pour répondre aux demandes qui leur sont passées par la charge de travail de l’application.

En général, vous devez déployer des composants pour réduire la communication entre les composants entre les processus et, en particulier, entre les ordinateurs. Si la conception de votre application est efficace, les classes d’un composant sont regroupées à l’aide de et de la fonction pour optimiser les communications au sein des composants. Lors du déploiement de composants, vous devez vous assurer que les composants sont logiquement localisés pour utiliser les relations entre les composants et pour réduire la quantité de messagerie entre les composants.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conception pour le déploiement](designing-for-deployment.md)
</dt> </dl>

 

 



