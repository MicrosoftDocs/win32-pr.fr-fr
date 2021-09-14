---
description: Après avoir ajusté l’intensité lumineuse pour tout effet d’atténuation, le moteur d’éclairage calcule la quantité de lumière restante à partir d’un vertex, en fonction de l’angle de la normale du vertex et de la direction du feu incident.
ms.assetid: 29280a02-1c26-4b54-8468-707dd96dea1d
title: Lumière diffuse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51e45093786348aaa115ec38c420acec471f718
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855148"
---
# <a name="diffuse-lighting-direct3d-9"></a>Lumière diffuse (Direct3D 9)

Après avoir ajusté l’intensité lumineuse pour tout effet d’atténuation, le moteur d’éclairage calcule la quantité de lumière restante à partir d’un vertex, en fonction de l’angle de la normale du vertex et de la direction du feu incident. Le moteur d’éclairage passe à cette étape pour les lumières directionnelles, car elles n’atténuent pas les distances. Le système considère deux types de réflexion, diffus et spéculaire, et utilise une formule différente pour déterminer la quantité de lumière reflétée pour chacun. Après avoir calculé les quantités de lumière réfléchie, Direct3D applique ces nouvelles valeurs aux propriétés de réflectivité diffuse et spéculaire du matériau actuel. Les valeurs de couleur résultantes sont les composants diffus et spéculaire utilisés par le rastériseur pour produire un ombrage Gouraud et une mise en surbrillance spéculaire.

L’éclairage diffus est décrit par l’équation suivante.

Éclairage diffus = somme \[ C<sub>d</sub> \* L<sub>d</sub> \* (N<sup>.</sup> L<sub>Rép</sub>) \* atten \*\]



| Paramètre       | Valeur par défaut | Type          | Description                                                                                                   |
|-----------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------|
| Sum             | N/A           | N/A           | Somme du composant de diffusion de chaque lumière.                                                                  |
| C<sub>d</sub>   | (0, 0, 0, 0)     | D3DCOLORVALUE | Couleur diffuse.                                                                                                |
| L<sub>d</sub>   | (0, 0, 0, 0)     | D3DCOLORVALUE | Couleur diffuse de la lumière.                                                                                          |
| N               | N/A           | D3DVECTOR     | Vertex-normal                                                                                                 |
| <sub>Rép</sub> . | N/A           | D3DVECTOR     | Vecteur de direction du sommet de l’objet à la lumière.                                                             |
| Atten           | N/A           | FLOAT         | Atténuation de la lumière. Consultez [facteur d’atténuation et de focalisation (Direct3D 9)](attenuation-and-spotlight-factor.md). |
| Zone            | N/A           | FLOAT         | Facteur Gong. Consultez [facteur d’atténuation et de focalisation (Direct3D 9)](attenuation-and-spotlight-factor.md).  |



 

La valeur de C<sub>d</sub> est :

-   Sommet color1, si DIFFUSEMATERIALSOURCE = D3DMCS \_ color1, et la première couleur de vertex est fournie dans la déclaration de vertex.
-   le sommet color2, si DIFFUSEMATERIALSOURCE = D3DMCS \_ color2, et la deuxième couleur du vertex sont fournies dans la déclaration de vertex.
-   couleur diffuse de matériau

> [!Note]  
> Si l’une des options DIFFUSEMATERIALSOURCE est utilisée et que la couleur du vertex n’est pas fournie, la couleur de diffusion matérielle est utilisée.

 

Pour calculer l’atténuation (atten) ou les caractéristiques de Spotlight (spot), consultez [facteur d’atténuation et de projecteur (Direct3D 9)](attenuation-and-spotlight-factor.md).

Les Composants diffuses sont ancrés de 0 à 255, après que toutes les lumières ont été traitées et interpolées séparément. La valeur d’éclairage diffus résultante est une combinaison des valeurs de lumière ambiante, diffuse et émissif.

## <a name="example"></a>Exemple

Dans cet exemple, l’objet est coloré à l’aide de la couleur lumière diffuse et d’une couleur diffuse de matériau. Le code est illustré ci-dessous.


```
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );

D3DLIGHT9 light;
ZeroMemory( &light, sizeof(light) );
light.Type = D3DLIGHT_DIRECTIONAL;

D3DXVECTOR3 vecDir;
vecDir = D3DXVECTOR3(0.5f, 0.0f, -0.5f);
D3DXVec3Normalize( (D3DXVECTOR3*)&light.Direction, &vecDir );

// set directional light diffuse color
light.Diffuse.r = 1.0f;
light.Diffuse.g = 1.0f;
light.Diffuse.b = 1.0f;
light.Diffuse.a = 1.0f;
m_pd3dDevice->SetLight( 0, &light );
m_pd3dDevice->LightEnable( 0, TRUE );

// if a material is used, SetRenderState must be used
// vertex color = light diffuse color * material diffuse color
mtrl.Diffuse.r = 0.75f;
mtrl.Diffuse.g = 0.0f;
mtrl.Diffuse.b = 0.0f;
mtrl.Diffuse.a = 0.0f;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_DIFFUSEMATERIALSOURCE, D3DMCS_MATERIAL);
```



D’après l’équation, la couleur résultante pour les vertex d’objet est une combinaison de la couleur de l’élément et de la couleur claire.

Les deux illustrations suivantes affichent la couleur de matériau, grise, et la couleur claire, qui est brillante rouge.

![illustration d’une sphère grise](images/amb1.jpg)![illustration d’une sphère rouge](images/lightred.jpg)

La scène qui en résulte est présentée dans l’illustration suivante. Le seul objet de la scène est une sphère. Le calcul de l’éclairage diffus prend la couleur diffuse de la lumière et du matériau, et le modifie selon l’angle entre la direction de la lumière et le sommet normal à l’aide du point. Par conséquent, le verso de la sphère est plus sombre lorsque la surface de la sphère est éloignée de la lumière.

![illustration d’une sphère avec éclairage diffus](images/lightd.jpg)

En associant l’éclairage diffus à l’éclairage ambiant de l’exemple précédent, la surface entière de l’objet est dégradée. La lumière ambiante dégrade la surface entière et la lumière diffuse permet de révéler la forme 3D de l’objet, comme indiqué dans l’illustration suivante.

![illustration d’une sphère avec éclairage diffus et éclairage ambiant](images/lightad.jpg)

L’éclairage diffus est plus gourmand en calcul que l’éclairage ambiant. Étant donné qu’elle dépend des normales aux sommets et de la direction de la lumière, vous pouvez voir la géométrie des objets dans l’espace 3D, ce qui produit un éclairage plus réaliste que l’éclairage ambiant. Vous pouvez utiliser des surbrillances spéculaires pour obtenir une apparence plus réaliste.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mathématiques d’éclairage](mathematics-of-lighting.md)
</dt> </dl>

 

 



