---
description: Les premières images 3D générées par ordinateur, bien qu’elles soient généralement avancées pour leur temps, ont tendance à avoir un aspect plastique brillant.
ms.assetid: 548ae140-c746-4fab-8000-421289d4f0a2
title: Concepts de base de la texturation (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 799504d2bb7f57952d55ca541155be09d10fed1a03a038d50d98069c2f1c1243
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952599"
---
# <a name="basic-texturing-concepts-direct3d-9"></a>Concepts de base de la texturation (Direct3D 9)

Les premières images 3D générées par ordinateur, bien qu’elles soient généralement avancées pour leur temps, ont tendance à avoir un aspect plastique brillant. Ils n’ont pas les mêmes types de marquages, tels que les scuffs, les fissures, les empreintes digitales et les taches, qui donnent aux objets 3D une complexité visuelle réaliste. Au cours des dernières années, les textures ont acquis la popularité des développeurs en tant qu’outil pour améliorer le réalisme des images 3D générées par ordinateur.

Dans son utilisation quotidienne, la texture de mot fait référence à la régularité ou à l’irrégularité d’un objet. Toutefois, dans les graphiques informatiques, une texture est une image bitmap de couleurs de pixels qui donne à un objet l’apparence de la texture.

Étant donné que les textures Direct3D sont des bitmaps, n’importe quelle bitmap peut être appliquée à une primitive Direct3D. Par exemple, les applications peuvent créer et manipuler des objets qui semblent avoir un modèle de grain de bois. L’herbe, le saleté et les roches peuvent être appliqués à un ensemble de primitives 3D formant une colline. Le résultat est un Hillside réaliste. Vous pouvez également utiliser la texturation pour créer des effets tels que des signes sur une route, des strates de roches dans une falaise ou l’apparence d’un marbre sur un étage.

En outre, Direct3D prend en charge des techniques de texturisation plus avancées, telles que la fusion de textures, avec ou sans transparence et un mappage de lumière. Pour plus d’informations, consultez [fusion de texture (Direct3D 9)](texture-blending.md) et [mappage de lumière avec des textures (Direct3D 9)](light-mapping-with-textures.md).

Si votre application crée un périphérique de couche d’abstraction matérielle (HAL) ou un périphérique logiciel, il peut utiliser des textures 8, 16, 24, 32, 64 ou 128 bits.

Des informations supplémentaires sont contenues dans les rubriques suivantes.

-   [Modes d’adressage de la texture (Direct3D 9)](texture-addressing-modes.md)
-   [Régions de modification de texture (Direct3D 9)](texture-dirty-regions.md)
-   [Palettes de texture (Direct3D 9)](texture-palettes.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Textures Direct3D](direct3d-textures.md)
</dt> </dl>

 

 



