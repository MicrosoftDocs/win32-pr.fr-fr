---
description: En bref, l’habillage de texture modifie la façon dont Direct3D pixellise les polygones texturés à l’aide des coordonnées de texture spécifiées pour chaque vertex.
ms.assetid: 00683d3f-3e3c-4ee4-9aec-a0d7fd9c8941
title: Habillage de texture (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c29ebe78bcfa237f46eacb247432185adedd1e53ae0774e767807269bb3bb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984764"
---
# <a name="texture-wrapping-direct3d-9"></a>Habillage de texture (Direct3D 9)

En bref, l’habillage de texture modifie la façon dont Direct3D pixellise les polygones texturés à l’aide des coordonnées de texture spécifiées pour chaque vertex. Lors de la pixellisation d’un polygone, le système interpole entre les coordonnées de la texture à chacun des sommets du polygone pour déterminer les texels à utiliser pour chaque pixel du polygone. Normalement, le système traite la texture comme un plan 2D, en interpolant les nouveaux texels en utilisant l’itinéraire le plus bref du point A dans une texture jusqu’au point B. Si le point A représente la position u, v (0,8, 0,1) et que le point B est à (0.1, 0.1), la ligne d’interpolation ressemble au diagramme suivant.

![diagramme d’une ligne d’interpolation entre deux points](images/interp1.png)

Notez que la distance la plus petite entre A et B dans cette illustration s’exécute approximativement au milieu de la texture. L’activation de l’encapsulation de la coordonnée u ou v-texture change la façon dont Direct3D perçoit l’itinéraire le plus rapide entre les coordonnées de texture dans les directions u et v. Par définition, l’habillage de texture amène le rastériseur à prendre l’itinéraire le plus bref entre les jeux de coordonnées de texture, en supposant que 0,0 et 1,0 coïncident. Le dernier bit est la partie délicate : vous pouvez imaginer que l’activation de l’habillage de texture dans une seule direction amène le système à traiter une texture comme si elle avait été entourée d’un cylindre. Par exemple, considérons le diagramme ci-dessous.

![diagramme d’une texture et deux points encapsulés autour d’un cylindre](images/interp2.png)

L’illustration précédente montre comment l’habillage dans la direction u affecte la façon dont le système interpole les coordonnées de texture. À l’aide des mêmes points que dans l’exemple pour les textures normales, ou non encapsulées, vous pouvez voir que l’itinéraire le plus rapide entre les points A et B n’est plus au milieu de la texture. C’est à présent dans la frontière que 0,0 et 1,0 existent ensemble. L’habillage dans l’axe v est similaire, à ceci près qu’il encapsule la texture autour d’un cylindre situé de son côté. L’habillage dans la direction u et la direction v est plus complexe. Dans ce cas, vous pouvez envisager la texture sous forme de tores, ou en anneau.

L’application pratique la plus courante pour l’habillage de texture consiste à effectuer un mappage d’environnement. En règle générale, un objet texturé avec une carte d’environnement apparaît très réfléchissant, affichant une image en miroir de l’environnement de l’objet dans la scène. Pour les besoins de cette discussion, Imaginez une salle avec quatre murs, chacun peint avec une lettre R, G, B, Y et les couleurs correspondantes : rouge, vert, bleu et jaune. La carte d’environnement pour une salle de ce type peut se présenter comme dans l’illustration suivante.

![illustration de rayures verticales de rouge, vert, bleu et jaune](images/envmap.png)

Imagine que le plafond de la pièce est maintenu par un pilier parfaitement réfléchissant et à quatre côtés. Le mappage de la texture de la carte de l’environnement au pilier est simple ; le fait de donner au pilier la même chose qu’il reflète les lettres et les couleurs n’est pas aussi simple. Le diagramme suivant montre une trame de câble du pilier avec les coordonnées de texture applicables figurant près des sommets supérieurs. La jointure dans laquelle le renvoi à la ligne franchira les bords de la texture est indiquée par une ligne en pointillés.

![diagramme d’un rectangle avec une ligne en pointillés bisectée](images/seam.png)

Lorsque l’habillage est activé dans la direction u, le pilier texturé affiche les couleurs et les symboles de la carte de l’environnement de manière appropriée et, à la couture au début de la texture, le rastériseur choisit correctement l’itinéraire le plus bref entre les coordonnées de la texture, en supposant que les coordonnées u 0,0 et 1,0 partagent le même emplacement. Le pilier texturé ressemble à l’illustration suivante.

![illustration d’un pilier constitué de quadrants rouge, vert, bleu et jaune](images/tex-seam.png)

Si l’habillage de texture n’est pas activé, le rastériseur n’effectue pas d’interpolation dans la direction nécessaire pour générer une image réfléchie et incroyable. Au lieu de cela, la zone au début du pilier contient une version compressée horizontalement des texels entre les coordonnées u-0,175 et 0,875, lorsqu’elles passent par le centre de la texture. L’effet de retour à la ligne est détruit.

## <a name="using-texture-wrapping"></a>Utilisation de l’habillage de texture

Pour activer l’encapsulation de texture, appelez la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) comme indiqué dans l’exemple de code ci-dessous.


```
d3dDevice->SetRenderState(D3DRS_WRAP0, D3DWRAPCOORD_0);
```



Le premier paramètre accepté par [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) est un état de rendu à définir. Spécifiez l’un des D3DRS \_ WRAP0 à l’aide de \_ valeurs énumérées D3DRS WRAP7 qui spécifient le niveau de texture pour lequel le renvoi à la valeur doit être défini. Spécifiez les \_ indicateurs D3DWRAPCOORD 0 à D3DWRAPCOORD \_ 3 dans le second paramètre pour activer l’habillage de la texture dans la direction correspondante, ou combinez-les pour activer le retour à la position dans plusieurs directions. Si vous omettez un indicateur, l’habillage de texture dans la direction correspondante est désactivé. Pour désactiver l’habillage de texture pour un ensemble de coordonnées de texture, affectez la valeur 0 à l’état de rendu correspondant.

Ne confondez pas l’habillage de texture avec les modes d’adressage de texture nommés de la même façon. L’habillage de texture est effectué avant l’adressage de texture. Veillez à ce que les données d’habillage de texture ne contiennent pas de coordonnées de texture en dehors de la plage \[ 0,0, 1,0, \] car cela produira des résultats indéfinis. Pour plus d’informations sur l’adressage des textures, consultez [modes d’adressage des textures (Direct3D 9)](texture-addressing-modes.md).

## <a name="displacement-map-wrapping"></a>Habillage de la carte de déplacement

Les mappages de déplacement sont interpolés par le moteur géométrique. Étant donné que le mode habillage ne peut pas être spécifié pour le moteur de polygonalisation, l’habillage de texture ne peut pas être effectué avec les mappages de déplacement. Une application peut utiliser un ensemble de vertex qui force l’interpolation à s’encapsuler dans n’importe quelle direction. L’application peut également spécifier l’interpolation à effectuer en tant qu’interpolation linéaire simple.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Textures Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
