---
title: Registre de coordonnées de texture (référence HLSL VS)
description: Ce registre de sortie du nuanceur de vertex contient des coordonnées de texture par vertex.
ms.assetid: d42c8e4c-8227-4fe8-9432-90c592011024
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ad3937b8f0b3f7acd6313774f6de7cde133e69c5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922423"
---
# <a name="texture-coordinate-register-hlsl-vs-reference"></a>Registre de coordonnées de texture (référence HLSL VS)

Ce registre de sortie du nuanceur de vertex contient des coordonnées de texture par vertex.

Un registre se compose de propriétés qui déterminent le comportement de chaque registre.



| Propriété        | Description   |
|-----------------|---------------|
| Nom            | oT0 - oT7     |
| Count           | Huit vecteurs |
| Autorisations d’e/s | Écriture seule    |



 

Les registres de coordonnées de texture de sortie sont un tableau de registres de données de sortie. Les données de Registre sont itérées et utilisées comme coordonnées de texture par les étapes d’échantillonnage de texture pour fournir des données au nuanceur de pixels.

Lors de l’écriture dans un registre de coordonnées de texture, il est recommandé de passer uniquement autant de valeurs à virgule flottante que la dimension de la carte de texture correspondante. Contrôler les valeurs passées avec un modificateur. Par exemple, utilisez. XY pour une carte de texture 2D.

Les indicateurs de pipeline de fonction fixe, [**D3DTEXTURETRANSFORMFLAGS**](/windows/desktop/direct3d9/d3dtexturetransformflags) (D3DTTFF \_ COUNT1, D3DTTFF \_ COUNT2, D3DTTFF \_ COUNT3, D3DTTFF \_ COUNT4), doivent être définis sur zéro si vous utilisez un nuanceur de sommet programmable.

Les données de vertex d’objet fournissent des coordonnées de texture d’entrée. Les objets qui n’utilisent pas les textures en mosaïque ont généralement des coordonnées de texture dans la plage \[ 0, 1 \] . Les objets qui utilisent des textures en mosaïque, telles que le terrain, ont généralement des coordonnées de texture comprises entre \[ -n, + n, \] où n peut être n’importe quel nombre à virgule flottante.

L’interpolation de coordonnée de texture est effectuée sur les données de vertex pour la pixellisation. Pendant la pixellisation, les coordonnées de texture sont interpolées entre les vertex d’objet, modifiées par habillage de texture et mises à l’échelle par la taille de la texture (en prenant également en compte les modes d’adressage de texture) pour produire un index d’entiers. L’index est ensuite utilisé pour effectuer une recherche de texture. Utilisez la valeur MaxTextureRepeat dans [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) pour déterminer combien de fois une texture peut être affichée en mosaïque.

## <a name="example"></a>Exemple

Déclarez le registre de coordonnées de texture.


```
dcl_texcoord v7
```



Copiez les coordonnées de texture par vertex dans le registre de sortie.


```
mov oT0, v7
```





| Versions de nuanceur vertex      | 1\_1 | 2 \_ 0 | 2 \_ logiciels | 2 \_ x | 3 \_ 0 | 3 \_ logiciels |
|-----------------------------|------|------|-------|------|------|-------|
| Registre de coordonnées de texture | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Registres de nuanceur vertex](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 