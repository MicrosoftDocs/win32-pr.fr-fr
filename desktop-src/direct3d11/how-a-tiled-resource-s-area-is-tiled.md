---
title: Mode de mosaïque de la zone d’une ressource en mosaïque
description: Lorsque vous créez une ressource en mosaïque, les dimensions, la taille de l’élément de format et le nombre de des mipmaps et/ou de groupes de tableaux (le cas échéant) déterminent le nombre de vignettes nécessaires pour sauvegarder la surface d’exposition entière.
ms.assetid: 834E317F-CFFD-460C-9F89-793081BA1853
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ae1bf4ad1ca308fb3c93a36c4b3478aabdb0f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990980"
---
# <a name="how-a-tiled-resources-area-is-tiled"></a>Mode de mosaïque de la zone d’une ressource en mosaïque

Lorsque vous créez une ressource en mosaïque, les dimensions, la taille de l’élément de format et le nombre de des mipmaps et/ou de groupes de tableaux (le cas échéant) déterminent le nombre de vignettes nécessaires pour sauvegarder la surface d’exposition entière. La disposition pixel/octet dans les mosaïques est déterminée par l’implémentation de. Le nombre de pixels qui tiennent dans une vignette, selon la taille de l’élément de format, est fixe et identique, que vous utilisiez ou non un Swizzle standard.

Le nombre de vignettes qui seront utilisées par une taille de surface donnée et une largeur d’élément de format est bien défini et prévisible en fonction des tables des sections suivantes. Pour les ressources qui contiennent des des mipmaps ou des cas où les dimensions de surface ne remplissent pas de vignette, certaines contraintes existent et sont abordées dans la [compression mipmap](mipmap-packing.md).

Les différentes ressources en mosaïque peuvent pointer vers une mémoire identique avec des formats différents tant que les applications ne reposent pas sur les résultats de l’écriture dans la mémoire avec un format et en lisant avec une autre. Toutefois, dans des circonstances contraignantes, les applications peuvent reposer sur les résultats de l’écriture dans la mémoire avec un format et la lecture avec un autre si les formats sont dans la même famille de format (autrement dit, ils ont le même format parent sans type). Par exemple, les formats DXGI \_ \_ R8G8B8A8 \_ UNORM et dxgi \_ format \_ R8G8B8A8 \_ uint sont compatibles les uns avec les autres, mais pas avec le \_ format dxgi \_ \_ R16G16 UNORM. Une application doit faire correspondre de manière restrictive toutes les propriétés de ressource pour réinterpréter les données entre deux textures, car les modèles de mosaïques sont très prudentment non définis. Évidemment, cependant, le format est plus Lax. Les formats doivent uniquement être compatibles, comme illustré ci-dessus. Une exception est l’endroit où les données de saignée d’un alias de format vers un autre sont bien définies : si une vignette contient entièrement 0 pour tous ses bits, cette vignette peut être utilisée avec n’importe quel format qui interprète le contenu de la mémoire comme étant égal à 0 (quelle que soit la disposition de la mémoire). Par conséquent, une vignette peut être déplacée au format 0x00 au format DXGI \_ \_ R8 \_ UNORM, puis utilisée avec un format comme dxgi \_ \_ R32G32 \_ float et le contenu est toujours (0.0 f, 0.0 f).

La disposition des données dans une vignette peut dépendre des propriétés de ressource, de la sous-ressource dans laquelle elle réside et de l’emplacement de la mosaïque dans la sous-ressource. Les principales exceptions sont illustrées ci-dessus : les formats compatibles avec d’autres propriétés de ressource étant égaux et lorsque toutes les textures sont du même modèle.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                             | Description                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Restitution des sous-ressources Texture2D et Texture2DArray sous forme de mosaïque](texture2d-and-texture2darray-subresource-tiling.md)<br/> | Ces tableaux montrent comment les sous-ressources [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) et [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) sont présentées en mosaïque. <br/>                                                                                                          |
| [Restitution de la sous-ressource Texture3D sous forme de mosaïque](texture3d-subresource-tiling.md)<br/>                                       | Ce tableau montre comment les sous-ressources [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) sont présentées en mosaïque. <br/>                                                                                                                                                                            |
| [Mosaïque de mémoires tampons](buffer-tiling.md)<br/>                                                                     | Une ressource de [mémoire tampon](overviews-direct3d-11-resources-buffers.md) est divisée en mosaïques de 64 Ko, avec un espace vide dans la dernière vignette si la taille n’est pas un multiple de 64 Ko.<br/>                                                                                                  |
| [Compression de mipmaps](mipmap-packing.md)<br/>                                                                   | En fonction du [niveau](tiled-resources-features-tiers.md) de prise en charge des ressources en mosaïque, les des mipmaps avec certaines dimensions ne suivent pas les formes de mosaïque standard et sont considérées comme toutes regroupées les unes avec les autres d’une manière qui est opaque pour l’application. <br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de ressources en mosaïque](creating-tiled-resources.md)
</dt> </dl>

 

