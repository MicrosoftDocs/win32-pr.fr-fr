---
description: Cette propriété interroge le décodeur à la fréquence d’images entières maximale que le décodeur prend en charge. Le type de données de cette propriété est une \_ structure am QueryRate.
ms.assetid: 98808ed4-6d34-437b-9729-9cc805bc81f0
title: AM_RATE_QueryFullFrameRate, propriété (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2c99564caa09253198b101a3e2467ec88c7e34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526777"
---
# <a name="am_rate_queryfullframerate-property"></a>\_ \_ Propriété QUERYFULLFRAMERATE rate AM

Cette propriété interroge le décodeur à la fréquence d’images entières maximale que le décodeur prend en charge. Le type de données de cette propriété est une structure **am \_ QueryRate** .

Cette propriété est définie pour la version 1,1 de ce jeu de propriétés ; consultez [**am \_ rate \_ UseRateVersion**](am-rate-userateversion-property.md).



|                   |                                       |
|-------------------|---------------------------------------|
| GUID de jeu de propriétés | AM \_ KSPROPSETID \_ TSRateChange         |
| ID de propriété       | \_ \_ Propriété QUERYFULLFRAMERATE rate AM |
| Type de données         | [**AM \_ QueryRate**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_queryrate) |



 

## <a name="remarks"></a>Notes

Si la vitesse de lecture dépasse la vitesse maximale du décodeur, le filtre source envoie des groupes d’échantillons continus séparés par des discontinuités. Les horodatages sautent dans les discontinuités. Le filtre source peut effectuer cette opération même si la vitesse de lecture est comprise dans la vitesse maximale du décodeur, car il peut y avoir d’autres facteurs, tels que les e/s disque, qui limitent la vitesse de lecture complète.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Définition de la propriété change rate**](rate-change-property-set.md)
</dt> </dl>

 

 




