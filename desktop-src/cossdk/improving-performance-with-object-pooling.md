---
description: Amélioration des performances avec la mise en pool d’objets
ms.assetid: 7a8a38d8-6549-4686-a298-f3b427b380e3
title: Amélioration des performances avec la mise en pool d’objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398b9140080d3a439293b5152b4da7251978e800
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515160"
---
# <a name="improving-performance-with-object-pooling"></a>Amélioration des performances avec la mise en pool d’objets

La mise en pool d’objets peut être extrêmement efficace dans certaines circonstances, entraînant des augmentations significatives des performances. L’idée générale de la réutilisation d’objets pour tirer le meilleur parti consiste à regrouper autant de ressources que possible, à mettre en œuvre l’initialisation à partir du travail réel effectué, puis à personnaliser administrativement les caractéristiques du pool sur le matériel réel au moment du déploiement. En d’autres termes, procédez comme suit :

1.  Écrivez l’objet afin de prendre en compte l’initialisation coûteuse et l’acquisition des ressources qui est effectuée pour n’importe quel client comme condition préalable à l’exécution du travail réel au nom du client. Écrire des constructeurs d’objets lourds pour regrouper autant de ressources que possible, afin qu’ils soient détenus par l’objet et immédiatement disponibles lorsque les clients obtiennent un objet à partir du pool.
2.  Configurez le pool de manière administrative pour obtenir le meilleur équilibre dans les ressources matérielles disponibles, en général la mémoire dédiée à la gestion d’un pool d’une certaine taille en échange d’un accès client et de l’utilisation des objets plus rapides. À un certain point, le regroupement permettra de réduire les retours et vous pourrez obtenir de bonnes performances tout en limitant l’utilisation possible des ressources par un composant particulier.

## <a name="doing-actual-work-or-acquiring-resources"></a>Travail réel ou acquisition de ressources

Si vous avez un composant que les clients utiliseront brièvement et en succession rapide, où une partie importante du temps d’utilisation des objets est passée à acquérir des ressources ou à s’initialiser avant d’effectuer un travail spécifique pour le client, il est probable que l’écriture de votre composant pour utiliser le regroupement d’objets sera un grand succès pour vous.

Vous pouvez écrire le composant de sorte que dans le constructeur de l’objet, vous réalisiez la plus grande partie du travail long qui est uniforme pour tous les clients, en obtenant une ou plusieurs connexions, en exécutant des scripts, en extrayant des données d’initialisation à partir de fichiers ou sur un réseau, etc. Cela a pour effet de regrouper toutes ces ressources. Vous regroupez la combinaison des ressources et de l’état générique nécessaire pour effectuer un travail.

Dans ce cas, lorsque les clients obtiennent un objet à partir du pool, ces ressources sont immédiatement disponibles. En règle générale, ils utilisent l’objet pour effectuer une petite unité de travail, en envoyant ou en extrayant des données, puis l’objet appellera [**IObjectContext :: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) ou [**IObjectContext :: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) et retournent. Avec les modèles d’utilisation à incendie rapide tels que celui-ci, le regroupement offre d’excellentes avantages en matière de performances. Vous pouvez tirer pleinement parti de la simplicité du modèle de programmation de transaction automatique sans État, tout en obtenant des performances avec des composants avec état traditionnels.

Toutefois, si les clients utilisent un objet pendant une longue période à chaque fois qu’ils l’appellent, le regroupement aura moins de sens. L’avantage en termes de vitesse que vous obtenez est marginal lorsque le temps d’utilisation augmente par rapport au temps d’initialisation. Vous gagnez des retours qui peuvent ne pas justifier le coût de la mémoire nécessaire à la conservation d’un pool d’objets actifs.

## <a name="sharing-cost-across-multiple-clients"></a>Partage des coûts entre plusieurs clients

Une variante de l’initialisation de la factorisation est que vous pouvez utiliser le regroupement pour amortir de façon statistique le coût de l’acquisition de ressources coûteuses. Si vous prenez l’acquisition ou l’initialisation une fois, puis réutilisez l’objet, vous partagez ce coût sur tous les clients qui utilisent l’objet pendant sa durée de vie. Une durée de construction lourde n’est générée qu’une seule fois par objet.

## <a name="preallocating-objects"></a>Préallouer des objets

Si vous spécifiez une taille de pool minimale différente de zéro, ce nombre minimal d’objets sera créé et regroupé au démarrage de l’application, prêt pour tous les clients qui appellent à l’application.

## <a name="governing-resource-use-with-pool-management"></a>Administration de l’utilisation des ressources avec la gestion des pools

Vous pouvez utiliser la taille de pool maximale pour régir très précisément la manière dont vous utilisez les ressources. Par exemple, si vous disposez d’une licence pour un certain nombre de connexions de base de données, vous pouvez contrôler le nombre de connexions ouvertes à tout moment.

Lorsque vous prenez en compte les modèles d’utilisation des clients, les caractéristiques d’utilisation des objets et les ressources physiques telles que la mémoire et les connexions, vous pouvez trouver un point d’équilibre optimal quand vous effectuez le réglage des performances. Le regroupement d’objets entraînera la diminution des retours après un certain point. Vous pouvez déterminer le niveau de performances dont vous avez besoin et équilibrer les ressources nécessaires pour y parvenir.

Pour faciliter le réglage des performances lors de la configuration de la mise en pool d’objets, vous pouvez surveiller les statistiques d’objets des composants d’une application. Pour plus d’informations, consultez [Monitoring Object Statistics](monitoring-object-statistics.md).

## <a name="improve-performance-of-jit-activated-components"></a>Améliorer les performances des composants de JIT-Activated

Le regroupement d’objets fonctionne très bien avec le service [d’activation juste-à-temps com+](com--just-in-time-activation.md) . En regroupant les objets qui sont activés juste-à-temps, vous pouvez accélérer la réactivation des objets. Vous bénéficiez des avantages du maintien du canal ouvert par l’activation JIT tout en réduisant le coût de la réactivation. Vous pouvez utiliser le regroupement dans ce cas pour déterminer la quantité de mémoire que vous souhaitez allouer aux objets dont les références sont actives.

Il est très probable que vous regroupez des composants activés juste-à-temps lorsqu’ils sont transactionnels. Le mise en pool d’objets est optimisé pour gérer les composants transactionnels. Pour plus d’informations, consultez [regroupement d’objets transactionnels](pooling-transactional-objects.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Chaînes du constructeur d’objet COM+](com--object-constructor-strings.md)
</dt> <dt>

[Contrôle de la durée de vie et de l’état des objets](controlling-object-lifetime-and-state.md)
</dt> <dt>

[Fonctionnement du regroupement d’objets](how-object-pooling-works.md)
</dt> <dt>

[Regroupement d’objets transactionnels](pooling-transactional-objects.md)
</dt> <dt>

[Conditions requises pour les objets regroupables](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



