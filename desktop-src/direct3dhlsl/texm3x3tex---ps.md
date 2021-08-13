---
title: texm3x3tex-PS
description: Effectue une multiplication de matrice 3x3 et utilise le résultat pour effectuer une recherche de texture. texm3x3tex doit être utilisé avec deux instructions texm3x3pad-PS.
ms.assetid: bb61cd6f-57d0-4b2d-9186-f04f7f4d3516
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2a40c78fddadde5d58186f9a1ebb01f4d021620862f9d3534e535842a848a2e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118787558"
---
# <a name="texm3x3tex---ps"></a>texm3x3tex-PS

Effectue une multiplication de matrice 3x3 et utilise le résultat pour effectuer une recherche de texture. texm3x3tex doit être utilisé avec deux instructions [texm3x3pad-PS](texm3x3pad---ps.md) .

## <a name="syntax"></a>Syntaxe



| texm3x3tex DST, SRC |
|---------------------|



 

where

-   l’heure d’été est le registre de destination.
-   SRC est un registre source.

## <a name="remarks"></a>Remarques



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3tex            | x    | x    | x    |      |      |      |       |      |       |



 

Cette instruction est utilisée comme dernière des trois instructions représentant une opération de multiplication de matrice 3x3, suivie d’une recherche de texture. La matrice 3x3 est composée des coordonnées de texture de la troisième étape de texture et des deux étapes de texture précédentes. Le vecteur à trois composants résultant (u, v, w) est utilisé pour échantillonner la texture à l’étape 3. Toute texture assignée aux deux étapes de texture précédentes est ignorée. La multiplication de matrice 3x3 est généralement utile pour orienter un vecteur normal vers l’espace tangent correct pour la surface rendue.

Cette instruction doit être utilisée avec l’instruction texm3x3pad. Les registres de texture doivent utiliser la séquence suivante.


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         //   be defined in some way before it is used)
texm3x3pad t(m),   t(n)  //   where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3tex t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         //   3-vector with which to sample texture
                         //   associated with texture stage m+2
```



Voici plus de détails sur la façon dont la multiplication 3x3 est accomplie.

La première instruction texm3x3pad exécute la première ligne de la multiplication pour<sup>Rechercher u.</sup>

u<sup>'</sup> = TextureCoordinates (stage m)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

La deuxième instruction texm3x3pad exécute la deuxième ligne de la multiplication pour rechercher v<sup>»</sup>.

v<sup>'</sup> = TextureCoordinates (étape m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

L’instruction texm3x3spec effectue la troisième ligne de la multiplication pour rechercher w<sup>'</sup>.

w<sup>'</sup> = TextureCoordinates (étape m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

Enfin, l’instruction texm3x3tex échantillonne t (m + 2) avec (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) et stocke le résultat dans t (m + 2).

t (m + 2)<sub>RVBA</sub> = TextureSample (étape m + 2)<sub>RVBA</sub> en utilisant (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) comme coordonnées.

## <a name="examples"></a>Exemples

Voici un exemple de nuanceur avec les cartes de texture identifiées et les étapes de texture identifiées.


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x3pad  t1,  t0   // First row of matrix multiply
texm3x3pad  t2,  t0   // Second row of matrix multiply
texm3x3tex  t3,  t0   // Third row of matrix multiply to get a
                      // 3-vector with which to sample texture at 
mov r0, t3            // stage 3 output result
```



Cet exemple requiert la configuration de la phase de texture suivante.

-   Une carte de texture avec des données normales est assignée à l’étape 0. On parle souvent de carte de relief. Les données sont (XYZ) normales pour chaque Texel. Le jeu de coordonnées de texture 0 définit comment échantillonner cette carte normale.
-   Le jeu de coordonnées de texture 1 est affecté à la ligne 1 de la matrice 3x3. Toute texture assignée à l’étape 1 est ignorée.
-   Le jeu de coordonnées de texture 2 est affecté à la ligne 2 de la matrice 3x3. Toute texture assignée à l’étape 2 est ignorée.
-   Le jeu de coordonnées de texture 3 est affecté à la ligne 3 de la matrice 3x3. Une texture de volume ou de cube doit être définie sur la phase 3 pour la recherche par le vecteur 3D transformé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




