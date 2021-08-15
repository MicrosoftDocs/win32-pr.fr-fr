---
description: Spécifie si l’encodeur utilise l’encodage VBR moyen-contrôlable.
ms.assetid: 2c150eb1-4ffe-4f77-8ef8-e3bf29b17b10
title: MFPKEY_AVGCONSTRAINED, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3e7231cb3807be8f4467592ac0138a75ea277bdf8a13dfb3564d3572036e7ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874091"
---
# <a name="mfpkey_avgconstrained-property"></a>MFPKEY \_ propriété AVGCONSTRAINED

Spécifie si l’encodeur utilise l’encodage VBR moyen-contrôlable.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

**VT \_ bool**

## <a name="default-value"></a>Valeur par défaut

**VARIANTE \_ false**

## <a name="remarks"></a>Remarques

Si cette propriété et la [**propriété \_ VBRENABLED MFPKEY**](mfpkey-vbrenabledproperty.md) ont toutes les deux la valeur **Variant \_ true**, l’encodeur utilise l’encodage VBR moyen-contrôlable. Dans ce cas, l’encodeur configure lui-même en fonction des valeurs de [**MFPKEY \_ dyn \_ VBR \_ BAVG**](mfpkey-dyn-vbr-bavgproperty.md) et [**MFPKEY \_ dyn \_ VBR \_ RAVG**](mfpkey-dyn-vbr-ravgproperty.md).

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

 

 
