---
description: Spécifie la fenêtre de mémoire tampon, en millisecondes, pour un encodeur qui est configuré pour utiliser l’encodage VBR moyen-contrôlable.
ms.assetid: ce330ce0-4bda-4340-b21c-63a8b9168cf4
title: MFPKEY_DYN_VBR_BAVG, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77ba4d3f3d7a5587a7c8aa90771f58accd8a80864dd5a875c6c580eb9e29e01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738159"
---
# <a name="mfpkey_dyn_vbr_bavg-property"></a>MFPKEY \_ dyn \_ VBR \_ BAVG, propriété

Spécifie la fenêtre de mémoire tampon, en millisecondes, pour un encodeur qui est configuré pour utiliser l’encodage VBR moyen-contrôlable.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

**VT \_**

## <a name="remarks"></a>Remarques

Si les propriétés [**MFPKEY \_ AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) et [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) sont toutes deux définies sur **Variant \_ true**, l’encodeur utilise l’encodage VBR moyen-contrôlable. Dans ce cas, l’encodeur configure lui-même en fonction de la valeur de cette propriété et de la propriété [**MFPKEY \_ dyn \_ VBR \_ RAVG**](mfpkey-dyn-vbr-ravgproperty.md) .

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

 

 
