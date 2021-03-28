---
title: Création de ressources en mosaïque
description: Les ressources en mosaïque sont créées en spécifiant l' \_ indicateur de mosaïque diverse de la ressource d3d11 \_ \_ quand vous créez une ressource.
ms.assetid: DED2B70C-1E95-4A85-A818-FD32165FBF6C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd6e2c0e457bfd8534d3a42c6f658095b3349572
ms.sourcegitcommit: 4dcafeb002cbee4f6028b32a956ec22cb95cbc44
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/13/2019
ms.locfileid: "104381114"
---
# <a name="creating-tiled-resources"></a>Création de ressources en mosaïque

Les ressources en mosaïque sont créées en spécifiant l’indicateur de [**\_ \_ \_ mosaïque diverse de la ressource d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) quand vous créez une ressource.

Les restrictions sur le moment où vous pouvez utiliser des [**ressources d3d11 en \_ \_ \_ mosaïque diverse**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) pour créer une ressource sont décrites dans [paramètres de création de ressources en mosaïque](tiled-resource-creation-parameters.md).

Le stockage d’une ressource non en mosaïque est alloué dans le système graphique lors de la création de la ressource. Par exemple, quand vous appelez [**ID3D11Device :: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) pour créer un tableau de textures 2D, le système graphique alloue le stockage pour ces textures 2D. Quand une ressource en mosaïque est créée, le système graphique n’alloue pas le stockage pour le contenu de la ressource. Au lieu de cela, quand une application crée une ressource en mosaïque, le système graphique effectue une réservation d’espace d’adressage uniquement pour la zone de la surface en mosaïque, puis permet au mappage des vignettes d’être contrôlé par l’application. Le « mappage » d’une vignette est simplement l’emplacement physique dans la mémoire qu’une vignette logique dans une ressource pointe (ou **null** pour une vignette non mappée). Ne confondez pas ce concept avec la notion de mappage d’une ressource Direct3D pour l’accès au processeur, qui, malgré l’utilisation du même nom, est complètement indépendant. Vous serez en mesure de définir et de modifier le mappage de chaque vignette individuellement si nécessaire, sachant que toutes les vignettes d’une surface n’ont pas besoin d’être mappées à la fois, ce qui permet d’utiliser efficacement la quantité de mémoire disponible.

Cette section fournit plus d’informations sur la création de ressources en mosaïque.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                             | Description                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Mappages dans un pool de vignettes](mappings-are-into-a-tile-pool.md)<br/>                                     | Lorsqu’une ressource est créée avec l’indicateur de [**\_ \_ \_ mosaïque diverse de la ressource d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) , les vignettes qui composent la ressource proviennent d’un pointage sur des emplacements d’un pool de mosaïques. Un pool de mosaïques est un pool de mémoire (sauvegardé par une ou plusieurs allocations en arrière-plan, non visible par l’application). <br/> |
| [Paramètres de création de ressources en mosaïque](tiled-resource-creation-parameters.md)<br/>                           | Il existe certaines contraintes sur le type de ressources Direct3D que vous pouvez créer avec l’indicateur de [**\_ \_ \_ mosaïque diverse de la ressource d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) . Cette section fournit les paramètres valides pour la création de ressources en mosaïque.<br/>                                                |
| [Espace d’adressage disponible pour les ressources en mosaïque](address-space-available-for-tiled-resources.md)<br/>         | Cette section spécifie l’espace d’adressage virtuel disponible pour les ressources en mosaïque. <br/>                                                                                                                                                                                                                           |
| [Paramètres de création d’un pool de vignettes](tile-pool-creation-parameters.md)<br/>                                     | Utilisez les paramètres de cette section pour définir des pools de mosaïques via l’API [**ID3D11Device :: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) . <br/>                                                                                                                                                                              |
| [Partage de ressources en mosaïque et partage d’appareils](tiled-resource-cross-process-and-device-sharing.md)<br/> | Les pools de mosaïques peuvent être partagés avec d’autres processus comme les ressources traditionnelles. Les ressources en mosaïque qui font référence à des pools de vignettes ne peuvent pas être partagées entre des appareils et des processus. Toutefois, des processus distincts peuvent créer leurs propres ressources en mosaïque qui mappent aux pools de mosaïques partagés entre ces ressources en mosaïque. <br/>          |
| [Opérations disponibles sur les ressources en mosaïque](operations-available-on-tiled-resources.md)<br/>                 | Cette section répertorie les opérations que vous pouvez effectuer sur les ressources en mosaïque.<br/>                                                                                                                                                                                                                                             |
| [Opérations disponibles sur les pools de vignettes](operations-available-on-tile-pools.md)<br/>                           | Cette section répertorie les opérations que vous pouvez effectuer sur les pools de mosaïques.<br/>                                                                                                                                                                                                                                                  |
| [Mode de mosaïque de la zone d’une ressource en mosaïque](how-a-tiled-resource-s-area-is-tiled.md)<br/>                       | Lorsque vous créez une ressource en mosaïque, les dimensions, la taille de l’élément de format et le nombre de des mipmaps et/ou de groupes de tableaux (le cas échéant) déterminent le nombre de vignettes nécessaires pour sauvegarder la surface d’exposition entière. <br/>                                                                                                 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ressources en mosaïque](tiled-resources.md)
</dt> </dl>

 

 





