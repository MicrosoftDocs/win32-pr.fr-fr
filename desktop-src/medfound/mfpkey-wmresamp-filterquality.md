---
description: Spécifie la qualité de la sortie.
ms.assetid: 7b45633b-7f1c-4951-a462-ad6240b9ca31
title: MFPKEY_WMRESAMP_FILTERQUALITY, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf00b757bd07add37f6a5b82459f37df40f9fb36ea6ef813e011adcadde196e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119603369"
---
# <a name="mfpkey_wmresamp_filterquality-property"></a>MFPKEY \_ WMRESAMP \_ FILTERQUALITY, propriété

Spécifie la qualité de la sortie.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

VT \_

## <a name="applies-to"></a>S'applique à

-   [Modèle de rééchantillonnage audio DSP](audioresampler.md)

## <a name="remarks"></a>Remarques

La plage valide de cette propriété est comprise entre 1 et 60 inclus. Des valeurs plus élevées produisent une sortie de qualité supérieure, mais introduisent plus de latence. La valeur 1 est fondamentalement identique à l’interpolation linéaire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
