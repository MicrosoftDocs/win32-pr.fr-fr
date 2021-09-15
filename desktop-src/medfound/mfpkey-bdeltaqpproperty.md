---
description: Spécifie l’augmentation Delta entre le quantificateur d’image du frame d’ancrage et le quantificateur d’image du cadre B.
ms.assetid: 8ab9401b-6fed-4178-955f-2e0bf950bf60
title: MFPKEY_BDELTAQP, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ba1ca7d30e17841badeda0312f77471116a8e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294899"
---
# <a name="mfpkey_bdeltaqp-property"></a>MFPKEY \_ propriété BDELTAQP

Spécifie l’augmentation Delta entre le quantificateur d’image du frame d’ancrage et le quantificateur d’image du cadre B.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCBDeltaQP g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

0

## <a name="remarks"></a>Notes

Le quantificateur d’image (QP) est une mesure de la compression d’un cadre. Des valeurs plus élevées représentent des taux de compression plus élevés. Le QP peut être défini par incréments de demi-point. Un frame B est généralement compressé à un QP de la même façon que ou 0,5 plus haut que le QP du frame d’ancrage. En spécifiant un delta de trame de B-Frame supérieur à 0, il est possible de compresser les images B à un taux de compression encore plus élevé.

Le delta du frame B ne peut être défini que dans des incréments de point entier. Cette propriété doit être définie sur une valeur entière comprise entre 0 et 31. La valeur recommandée est 1.

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

 

 




