---
title: Optimisations UMA les textures accessibles par le processeur et les Swizzle standard
description: Les GPU (Universal Memory Architecture, UMA) offrent des avantages en termes de performances par rapport aux GPU discrets, en particulier lors de l’optimisation des appareils mobiles.
ms.assetid: 26C41948-9625-4786-BBDF-552D1F8A2437
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47725702676d385d607fa87533680b9ffe0fc0df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293627"
---
# <a name="uma-optimizations-cpu-accessible-textures-and-standard-swizzle"></a>Optimisations UMA : textures accessibles par le processeur et Swizzle standard

Les GPU (Universal Memory Architecture, UMA) offrent des avantages en termes de performances par rapport aux GPU discrets, en particulier lors de l’optimisation des appareils mobiles. L’octroi d’un accès processeur aux ressources lorsque le GPU est UMA peut réduire la quantité de copie qui se produit entre le processeur et le GPU. Bien que nous ne recommandons pas aux applications d’accéder aux ressources de toutes les ressources des conceptions UMA, il est possible d’améliorer l’efficacité en donnant aux ressources des droits d’accès au processeur. Contrairement aux GPU discrètes, le processeur peut techniquement avoir un pointeur vers toutes les ressources auxquelles le GPU peut accéder.

-   [Vue d’ensemble des textures accessibles par le processeur](#overview-of-cpu-accessible-textures)
-   [Vue d’ensemble des Swizzle standard](#overview-of-standard-swizzle)
-   [API](#apis)
-   [Rubriques connexes](#related-topics)

## <a name="overview-of-cpu-accessible-textures"></a>Vue d’ensemble des textures accessibles par le processeur

Les textures accessibles par le processeur, dans le pipeline Graphics, sont une fonctionnalité de l’architecture UMA, qui permet aux UC d’accéder en lecture et en écriture aux textures. Sur les GPU discrètes les plus courants, l’UC n’a pas accès aux textures dans le pipeline Graphics.

Les bonnes pratiques générales pour les textures consistent à prendre en charge les GPU discrètes, ce qui implique généralement de suivre les processus de [chargement des données de texture par le biais de mémoires tampons](upload-and-readback-of-texture-data.md), résumé comme suit :

-   Aucun accès de l’UC n’est nécessaire pour la majorité des textures.
-   Définition de la disposition de texture sur la \_ disposition de texture D3D12 \_ \_ inconnue.
-   Chargement des textures dans le GPU avec [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).

Toutefois, dans certains cas, le processeur et le GPU peuvent interagir si fréquemment sur les mêmes données, ces textures de mappage deviennent utiles pour économiser de l’énergie ou pour accélérer une conception particulière sur des cartes ou des architectures particulières. Les applications doivent détecter ces cas et optimiser les copies inutiles. Dans ce cas, pour des performances optimales, tenez compte des points suivants :

-   Démarrez uniquement les meilleures performances de mappage des textures lorsque l’architecture des données de la [**\_ fonctionnalité \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture):: UMA a la valeur true. Faites ensuite attention à *CacheCoherentUMA* si vous décidez des propriétés du cache de l’UC à choisir sur le segment de mémoire.

-   L’utilisation de l’accès au processeur pour les textures est plus complexe que pour les mémoires tampons. Les dispositions de texture les plus efficaces pour les GPU sont rarement des lignes \_ majeures. En fait, certains GPU peuvent uniquement prendre en charge les \_ textures principales de ligne lors de la copie des données de texture.

-   Les GPU UMA doivent universellement tirer parti d’une optimisation simple pour réduire les temps de chargement de niveau. Après avoir reconnu la UMA, l’application peut optimiser le [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) initial pour remplir les textures que le GPU ne modifiera pas. Au lieu de créer la texture dans un segment de mémoire avec le \_ type de segment D3D12 \_ \_ par défaut et de marshaler les données de texture via, l’application peut utiliser [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) pour éviter de comprendre la disposition de texture réelle.

-   Dans D3D12, les textures créées \_ avec \_ la mise en page de texture D3D12 \_ sont inconnues et aucun accès au processeur n’est le plus efficace pour un rendu et un échantillonnage GPU fréquents. Lors des tests de performances, ces textures doivent être comparées à la \_ \_ mise en page de texture D3D12 \_ inconnue avec l’accès de l’UC, à la \_ mise en \_ page de texture D3D12 \_ standard \_ SWIZZLE avec accès au processeur et à la \_ \_ \_ ligne de disposition de texture D3D12 \_ principale pour la prise en charge des adaptateurs

-   L’utilisation \_ \_ de la mise en forme de texture D3D12 \_ inconnue avec l’accès de l’UC active les méthodes [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource), [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource), [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (en évitant l’accès à l’application au pointeur) et le [**mappage**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap), mais peut sacrifier l’efficacité de l’accès GPU.

-   À l' \_ aide \_ de la disposition de texture D3D12 \_ standard \_ SWIZZLE avec accès de l’UC active [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource), [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource), [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (qui retourne un pointeur valide vers l’application) et [**DEMAPPAGE**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap). Elle peut également sacrifier l’efficacité de l’accès au GPU plus que la \_ \_ mise en page de texture D3D12 \_ inconnue avec l’accès au processeur.

## <a name="overview-of-standard-swizzle"></a>Vue d’ensemble des Swizzle standard

D3D12 (et D3D 11.3) introduisent une disposition de données multidimensionnelles standard. Cette opération est effectuée pour permettre à plusieurs unités de traitement de fonctionner sur les mêmes données sans copier les données ou swizzling les données entre plusieurs dispositions. Une mise en page standardisée permet de gagner de l’efficacité grâce à des effets réseau et permet aux algorithmes de faire des petits morceaux en supposant un modèle particulier.

Pour obtenir une description détaillée des dispositions de texture, reportez-vous à la [**\_ \_ Présentation de texture D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout).

Notez cependant que cette Swizzle standard est une fonctionnalité matérielle et peut ne pas être prise en charge par tous les GPU.

Pour obtenir des informations générales sur swizzling, reportez-vous à la [courbe ordre de plan](https://en.wikipedia.org/wiki/Z-order_curve).

## <a name="apis"></a>API

Contrairement à D3D 11.3, D3D12 prend en charge le mappage de texture par défaut. il n’est donc pas nécessaire d’interroger les [**\_ \_ \_ \_ options D3D12 des données de la fonctionnalité D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options). Toutefois, D3D12 ne prend pas toujours en charge les Swizzle standard. cette fonctionnalité doit être interrogée avec un appel à [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) et la vérification du champ *StandardSwizzle64KBSupported* des **\_ \_ \_ \_ options** D3D12 des données de la fonctionnalité D3D12.

Le mappage de texture de référence des API suivantes :

Énumérations

-   [**D3D12 \_ \_Disposition**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) de la texture : contrôle le modèle Swizzle des textures par défaut et active la prise en charge des cartes sur les textures accessibles par le processeur.

Structures

-   [**D3D12 \_ \_Description**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) de la ressource : décrit une ressource, telle qu’une texture, il s’agit d’une structure largement utilisée.
-   [**D3D12 \_ \_Description du tas**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) : décrit un segment de mémoire.

Méthodes

-   [**ID3D12Device :: CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) : crée une ressource unique et un tas de stockage de la taille et de l’alignement appropriés.
-   [**ID3D12Device :: CreateHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap) : crée un tas pour une mémoire tampon ou une texture.
-   [**ID3D12Device :: CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource) : crée une ressource placée dans un tas spécifique, généralement une méthode plus rapide pour créer une ressource que [**CreateHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap).
-   [**ID3D12Device :: CreateReservedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource) : crée une ressource qui est réservée, mais qui n’est pas encore validée ou placée dans un segment de mémoire.
-   [**ID3D12CommandQueue :: UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) : met à jour les mappages des emplacements de mosaïques dans les ressources en mosaïque aux emplacements de mémoire dans un tas de ressources.
-   [**ID3D12Resource :: Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) : obtient un pointeur vers les données spécifiées dans la ressource et refuse l’accès au GPU à la sous-ressource.
-   [**ID3D12Resource :: GetDesc**](id3d12resource-getdesc.md) : obtient les propriétés de ressource.
-   [**ID3D12Heap :: GetDesc**](id3d12heap-getdesc.md) obtient les propriétés du tas.
-   [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) : copie les données d’une texture qui a été mappée à l’aide de [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map).
-   [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) : copie les données dans une texture qui a été mappée à l’aide de [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map).

Les ressources et les tas parents ont des exigences d’alignement :

-   D3D12 \_ \_ \_ \_ alignement du positionnement des ressources MSAA par défaut \_ (4 Mo) pour les textures à échantillons multiples.
-   D3D12 \_ \_ \_ alignement du positionnement des ressources par défaut \_ (64 Ko) pour les textures et les mémoires tampons d’échantillon unique.
-   La copie linéaire des sous-ressources doit être alignée sur l’alignement de l' \_ \_ emplacement des données de texture D3D12 \_ \_ (512 octets), avec la largeur des lignes alignées sur l' \_ alignement des données de texture D3D12 \_ \_ \_ (256 octets).
-   Les vues de mémoire tampon constantes doivent être alignées sur l’alignement de l' \_ \_ emplacement des données de mémoire tampon constante D3D12 \_ \_ \_ (256 octets).

Les textures inférieures à 64 Ko doivent être traitées par le biais de [**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).

Avec les textures dynamiques (textures qui changent chaque trame), l’UC écrit de manière linéaire dans le tas de chargement, suivi d’une opération de copie GPU.

En général, pour créer des ressources dynamiques, créez un tampon de grande taille dans un tas de chargement (reportez-vous à [Suballocation dans les mémoires tampons](large-buffers.md)). Pour créer des ressources de mise en lots, créez un tampon de grande taille dans un segment de mémoire readback. Pour créer des ressources statiques par défaut, créez des ressources adjacentes dans un segment de mémoire par défaut. Pour créer des ressources avec alias par défaut, créez des ressources qui se chevauchent dans un tas par défaut.

[**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) et [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) réorganisent les données de texture entre une disposition de ligne principale et une disposition de ressources non définie. L’opération étant synchrone, l’application doit garder à l’esprit la planification de l’UC. L’application peut toujours fractionner la copie en régions plus petites ou planifier cette opération dans une autre tâche. Les ressources MSAA et les ressources de stencil de profondeur avec des mises en page de ressources opaques ne sont pas prises en charge par ces opérations de copie de l’UC et provoquent une défaillance. Les formats qui n’ont pas de taille de l’élément Power-of-Two ne sont pas non plus pris en charge et provoquent également un échec. Des codes de retour de mémoire insuffisante peuvent se produire.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Constantes principales**](constants.md)
</dt> <dt>

[**ID3D12Heap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[Liaison de ressource](resource-binding.md)
</dt> </dl>

 

 




