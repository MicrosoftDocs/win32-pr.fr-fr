---
title: texm3x3-PS
description: Effectue une multiplication de matrice 3x3 quand elle est utilisée conjointement avec deux instructions texm3x3pad-PS.
ms.assetid: d0b14c87-3507-4237-9f2c-1eb94a6df71c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6238a4b148de67275af1b288d57686cc4d381ee9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971550"
---
# <a name="texm3x3---ps"></a>texm3x3-PS

Effectue une multiplication de matrice 3x3 quand elle est utilisée conjointement avec deux instructions [texm3x3pad-PS](texm3x3pad---ps.md) .

## <a name="syntax"></a>Syntaxe



| texm3x3 DST, SRC |
|------------------|



 

where

-   l’heure d’été est le registre de destination.
-   SRC est un registre source.

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3               |      | x    | x    |      |      |      |       |      |       |



 

Cette instruction est la même que l’instruction [texm3x3tex-PS](texm3x3tex---ps.md) , sans la recherche de texture.

Cette instruction est utilisée comme dernière des trois instructions représentant une opération de multiplication de matrice 3x3. La matrice 3x3 est composée des coordonnées de texture de la troisième étape de texture et des deux étapes de texture précédentes. Toute texture assignée à l’une des trois étapes de texture est ignorée.

Cette instruction doit être utilisée avec deux instructions texm3x3pad. Les registres de texture doivent respecter la séquence suivante.


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         // be defined in some way before it is used)
texm3x3pad t(m),   t(n)  // where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3    t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         // 3-vector result
```



Voici plus de détails sur la façon dont la multiplication 3x3 est accomplie.

La première instruction texm3x3pad exécute la première ligne de la multiplication pour<sup>Rechercher u.</sup>

u<sup>'</sup> = TextureCoordinates (stage m)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

La deuxième instruction texm3x3pad exécute la deuxième ligne de la multiplication pour rechercher v<sup>»</sup>.

v<sup>'</sup> = TextureCoordinates (étape m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

L’instruction texm3x3tex effectue la troisième ligne de la multiplication pour rechercher w<sup>'</sup>.

w<sup>'</sup> = TextureCoordinates (étape m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

Placez le résultat de la multiplication de la matrice dans le registre de destination.

t (m + 2)<sub>RVBA</sub> = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> , 1)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




