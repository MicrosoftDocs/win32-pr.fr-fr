---
title: texreg2rgb-PS
description: Interprète les composants de couleur rouge, vert et bleu (RVB) du Registre source comme des données d’adresse de texture afin d’échantillonner la texture à l’étape correspondant au numéro de registre de destination. Le résultat est stocké dans le registre de destination.
ms.assetid: 8ec44014-d796-407c-8fe0-036decaf2a3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f8bcd2bbd7e57ba9dc692f34404a5610cdc517f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921207"
---
# <a name="texreg2rgb---ps"></a>texreg2rgb-PS

Interprète les composants de couleur rouge, vert et bleu (RVB) du Registre source comme des données d’adresse de texture afin d’échantillonner la texture à l’étape correspondant au numéro de registre de destination. Le résultat est stocké dans le registre de destination.

## <a name="syntax"></a>Syntaxe



| texreg2rgb DST, SRC |
|---------------------|



 

where

-   l’heure d’été est le registre de destination.
-   SRC est un registre source.

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texreg2rgb            |      | x    | x    |      |      |      |       |      |       |



 

Cette instruction est utile pour les opérations de remappage de l’espace colorimétrique. Il prend en charge les coordonnées à deux dimensions (2D) et à trois dimensions (3D). Il peut être utilisé comme [texreg2ar-PS](texreg2ar---ps.md) ou [texreg2gb-PS](texreg2gb---ps.md) pour remapper les données 2D. Toutefois, cette instruction prend également en charge les données 3D afin qu’elles puissent être utilisées avec les textures de cube et de volume 3D.

Voici un exemple de la séquence suivi par l’instruction.


```
 
tex t(n)
texreg2rgb t(m), t(n)     where m > n
```



Voici plus de détails sur la façon dont le remappage est accompli.

<dl> La première instruction charge la couleur de texture (RVBA) dans le registre TN  
Tex TN  
La deuxième instruction remappe la couleur.  
t (m)<sub>RVBA</sub> = TextureSample (stage m)<sub>RVBA</sub> utilisant t (n)<sub>RGB</sub> en tant que coordonnées
</dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




