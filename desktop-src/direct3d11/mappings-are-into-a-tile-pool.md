---
title: Mappages dans un pool de vignettes
description: Lorsqu’une ressource est créée avec l' \_ indicateur de mosaïque diverse de la ressource d3d11 \_ \_ , les vignettes qui composent la ressource proviennent d’un pointage sur des emplacements d’un pool de mosaïques.
ms.assetid: 1DBE23B2-A1E6-4491-9B74-4E92508A68FC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1537113d6685e39cab94445c8d3f16d406638820
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990908"
---
# <a name="mappings-are-into-a-tile-pool"></a>Mappages dans un pool de vignettes

Lorsqu’une ressource est créée avec l’indicateur de [**\_ \_ \_ mosaïque diverse de la ressource d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) , les vignettes qui composent la ressource proviennent d’un pointage sur des emplacements d’un pool de mosaïques. Un pool de mosaïques est un pool de mémoire (sauvegardé par une ou plusieurs allocations en arrière-plan, non visible par l’application). Le système d’exploitation et le pilote d’affichage gèrent ce pool de mémoire, et l’encombrement mémoire est facilement compréhensible par une application. Les ressources en mosaïque mappent des régions de 64 Ko en pointant sur des emplacements dans un pool de mosaïques. Un Fallout de cette installation permet à plusieurs ressources de partager et réutiliser les mêmes vignettes, et également de réutiliser les mêmes vignettes à différents emplacements au sein d’une ressource, si vous le souhaitez.

Le coût de la flexibilité de remplissage des vignettes pour une ressource à partir d’un pool de mosaïques est que la ressource doit effectuer la définition et la maintenance du mappage des vignettes dans le pool de mosaïques pour représenter les vignettes nécessaires pour la ressource. Les mappages de vignette peuvent être modifiés. En outre, toutes les vignettes d’une ressource n’ont pas besoin d’être mappées à la fois ; une ressource peut avoir des mappages **null** . Un mappage **null** définit une vignette comme n’étant pas disponible du point de vue de la ressource qui y accède.

Vous pouvez créer plusieurs pools de mosaïques, et n’importe quel nombre de ressources en mosaïque peut être mappé à un pool de mosaïques donné en même temps. Les pools de vignettes peuvent également être développés ou réduits. Pour plus d’informations, consultez [redimensionnement de pool de mosaïques](tile-pool-resizing.md). Une contrainte qui existe pour simplifier l’implémentation du pilote d’affichage et du runtime est qu’une ressource en mosaïque donnée ne peut avoir que des mappages dans un seul pool de mosaïques à la fois (par opposition à un mappage simultané à plusieurs pools de mosaïques).

La quantité de stockage associée à une ressource en mosaïque proprement dite (autrement dit, la mémoire de pool de mosaïques indépendante) est à peu près proportionnelle au nombre de vignettes réellement mappées au pool à un moment donné. Dans le matériel, cela se résume à la mise à l’échelle de l’empreinte mémoire pour le stockage des tables de pages avec la quantité de vignettes mappées (par exemple, en utilisant un modèle de table de pages à plusieurs niveaux, le cas échéant).

Le pool de mosaïques peut être considéré comme une abstraction logicielle complète qui permet aux applications Direct3D de programmer efficacement les tables de pages sur l’unité de traitement graphique (GPU) sans avoir à connaître les détails d’implémentation de bas niveau (ou gérer directement les adresses de pointeur). Les pools de mosaïques n’appliquent pas d’autres niveaux d’indirection dans le matériel. Les optimisations d’une table de page de niveau unique à l’aide de constructions telles que des répertoires de pages sont indépendantes du concept de pool de mosaïques.

Examinons le stockage que la table de page lui-même peut nécessiter dans le pire des cas (Toutefois, dans les implémentations de la pratique, vous n’avez besoin que d’un stockage à peu près proportionnel à ce qui est mappé).

Supposons que chaque entrée de table de pages soit 64 bits.

Pour l’accès à la taille de la table de pages le plus défavorable pour une seule surface, étant donné les limites de ressources dans Direct3D 11, supposons qu’une ressource en mosaïque est créée avec un format de bit par élément de 128 (par exemple, un nombre maximal de bits), de sorte qu’une vignette de 64 Ko ne contient que 4096 pixels. La taille de [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) maximale prise en charge de 16384 \* 16384 \* 2048 (mais avec un seul mipmap) nécessite environ 1 Go de stockage dans la table de page en cas de remplissage complet (à l’exception de des mipmaps) à l’aide des entrées de table de bits 64. L’ajout de des mipmaps augmenterait le stockage de table de pages entièrement mappé (cas le plus défavorable) d’une troisième, à environ 1,3 Go.

Ce cas donne accès à environ 10,6 téraoctets de mémoire adressable. Toutefois, il peut y avoir une limite sur la quantité de mémoire adressable, ce qui réduirait éventuellement les limites de la plage de téraoctets.

Un autre cas à prendre en compte est une ressource en mosaïque [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) unique de 16384 \* 16384 avec un format binaire par élément de 32, y compris des mipmaps. L’espace nécessaire dans une table de pages entièrement remplie serait 170KB à peu près avec des entrées de table de bits 64.

Enfin, prenons un exemple utilisant un format BC, par exemple BC7 avec 128 bits par mosaïque de 4 x 4. Il s’agit d’un octet par pixel. Un [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) de 16384 \* 16384 \* 2048, y compris des MIPMAPS, nécessite environ 85MB pour remplir entièrement cette mémoire dans une table de pages. Cela n’est pas une mauvaise considération. cela permet à une ressource en mosaïque de s’étendre sur 550 gigapixels (512 Go de mémoire dans ce cas).

Dans la pratique, rien près de ces mappages complets serait défini, étant donné que la quantité de mémoire physique disponible ne permettrait pas à quelque point près qu’il soit possible de le mapper et de le référencer à la fois. Toutefois, avec un pool de mosaïques, les applications peuvent choisir de réutiliser les vignettes (en guise d’exemple simple, en réutilisant efficacement une vignette de couleur noire pour les grandes régions noires dans une image), en utilisant efficacement le pool de mosaïques (autrement dit, les mappages de tables de pages) comme un outil pour la compression de mémoire.

Le contenu initial de la table de page a la **valeur null** pour toutes les entrées. Les applications ne peuvent pas non plus transmettre des données initiales pour le contenu de la mémoire de l’aire, car elles démarrent sans stockage de mémoire.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                   | Description                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Création d’un pool de vignettes](tile-pool-creation.md)<br/>                                                 | Un pool de mosaïques est créé via l’API [**ID3D11Device :: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) en passant l’indicateur de [**\_ \_ \_ \_ pool de mosaïques divers de la ressource d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) dans le membre **MiscFlags** de  la structure [**\_ \_ desc de mémoire tampon d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) vers laquelle pointe le paramètre pDesc. <br/> |
| [Redimensionnement d’un pool de vignettes](tile-pool-resizing.md)<br/>                                                 | Utilisez l’API [**ID3D11DeviceContext2 :: ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) pour augmenter un pool de mosaïques si l’application a besoin d’une plus grande plage de travail pour le mappage des ressources en mosaïque, ou pour réduire l’espace nécessaire. <br/>                                                                                                                    |
| [Suivi des risques ou ressources d’un pool de vignettes](hazard-tracking-versus-tile-pool-resources.md)<br/> | Pour les ressources qui ne sont pas en mosaïque, Direct3D peut empêcher certaines conditions de danger pendant le rendu, mais comme le suivi des risques se trouve au niveau de la mosaïque pour les ressources en mosaïque, le suivi des conditions de danger lors du rendu des ressources en mosaïque peut être trop onéreux. <br/>                                                                                                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de ressources en mosaïque](creating-tiled-resources.md)
</dt> </dl>

 

