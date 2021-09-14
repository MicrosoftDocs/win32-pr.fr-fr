---
description: Spécifie la matrice de canal, qui est utilisée pour convertir les canaux sources en canaux de destination (par exemple, pour convertir 5,1 en stéréo).
ms.assetid: 2f2a82bd-f051-4b05-a9c8-37aa4403fab4
title: MFPKEY_WMRESAMP_CHANNELMTX, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e39f9a9344dd080362859592fcf1f71657ee8f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414077"
---
# <a name="mfpkey_wmresamp_channelmtx-property"></a>MFPKEY \_ WMRESAMP \_ CHANNELMTX, propriété

Spécifie la matrice de canal, qui est utilisée pour convertir les canaux sources en canaux de destination (par exemple, pour convertir 5,1 en stéréo).

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

\_Tableau VT I4 \| VT \_

## <a name="applies-to"></a>S'applique à

-   [Modèle de rééchantillonnage audio DSP](audioresampler.md)

## <a name="remarks"></a>Notes

La valeur de la propriété est une matrice de coefficients NS x ND, où ns est le nombre de canaux sources et ND le nombre de canaux de destination. Les coefficients sont spécifiés en décibels à l’aide de la formule suivante :

tiers (65536 \* 20 \* log10 (dB))

La matrice est stockée sous la forme d’un tableau dans l’ordre ligne-principal, où le numéro de ligne est le canal source et le numéro de colonne est le canal de destination.

Par conséquent, si la matrice est la suivante :

``` syntax
00       01       ...      0(Ns-1)
10       11       ...      1(Ns-1)
...      ...      ...      ...
(Nd-1)0 (Nd-1)1 ... (Nd-1)(Ns-1)
```

vous devez ensuite spécifier le tableau comme suit :

``` syntax
[ 00, 01, ..., 0(Ns-1), 10, 11, ..., 1(Ns-1), ..., (Nd-1)0, (Nd-1)1, ..., (Nd-1)(Ns-1) ]
```

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
