---
title: texdp3tex-PS
description: Exécute un produit scalaire à trois composants et utilise le résultat pour effectuer une recherche de texture 1D.
ms.assetid: vs|directx_sdk|~\texdp3tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dfe74dd0a73bc47cd2855d35b239e80a1b5153c1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921228"
---
# <a name="texdp3tex---ps"></a>texdp3tex-PS

Exécute un produit scalaire à trois composants et utilise le résultat pour effectuer une recherche de texture 1D.

## <a name="syntax"></a>Syntaxe



| texdp3tex DST, SRC |
|--------------------|



 

where

-   l’heure d’été est le registre de destination.
-   SRC est un registre source.

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texdp3tex             |      | x    | x    |      |      |      |       |      |       |



 

Les registres de texture doivent utiliser la séquence suivante.


```
 
tex       t(n)        // Define tn as a standard 3-vector (tn must be 
                      // defined in some way before texdp3tex uses it)
texdp3tex t(m), t(n)  // where m > n                 
                      // Perform a three-component dot product between t(n) and 
                      // the texture coordinate set m. Use the scalar result to
                      // do a 1D texture lookup at texturestage m and place
                      // the result in t(m)
```



Voici plus de détails sur la façon dont le produit scalaire et la recherche de texture sont effectués.

L’instruction texdp3tex exécute un produit à trois composants.

u' = TextureCoordinates (stage m)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

Le résultat est utilisé pour échantillonner la texture à l’étape de texture m en effectuant une recherche 1D.

t (m)<sub>RVBA</sub> = TextureSample (stage m)<sub>RVBA</sub> utilisant (u', 0,0) comme coordonnées

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




