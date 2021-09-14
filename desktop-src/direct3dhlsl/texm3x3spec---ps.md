---
title: texm3x3spec-PS
description: Effectue une multiplication de matrice 3x3 et utilise le résultat pour effectuer une recherche de texture. Cela peut être utilisé pour la réflexion spéculaire et le mappage d’environnement. texm3x3spec doit être utilisé conjointement avec deux instructions texm3x3pad-PS.
ms.assetid: 74269bcf-de1d-48b4-a4d0-aa08fd54b8e6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d872a5f9ebf716142fb5bc506edb77bb0b66850a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921223"
---
# <a name="texm3x3spec---ps"></a>texm3x3spec-PS

Effectue une multiplication de matrice 3x3 et utilise le résultat pour effectuer une recherche de texture. Cela peut être utilisé pour la réflexion spéculaire et le mappage d’environnement. texm3x3spec doit être utilisé conjointement avec deux instructions [texm3x3pad-PS](texm3x3pad---ps.md) .

## <a name="syntax"></a>Syntaxe



| texm3x3spec DST, src0, src1 |
|-----------------------------|



 

where

-   l’heure d’été est le registre de destination.
-   src0 et src1 sont des registres sources.

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3spec           | x    | x    | x    |      |      |      |       |      |       |



 

Cette instruction effectue une multiplication de la dernière ligne d’une matrice 3x3, utilise le vecteur résultant comme vecteur normal pour refléter un vecteur de rayons oculaires, puis utilise le vecteur réfléchi pour effectuer une recherche de texture. Le nuanceur lit le vecteur de rayon oculaire à partir d’un registre de constante. La multiplication de matrice 3x3 est généralement utile pour orienter un vecteur normal vers l’espace tangent correct pour la surface rendue.

La matrice 3x3 est composée des coordonnées de texture de la troisième étape de texture et des deux étapes de texture précédentes. Le vecteur de réflexion de publication résultant (u, v, w) est utilisé pour échantillonner la texture à l’étape de texture finale. Toute texture assignée aux deux étapes de texture précédentes est ignorée.

Cette instruction doit être utilisée avec deux instructions texm3x3pad. Les registres de texture doivent utiliser la séquence suivante.


```
 
tex t(n)                      // Define tn as a standard 3-vector (tn must
                              //   be defined in some way before it is used)
texm3x3pad t(m),   t(n)       //   where m > n
                              // Perform first row of matrix multiply
texm3x3pad  t(m+1), t(n)      // Perform second row of matrix multiply
texm3x3spec t(m+2), t(n), c0  // Perform third row of matrix multiply
                              // Then do a texture lookup on the texture
                              //   associated with texture stage m+2
```



La première instruction texm3x3pad exécute la première ligne de la multiplication pour<sup>Rechercher u.</sup>

u<sup>'</sup> = TextureCoordinates (stage m)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

La deuxième instruction texm3x3pad exécute la deuxième ligne de la multiplication pour rechercher v<sup>»</sup>.

v<sup>'</sup> = TextureCoordinates (étape m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

L’instruction texm3x3spec effectue la troisième ligne de la multiplication pour rechercher w<sup>'</sup>.

w<sup>'</sup> = TextureCoordinates (étape m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

L’instruction texm3x3spec effectue ensuite un calcul de réflexion.

(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2 \* \[ (n \* E)/(n \* n) \] \* n-E

où le N normal est donné par

N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )

et le vecteur de rayon œil E est fourni par le registre de constante

E = c \# (n’importe quel Registre de constante--C0, C1, C2, etc.--peut être utilisé)

Enfin, l’instruction texm3x3spec échantillonne t (m + 2) avec (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) et stocke le résultat dans t (m + 2).

t (m + 2)<sub>RVBA</sub> = TextureSample (étape m + 2)<sub>RVBA</sub> à l’aide de (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) en tant que coordonnées

## <a name="examples"></a>Exemples

Voici un exemple de nuanceur avec les cartes de texture et les étapes de texture identifiées.


```
ps_1_1
tex t0                    // Bind texture in stage 0 to register t0 (tn must
                          //   be defined in some way before it is used)
texm3x3pad  t1,  t0       // First row of matrix multiply
texm3x3pad  t2,  t0       // Second row of matrix multiply
texm3x3spec t3,  t0,  c#  // Third row of matrix multiply to get a 3-vector
                          // Reflect 3-vector by the eye-ray vector in c#  
                          // Use reflected vector to lookup texture in
                          //   stage 3
mov r0, t3                // Output the result
```



Cet exemple requiert la configuration de la phase de texture suivante.

-   Une carte de texture avec des données normales est assignée à l’étape 0. On parle souvent de carte de relief. Les données sont (XYZ) normales pour chaque Texel. Les coordonnées de texture à l’étape n définissent où échantillonner cette carte normale.
-   Le jeu de coordonnées de texture m est affecté à la ligne 1 de la matrice 3x3. Toute texture assignée à l’étape m est ignorée.
-   Le jeu de coordonnées de texture m + 1 est affecté à la ligne 2 de la matrice 3x3. Toute texture assignée à l’étape m + 1 est ignorée.
-   Le jeu de coordonnées de texture m + 2 est affecté à la ligne 3 de la matrice 3x3. L’étape m + 2 est assignée à un mappage de texture de volume ou de cube. La texture fournit des données de couleur (RVBA).
-   Le vecteur de rayon œil E est fourni par un registre constant E = c \# .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




