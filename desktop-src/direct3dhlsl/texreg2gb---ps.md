---
title: texreg2gb-PS
description: Interprète les composants de couleur vert et bleu du Registre source comme des données d’adresse de texture pour échantillonner la texture à l’étape correspondant au numéro de registre de destination.
ms.assetid: 81d3fb3e-ef53-4d25-b65d-c4c9fea0c74c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb18a2a79132a08e2659c6df426299ce996beba79566af277500ab9eb0a885f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118505747"
---
# <a name="texreg2gb---ps"></a>texreg2gb-PS

Interprète les composants de couleur vert et bleu du Registre source comme des données d’adresse de texture pour échantillonner la texture à l’étape correspondant au numéro de registre de destination.

## <a name="syntax"></a>Syntaxe



| texreg2gb DST, SRC |
|--------------------|



 

where

-   l’heure d’été est le registre de destination.
-   SRC est un registre source.

## <a name="remarks"></a>Remarques



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texreg2gb             |      | x    | x    |      |      |      |       |      |       |



 

Cette instruction est utile pour les opérations de remappage de l’espace colorimétrique.

Voici un exemple de la séquence suivi par l’instruction.

<dl> Tex t (n)  
texreg2gb t (m), t (n) où m > n  
La première instruction charge la couleur de texture (RVBA)  
dans Register TN  
Tex TN  
La deuxième instruction remappe la couleur.  
t (m)<sub>RVBA</sub> = TextureSample (stage m)<sub>RVBA</sub> utilisant t (n)<sub>Go</sub> en tant que coordonnées
</dl>

\_BX2 ne peut pas être utilisé sur le registre SRC pour les instructions [texreg2ar-PS](texreg2ar---ps.md) ou texreg2gb.

Pour cette instruction, le registre source doit utiliser des données non signées. L’utilisation de données signées ou mixtes dans le registre source produira des résultats indéfinis. Pour plus d’informations, consultez [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 