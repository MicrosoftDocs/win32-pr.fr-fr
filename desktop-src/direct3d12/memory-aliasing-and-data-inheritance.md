---
title: Alias de mémoire et héritage de données
description: Les ressources placées et réservées peuvent avoir un alias de la mémoire physique dans un segment. Les ressources passées activent davantage de scénarios d’héritage de données que les ressources réservées lorsque l’indicateur partagé est défini pour le tas ou lorsque les ressources avec alias ont des dispositions de mémoire entièrement définies.
ms.assetid: 53C5804B-0F81-41AF-83D2-A96DCDFDC94A
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b584ef95f4ee89bc98940c8407427203a19f55046134e1d3c15cb672fef8fef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460919"
---
# <a name="memory-aliasing-and-data-inheritance"></a>Alias de mémoire et héritage de données

Les ressources placées et réservées peuvent avoir un alias de la mémoire physique dans un segment. Les ressources passées activent davantage de scénarios d’héritage de données que les ressources réservées lorsque l’indicateur partagé est défini pour le tas ou lorsque les ressources avec alias ont des dispositions de mémoire entièrement définies.

-   [Alias](#memory-aliasing-and-data-inheritance)
-   [Héritage de données](#data-inheritance)
-   [Rubriques connexes](#related-topics)

## <a name="aliasing"></a>Alias

Une barrière d’alias doit être émise entre l’utilisation de deux ressources qui partagent la même mémoire physique, même si l’héritage des données n’est pas souhaité. Les modèles d’utilisation simples doivent désigner au moins la ressource de destination impliquée dans une telle opération. Pour plus d’informations et pour obtenir des modèles d’utilisation avancée, consultez [**CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource) .

Après l’accès à une ressource, toutes les ressources qui partagent la mémoire physique avec cette ressource deviennent invalidées, sauf si l’héritage des données est autorisé. Les lectures de ressources invalidées entraînent un contenu de ressource non défini. Les écritures dans les ressources invalidées entraînent également un contenu de ressource non défini, à moins que deux conditions ne se produisent :

-   La ressource ne dispose pas de l’indicateur de \_ ressource D3D12 \_ autoriser le \_ \_ rendu cible ou de l’indicateur de \_ \_ ressource D3D12 autoriser le stencil de \_ \_ \_ profondeur \_ .
-   L’écriture est une opération de copie ou d’effacement d’une sous-ressource ou d’une vignette entière. L’initialisation des vignettes est uniquement disponible pour les ressources avec des SWIZZLE de 64 Ko non \_ \_ définis \_ et des SWIZZLE standard de la mosaïque de 64 Ko \_ \_ \_ .

Les invalidations qui se chevauchent sont limitées à des granularité plus petites, lorsque les dispositions fournissent des informations sur l’emplacement des données de Texel et lorsque les ressources se trouvent dans certains États de barrière de transition. Toutefois, les invalidations ne peuvent pas être plus petites que les granularité d’alignement des ressources.

Une granularité de l’alignement de la mémoire tampon est de 64 Ko, et la granularité d’alignement supérieure est prioritaire. Cela est important lorsque vous envisagez des textures de 4 Ko, car il peut se trouver dans une région de 64 Ko. Toutefois, un alias de mémoire tampon de la même région 64 Ko ne peut pas être utilisé conjointement avec ces textures de 4 Ko. L’application ne peut pas empêcher de manière fiable l’accès à la mémoire tampon d’intersecter les textures de 4 Ko, car les GPU sont autorisés à Swizzle 4 Ko de données de texture au sein de la région de 64Ko dans un modèle non défini.

\_ \_ \_ les mises en page de texture principale SWIZZLE de 64 Ko non définies, 64 Ko de \_ mosaïque \_ standard \_ SWIZZLE et de ligne \_ principale informent l’application que les granularité d’alignement qui se chevauchent ne sont plus valides. Par exemple : une application peut créer un tableau de texture de cible de rendu 2D avec 2 tranches de tableau, un niveau MIP unique et une \_ \_ disposition SWIZZLE non définie de mosaïque de 64 Ko \_ . Supposons que l’application comprend que chaque tranche de groupe occupe 100 mosaïques de 64 Ko. L’application peut renoncer à utiliser la tranche de tableau 0 et réutiliser cette mémoire pour une mémoire tampon d’une valeur de 6 Mo, une texture de ~ 6 Mo avec une disposition non définie, etc. Pour aller plus loin, supposez que l’application n’a plus besoin de la première vignette de la tranche de tableau 1. Ensuite, l’application peut également localiser une mémoire tampon de 64 Ko jusqu’à ce que le rendu nécessite à nouveau la première vignette de la tranche de tableau 1. L’application doit effectuer une suppression de vignette complète ou une copie pour réutiliser la première vignette avec le tableau de texture.

Toutefois, même les textures avec des dispositions définies comportent toujours des cas problématiques. Les tailles des ressources de texture peuvent varier considérablement par rapport à ce que l’application peut calculer elle-même, car certaines architectures d’adaptateur allouent de la mémoire supplémentaire pour les textures afin de réduire la bande passante effective pendant les scénarios de rendu courants. Les invalidations dans cette région de mémoire supplémentaire entraînent l’invalidation de la ressource entière. Pour plus d’informations, consultez [**GetResourceAllocationInfo**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo) .

## <a name="data-inheritance"></a>Héritage de données

Les ressources passées activent le plus d’héritage de données pour les textures, même avec des dispositions de mémoire non définies. Les applications peuvent imiter les fonctionnalités d’héritage de données que les ressources validées partagées activent en localisant deux textures avec des propriétés de ressource identiques au même décalage dans un tas partagé. L’intégralité de la description de la ressource doit être identique, y compris la valeur Clear optimisée et le type de la méthode de création de ressource (placée ou réservée). Toutefois, les deux ressources peuvent avoir des États de cloisonnement de transition initiaux différents.

Les ressources réservées permettent l’héritage des données par mosaïque ; mais des restrictions existent couramment pour les États de barrière de transition de ressource.

Pour hériter des données, les deux ressources doivent se trouver dans un état de barrière de transition de ressource compatible :

-   Pour les mémoires tampons, les textures d’accès simultanées et les textures entre les adaptateurs, l’état de transition des ressources n’est pas important et tous les États sont « compatibles ».
-   Pour les textures réservées sans les propriétés précédentes ou pour l’héritage des données par mosaïque par le biais de la mosaïque 64 Ko \_ \_ non définie \_ SWIZZLE ou 64 Ko \_ de la mosaïque \_ standard \_ SWIZZLE, l’état de la barrière de transition des ressources incluant la vignette doit être dans l’État commun.
-   Pour toutes les autres textures, où les descriptions des ressources correspondent exactement, l’état de la barrière de transition des ressources pour chaque paire de sous-ressources correspondante doit :
    -   Être dans l’État commun.
    -   Être égal lorsque l’État a le même indicateur GPU-Write.

Lorsque le GPU prend en charge les Swizzle standard, les mémoires tampons et les textures Swizzle standard peuvent être affectées de la même mémoire et hériter de données. L’application peut manipuler des texels à partir de la représentation de la mémoire tampon, car le modèle Swizzle standard décrit comment les texels sont disposés en mémoire. Le modèle de Swizzle visible par le processeur est équivalent au modèle de Swizzle visible par le GPU vu dans les tampons.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sous-allocation au sein des tas](suballocation-within-heaps.md)
</dt> </dl>

 

 




