---
description: L’éclairage émissif est décrit par un terme unique.
ms.assetid: b6ccf274-a6c5-4b26-8c43-c857c2c24e0f
title: Éclairage émissif (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19cb0566d2409fb68e5fbbdca1cc609c31120e95
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916612"
---
# <a name="emissive-lighting-direct3d-9"></a>Éclairage émissif (Direct3D 9)

L’éclairage émissif est décrit par un terme unique.

Éclairage émissif = C ₑ

Où :



| Paramètre | Valeur par défaut | Type          | Description     |
|-----------|---------------|---------------|-----------------|
| C ₑ        | (0, 0, 0, 0)     | D3DCOLORVALUE | Couleur émissif. |



 

La valeur de C ₑ est :

-   Sommet color1, si EMISSIVEMATERIALSOURCE = D3DMCS \_ color1, et la première couleur de vertex est fournie dans la déclaration de vertex.
-   le sommet color2, si EMISSIVEMATERIALSOURCE = D3DMCS \_ color2, et la deuxième couleur du vertex sont fournies dans la déclaration de vertex.
-   couleur de matériau émissif

> [!Note]  
> Si l’une des options EMISSIVEMATERIALSOURCE est utilisée et que la couleur du vertex n’est pas fournie, la couleur de la matière émissif est utilisée.

 

## <a name="example"></a>Exemple

Dans cet exemple, l’objet est coloré à l’aide de la lumière ambiante de scène et d’une couleur ambiante de matériau. Le code est illustré ci-dessous.


```
// create material
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );
mtrl.Emissive.r = 0.0f;
mtrl.Emissive.g = 0.75f;
mtrl.Emissive.b = 0.0f;
mtrl.Emissive.a = 0.0f;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_EMISSIVEMATERIALSOURCE, D3DMCS_MATERIAL);
```



D’après l’équation, la couleur résultante pour les vertex de l’objet est la couleur du matériau.

L’illustration suivante montre la couleur de matériau, qui est verte. Lumière luminescente tous les vertex d’objets avec la même couleur. Elle n’est pas dépendante de la normale du vertex ou de la direction de la lumière. Par conséquent, la sphère ressemble à un cercle 2D, car il n’y a aucune différence dans l’ombrage autour de la surface de l’objet.

![illustration d’une sphère verte](images/lighte.jpg)

L’illustration suivante montre comment la lumière émissif fusionne avec les trois autres types d’éclairage, des exemples précédents. Sur le côté droit de la sphère, il y a une fusion du vert émissif et de la lumière ambiante rouge. Sur le côté gauche de la sphère, le feu vert émissif est mélangé avec un voyant rouge ambiant et diffus produisant un dégradé rouge. La surbrillance spéculaire est blanche au centre et crée un anneau jaune lorsque la valeur de la lumière spéculaire s’arrête brusquement en laissant les valeurs ambiantes ambiantes, diffuses et émissif qui se mélangent pour s’afficher en jaune.

![illustration d’une sphère verte avec une lumière émissif](images/lightadse.jpg)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mathématiques d’éclairage](mathematics-of-lighting.md)
</dt> </dl>

 

 



