---
description: L’éclairage ambiant offre une lumière constante pour une scène.
ms.assetid: 327095a7-f4e0-48c2-9e4d-bec8493fe37e
title: Éclairage ambiant (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a1d1d890d2de0a9cb617759ac3a9bb6d57f81b13440049bfb54575aee7a6546
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069443"
---
# <a name="ambient-lighting-direct3d-9"></a>Éclairage ambiant (Direct3D 9)

L’éclairage ambiant offre une lumière constante pour une scène. Il prend en compte tous les sommets d’objets, car il ne dépend pas d’autres facteurs d’éclairage tels que les normales aux sommets, la direction de la lumière, la position de la lumière, la plage ou l’atténuation. Il s’agit du type d’éclairage le plus rapide, mais il produit des résultats moins réalistes. Direct3D contient une seule propriété de lumière ambiante globale que vous pouvez utiliser sans créer de lumière. Vous pouvez également définir n’importe quel objet Light pour fournir un éclairage ambiant. L’éclairage ambiant d’une scène est décrit par l’équation suivante.

Éclairage ambiant = C ₐ \* \[ g ₐ + Sum (atten<sub>i</sub> \* point<sub>i</sub> \* L<sub>ai</sub>)\]

Où :



| Paramètre         | Valeur par défaut | Type          | Description                                                                                                                    |
|-------------------|---------------|---------------|--------------------------------------------------------------------------------------------------------------------------------|
| C ₐ                | (0, 0, 0, 0)     | D3DCOLORVALUE | Couleur ambiante du matériau                                                                                                         |
| ₐ g                | (0, 0, 0, 0)     | D3DCOLORVALUE | Couleur ambiante globale                                                                                                           |
| Atten<sub>i</sub> | (0, 0, 0, 0)     | D3DCOLORVALUE | Atténuation de la lumière de la énièmeté. Consultez [facteur d’atténuation et de focalisation (Direct3D 9)](attenuation-and-spotlight-factor.md). |
| Point<sub>i</sub>  | (0, 0, 0, 0)     | D3DVECTOR     | Facteur Gong de la énième lumière. Consultez [facteur d’atténuation et de focalisation (Direct3D 9)](attenuation-and-spotlight-factor.md).  |
| Sum               | N/A           | N/A           | Somme de la lumière ambiante                                                                                                       |
| L<sub>ai</sub>    | (0, 0, 0, 0)     | D3DVECTOR     | Couleur ambiante claire de la énième lumière                                                                                           |



 

La valeur de C ₐ est :

-   Sommet color1, si AMBIENTMATERIALSOURCE = D3DMCS \_ color1, et la première couleur de vertex est fournie dans la déclaration de vertex.
-   le sommet color2, si AMBIENTMATERIALSOURCE = D3DMCS \_ color2, et la deuxième couleur du vertex sont fournies dans une déclaration de vertex.
-   couleur ambiante du matériau.

> [!Note]  
> Si l’une des options AMBIENTMATERIALSOURCE est utilisée et que la couleur du vertex n’est pas fournie, la couleur ambiante du matériau est utilisée.

 

Pour utiliser la couleur ambiante du matériau, utilisez SetMaterial comme indiqué dans l’exemple de code ci-dessous.

G ₐ est la couleur ambiante globale. Il est défini à l’aide de SetRenderState (D3DRS \_ ambiant). Une scène Direct3D contient une couleur ambiante globale. Ce paramètre n’est pas associé à un objet Light Direct3D.

L<sub>ai</sub> est la couleur ambiante de l’énième lumière dans la scène. Chaque lumière Direct3D a un ensemble de propriétés, dont l’une est la couleur ambiante. Le terme somme (L<sub>ai</sub>) est la somme de toutes les couleurs ambiantes de la scène.

## <a name="example"></a>Exemple

Dans cet exemple, l’objet est coloré à l’aide de la lumière ambiante de scène et d’une couleur ambiante de matériau.


```
#define GRAY_COLOR  0x00bfbfbf

// create material
D3DMATERIAL9 mtrl;
ZeroMemory(&mtrl, sizeof(mtrl));
mtrl.Ambient.r = 0.75f;
mtrl.Ambient.g = 0.0f;
mtrl.Ambient.b = 0.0f;
mtrl.Ambient.a = 0.0f;
m_pd3dDevice->SetMaterial(&mtrl);
m_pd3dDevice->SetRenderState(D3DRS_AMBIENT, GRAY_COLOR);
```



D’après l’équation, la couleur résultante pour les vertex d’objet est une combinaison de la couleur de l’élément et de la couleur claire.

Les deux illustrations suivantes affichent la couleur de matériau, grise, et la couleur claire, qui est brillante rouge.

![illustration d’une sphère grise](images/amb1.jpg)![illustration d’une sphère rouge](images/lightred.jpg)

La scène qui en résulte est présentée dans l’illustration suivante. Le seul objet de la scène est une sphère. La lumière ambiante illumine tous les vertex d’objets avec la même couleur. Elle n’est pas dépendante de la normale du vertex ou de la direction de la lumière. Par conséquent, la sphère ressemble à un cercle 2D, car il n’y a aucune différence dans l’ombrage autour de la surface de l’objet.

![illustration d’une sphère avec éclairage ambiant](images/lighta.jpg)

Pour donner une apparence plus réaliste aux objets, appliquez une lumière diffuse ou spéculaire en plus de l’éclairage ambiant.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mathématiques d’éclairage](mathematics-of-lighting.md)
</dt> </dl>

 

 



