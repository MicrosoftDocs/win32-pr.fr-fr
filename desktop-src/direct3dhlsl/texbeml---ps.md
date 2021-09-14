---
title: texbeml-PS
description: Appliquez une transformation de placage d’environnement factice avec correction de luminance. Pour ce faire, vous devez modifier les données d’adresse de texture du registre de destination, en utilisant les données de perturbation d’adresse (du, DV), la matrice d’environnement de relief 2D et la luminance.
ms.assetid: 345a0b77-8d4e-4a0b-a31a-1153f8cb5961
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d97877c67970f43a995fcfbe21d9aead2d792e09
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918099"
---
# <a name="texbeml---ps"></a>texbeml-PS

Appliquez une transformation de placage d’environnement factice avec correction de luminance. Pour ce faire, vous devez modifier les données d’adresse de texture du registre de destination, en utilisant les données de perturbation d’adresse (du, DV), la matrice d’environnement de relief 2D et la luminance.

## <a name="syntax"></a>Syntaxe



| texbeml DST, SRC |
|------------------|



 

where

-   l’heure d’été est le registre de destination.
-   SRC est un registre source.

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texbeml               | x    | x    | x    |      |      |      |       |      |       |



 

Les données de couleur rouge et verte dans le registre SRC sont interprétées comme les données de perturbation (du, DV). Les données de couleur bleue dans le registre SRC sont interprétées comme les données de luminance.

Cette instruction transforme les composants rouge et vert dans le registre source à l’aide de la matrice de mappage d’environnement de relief 2D. Le résultat est ajouté au jeu de coordonnées de texture correspondant au numéro de registre de destination. Une correction de luminance est appliquée à l’aide de la valeur de luminance et des valeurs d’étape de texture biaisée. Le résultat est utilisé pour échantillonner l’étape de texture actuelle.

Cela peut être utilisé pour diverses techniques basées sur la perturbation des adresses, telles que le mappage d’environnement factice par pixel.

Cette opération interprète toujours les et DV comme des quantités signées. Pour les versions 1 \_ 0 et 1 \_ 1, le modificateur d’entrée de [mise à l’échelle signée du Registre source](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ BX2) n’est pas autorisé sur l’argument d’entrée.

Cette instruction produit des résultats définis lorsque les textures d’entrée contiennent des données au format mixte. Pour plus d’informations sur les formats de surface, consultez [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).


```
// When using this instruction, texture registers must follow 
//   the following sequence:
// The texture assigned to stage tn contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbeml t(m),  t(n)      where m > n
```



Cet exemple montre les calculs effectués dans l’instruction.


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
// 3. Luminance correction is applied
```



u' = TextureCoordinates (étape m)<sub>u</sub> +

D3DTSS \_ BUMPENVMAT00 (étape m) \* t (n)<sub>R</sub> +

D3DTSS \_ BUMPENVMAT10 (étape m) \* t (n)<sub>G</sub>

v' = TextureCoordinates (étape m)<sub>v</sub> +

D3DTSS \_ BUMPENVMAT01 (étape m) \* t (n)<sub>R</sub> +

D3DTSS \_ BUMPENVMAT11 (étape m) \* t (n)<sub>G</sub>

t (m)<sub>RVBA</sub> = TextureSample (étape m) utilisation de (u’v') en tant que coordonnées

t (m)<sub>RVBA</sub> = t (m)<sub>RVBA</sub>\*

\[(t (n)<sub>B</sub> \* D3DTSS \_ BUMPENVLSCALE (étape m)) +

D3DTSS \_ BUMPENVLOFFSET (étape m)\]

Les données d’enregistrement qui ont été lues par une instruction [texbem](texbem---ps.md) ou texbeml ne peuvent pas être lues ultérieurement, sauf par un autre texbem ou texbeml.


```
// This example demonstrates the validation error caused by 
//   t0 being reread
ps_1_1
tex t0
texbem t1, t0
add r0, t1, t0

(Instruction Error) (Statement 4) Register data that has been read by 
texbem or texbeml instruction cannot be read by other instructions
```



## <a name="examples"></a>Exemples

Voici un exemple de nuanceur avec les cartes de texture identifiées et les étapes de texture identifiées.


```
ps_1_1
tex t0              ; Define t0 to get a 2-tuple DuDv
texbeml t1, t0      ; Compute (u',v')
                    ; Apply luminance correction                    
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



Cet exemple requiert les textures suivantes dans les étapes de texture suivantes.

-   Une carte de relief est assignée à l’étape 0 avec des données de perturbation (du, DV).
-   Une carte de texture avec des données de couleur est assignée à la phase 1.
-   texbeml définit les données de la matrice sur l’étape de texture échantillonnée. Cela diffère de la fonctionnalité du pipeline de fonction fixe dans lequel les données de perturbation et les matrices occupent la même étape de texture.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 