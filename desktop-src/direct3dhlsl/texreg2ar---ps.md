---
title: texreg2ar-PS
description: Interprète les composants de couleur alpha et rouges du Registre source en tant que données d’adresse de texture (u, v) pour échantillonner la texture à l’étape correspondant au numéro de registre de destination. Le résultat est stocké dans le registre de destination.
ms.assetid: b31a2ee4-f9b9-4aee-b3be-7ccc5b8c6f3e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 93418e7e9e87178cd64c2d7238b5227de0990378
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921216"
---
# <a name="texreg2ar---ps"></a>texreg2ar-PS

Interprète les composants de couleur alpha et rouges du Registre source en tant que données d’adresse de texture (u, v) pour échantillonner la texture à l’étape correspondant au numéro de registre de destination. Le résultat est stocké dans le registre de destination.

## <a name="syntax"></a>Syntaxe



| texreg2ar DST, SRC |
|--------------------|



 

where

-   l’heure d’été est le registre de destination.
-   SRC est un registre source.

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texreg2ar             | x    | x    | x    |      |      |      |       |      |       |



 

Cette instruction est utile pour les opérations de remappage de l’espace colorimétrique.

Voici un exemple de la séquence que l’instruction suit :

<dl> Tex t (n)  
texreg2ar t (m), t (n) où m > n  
La première instruction charge la couleur de texture (RVBA)  
dans Register TN  
Tex TN  
La deuxième instruction remappe la couleur.  
t (m)<sub>RVBA</sub> = TextureSample (stage m)<sub>RVBA</sub> utilisant t (n)<sub>AR</sub> comme coordonnées
</dl>

\_BX2 ne peut pas être utilisé sur le registre SRC pour les instructions texreg2ar ou [texreg2gb-PS](texreg2gb---ps.md) .

Pour cette instruction, le registre source doit utiliser des données non signées. L’utilisation de données signées ou mixtes dans le registre source produira des résultats indéfinis. Pour plus d’informations, consultez [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 