---
title: lit-vs
description: Fournit une prise en charge partielle de l’éclairage en calculant les coefficients d’éclairage à partir de deux produits points et d’un exposant.
ms.assetid: e0ed1a75-6682-4d05-b0e5-dc65e201de98
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3e5b5ff3451424251d778886af3841c673ce5a85d91022db9144c62574c16640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118089322"
---
# <a name="lit---vs"></a>lit-vs

Fournit une prise en charge partielle de l’éclairage en calculant les coefficients d’éclairage à partir de deux produits points et d’un exposant.

## <a name="syntax"></a>Syntaxe



| allumé DST, SRC |
|--------------|



 

where

-   l’heure d’été est le registre de destination.
-   SRC est un registre source.

## <a name="remarks"></a>Remarques



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| orange                    | x    | x    | x    | x     | x    | x     |



 

Le vecteur source est supposé contenir les valeurs indiquées dans le pseudo-code suivant.


```
src.x = N*L        ; The dot product between normal and direction to light
src.y = N*H        ; The dot product between normal and half vector
src.z = ignored    ; This value is ignored
src.w = exponent   ; The value must be between -128.0 and 128.0
```



Le fragment de code suivant montre les opérations effectuées.


```
dest.x = 1;
dest.y = 0;
dest.z = 0;
dest.w = 1;

float power = src.w;
const float MAXPOWER = 127.9961f;
if (power < -MAXPOWER)
    power = -MAXPOWER;          // Fits into 8.8 fixed point format
else if (power > MAXPOWER)
    power = MAXPOWER;          // Fits into 8.8 fixed point format

if (src.x > 0)
{
    dest.y = src.x;
    if (src.y > 0)
    {
        // Allowed approximation is EXP(power * LOG(src.y))
        dest.z = (float)(pow(src.y, power));
    }
}
```



Une opération arithmétique de précision réduite est acceptable pour l’évaluation du composant y de destination (dest. y). Une implémentation doit prendre en charge au moins huit bits fractionnaires dans l’argument Power. Les produits scalaires sont calculés avec des vecteurs normalisés, et les limites de fixation sont com128 à 128.

L’erreur doit correspondre à une combinaison [logP-vs](logp---vs.md) et [exp-vs](exp---vs.md) , ou à environ un bit significatif pour un composant de couleur de 8 bits.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




