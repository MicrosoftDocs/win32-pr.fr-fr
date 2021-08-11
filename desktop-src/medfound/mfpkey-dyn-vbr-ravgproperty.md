---
description: Spécifie la vitesse de transmission moyenne, en bits par seconde, pour un encodeur qui est configuré pour utiliser l’encodage VBR moyen-contrôlable.
ms.assetid: d689a34c-97f7-4b1c-82b6-863ce3b8403f
title: MFPKEY_DYN_VBR_RAVG, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48ee3d3a9b9a60b664041b9c6f84c38b8da9ceef87f73177f2ace792cf043992
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118242611"
---
# <a name="mfpkey_dyn_vbr_ravg-property"></a>MFPKEY \_ dyn \_ VBR \_ RAVG, propriété

Spécifie la vitesse de transmission moyenne, en bits par seconde, pour un encodeur qui est configuré pour utiliser l’encodage VBR moyen-contrôlable.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

**VT \_**

## <a name="remarks"></a>Notes

Si les propriétés [**MFPKEY \_ AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) et [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) sont toutes deux définies sur **Variant \_ true**, l’encodeur utilise l’encodage VBR moyen-contrôlable. Dans ce cas, l’encodeur configure lui-même en fonction de la valeur de cette propriété et de la propriété [**MFPKEY \_ dyn \_ VBR \_ BAVG**](mfpkey-dyn-vbr-bavgproperty.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
