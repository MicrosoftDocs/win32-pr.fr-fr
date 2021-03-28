---
title: texm3x3vspec-PS
description: Effectue une multiplication de matrice 3x3 et utilise le résultat pour effectuer une recherche de texture.
ms.assetid: 3798bc23-2929-48fe-93ae-5aa025823714
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 28f1ee1ddb0193f9ccdaa4976e4963e748091f37
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103940573"
---
# <a name="texm3x3vspec---ps"></a>texm3x3vspec-PS

Effectue une multiplication de matrice 3x3 et utilise le résultat pour effectuer une recherche de texture. Cela peut être utilisé pour la réflexion spéculaire et le mappage d’environnement où le vecteur de rayons oculaires n’est pas constant. texm3x3vspec doit être utilisé conjointement avec deux instructions [texm3x3pad-PS](texm3x3pad---ps.md) . Si le vecteur de rayon oculaire est constant, l’instruction [texm3x3spec-PS](texm3x3spec---ps.md) effectue la même multiplication de matrices et la même recherche de texture.

## <a name="syntax"></a>Syntaxe



| texm3x3vspec DST, SRC |
|-----------------------|



 

where

-   l’heure d’été est le registre de destination.
-   SRC est un registre source.

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3vspec          | x    | x    | x    |      |      |      |       |      |       |



 

Cette instruction effectue la dernière ligne d’une opération de multiplication de matrice 3x3, interprète le vecteur résultant comme un vecteur normal pour refléter un vecteur de rayons oculaires, puis utilise le vecteur réfléchi comme une adresse de texture pour une recherche de texture. Il fonctionne de la même façon que [texm3x3spec-PS](texm3x3spec---ps.md), sauf que le vecteur de rayon oculaire est extrait du quatrième composant des coordonnées de texture. La multiplication de matrice 3x3 est généralement utile pour orienter un vecteur normal vers l’espace tangent correct pour la surface rendue.

La matrice 3x3 est composée des coordonnées de texture de la troisième étape de texture et des deux étapes de texture précédentes. Le vecteur de publication (UVW) qui en résulte est utilisé pour échantillonner la texture à l’étape 3. Toute texture assignée aux deux étapes de texture précédentes est ignorée.

Cette instruction doit être utilisée avec l’instruction texm3x3pad. Les registres de texture doivent utiliser la séquence suivante.


```
tex t(n)                    // Define tn as a standard 3-vector (tn must
                            //   be defined in some way before it is used)
texm3x3pad   t(m),   t(n)   // where m > n
                            // Perform first row of matrix multiply
texm3x3pad   t(m+1), t(n)   // Perform second row of matrix multiply
texm3x3vspec t(m+2), t(n)   // Perform third row of matrix multiply
                            // Then do a texture lookup on the texture
                            // associated with texture stage m+2
```



La première instruction texm3x3pad exécute la première ligne de la multiplication pour<sup>Rechercher u.</sup>

u<sup>'</sup> = TextureCoordinates (stage m)<sub>UVW</sub> \* t (n) <sub>RGB</sub>

La deuxième instruction texm3x3pad exécute la deuxième ligne de la multiplication pour rechercher v<sup>»</sup>.

v<sup>'</sup> = TextureCoordinates (étape m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

L’instruction texm3x3spec effectue la troisième ligne de la multiplication pour rechercher w<sup>'</sup>.

w<sup>'</sup> = TextureCoordinates (étape m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

L’instruction texm3x3vspec effectue également un calcul de réflexion.

(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2 \* \[ (n \* E)/(n \* n) \] \* n-E

où le N normal est donné par

N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )

et le vecteur de rayon œil E est fourni par

E = (TextureCoordinates (étape m)<sub>Q</sub> ,

TextureCoordinates (étape m + 1)<sub>Q</sub> ,

TextureCoordinates (étape m + 2)<sub>Q</sub> )

Enfin, l’instruction texm3x3vspec échantillonne t (m + 2) avec (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) et stocke le résultat dans t (m + 2).

t (m + 2)<sub>RVBA</sub> = TextureSample (étape m + 2)<sub>RVBA</sub> à l’aide de (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) en tant que coordonnées

## <a name="examples"></a>Exemples

Voici un exemple de nuanceur avec les cartes de texture identifiées et les étapes de texture identifiées.


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x3pad   t1,  t0  // First row of matrix multiply
texm3x3pad   t2,  t0  // Second row of matrix multiply
texm3x3vspec t3,  t0  // Third row of matrix multiply to get a 3-vector
                      // Reflect 3-vector by the eye-ray vector
                      // Use reflected vector to do a texture lookup
                      //   at stage 3
mov r0, t3            // Output the result
```



Cet exemple requiert la configuration de la phase de texture suivante.

-   Une carte de texture avec des données normales est assignée à l’étape 0. On parle souvent de carte de relief. Les données sont (XYZ) normales pour chaque Texel. Les coordonnées de texture à l’étape n définissent comment échantillonner cette carte normale.
-   Le jeu de coordonnées de texture m est affecté à la ligne 1 de la matrice 3x3. Toute texture assignée à l’étape m est ignorée.
-   Le jeu de coordonnées de texture m + 1 est affecté à la ligne 2 de la matrice 3x3. Toute texture assignée à l’étape m + 1 est ignorée.
-   Le jeu de coordonnées de texture m + 2 est affecté à la ligne 3 de la matrice 3x3. L’étape m + 2 est assignée à un mappage de texture de volume ou de cube. La texture fournit des données de couleur (RVBA).
-   Le vecteur de rayon œil E est passé dans l’instruction dans le quatrième composant (q) des données de coordonnée de texture aux étapes m, m + 1 et m + 2.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




