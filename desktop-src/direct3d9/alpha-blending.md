---
description: La fusion alpha est utilisée pour afficher une image dont les pixels sont transparents ou semi-transparents.
ms.assetid: 553b0bc8-1bd8-4282-9260-cdc5f2b8788d
title: Fusion alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f4ae2883c7a9a92ba1b62306dc26bf09d0d9947
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111123"
---
# <a name="alpha-blending-direct3d-9"></a>Fusion alpha (Direct3D 9)

La fusion alpha est utilisée pour afficher une image dont les pixels sont transparents ou semi-transparents. Outre un canal de couleur rouge, vert et bleu, chaque pixel d’une bitmap Alpha possède un composant de transparence appelé « canal alpha ». Le canal alpha contient généralement autant de bits qu’un canal de couleurs. Par exemple, un canal alpha 8 bits peut représenter 256 niveaux de transparence, à partir de 0 (le pixel entier est transparent) à 255 (le pixel entier est opaque). La liste ci-dessous présente certains effets spéciaux que vous pouvez créer à l’aide de la fusion alpha.

La couleur peut être définie avec ou sans valeurs alpha. La couleur sans alpha est la couleur RVB avec alpha est stockée en tant que ARGB. Les données de vertex, les données de matériau et les données de texture peuvent être utilisées pour fournir la transparence de l’objet. La mémoire tampon de trame peut également être utilisée pour générer des effets de transparence.

-   [Vertex alpha (Direct3D 9)](vertex-alpha.md)
-   [Matériau alpha (Direct3D 9)](material-alpha.md)
-   [Texture alpha (Direct3D 9)](texture-alpha.md)
-   [Mémoire tampon de trame alpha (Direct3D 9)](frame-buffer-alpha.md)
-   [Rendu de la cible Alpha (Direct3D 9)](render-target-alpha.md)

Les exemples qui illustrent alpha sont les suivants :

-   [Billboarding (Direct3D 9)](billboarding.md)
-   [Clouds, fumées et traces de vapeur (Direct3D 9)](clouds--smoke--and-vapor-trails.md)
-   [Incendie, halos et explosions (Direct3D 9)](fire--flares--and-explosions.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu Direct3D](direct3d-rendering.md)
</dt> </dl>

 

 



