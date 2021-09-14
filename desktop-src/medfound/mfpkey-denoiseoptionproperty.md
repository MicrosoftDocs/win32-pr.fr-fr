---
description: Spécifie si le codec doit utiliser le filtre de bruit lors de l’encodage.
ms.assetid: 9e099378-bb77-4dca-9171-7fe58e0139de
title: MFPKEY_DENOISEOPTION, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7f318e294f69095758fe300fce19043c23cf376
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127227520"
---
# <a name="mfpkey_denoiseoption-property"></a>MFPKEY \_ propriété DENOISEOPTION

Spécifie si le codec doit utiliser le filtre de bruit lors de l’encodage.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCDenoiseOption g

## <a name="data-type"></a>Type de données

VT \_ bool

## <a name="default-value"></a>Valeur par défaut

FALSE

## <a name="remarks"></a>Notes

Le filtre de bruit peut améliorer la qualité des sources vidéo bruyantes, telles que les films contenant un grand nombre de grains ou d’images vidéo en faible luminosité. Ce filtre peut être utilisé dans les scénarios d’encodage en temps réel où le prétraitement externe n’est pas une option.

Ce filtre doit être désactivé pour les sources vidéo propres, car il peut réduire la qualité de l’image lorsque la qualité est bonne.

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

 

 




