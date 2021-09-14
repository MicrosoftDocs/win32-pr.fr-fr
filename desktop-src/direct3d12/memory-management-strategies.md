---
title: Stratégies de gestion de la mémoire
description: Un gestionnaire de mémoire pour Direct3D 12 peut être très compliqué rapidement avec les différents niveaux de prise en charge, pour les adaptateurs UMA ou discrets (non-UMA) et avec un large éventail de différences d’architecture entre les adaptateurs GPU. La stratégie recommandée pour la gestion de la mémoire Direct3D 12, décrite dans cette section, est \ 0034 ; classifier, budget et flux \ 0034 ;.
ms.assetid: BC9894F7-D496-46F2-A5C3-C7CA31FD4BA8
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dad04055a5acdeeeaead3a56f0bd04e64aa90fe0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012943"
---
# <a name="memory-management-strategies"></a>Stratégies de gestion de la mémoire

Un gestionnaire de mémoire pour Direct3D 12 peut être très compliqué rapidement avec les différents niveaux de prise en charge, pour les adaptateurs UMA ou discrets (non-UMA) et avec un large éventail de différences d’architecture entre les adaptateurs GPU.

La stratégie recommandée pour la gestion de la mémoire Direct3D 12, décrite dans cette section, est « classification, budget et flux ».

-   [Types de ressources](#resource-types)
-   [Budget de mémoire](#memory-budget)
-   [Stratégie de classification](#classification-strategy)
-   [Rubriques connexes](#related-topics)

## <a name="resource-types"></a>Types de ressources

Le concept de base d’une « ressource validée » (création d’espaces d’adressage virtuels et physiques initialisés dans la mémoire physique gérée) a été pris en compte depuis Direct3D 9, bien que l’adressage virtuel et l’adressage physique puissent être reteass dans Direct3D 12 pour permettre à l’application de gérer avec soin la mémoire physique.

En plus des ressources validées, la construction du tas de Direct3D 12 permet deux autres types de ressources : « placé » et « réservé ». Dans Direct3D 11, une ressource « réservée » était connue sous le nom de « ressource en mosaïque ».

Les ressources réservées diffèrent des ressources passées, car les ressources réservées ont leur propre espace d’adressage virtuel GPU unique. Cela permet une allocation importante de l’espace VA, puis active le mappage des pages VA à certaines sections du tas ultérieurement, et l’application reconfigure la configuration à la volée. L’espace VA est contigu et peut être faiblement mappé à.

La ressource réservée peut être créée pour référencer des régions dans le tas avec des appels d’API tels que [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) et elles peuvent être rendues résidentes par l’application en mettant à jour les tables de pages à la volée. Quand une plage VA est mappée à une valeur NULL ou à un segment de mémoire non résident, cette partie de la ressource est considérée comme non résidente. Quand une plage VA est mappée à un tas résident, cette partie de la ressource est considérée comme résidente. Les tas résident lors de leur création.

Les ressources passées sont une conception bien plus simple, simplement un pointeur vers une certaine région d’un segment de mémoire (par exemple, une région de 1 Mo pour une texture dans un tas de 5 Mo). Les barrières d’alias permettent d’utiliser des ressources placées qui se chevauchent (consultez [**CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource) et [**ResourceBarrier**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)).

Les ressources réservées ne sont pas disponibles sur tout le matériel Direct3D 12 et les ressources placées sont une solution de secours raisonnable, bien que les ressources placées doivent être contiguës et ne pas être partiellement résidentes.

## <a name="memory-budget"></a>Budget de mémoire

Dans Direct3D 12, lorsque vous allouez un segment, vous créez l’aspect de la mémoire physique d’une ressource validée. Un choix de segment de mémoire plus explicite est disponible dans Direct3D 12 (choix entre la mémoire vidéo et la mémoire système). Les adaptateurs UMA n’ont qu’un seul segment de mémoire, la mémoire système.

Les GPU ne prennent pas en charge les défaillances de page. par conséquent, les développeurs doivent être conscients qu’ils n’effectuent pas de validation, en particulier pour les systèmes avec seulement 1 Go de mémoire système. Si une application effectue une validation sur Commit, le système d’exploitation utilise la planification à granularité plus grossière des processus en fonction de la mémoire physique. Le planificateur fige les processus de premier plan et en fait une page en arrière-plan, afin de paginer un processus en arrière-plan qui souhaite s’exécuter. La mémoire physique disponible peut varier considérablement en fonction de ce que l’utilisateur fait en arrière-plan (par exemple, en exécutant un navigateur ou en regardant une vidéo).

L’API pour le budget de la mémoire est [**QueryVideoMemoryInfo**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo). Pour les adaptateurs discrets « local » est la mémoire vidéo, « non locale » est la mémoire système. Pour les adaptateurs UMA non locaux est toujours égal à zéro. Une question de conception est de savoir si votre moteur gère à la fois les budgets ou uniquement le budget local. La gestion du budget local uniquement est plus simple mais présente des inconvénients. par exemple, imaginons un budget local maximal de 1 Go, alors tous les tas proviennent de 1 Go dans un système UMA et il n’y a pas de dépassement de capacité de la mémoire système (en clair, car il n’y en a aucun).

Étant donné que la mémoire gérée par Direct3D11 pour les applications, les ressources inutilisées seraient en fait paginées.

Choisissez les dimensions de ressource les plus appropriées. Déterminez si la taille d’une ressource est appropriée pour la situation dans laquelle l’application s’exécute réellement. Certains utilisateurs peuvent exécuter l’application dans une fenêtre ou avec une résolution d’écran de 800x600.

## <a name="classification-strategy"></a>Stratégie de classification

Pour gérer efficacement les ressources dans les scénarios liés à la mémoire, envisagez de classer les ressources comme suit :



| classification ;      | Exemples                                                                                         | Objets et fonctionnalités d’API                                                                                           | Remarques sur la gestion                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Critique            | Interface utilisateur du jeu                                                                                          | Allocateur de commande, files d’attente de commandes, tas de requêtes, ressources et tas de ressources.                                      | Ces éléments doivent se trouver dans la mémoire non paginable/toujours validée.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Mis à l’échelle/facultatif    | Modèles et textures spécifiques au niveau, chaînes de permutation, zones de ciel, modèles de caractères de joueur de première personne | Les ressources et les tas. Les ressources validées, mais également les ressources placées et réservées peuvent fonctionner aussi bien.          | Intégrer le budget de la résidence en mémoire dans les algorithmes de rendu. Choisissez le niveau approprié des détails disponibles et Réévaluez moins d’une fois par image. Les techniques incluent l’utilisation de ressources de taille variable et l’évolution de la chaîne de permutation.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| Ressources réutilisées   | Mémoires tampons occultées, ressources de rendu différées, ressources de traitement postérieures, caches de données d’éclairage    | Les ressources et les tas. Chevauchement des ressources placées sur les tas et les barrières d’alias.                                  | Réutiliser des ressources volumineuses ou des régions de tas dans un cadre pour réduire les besoins de l’ensemble du frame. Utilisez la technique de réutilisation de la mémoire intra-image. Dans Direct3D 11, les applications pouvaient uniquement réutiliser des ressources avec le même type et des dimensions potentiellement suffisamment grandes. Les tas Direct3D 12 permettent d’utiliser des ressources qui se chevauchent pour une plus grande simplicité et une plus grande réutilisation.<br/>                                                                                                                                                                                                                              |
| Ressources de streaming | Textures et géométries du monde ouvert                                                        | Les ressources et les tas. Création de threads libres, threads d’UC d’arrière-plan et files d’attente et listes de commandes de copie en arrière-plan. | Une résidence partielle, en fonction de la visibilité (à l’aide de l’évaluation de la frustum ou de la distance) et de la réévaluation des besoins en résidence, chaque cadre.<br/> La technique consistant à utiliser la gestion de la durée de résidence partielle par vignette et la réutilisation inter-frame est disponible lorsque l’adaptateur GPU prend en charge les ressources réservées dans les tas.<br/> À l’aide de la technique d’utilisation de la réutilisation de mémoire inter-frame, la délégation de ressources partielles peut être accomplie, mais elle est moins optimale. Les ressources placées avec des segments de mémoire devraient permettre un recyclage plus rapide, mais les ressources validées peuvent être utilisées comme secours.<br/> |



 

Plus le nombre d’applications est Gravitate de diffuser des ressources pour la plupart du travail, plus elles tireront parti des ressources mises en place et réservées, ce qui augmentera la réutilisation de la mémoire entre ces quatre classifications. Plus le flux d’applications est grand, plus le budget est grand et la bande passante est prioritaire.

En général, avec les moteurs graphiques Direct3D 12, vous devez honorer un budget plus diversifié et dynamique et le faire plus rigoureusement que dans le passé. Les meilleures applications localisent les quatre catégories dans le budget donné au processus, en mettant à l’échelle le jeu à partir d’une application mobile en arrière-plan vers des budgets discrets en plein écran. Toutefois, de nombreuses applications auront probablement des difficultés à démarrer avec un trop grand nombre de types de ressources critiques. Les ressources compatibles Direct3D 11 sont créées de manière anonyme et occupent l’état critique sans impacter les performances. Toutefois, pour Direct3D 12, les développeurs doivent effectuer une recherche dans les ressources créées de façon aléatoire dans tout le moteur et l’intergiciel et les réaffecter à l’une des autres catégories.

Les composants de l’intergiciel (middleware), les contrôles utilisateur et la diffusion en continu intra-Frame sont d’autres domaines problématiques. Les composants de l’intergiciel (middleware) peuvent ne pas être exposés à un budget, ni fonctionner étroitement ensemble. Les composants de l’intergiciel (middleware) pourraient exposer des fonctionnalités comme techniques de rendu ; et l’application peut s’appuyer sur l’exposition des paramètres de l’intergiciel et du moteur. Les développeurs peuvent utiliser Direct3D 11 pour effectuer la pagination et atteindre la fréquence d’images appropriée. Dans certains cas, les applications Direct3D 11 ont peut-être contenu la pagination du contenu des ressources dans chaque frame. et cela a entraîné des fréquences d’images acceptables pour l’utilisateur. La plupart des moteurs diffusent uniquement des données de ressource en tant qu’activité en arrière-plan, où il n’a pas de secours approprié à la diffusion en continu intra-Frame haute priorité. Demander aux moteurs de mettre en œuvre qui éroderont certains des gains de charge processeur qu’ils recherchent en passant à Direct3D 12. Les développeurs de moteurs peuvent analyser leurs images en plusieurs phases pour offrir davantage d’opportunités pour les ressources réutilisables. et fonctionnent probablement avec les fournisseurs d’intergiciels (middleware) pour prendre en charge les ressources placées et les tas pour la réutilisation de la mémoire intra-Frame.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)
</dt> <dt>

[**CreateReservedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource)
</dt> <dt>

[Guide de programmation de Direct3D 12](directx-12-programming-guide.md)
</dt> <dt>

[Gestion de la mémoire](memory-management.md)
</dt> <dt>

[Liaison de ressource](resource-binding.md)
</dt> </dl>

 

