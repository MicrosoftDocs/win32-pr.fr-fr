---
description: La modélisation de la réflexion spéculaire nécessite que le système sache non seulement dans quel sens le feu est en déplacement, mais également dans la direction de l’oeil du spectateur.
ms.assetid: 35da0ac3-4e68-4d37-a987-405fc15d0cbf
title: Éclairage spéculaire (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b16d71bd8d814e104cf8a90d1d1fe9b15ba10f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127291771"
---
# <a name="specular-lighting-direct3d-9"></a>Éclairage spéculaire (Direct3D 9)

La modélisation de la réflexion spéculaire nécessite que le système sache non seulement dans quel sens le feu est en déplacement, mais également dans la direction de l’oeil du spectateur. Le système utilise une version simplifiée du modèle de réflexion spéculaire Phong, qui utilise un vecteur à mi-chemin pour rapprocher l’intensité de la réflexion spéculaire.

L’état d’éclairage par défaut ne calcule pas les surbrillances spéculaires. Pour activer l’éclairage spéculaire, veillez à définir D3DRS \_ SpecularEnable sur **true**.

## <a name="specular-lighting-equation"></a>Équation d’éclairage spéculaire

L’éclairage spéculaire est décrit par l’équation suivante :

**Éclairage spéculaire = cs \* Sum \[ ls \* (N · H)<sup>P</sup> \* atten \*\]**



 

Le tableau suivant identifie les variables, leurs types et leurs plages.



| Paramètre    | Valeur par défaut | Type          | Description                                                                                                         |
|--------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------------|
| C           | (0, 0, 0, 0)     | D3DCOLORVALUE | Couleur spéculaire.                                                                                                     |
| Sum          | N/A           | N/A           | Somme du composant spéculaire de chaque lumière.                                                                       |
| N            | N/A           | D3DVECTOR     | Normale au vertex.                                                                                                      |
| H            | N/A           | D3DVECTOR     | Vecteur à demi-sens. Consultez la section sur le vecteur à mi-chemin.                                                             |
| <sup>P</sup> | 0.0           | FLOAT         | Puissance de réflexion spéculaire. La plage est comprise entre 0 et + infini                                                                  |
| LS           | (0, 0, 0, 0)     | D3DCOLORVALUE | Couleur spéculaire clair.                                                                                               |
| Atten        | N/A           | FLOAT         | Valeur d’atténuation de la lumière. Consultez [facteur d’atténuation et de focalisation (Direct3D 9)](attenuation-and-spotlight-factor.md). |
| Zone         | N/A           | FLOAT         | Facteur Gong. Consultez [facteur d’atténuation et de focalisation (Direct3D 9)](attenuation-and-spotlight-factor.md).        |



 

La valeur de CS est l’une des suivantes :


```
if(SPECULARMATERIALSOURCE == D3DMCS_COLOR1)
  C = color1;
```



-   Sommet color1, si la source de matériau spéculaire est D3DMCS \_ color1, et la première couleur de vertex est fournie dans la déclaration de vertex.
-   le vertex color2, si la source de matériau spéculaire est D3DMCS \_ color2, et la deuxième couleur de vertex est fournie dans la déclaration de vertex.
-   couleur spéculaire

> [!Note]  
> Si l’option source de matériau spéculaire est utilisée et que la couleur du vertex n’est pas fournie, la couleur spéculaire est utilisée.

 

Les composants spéculaires sont ancrés à une valeur comprise entre 0 et 255, après que toutes les lumières ont été traitées et interpolées séparément.

## <a name="the-halfway-vector"></a>Vecteur à mi-chemin

Le vecteur à mi-chemin (H) existe à mi-chemin entre deux vecteurs : le vecteur d’un sommet d’objet à la source de lumière et le vecteur d’un sommet d’objet à la position de la caméra. Direct3D offre deux façons de calculer le vecteur à mi-chemin. Quand D3DRS \_ LOCALVIEWER est défini sur **true**, le système calcule le vecteur à mi-chemin à l’aide de la position de la caméra et la position du vertex, ainsi que le vecteur de direction de la lumière. La formule suivante illustre cela.

**H = normal (normal (CP-VP) + L <sub>Rép</sub>)**



 



| Paramètre       | Valeur par défaut | Type      | Description                                                  |
|-----------------|---------------|-----------|--------------------------------------------------------------|
| CP              | N/A           | D3DVECTOR | Position de l'appareil photo.                                             |
| VP              | N/A           | D3DVECTOR | Position du vertex.                                             |
| <sub>Rép</sub> . | N/A           | D3DVECTOR | Vecteur de direction de la position du vertex à la position de la lumière. |



 

La détermination du vecteur à mi-chemin de cette manière peut nécessiter de nombreuses ressources de calcul. En guise d’alternative, la définition de D3DRS \_ LOCALVIEWER = **false** indique au système d’agir comme si le point de vue est distant de façon infinie sur l’axe z. Cela se reflète dans la formule suivante.

**H = normal ((0, 0, 1) + L <sub>répertoire</sub>)**



 

Ce paramètre est moins gourmand en calculs, mais beaucoup moins précis. il est donc mieux utilisé par les applications qui utilisent la projection orthogonale.

## <a name="example"></a>Exemple

Dans cet exemple, l’objet est coloré à l’aide de la couleur de la lumière spéculaire et d’une couleur spéculaire. Le code est illustré ci-dessous.


```
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );

D3DLIGHT9 light;
ZeroMemory( &light, sizeof(light) );
light.Type = D3DLIGHT_DIRECTIONAL;

D3DXVECTOR3 vecDir;
vecDir = D3DXVECTOR3(0.5f, 0.0f, -0.5f);
D3DXVec3Normalize( (D3DXVECTOR3*)&light.Direction, &vecDir );

light.Specular.r = 1.0f;
light.Specular.g = 1.0f;
light.Specular.b = 1.0f;
light.Specular.a = 1.0f;

light.Range = 1000;
light.Falloff = 0;
light.Attenuation0 = 1;
light.Attenuation1 = 0;
light.Attenuation2 = 0;
m_pd3dDevice->SetLight( 0, &light );
m_pd3dDevice->LightEnable( 0, TRUE );
m_pd3dDevice->SetRenderState( D3DRS_SPECULARENABLE, TRUE );

mtrl.Specular.r = 0.5f;
mtrl.Specular.g = 0.5f;
mtrl.Specular.b = 0.5f;
mtrl.Specular.a = 0.5f;
mtrl.Power = 20;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_SPECULARMATERIALSOURCE, D3DMCS_MATERIAL);
```



D’après l’équation, la couleur résultante pour les vertex d’objet est une combinaison de la couleur de l’élément et de la couleur claire.

L’illustration suivante montre la couleur de matériau spéculaire, grise, et la couleur d’éclairage spéculaire, qui est blanche.

![illustration d’une sphère grise](images/amb1.jpg)![illustration d’une sphère blanche](images/lightwhite.jpg)

La surbrillance spéculaire qui en résulte est présentée dans l’illustration suivante.

![illustration de la surbrillance spéculaire](images/lights.jpg)

La combinaison de la surbrillance spéculaire avec l’éclairage ambiant et diffus produit l’illustration suivante. Avec les trois types d’éclairage appliqués, cela ressemble plus clairement à un objet réaliste.

![illustration de la combinaison de la mise en surbrillance spéculaire, de l’éclairage ambiant et de l’éclairage diffus](images/lightads.jpg)

L’éclairage spéculaire est plus gourmand en calcul que l’éclairage diffus. Il est généralement utilisé pour fournir des indices visuels sur le matériau en surface. La mise en surbrillance spéculaire varie en fonction de la taille et de la couleur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mathématiques d’éclairage](mathematics-of-lighting.md)
</dt> </dl>

 

 



