---
description: La plupart des textures, comme les bitmaps, sont un tableau à deux dimensions de valeurs de couleur.
ms.assetid: vs|directx_sdk|~\texture_coordinates.htm
title: Coordonnées de texture (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dcf4c886c187aaa2218508a180e23644a544739
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482689"
---
# <a name="texture-coordinates-direct3d-9"></a>Coordonnées de texture (Direct3D 9)

La plupart des textures, comme les bitmaps, sont un tableau à deux dimensions de valeurs de couleur. Les textures de la carte d’environnement cubique sont une exception. Pour plus d’informations, consultez [mappage d’environnement cubique (Direct3D 9)](cubic-environment-mapping.md). Les différentes valeurs de couleur sont appelées élément de texture, ou Texel. Chaque Texel a une adresse unique dans la texture. L’adresse peut être considérée comme un numéro de colonne et de ligne, qui sont étiquetés vous et v, respectivement dans l’illustration suivante.

![illustration d’une adresse Texel sous forme de numéros de colonne et de ligne](images/uvcoordinates.jpg)

Les coordonnées de texture sont dans l’espace de texture. Autrement dit, ils sont relatifs à l’emplacement (0, 0) dans la texture. Quand une texture est appliquée à une primitive dans l’espace 3D, ses adresses Texel doivent être mappées en coordonnées d’objet. Ils doivent ensuite être traduits en coordonnées d’écran ou en pixels.

## <a name="mapping-texels-to-screen-space"></a>Mappage des texels à l’espace à l’écran

Direct3D mappe les texels dans l’espace de texture directement aux pixels de l’espace à l’écran, ce qui permet d’obtenir une plus grande efficacité. Ce processus de mappage est en fait un mappage inverse. Autrement dit, pour chaque pixel de l’espace à l’écran, la position de Texel correspondante dans l’espace de texture est calculée. La couleur de texture à l’emplacement ou autour de ce point est échantillonnée. Le processus d’échantillonnage est appelé filtrage de texture. Pour plus d’informations, consultez [filtrage de texture (Direct3D 9)](texture-filtering.md).

Chaque Texel dans une texture peut être spécifié par sa coordonnée Texel. Toutefois, pour mapper des texels sur des primitives, Direct3D requiert une plage d’adresses uniforme pour tous les texels dans toutes les textures. Par conséquent, elle utilise un schéma d’adressage générique dans lequel toutes les adresses Texel sont comprises dans la plage comprise entre 0,0 et 1,0 inclus. Les applications Direct3D spécifient des coordonnées de texture par rapport à vous, les valeurs v, comme les coordonnées cartésiennes 2D, sont spécifiées en termes de coordonnées x, y. Techniquement, le système peut réellement traiter des coordonnées de texture en dehors de la plage de 0,0 et 1,0, et utilise les paramètres que vous définissez pour l’adressage de la texture. Pour plus d’informations, consultez [modes d’adressage de texture (Direct3D 9)](texture-addressing-modes.md).

Cela est dû au fait que des adresses de texture identiques peuvent être mappées à différentes coordonnées texels dans différentes textures. Dans l’illustration suivante, l’adresse de la texture est (0.5, 1,0). Toutefois, étant donné que les textures sont de tailles différentes, l’adresse de texture est mappée à différents texels. La texture 1, sur la gauche, est 5x5. L’adresse de texture (0.5, 1.0) est mappée à Texel (2,4). La texture 2, sur la droite, est 7X7. L’adresse de texture (0.5, 1.0) est mappée à Texel (3,4).

![illustration du même mappage d’adresse de texture à différents texels sur différentes textures](images/texadr1.png)

Une version simplifiée du processus de mappage de Texel est présentée dans l’illustration suivante. Il est vrai que cet exemple est très simple. Pour plus d’informations, consultez [mappage direct des texels à des pixels (Direct3D 9)](directly-mapping-texels-to-pixels.md).

![illustration de pixel (carré de couleur) qui est mappée dans l’espace d’objet](images/texadr2.png)

Pour cet exemple, un pixel, indiqué à gauche de l’illustration, est idéal dans un carré de couleur. Les adresses des quatre angles du pixel sont mappées dans la primitive 3D dans l’espace de l’objet. La forme du pixel est souvent déformée en raison de la forme de la primitive dans l’espace 3D et de l’angle de visualisation. Les angles de la surface d’exposition sur la primitive qui correspondent aux angles du pixel sont ensuite mappés dans l’espace de texture. Le processus de mappage déforme à nouveau la forme du pixel, ce qui est courant. La valeur de couleur finale du pixel est calculée à partir des texels de la région vers laquelle les pixels sont mappés. Vous déterminez la méthode utilisée par Direct3D pour atteindre la couleur de pixel quand vous définissez la méthode de filtrage de texture. Pour plus d’informations, consultez [filtrage de texture (Direct3D 9)](texture-filtering.md).

Votre application peut affecter des coordonnées de texture directement aux vertex. Cette fonctionnalité vous permet de contrôler la partie d’une texture qui est mappée dans une primitive. Par exemple, supposons que vous créez une primitive rectangulaire qui a exactement la même taille que la texture de l’illustration suivante. Dans cet exemple, vous souhaitez que votre application mappe la texture entière sur l’ensemble du mur. Les coordonnées de la texture assignées à votre application aux sommets de la primitive sont (0.0, 0.0), (1,0, 0.0), (1.0, 1.0) et (0.0, 1.0).

![illustration d’un mur mappé à la texture](images/texadr3.png)

Si vous décidez de réduire d’une demie la hauteur du mur, vous pouvez déformer la texture pour l’ajuster au mur le plus petit, ou vous pouvez assigner des coordonnées de texture qui obligent Direct3D à utiliser la moitié inférieure de la texture.

Si vous décidez de déformer ou de mettre à l’échelle la texture pour l’ajuster au mur le plus petit, la méthode de filtrage de texture que vous utilisez influencera la qualité de l’image. Pour plus d’informations, consultez [filtrage de texture (Direct3D 9)](texture-filtering.md).

Si, à la place, vous décidez d’assigner des coordonnées de texture pour que Direct3D utilise la moitié inférieure de la texture pour le mur le plus petit, la texture coordonne l’affectation de votre application aux sommets de la primitive dans cet exemple : (0.0, 0.5), (1.0, 0.5), (1.0, 1.0) et (0.0, 1.0). Direct3D applique la moitié inférieure de la texture au mur.

Il est possible que les coordonnées de texture d’un vertex soient supérieures à 1,0. Lorsque vous affectez des coordonnées de texture à un vertex qui ne sont pas dans la plage comprise entre 0,0 et 1,0, vous devez également définir le mode d’adressage de la texture. Pour plus d’informations, consultez [modes d’adressage de texture (Direct3D 9)](texture-addressing-modes.md).

## <a name="texture-coordinates-and-texture-stages"></a>Coordonnées de texture et étapes de texture

Les coordonnées de texture sont associées à des textures par le biais d’étapes de texture. Les textures sont affectées aux étapes de texture avec SetTexture (stageIndex, pTexture). Consultez [**IDirect3DDevice9 :: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).

Un code de format de vertex flexible peut définir jusqu’à huit jeux de coordonnées de texture. Les données de coordonnée de texture sont fournies par l’utilisateur dans les données de vertex. Les données sont référencées à l’aide d’un index de base zéro : 0-7. Il existe jusqu’à huit étapes de fusion de texture. Une texture est associée à une étape particulière à l’aide de SetTexture (stageIndex, pTexture).

Une fois cette opération effectuée, tout ensemble de coordonnées de texture peut être utilisé par n’importe quelle étape. Chaque ensemble de coordonnées est associé à une étape à l’aide de SetTextureStageState (stageIndex, D3DTSS \_ TEXCOORDINDEX, textureCoordinateIndex). Consultez [**IDirect3DDevice9 :: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate). De cette façon, les étapes de fusion peuvent être configurées pour utiliser n’importe quelle texture et toute coordonnée de texture. Plusieurs étapes peuvent utiliser les mêmes textures ou coordonnées de texture.

Des informations supplémentaires sont contenues dans les rubriques suivantes.

-   [Formats de coordonnée de texture (Direct3D 9)](texture-coordinate-formats.md)
-   [Traitement des coordonnées de texture (Direct3D 9)](texture-coordinate-processing.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Textures Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
