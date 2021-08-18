---
title: texdp3-PS
description: Exécute un produit scalaire à trois composants entre les données du numéro du registre de texture et le jeu de coordonnées de texture correspondant au numéro de registre de destination.
ms.assetid: 82e02f3f-4b88-4007-b4be-0c66223d9c66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e39f2682aac7741af304269b0584f3552158b2f83596c7fd55f1c83948d09f0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788199"
---
# <a name="texdp3---ps"></a>texdp3-PS

Exécute un produit scalaire à trois composants entre les données du numéro du registre de texture et le jeu de coordonnées de texture correspondant au numéro de registre de destination.

## <a name="syntax"></a>Syntaxe



| texdp3 DST, SRC |
|-----------------|



 

where

-   l’heure d’été est le registre de destination.
-   SRC est un registre source.

## <a name="remarks"></a>Remarques



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texdp3                |      | x    | x    |      |      |      |       |      |       |



 

Les registres de texture doivent utiliser la séquence suivante.


```
 
tex    t(n)        // Define tn as a standard 3-vector (tn must be 
                   //   defined in some way before texdp3 uses it)
texdp3 t(m), t(n)  // where m > n
                   // Perform a three-component dot product between tn and 
                   //   the texture coordinate set m. The scalar result is
                   //   replicated to all components of t(m)
```



Voici plus de détails sur la façon dont le produit scalaire est accompli.

L’instruction texdp3 exécute un produit à trois composants et la réplique sur les quatre canaux de couleurs.

t (m)<sub>RVBA</sub> = TextureCoordinates (étape m)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




