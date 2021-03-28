---
title: texm3x2tex-PS
description: Effectue la multiplication de la dernière ligne d’une matrice matrice et utilise le résultat pour effectuer une recherche de texture. texm3x2tex doit être utilisé conjointement avec l’instruction texm3x2pad-PS.
ms.assetid: c6cfbf75-4a63-4c82-9fb6-286b51b7f883
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 62206bc4ef1e1b64ec760a240a087ec13526d896
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990769"
---
# <a name="texm3x2tex---ps"></a>texm3x2tex-PS

Effectue la multiplication de la dernière ligne d’une matrice matrice et utilise le résultat pour effectuer une recherche de texture. texm3x2tex doit être utilisé conjointement avec l’instruction [texm3x2pad-PS](texm3x2pad---ps.md) .

## <a name="syntax"></a>Syntaxe



| texm3x2tex DST, SRC |
|---------------------|



 

where

-   l’heure d’été est le registre de destination.
-   SRC est un registre source.

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x2tex            | x    | x    | x    |      |      |      |       |      |       |



 

L’instruction est utilisée comme l’une des deux instructions représentant une opération de multiplication de matrice matrice. Cette instruction doit être utilisée avec l’instruction [texm3x2pad-PS](texm3x2pad---ps.md) .

Lors de l’utilisation de ces deux instructions, les registres de texture doivent utiliser la séquence suivante.


```
 
tex t(n)                      // Define tn as a standard 3-vector (tn must 
                              // be defined in some way before it is used)
texm3x2pad  t(m),   t(n)      // where m > n
                              // Perform first row of matrix multiply
texm3x2tex  t(m+1), t(n)      // Perform second row of matrix multiply 
                              // to get (u,v) to sample texture 
                              // associated with stage m+1
```



Voici plus de détails sur la façon dont la multiplication matrice est accomplie.

L’instruction texm3x2pad exécute la première ligne de la multiplication pour<sup>Rechercher u.</sup>

u<sup>'</sup> = t (n)<sub>RGB</sub> \* TextureCoordinates (étape m)<sub>UVW</sub>

L’instruction texm3x2tex effectue la deuxième ligne de la multiplication pour rechercher v<sup>'</sup>.

v<sup>'</sup> = t (n)<sub>RGB</sub> \* TextureCoordinates (étape m + 1)<sub>UVW</sub>

L’instruction texm3x2tex échantillonne la texture à l’étape (m + 1) avec (u<sup>'</sup>, v<sup>'</sup>) et stocke le résultat dans t (m + 1).

t (m + 1)<sub>RGB</sub> = TextureSample (étape m + 1)<sub>RGB</sub> avec (u<sup>'</sup>, v<sup>'</sup> ) en tant que coordonnées

## <a name="examples"></a>Exemples

Voici un exemple de nuanceur avec les cartes de texture et les étapes de texture identifiées.


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x2pad  t1,  t0   // First row of matrix multiply
texm3x2tex  t2,  t0   // Second row of matrix multiply to get (u,v)
                      // with which to sample texture in stage 2
mov r0, t2            // Output result
```



Cet exemple requiert les textures suivantes dans les étapes de texture suivantes.

-   L’étape 0 prend un mappage avec les données de perturbation (x, y, z).
-   L’étape 1 contient des coordonnées de texture. Aucune texture n’est nécessaire dans l’étape de texture.
-   L’étape 2 contient les coordonnées de texture ainsi qu’une texture 2D définie à cette étape de texture.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




