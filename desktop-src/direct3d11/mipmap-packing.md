---
title: Compression de mipmaps
description: En fonction du niveau de prise en charge des ressources en mosaïque, les des mipmaps avec certaines dimensions ne suivent pas les formes de mosaïque standard et sont considérées comme toutes regroupées les unes avec les autres d’une manière qui est opaque pour l’application.
ms.assetid: 3B416324-7656-495F-9BA9-8F5BE475ABC1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd29098b2668b5b4aab51dd26924d8f166df6fab9a4c5f8c78d0c8f5166b28a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408039"
---
# <a name="mipmap-packing"></a>Compression de mipmaps

En fonction du [niveau](tiled-resources-features-tiers.md) de prise en charge des ressources en mosaïque, les des mipmaps avec certaines dimensions ne suivent pas les formes de mosaïque standard et sont considérées comme toutes regroupées les unes avec les autres d’une manière qui est opaque pour l’application. Les niveaux supérieurs de la prise en charge ont des garanties plus larges sur les types de dimensions de surface qui tiennent dans les formes de mosaïque standard (et peuvent donc être mappées individuellement par les applications).

Ce qui peut varier entre les implémentations, c’est que, étant donné les dimensions, le format, le nombre de des mipmaps et les tranches de tableaux d’une ressource en mosaïque, un nombre M de MIPS (par tranche de groupe) peut être compressé dans un nombre N de vignettes. L’API [**ID3D11Device2 :: GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) permet au pilote de signaler à l’application les M et N suivants (parmi d’autres détails sur la surface que cette API signale comme standard et ne varient pas selon le fabricant du matériel). L’ensemble de vignettes pour les mips compressés est toujours de 64 Ko et peut être mappé individuellement en emplacements disparates dans un pool de mosaïques. Toutefois, la forme de pixel des vignettes et la façon dont les des mipmaps s’ajustent à l’ensemble des vignettes sont spécifiques à un fournisseur de matériel et trop complexes à exposer. Ainsi, les applications doivent mapper toutes les vignettes qui sont désignées comme compressées, ou aucune d’entre elles, à la fois. Dans le cas contraire, le comportement d’accès à la ressource en mosaïque n’est pas défini.

Pour les surfaces groupées, l’ensemble des mips et le nombre de vignettes empaquetées qui stockent ces MIPS (M et N décrits précédemment) s’appliquent individuellement pour chaque tranche de tableau.

Les API dédiées pour la copie des vignettes ([**ID3D11DeviceContext2 :: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) et [**ID3D11DeviceContext2 :: UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)) ne peuvent pas accéder aux mips compressés. Les applications qui souhaitent copier des données vers et depuis des mips compressés peuvent le faire à l’aide de toutes les API spécifiques à la ressource non en mosaïque pour la copie et le rendu des surfaces.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mode de mosaïque de la zone d’une ressource en mosaïque](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 




