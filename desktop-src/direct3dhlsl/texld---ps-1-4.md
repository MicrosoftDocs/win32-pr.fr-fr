---
title: texld-ps_1_4
description: Charge le registre de destination avec les données de couleur (RVBA) échantillonnées en utilisant le contenu du Registre source comme coordonnées de texture. La texture échantillonnée est la texture associée au numéro de registre de destination.
ms.assetid: 1970aed4-4da7-40a1-960d-fba4dfd8c433
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ca305b16db0f390354962a3e959f08b6e956f2ef
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996866"
---
# <a name="texld---ps_1_4"></a>texld-PS \_ 1 \_ 4

Charge le registre de destination avec les données de couleur (RVBA) échantillonnées en utilisant le contenu du Registre source comme coordonnées de texture. La texture échantillonnée est la texture associée au numéro de registre de destination.



| texld DST, SRC |
|----------------|



 

## <a name="registers"></a>Registres



|          |                      | VN        | 8525  | TN  | RN  |              |
|----------|----------------------|-----------|-----|-----|-----|--------------|
| dst      | Registre de destination |           |     |     | x   | 1\_4         |
| src      | Registre source      |           |     | x   |     | 1 \_ 4 phase 1 |
|          |                      |           |     | x   | x   | 1 \_ phase   |



 

Lors de l’utilisation de r (n) comme Registre source, les trois premiers composants (XYZ) doivent avoir été initialisés au cours de la phase précédente du nuanceur.

Pour en savoir plus sur les registres, consultez les [registres PS 1 \_ \_ 1 \_ \_ PS 1 \_ \_ 2 \_ \_ \_ \_ \_ \_ \_ \_ ](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)PS 1 3 PS 1 4.

## <a name="remarks"></a>Remarques

Cette instruction échantillonne la texture dans l’étape de texture associée au numéro de registre de destination. La texture est échantillonnée à l’aide des données de coordonnée de texture du Registre source.

La syntaxe des instructions texld et texcrd expose la prise en charge d’une division projective avec un modificateur de registre de texture. Pour le nuanceur de pixels version 1,4, l' \_ indicateur de transformation de texture projeté D3DTTFF est toujours ignoré.

Règles d’utilisation de texld :

1.  Le même modificateur. xyz ou. XYW doit être appliqué à chaque lecture d’un registre t (n) individuel dans les instructions texcrd ou texld. Si. XYW est utilisé sur les lectures de Registre t (n), il peut être mélangé à d’autres lectures du même registre t (n) à l’aide de la fonction dw. XYW \_ .
2.  Le \_ modificateur de source DZ est uniquement valide sur texld avec le registre source r (n) (donc la phase 2 uniquement).
3.  Le \_ modificateur de source DZ ne peut pas être utilisé plus de deux fois par nuanceur.



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texld                 |      |      |      | x    |      |      |       |      |       |



 

## <a name="examples"></a>Exemples

L’instruction texld offre un certain contrôle sur les composants des données de coordonnée de texture source qui sont utilisés. L’ensemble complet de syntaxe autorisée pour texld suit et comprend tous les modificateurs de Registre source valides, les sélecteurs et les combinaisons de masques d’écriture.


```
texld  r(m), t(n).xyz
// Uses xyz from t(n) to sample 1D, 2D, or 3D texture
```




```
texld  r(m), t(n)
// Same as previous
```




```
texld  r(m), t(n).xyw
// Uses xyw (skipping z) from t(n) to sample 1D, 2D or 3D texture
```




```
texld  r(m), t(n)_dw.xyw  
// Samples 1D or 2D texture at x/w, y/w from t(n). The result
// is undefined for a cube-map lookup.
```




```
texld  r(m), r(n).xyz
// Samples 1D, 2D, or 3D texture at xyz from r(m) 
// This is possible in the second phase of the shader
```




```
texld  r(m), r(n)
// Same as previous
```




```
texld  r(m), r(n)_dz.xyz
// Samples 1D or 2D texture at x/z, y/z from r(m)
// Possible only in second phase
// The result is undefined for a cube-map lookup
```




```
texld  r(n), r(n)_dz
// Same as previous
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




