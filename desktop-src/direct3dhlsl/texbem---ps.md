---
title: texbem-PS
description: Appliquez une transformation de mappage d’environnement factice. Pour ce faire, vous devez modifier les données d’adresse de texture du registre de destination, en utilisant les données de perturbation d’adresse (du, DV) et une matrice d’environnement de relief 2D.
ms.assetid: 8e773f4a-c7a2-4caf-973f-8f50dccc9c04
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f026819b268836fd7d4c1d550033ceefdf0bbbf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971719"
---
# <a name="texbem---ps"></a>texbem-PS

Appliquez une transformation de mappage d’environnement factice. Pour ce faire, vous devez modifier les données d’adresse de texture du registre de destination, en utilisant les données de perturbation d’adresse (du, DV) et une matrice d’environnement de relief 2D.

## <a name="syntax"></a>Syntaxe



| texbem DST, SRC |
|-----------------|



 

where

-   l’heure d’été est le registre de destination.
-   SRC est un registre source.

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texbem                | x    | x    | x    |      |      |      |       |      |       |



 

Les données de couleur rouge et verte dans le registre SRC sont interprétées comme les données de perturbation (du, DV).

Cette instruction transforme les composants rouge et vert dans le registre source à l’aide de la matrice de mappage d’environnement 2D Bump. Le résultat est ajouté au jeu de coordonnées de texture correspondant au numéro de registre de destination, et est utilisé pour échantillonner l’étape de texture actuelle.

Cette opération interprète toujours les et DV comme des quantités signées. Pour les versions 1 \_ 0 et 1 \_ 1, le modificateur d’entrée de [mise à l’échelle signée du Registre source](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ BX2) n’est pas autorisé sur l’argument d’entrée.

Cette instruction produit des résultats définis lorsque les textures d’entrée contiennent des données au format signé. Les données au format mixte fonctionnent uniquement si les deux premiers canaux contiennent des données signées. Pour plus d’informations sur les formats de surface, consultez [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).

Cela peut être utilisé pour diverses techniques basées sur la perturbation des adresses, y compris le mappage d’environnement factice par pixel et l’éclairage diffus (placage de relief).

Lors de l’utilisation de cette instruction, les registres de texture doivent respecter la séquence suivante.


```
// The texture assigned to stage t(n) contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbem  t(m),  t(n)      where m > n
```



Les calculs effectués dans l’instruction sont indiqués ci-dessous.


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
```



u' = TextureCoordinates (stage m)<sub>u</sub> + D3DTSS \_ BUMPENVMAT00 (étape m) \* t (n)<sub>R</sub> + D3DTSS \_ BUMPENVMAT10 (étape m) \* t (n)<sub>G</sub> v' = TextureCoordinates (étape m)<sub>v</sub> + D3DTSS \_ BUMPENVMAT01 (étape m) \* t (n)<sub>R</sub> + D3DTSS \_ BUMPENVMAT11 (étape m) \* t (n)<sub>G</sub> t (m)<sub>RVBA</sub> = TextureSample (étape m)

utilisation de (u', v') comme coordonnées

Les données d’enregistrement qui ont été lues par une instruction texbem-PS ou [texbeml-PS](texbeml---ps.md) ne peuvent pas être lues ultérieurement, sauf par un autre texbem-PS ou texbeml-PS.


```
// This example demonstrates the validation error caused by t0 being reread:
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
texbem t1, t0       ; Compute (u',v')
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



texbem requiert les textures suivantes dans les étapes de texture suivantes.

-   Une carte de relief est assignée à l’étape 0 avec des données de perturbation (du, DV).
-   L’étape 1 utilise une carte de texture avec des données de couleur.
-   Cette instruction définit les données de la matrice sur l’étape de texture échantillonnée.
-   Cela diffère de la fonctionnalité du pipeline de fonction fixe dans lequel les données de perturbation et les matrices occupent la même étape de texture.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 