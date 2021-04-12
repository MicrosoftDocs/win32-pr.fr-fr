---
description: Le mise en pool d’objets est un service automatique fourni par COM+ qui vous permet de configurer un composant pour que des instances de lui-même restent actives dans un pool, prêtes à être utilisées par n’importe quel client qui demande le composant.
ms.assetid: 74a45220-449a-4d89-a979-a206e5e3d3ad
title: Concepts de mise en pool d’objets COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fb2aa6481b2493371801d0d274420d356b0a32e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393015"
---
# <a name="com-object-pooling-concepts"></a>Concepts de mise en pool d’objets COM+

Le mise en pool d’objets est un service automatique fourni par COM+ qui vous permet de configurer un composant pour que des instances de lui-même restent actives dans un pool, prêtes à être utilisées par n’importe quel client qui demande le composant. Vous pouvez configurer et surveiller de manière administrative le pool maintenu pour un composant donné, en spécifiant des caractéristiques telles que la taille du pool et les valeurs de délai d’attente de la demande de création. Lorsque l’application est en cours d’exécution, COM+ gère le pool pour vous, en gérant les détails de l’activation et de la réutilisation des objets en fonction des critères que vous avez spécifiés.

Vous pouvez obtenir des avantages significatifs en termes de performances et de mise à l’échelle en réutilisant les objets de cette manière, en particulier lorsqu’ils sont écrits pour tirer pleinement parti de la réutilisation. Avec la mise en pool d’objets, vous bénéficiez des avantages suivants :

-   Vous pouvez accélérer l’utilisation des objets pour chaque client, en déterminant l’initialisation et l’acquisition des ressources fastidieuses à partir du travail réel effectué par l’objet pour les clients.
-   Vous pouvez partager le coût de l’acquisition de ressources coûteuses sur tous les clients.
-   Vous pouvez préallouer des objets au démarrage de l’application avant que les demandes des clients ne soient générées.
-   Vous pouvez régir l’utilisation des ressources avec la gestion des pools d’administration. par exemple, en définissant un niveau de pool maximal approprié, vous ne pouvez garder l’Open que le nombre de connexions à la base de données que vous disposez d’une licence pour.
-   Vous pouvez configurer de façon administrative la mise en pool pour tirer le meilleur parti des ressources matérielles disponibles. vous pouvez facilement ajuster la configuration du pool en fonction de la modification des ressources matérielles disponibles.
-   Vous pouvez accélérer la réactivation des objets qui utilisent [l’activation juste-à-temps (JIT)](com--just-in-time-activation.md), tout en contrôlant délibérément la façon dont les ressources sont dédiées aux clients.

## <a name="writing-poolable-objects"></a>Écriture d’objets regroupables

Les objets regroupables doivent répondre à certaines exigences pour permettre l’utilisation d’une instance d’objet unique par plusieurs clients. Par exemple, ils ne peuvent pas conserver l’état du client ou avoir une affinité de thread. Les objets transactionnels ont également des exigences particulières, dans la mesure où les ressources managées détenues par un objet mis en pool doivent être inscrites manuellement dans une transaction.

Les objets regroupés peuvent implémenter [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) pour contrôler la façon dont ils sont réutilisés. Cela leur permet d’effectuer l’initialisation lorsqu’elle est activée dans un contexte donné, de nettoyer tout état du client lors de la désactivation et d’indiquer quand ils sont dans un État non réutilisable.

Souvent, il est utile d’écrire des objets pouvant être regroupés de façon quelque peu générique, afin qu’ils puissent être personnalisés de façon administrative avec une chaîne de constructeur. Par exemple, un objet peut être écrit pour contenir une connexion ODBC générique, avec un nom de source de données particulier, défini administrativement dans une chaîne de constructeur.

Les rubriques de cette section, décrites dans le tableau suivant, fournissent des informations sur le fonctionnement du regroupement d’objets dans COM+, ainsi que des informations sur l’écriture, la configuration et l’implémentation d’objets regroupables.



| Rubrique                                                                                                 | Description                                                                                              |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Fonctionnement du regroupement d’objets](how-object-pooling-works.md)<br/>                                   | Présente les concepts de base.<br/>                                                                      |
| [Amélioration des performances avec la mise en pool d’objets](improving-performance-with-object-pooling.md)<br/> | Fournit des détails spécifiques sur la façon dont vous pouvez utiliser le regroupement d’objets le plus efficacement possible.<br/>                 |
| [Conditions requises pour les objets regroupables](requirements-for-poolable-objects.md)<br/>                 | Fournit des détails sur l’écriture d’un objet qui doit être regroupé.<br/>                              |
| [Regroupement d’objets transactionnels](pooling-transactional-objects.md)<br/>                         | Fournit des détails sur les exigences spéciales qui s’appliquent aux objets transactionnels regroupables.<br/> |
| [Contrôle de la durée de vie et de l’état des objets](controlling-object-lifetime-and-state.md)<br/>         | Décrit comment implémenter des objets regroupés pour contrôler la façon dont ils sont réutilisés.<br/>               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tâches de mise en pool d’objets COM+](com--object-pooling-tasks.md)
</dt> </dl>

 

 




