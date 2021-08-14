---
title: Mappage de texture par défaut
description: L’utilisation du mappage de texture par défaut réduit la copie et l’utilisation de la mémoire tout en partageant des données d’image entre le GPU et le processeur.
ms.assetid: 77AF4BFA-09B5-4181-9408-002764F2A923
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edc81fc1bf59a974f9bd901fc96d43afc16019edce68fbaabfbf3259c0d4a3b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752289"
---
# <a name="default-texture-mapping"></a>Mappage de texture par défaut

L’utilisation du mappage de texture par défaut réduit la copie et l’utilisation de la mémoire tout en partageant des données d’image entre le GPU et le processeur. Toutefois, il ne doit être utilisé que dans des situations spécifiques. La disposition standard Swizzle évite la copie ou la swizzling des données dans plusieurs dispositions.

-   [Vue d'ensemble](#overview)
-   [API D3D 11.3](#d3d113-apis)
-   [Rubriques connexes](#related-topics)

## <a name="overview"></a>Vue d’ensemble

Le mappage des textures par défaut ne doit pas être le premier choix pour les développeurs. Les développeurs doivent d’abord coder de manière discrète avec GPU (autrement dit, ils n’ont pas d’accès au processeur pour la majorité des textures et les télécharger avec [**CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1)). Toutefois, dans certains cas, le processeur et le GPU peuvent interagir si fréquemment sur les mêmes données, ce qui permet de réduire les textures par défaut pour économiser de l’énergie ou pour accélérer une conception particulière sur des cartes ou des architectures spécifiques. Les applications doivent détecter ces cas et optimiser les copies inutiles.

Dans D3D 11.3, les textures créées \_ avec \_ une disposition de texture d3d11 \_ non définie (un membre de l’énumération de [**\_ \_ Présentation de texture d3d11**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_texture_layout) ) et aucun accès à l’UC n’est le plus efficace pour un rendu et un échantillonnage GPU fréquents. Lors des tests de performances, ces textures doivent être comparées à la \_ \_ disposition de texture d3d11 \_ non définie avec l’accès de l’UC, et à la disposition de \_ texture d3d11 \_ \_ 64 Ko \_ standard \_ SWIZZLE avec accès de l’UC, et à la \_ \_ \_ ligne de disposition de texture d3d11 \_ principale pour la prise en charge entre les adaptateurs.

L’utilisation \_ de \_ la disposition de texture d3d11 \_ non définie avec l’accès de l’UC active les méthodes [**WriteToSubresource**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-writetosubresource), [**ReadFromSubresource**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-readfromsubresource), [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) (en évitant l’accès à l’application au pointeur) et le [**mappage**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap), mais peut sacrifier l’efficacité de l’accès GPU. Utilisation \_ de la \_ disposition de texture d3d11 \_ 64 Ko \_ standard \_ SWIZZLE avec accès à l’UC active **WriteToSubresource**, **ReadFromSubresource**, **Map** (qui retourne un pointeur valide vers l’application) et unout. Il peut également sacrifier l’efficacité de l’accès au GPU plus que la \_ disposition de texture d3d11 \_ \_ non définie avec l’accès au processeur.

En général, les applications doivent créer la majorité des textures comme étant accessibles au GPU uniquement, et avec une disposition de texture D3D11 non \_ \_ \_ définie.

Avant la fonctionnalité de mappage des textures par défaut, il n’existait qu’une seule disposition standardisée pour les données multidimensionnelles : « linéaire », également appelée « ligne-principale ». Les applications doivent éviter \_ les textures dynamiques de l’utilisation et de la mise \_ en lots lorsque la valeur par défaut de la carte est disponible. Les \_ textures dynamiques d’utilisation et de mise \_ en lots utilisent la disposition linéaire.

D3D 11.3 (et D3D12) introduisent une disposition de données multidimensionnelles standard. Cette opération est effectuée pour permettre à plusieurs unités de traitement de fonctionner sur les mêmes données sans copier les données ou swizzling les données entre plusieurs dispositions. Une mise en page standardisée permet de gagner de l’efficacité grâce à des effets réseau et permet aux algorithmes de faire des petits morceaux en supposant un modèle particulier.

Notez cependant que cette Swizzle standard est une fonctionnalité matérielle et peut ne pas être prise en charge par tous les GPU.

## <a name="d3d113-apis"></a>API D3D 11.3

Contrairement à D3D12, D3D 11.3 ne prend pas en charge le mappage de texture par défaut. vous devez donc interroger [**d3d11 \_ Feature \_ Data \_ d3d11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2). Les Swizzle standard doivent également être interrogés avec un appel à [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) et la vérification du `StandardSwizzle64KBSupported` champ de données de la **\_ fonctionnalité d3d11 \_ \_ d3d11 \_ OPTIONS2**.

Le mappage de texture de référence des API suivantes :

Énumérations

-   [**D3d11 \_ \_Disposition**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_texture_layout) de la texture : contrôle le modèle Swizzle des textures par défaut et active la prise en charge des cartes sur les textures par défaut.
-   [**D3d11 \_ FONCTIONNALITÉ**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) : référence [**les \_ données de fonctionnalités d3d11 \_ \_ d3d11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2).
-   [**D3d11 \_ \_ \_ Indicateur de copie de vignette**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : contient des indicateurs pour copier des ressources en mosaïque swizzled vers et à partir de mémoires tampons linéaires.

Structures

-   [**D3d11 \_ TEXTURE2D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture2d_desc1) : décrit une texture 2D. Notez la \_ \_ structure d’assistance CD3D11 TEXTURE2D DESC1.
-   [**D3d11 \_ TEXTURE3D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture3d_desc1) : décrit une texture 3D. Notez la \_ \_ structure d’assistance CD3D11 TEXTURE3D DESC1.

Méthodes

-   [**ID3D11Device3 :: CreateTexture2D1**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11device3-createtexture2d1) : crée un tableau de textures 2D.
-   [**ID3D11Device3 :: CreateTexture3D1**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11device3-createtexture3d1) : crée une texture 3D unique.
-   [**ID3D11Device3 :: WriteToSubresource**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-writetosubresource) : copie les données dans une \_ \_ texture par défaut d’utilisation d3d11 qui a été mappée à l’aide de [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).
-   [**ID3D11Device3 :: ReadFromSubresource**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-readfromsubresource) : copie les données d’une \_ \_ texture par défaut d’utilisation d3d11 qui a été mappée à l’aide de [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).
-   [**ID3D11DeviceContext :: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) : obtient un pointeur vers les données contenues dans une sous-ressource et refuse l’accès GPU à cette sous-ressource.
-   [**ID3D11DeviceContext :: DEMAPPAGE**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) : invalide le pointeur vers une ressource et réactive l’accès du GPU à cette ressource.
-   [**ID3D11Texture2D1 :: GetDesc1**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11texture2d1-getdesc1) : obtient les propriétés d’une ressource de texture 2D.
-   [**ID3D11Texture3D1 :: GetDesc1**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11texture3d1-getdesc1) : obtient les propriétés d’une ressource de texture 3D.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctionnalités Direct3D 11,3](direct3d-11-3-features.md)
</dt> </dl>

 

 




