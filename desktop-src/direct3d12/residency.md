---
title: Résidence
description: Un objet est considéré comme résident lorsqu’il est accessible par le GPU.
ms.assetid: 956F80D7-EEC8-4D88-B251-EE325614F31E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b842ce5b3e89c3877f50036e747a90f14104bce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012890"
---
# <a name="residency"></a>Résidence

Un objet est considéré comme *résident* lorsqu’il est accessible par le GPU.

-   [Budget de la résidence](#residency-budget)
-   [Ressources du tas](#heap-resources)
-   [Priorités de résidence](#residency-priorities)
    -   [Algorithme de priorité par défaut](#default-priority-algorithm)
-   [Programmation de la gestion des compétences](#programming-residency-management)
-   [Rubriques connexes](#related-topics)

## <a name="residency-budget"></a>Budget de la résidence

Les GPU ne prennent pas encore en charge les pannes de page, de sorte que les applications doivent valider les données dans la mémoire physique alors que le GPU peut y accéder. Ce processus est appelé « créer un résident » et doit être effectué pour la mémoire système physique et la mémoire vidéo discrète physique. Dans D3D12, la plupart des objets d’API encapsulent une certaine quantité de mémoire accessible par le GPU. Cette mémoire accessible par GPU est rendue résidente pendant la création de l’objet API, et supprimée lors de la destruction de l’objet API.

La quantité de mémoire physique disponible pour le processus est connue sous le nom de budget de la mémoire vidéo. Le budget peut fluctuer de façon notable au fur et à mesure de l’éveil et du sommeil des processus d’arrière-plan ; et fluctuent considérablement lorsque l’utilisateur passe à une autre application. L’application peut être avertie lorsque le budget change et interroger à la fois le budget actuel et la quantité de mémoire actuellement consommée. Si une application ne reste pas dans son budget, le processus sera gelé par intermittence pour permettre à d’autres applications de s’exécuter et/ou les API de création renverront un échec. L’interface [**IDXGIAdapter3**](/windows/desktop/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3) fournit les méthodes relatives à cette fonctionnalité, en particulier [**QueryVideoMemoryInfo**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo) et [**RegisterVideoMemoryBudgetChangeNotificationEvent**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent).

Les applications sont encouragées à utiliser une réservation pour indiquer la quantité de mémoire qu’elles ne peuvent pas sans. Dans l’idéal, les paramètres graphiques « bas » spécifiés par l’utilisateur, ou encore moins, constituent la valeur appropriée pour une telle réservation. La définition d’une réservation ne donnera jamais à une application un budget plus élevé qu’elle ne le recevrait normalement. Au lieu de cela, les informations de réservation permettent au noyau du système d’exploitation de réduire rapidement l’impact d’une grande sollicitation de la mémoire. Même la réservation n’est pas garantie d’être disponible pour l’application lorsque celle-ci n’est pas l’application de premier plan.

## <a name="heap-resources"></a>Ressources du tas

Bien que de nombreux objets API encapsulent une certaine mémoire accessible par GPU, les tas & ressources sont censés être les applications les plus significatives qui consomment et gèrent la mémoire physique. Un segment de mémoire est l’unité de niveau le plus bas pour gérer la mémoire physique. il est donc judicieux de vous familiariser avec ses propriétés de résidence.

-   Les segments de mémoire ne peuvent pas être partiellement résidents, mais des solutions de contournement existent avec les ressources réservées.
-   Les segments de mémoire doivent être budgétés dans le cadre d’un pool particulier. Les adaptateurs UMA possèdent un pool, tandis que les cartes discrètes ont deux pools. S’il est vrai que le noyau peut déplacer certains segments de mémoire sur des cartes discrètes de la mémoire vidéo vers la mémoire système, il le fait uniquement en dernier recours extrême. Les applications ne doivent pas s’appuyer sur le comportement de dépassement de budget du noyau et doivent plutôt se concentrer sur une bonne gestion du budget.
-   Les segments de mémoire peuvent être supprimés de la résidence, ce qui permet de paginer leur contenu sur le disque. Toutefois, la destruction des segments de mémoire est une technique plus fiable pour libérer la résidence sur toutes les architectures d’adaptateur. Sur les adaptateurs où le champ *theMaxGPUVirtualAddressBitsPerProcess* de la [**\_ \_ \_ \_ \_ \_ prise en charge des adresses virtuelles du GPU des données de fonctionnalités D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support) est proche de la taille du budget, la [**suppression**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-evict) ne permet pas de récupérer de façon fiable la résidence
-   La création du tas peut être lente ; Toutefois, il est optimisé pour le traitement des threads en arrière-plan. Il est recommandé de créer des tas sur les threads d’arrière-plan pour éviter de faire tourner le thread de rendu. Dans D3D12, plusieurs threads peuvent appeler en toute sécurité des routines de création simultanément.

D3D12 apporte plus de flexibilité et d’orthogonalité à son modèle de ressources afin d’activer davantage d’options pour les applications. Il existe trois types de ressources de haut niveau dans D3D12 : validées, placées et réservées.

-   Les ressources validées créent une ressource et un segment de mémoire en même temps. Le segment de mémoire est implicite et n’est pas accessible directement. Le tas est dimensionné correctement pour localiser la ressource entière dans le segment de mémoire.
-   Les ressources placées permettent de placer une ressource à un offset différent de zéro au sein d’un segment de mémoire. Les décalages doivent généralement être alignés à 64 Ko ; Toutefois, certaines exceptions existent dans les deux sens. Les ressources MSAA nécessitent un alignement de décalage de 4 Mo, et 4 Ko d’alignement de décalage sont disponibles pour les petites textures. Les ressources placées ne peuvent pas être déplacées ou remappées directement à un autre segment de mémoire. mais elles permettent un déplacement simple des données de ressources entre les tas. Après la création d’une ressource passée dans un segment de mémoire différent et la copie des données de ressource, de nouveaux descripteurs de ressources doivent être utilisés pour l’emplacement des données de la nouvelle ressource.
-   Les ressources réservées sont disponibles uniquement lorsque l’adaptateur prend en charge les ressources en mosaïque niveau 1 ou supérieur. Lorsqu’ils sont disponibles, ils proposent les techniques de gestion de résidence les plus avancées disponibles. mais tous les adaptateurs ne les prennent pas en charge actuellement. Ils permettent de remapper une ressource sans avoir à régénérer les descripteurs de ressources, les dépassements partiels de la résidence du niveau MIP et les scénarios de texture éparse, etc. Les types de ressources ne sont pas tous pris en charge, même lorsque les ressources réservées sont disponibles. un gestionnaire de délégation de site entièrement général basé sur des pages n’est pas encore faisable.

## <a name="residency-priorities"></a>Priorités de résidence

le Windows 10 Creators Update permet aux développeurs d’influencer les tas et les ressources qui seront préférés pour rester résidents lorsque la sollicitation de la mémoire nécessite que certaines de ses ressources soient rétrogradées. Cela permet aux développeurs de créer des applications plus performantes en tirant parti de la connaissance que le runtime ne peut pas déduire de l’utilisation de l’API. Il s’attend à ce que les développeurs soient plus confortables et en mesure de spécifier des priorités lorsqu’ils passent de l’utilisation des ressources validées aux ressources réservée, et en mosaïque.

L’application de ces priorités doit être plus facile que la gestion de deux budgets de mémoire dynamique, la rétrogradation manuelle et la promotion des ressources bettween, car les applications peuvent déjà le faire. Par conséquent, la conception de l’API de priorité de la résidence est à la une des priorités par défaut assignées à chaque segment de mémoire ou ressource comme créé. Pour plus d’informations, consultez [**ID3D12Device1 :: SetResidencyPriority**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device1-setresidencypriority) et l’énumération priorité de la [**délégation de \_ site \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_residency_priority) .

Avec les priorités, les développeurs sont censés :

-   Augmentez la priorité de quelques tas exceptionnels pour mieux atténuer l’impact de ces tas sur les performances rencontrées plus tôt ou plus fréquemment que leurs modèles d’accès naturel. Cette approche doit être exploitée par les applications portées à partir d’API graphiques telles que Direct3D 11 ou OpenGL, le modèle de gestion des ressources qui est très différent de celui de Direct3D 12.
-   Substituez presque toutes les priorités de tas avec le schéma de compartimentage propre à l’application, résolu, en fonction de la connaissance de la fréquence d’accès du programmeur, ou dynamique. un schéma fixe est plus simple à gérer qu’un schéma dynamique, mais peut être moins efficace et nécessiter le programmeur boîte comme un changement de modèle d’utilisation au cours du développement. Cette approche doit être exploitée par les applications créées avec la gestion des ressources de type Direct3D 12 à l’esprit, telles que celles qui utilisent la bibliothèque de résidence (en particulier les schémas dynamiques).

### <a name="default-priority-algorithm"></a>Algorithme de priorité par défaut

Une application ne peut pas spécifier de priorités utiles pour un segment de mémoire qu’elle tente de gérer sans avoir au préalable utilisé l’algorithme de priorité par défaut. Cela est dû au fait que la valeur de l’affectation d’une priorité particulière à un segment de mémoire est dérivée de sa priorité relative à d’autres tas classés par ordre de priorité qui sont en concurrence pour la même mémoire.

La stratégie choisie pour générer des priorités par défaut consiste à classer les tas en deux compartiments, en privilégiant (donnant une priorité plus élevée) les tas supposés être écrits fréquemment par le GPU sur les tas qui ne le sont pas.

Le compartiment haute priorité contient des tas et des ressources qui sont créés avec des indicateurs qui les identifient comme cibles de rendu, mémoires tampons de stencil de profondeur ou vues d’accès non ordonnées (UAVs). Il s’agit de valeurs de priorité affectées dans la plage commençant à la **priorité de délégation de D3D12 \_ \_ \_ élevée**. pour améliorer la priorité entre ces tas et les ressources, les 16 bits les plus bas de la priorité sont définis sur la taille du segment de mémoire ou de la ressource divisée par 10 Mo (en saturant à 0xFFFF pour les tas extrêmement volumineux). Cette définition de priorités supplémentaire favorise les tas et les ressources de plus grande taille.

Le compartiment à priorité basse contient tous les autres segments et ressources, auxquels sont affectées une valeur de priorité de la priorité de la **\_ résidence D3D12 \_ \_ normale**. Aucune autre définition de priorité n’est effectuée entre ces tas et les ressources.

## <a name="programming-residency-management"></a>Programmation de la gestion des compétences

Les applications simples peuvent être en mesure de créer des ressources validées uniquement jusqu’à ce qu’elles rencontrent des défaillances de mémoire insuffisante. En cas de défaillance, l’application peut détruire d’autres ressources ou objets API validés pour permettre à d’autres créations de ressources de s’effectuer correctement. Toutefois, il est vivement recommandé d’utiliser des applications simples pour surveiller les modifications de budget négatives et de détruire les objets API inutilisés à peu près une fois de cadre.

La complexité d’une conception de gestion des dépassements s’affiche lorsque vous essayez d’optimiser les architectures d’adaptateur ou d’incorporer des priorités de résidence. La budgétisation et la gestion discrètes de deux pools de mémoire discrète seront plus complexes que la gestion d’une seule, et l’affectation de priorités fixes sur une grande échelle peut devenir une charge de maintenance si les modèles d’utilisation évoluent. Le débordement des textures dans la mémoire système augmente la complexité, car la mauvaise ressource dans la mémoire système peut avoir un impact considérable sur la fréquence d’images. De plus, il n’existe aucune fonctionnalité simple permettant d’identifier les ressources qui tireraient parti d’une plus grande bande passante GPU ou tolérer une faible bande passante GPU.

Des conceptions encore plus compliquées interrogeront les fonctionnalités de l’adaptateur actuel. Ces informations sont disponibles dans [**\_ \_ \_ \_ la \_ \_ prise en charge des adresses virtuelles du GPU de données de la fonctionnalité D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support), de l' [**\_ \_ \_ architecture des données de fonctionnalités D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture), du [**\_ \_ \_ niveau des ressources en mosaïque D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)et du [**\_ \_ \_ niveau du tas de ressources D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_heap_tier).

Plusieurs parties d’une application sont susceptibles d’être reportées à l’aide de différentes techniques. Par exemple, certaines textures volumineuses et des chemins de code rarement testés peuvent utiliser des ressources validées, tandis que de nombreuses textures peuvent être désignées avec une propriété de streaming et utiliser une technique de ressource imposée générale.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ID3D12Heap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[Gestion de la mémoire](memory-management.md)
</dt> </dl>

 

 