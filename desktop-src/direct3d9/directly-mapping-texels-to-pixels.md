---
description: Lors du rendu de la sortie 2D à l’aide de vertex prétransformés, vous devez veiller à ce que chaque zone Texel corresponde correctement à une zone de pixel unique, sinon une déformation de texture peut se produire.
ms.assetid: 6faeb1e3-ea6e-4cb1-a1e6-2a9a81b4c0c7
title: Mappage direct des texels à des pixels (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f86e9d05acff402128ddb83fc97898ff6a21d7c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916628"
---
# <a name="directly-mapping-texels-to-pixels-direct3d-9"></a>Mappage direct des texels à des pixels (Direct3D 9)

Lors du rendu de la sortie 2D à l’aide de vertex prétransformés, vous devez veiller à ce que chaque zone Texel corresponde correctement à une zone de pixel unique, sinon une déformation de texture peut se produire. En maîtrisant les principes de base du processus que Direct3D suit lors de la pixellisation et de la texturation des triangles, vous pouvez vous assurer que votre application Direct3D affiche correctement la sortie 2D.

![illustration d’un affichage de résolution de 6X6](images/maptex-fig1.png)

Le diagramme précédent montre les pixels modélisés comme des carrés. En réalité, toutefois, les pixels sont des points, et non des carrés. Chaque carré du diagramme précédent indique la zone allumée par le pixel, mais un pixel est toujours simplement un point au centre d’un carré. Cette distinction, bien qu’apparemment petite, est importante. Une meilleure illustration du même affichage est illustrée dans le diagramme suivant.

![illustration d’un affichage constitué de pixels](images/maptex-fig2.png)

Le diagramme précédent montre correctement chaque pixel physique en tant que point au centre de chaque cellule. La coordonnée de l’espace à l’écran (0,0) est située directement en haut à gauche du pixel, et par conséquent au centre de la cellule supérieure gauche. L’angle supérieur gauche de l’affichage est donc à (-0,5,-0,5), car il s’agit de 0,5 cellules à gauche et de 0,5 cellules en partant du pixel supérieur gauche. Direct3D affiche un quadruple avec des angles à (0, 0) et (4, 4), comme indiqué dans l’illustration suivante.

![illustration d’un plan d’un quadruple Quad non pixellisé entre (0, 0) et (4,4)](images/maptex-fig3.png)

L’illustration précédente montre où le quad mathématique est en rapport avec l’affichage, mais n’indique pas ce à quoi ressemblera une fois que Direct3D la pixellise et l’envoie à l’écran. En fait, il est impossible pour un affichage raster de remplir le quad exactement comme indiqué, car les bords du Quad ne coïncident pas avec les limites entre les cellules de pixels. En d’autres termes, étant donné que chaque pixel ne peut afficher qu’une seule couleur, chaque cellule de pixel est remplie avec une seule couleur ; Si l’affichage devait restituer le quad exactement comme indiqué, les cellules de pixels le long du bord de l’quadruple-mesure doivent afficher deux couleurs distinctes : bleu, qui est couvert par le quadruple et le blanc où seul l’arrière-plan est visible.

Au lieu de cela, le matériel graphique est chargé de déterminer les pixels à remplir pour rapprocher le quad. Ce processus est appelé pixellisation et est détaillé dans les [règles de pixellisation (Direct3D 9)](rasterization-rules.md). Pour ce cas particulier, le quad pixellisé est représenté dans l’illustration suivante.

![illustration d’un Quad non texturé dessiné de (0,0) à (4,4)](images/maptex-fig4.png)

Notez que le quad passé à Direct3D a des angles à (0, 0) et (4, 4), mais que la sortie pixellisée (l’illustration précédente) contient des angles à (-0.5,-0,5) et (3,5, 3.5). Comparez les deux illustrations précédentes pour le rendu des différences. Vous pouvez voir que la taille du rendu de l’affichage est correcte, mais qu’elle a été décalée par les cellules-0,5 dans les directions x et y. Toutefois, à l’exception des techniques d’échantillonnage multiple, il s’agit de la meilleure approximation possible du quadruple. (Voir l' [exemple antialias](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx) pour une couverture complète de l’échantillonnage multiple.) Sachez que si le rastériseur remplit chaque cellule du quadruple, la zone résultante serait de dimension 5 x 5 au lieu du 4 x 4 souhaité.

Si vous supposez que les coordonnées d’écran proviennent de l’angle supérieur gauche de la grille d’affichage au lieu du pixel supérieur gauche, le quadruple s’affiche exactement comme prévu. Toutefois, la différence devient évidente lorsque le quadruple reçoit une texture. L’illustration suivante montre la texture 4 x 4 que vous allez mapper directement sur le quadruple.

![illustration d’une texture 4x4](images/maptex-fig5.png)

Étant donné que la texture est de 4 x 4 texels et que le quad est de 4 x 4 pixels, vous pouvez vous attendre à ce que le quad texturé apparaisse exactement comme la texture, quel que soit l’emplacement de l’écran où le quadruple est dessiné. Toutefois, ce n’est pas le cas. même les modifications mineures de la position influencent le mode d’affichage de la texture. L’illustration suivante montre comment un quadruple entre (0, 0) et (4, 4) s’affiche après avoir été pixellisé et texturé.

![illustration d’un Quad texturé dessiné à partir de (0,0) et (4, 4)](images/maptex-fig6.png)

Le quadruple représenté dans l’illustration précédente montre la sortie texturée (avec un mode de filtrage linéaire et un mode d’adressage de serrage) avec la structure pixellisée superposée. Le reste de cet article explique exactement pourquoi la sortie ressemble à la façon dont elle se présente au lieu de regarder la texture, mais pour ceux qui veulent la solution, voici : les bords de la quadruple entrée doivent se trouver sur les lignes limites entre les cellules de pixels. En décalant simplement les coordonnées x et y de-0,5 unités, les cellules texels couvre parfaitement les cellules de pixels et le quad peut être parfaitement recréé à l’écran. (La dernière illustration de cette rubrique montre le Quad aux coordonnées corrigées.)

Les détails de la raison pour laquelle la sortie pixellisée n’a que peu de similarité avec la texture d’entrée sont directement liés à la façon dont les adresses Direct3D et les textures d’échantillons. Ce qui suit suppose que vous avez une bonne compréhension de l' [espace de coordonnées de texture](texture-coordinates.md) et du filtrage de [texture bilinéaire](bilinear-texture-filtering.md).

En revenons à notre investigation sur la sortie de pixel étrange, il est judicieux de remonter la couleur de sortie vers le nuanceur de pixels : le nuanceur de pixels est appelé pour chaque pixel sélectionné pour faire partie de la forme pixellisée. Le quadruple bleu plein représenté dans une illustration précédente peut avoir un nuanceur particulièrement simple :


```
float4 SolidBluePS() : COLOR
{ 
    return float4( 0, 0, 1, 1 );
} 
```



Pour le quad plaqué, le nuanceur de pixels doit être légèrement modifié :


```
texture MyTexture;

sampler MySampler = 
sampler_state 
{ 
    Texture = <MyTexture>;
    MinFilter = Linear;
    MagFilter = Linear;
    AddressU = Clamp;
    AddressV = Clamp;
};

float4 TextureLookupPS( float2 vTexCoord : TEXCOORD0 ) : COLOR
{
    return tex2D( MySampler, vTexCoord );
} 
```



Ce code suppose que la texture 4 x 4 est stockée dans MyTexture. Comme indiqué, l’échantillon de texture MySampler est défini pour effectuer un filtrage bilinéaire sur MyTexture. Le nuanceur de pixels est appelé une fois pour chaque pixel pixellisé, et chaque fois que la couleur retournée est la couleur de texture échantillonnée sur vTexCoord. Chaque fois que le nuanceur de pixels est appelé, l’argument vTexCoord est défini sur les coordonnées de texture à ce pixel. Cela signifie que le nuanceur demande à l’échantillonneur de texture la couleur de texture filtrée à l’emplacement exact du pixel, comme indiqué dans l’illustration suivante.

![illustration des emplacements d’échantillonnage des coordonnées de texture](images/maptex-fig7.png)

La texture (affichée superposée) est échantillonnée directement aux emplacements de pixels (représentés par des points noirs). Les coordonnées de texture ne sont pas affectées par la pixellisation (elles restent dans l’espace de l’écran projeté du Quad d’origine). Les points noirs indiquent où se trouvent les pixels de pixellisation. Les coordonnées de texture à chaque pixel sont facilement déterminées en interpolant les coordonnées stockées à chaque vertex : le pixel à (0,0) coïncide avec le vertex à (0,0); par conséquent, les coordonnées de texture à ce pixel sont simplement les coordonnées de texture stockées sur ce vertex, UV (0,0, 0,0). Pour le pixel à (3, 1), les coordonnées interpolées sont UV (0,75, 0,25), car ce pixel se situe à trois quarts de la largeur de la texture et d’un quart de sa hauteur. Ces coordonnées interpolées sont celles qui sont passées au nuanceur de pixels.

Les texels ne sont pas alignés avec les pixels de cet exemple ; chaque pixel (et par conséquent, chaque point d’échantillonnage) est positionné à l’angle de quatre texels. Étant donné que le mode de filtrage est défini sur linéaire, l’échantillonneur calcule la moyenne des couleurs des quatre texels partageant cet angle. Cela explique pourquoi le pixel attendu est en fait trois-quarts gris plus un quart rouge, le pixel supposé être vert est un demi-gris plus un quart rouge plus un quart de vert, et ainsi de suite.

Pour résoudre ce problème, il vous suffit de mapper correctement le Quad aux pixels sur lesquels il sera pixellisé et de mapper correctement les texels sur les pixels. L’illustration suivante montre les résultats du dessin du même quadruple entre (-0,5,-0,5) et (3,5, 3,5), qui est le quadruple à partir du début.

![illustration d’un Quad texturé qui correspond au Quad pixellisé](images/maptex-fig8.png)

L’illustration ci-dessus montre que le quad (indiqué dans (-0,5,-0,5) à (3,5, 3,5)) correspond exactement à la zone pixellisée.

## <a name="summary"></a>Résumé

En résumé, les pixels et les texels sont en fait des points, pas des blocs solides. L’espace à l’écran provient du pixel supérieur gauche, mais les coordonnées de texture proviennent de l’angle supérieur gauche de la grille de la texture. Plus important encore, n’oubliez pas de soustraire 0,5 unités des composants x et y de vos positions de vertex lorsque vous travaillez dans un espace d’écran transformé afin d’aligner correctement les éléments de texture avec les pixels.

Le code suivant est un exemple de décalage des vertex d’un carré 256 par 256 pour afficher correctement une texture 256 par 256 dans l’espace d’écran transformé.


```C++
//define FVF with vertex values in transformed screen space
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW|D3DFVF_TEX1)

struct CUSTOMVERTEX
{
    FLOAT x, y, z, rhw; // position
    FLOAT tu, tv;       // texture coordinates
};

//unadjusted vertex values
float left = 0.0f;
float right = 255.0f;
float top = 0.0f;
float bottom = 255.0f;


//256 by 256 rectangle matching 256 by 256 texture
CUSTOMVERTEX vertices[] =
{
    { left,  top,    0.5f, 1.0f, 0.0f, 0.0f}, // x, y, z, rhw, u, v
    { right, top,    0.5f, 1.0f, 1.0f, 0.0f},
    { right, bottom, 0.5f, 1.0f, 1.0f, 1.0f},
    { left,  top,    0.5f, 1.0f, 0.0f, 0.0f},
    { right, bottom, 0.5f, 1.0f, 1.0f, 1.0f},
    { left,  bottom, 0.5f, 1.0f, 0.0f, 1.0f},
    
};
```




```C++
//adjust all the vertices to correctly line up texels with pixels 
for (int i=0; i<6; i++)
{
    vertices[i].x -= 0.5f;
    vertices[i].y -= 0.5f;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Coordonnées de texture](texture-coordinates.md)
</dt> </dl>

 

 



