---
description: Spécifie si l’encodeur utilise l’encodage VBR moyen-contrôlable.
ms.assetid: 2c150eb1-4ffe-4f77-8ef8-e3bf29b17b10
title: MFPKEY_AVGCONSTRAINED, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0623fb4a73e3721f9079f2a1e5e330ecb466a774
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412942"
---
# <a name="mfpkey_avgconstrained-property"></a>MFPKEY \_ propriété AVGCONSTRAINED

Spécifie si l’encodeur utilise l’encodage VBR moyen-contrôlable.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

**VT \_ bool**

## <a name="default-value"></a>Valeur par défaut

**VARIANTE \_ false**

## <a name="remarks"></a>Notes

Si cette propriété et la [**propriété \_ VBRENABLED MFPKEY**](mfpkey-vbrenabledproperty.md) ont toutes les deux la valeur **Variant \_ true**, l’encodeur utilise l’encodage VBR moyen-contrôlable. Dans ce cas, l’encodeur configure lui-même en fonction des valeurs de [**MFPKEY \_ dyn \_ VBR \_ BAVG**](mfpkey-dyn-vbr-bavgproperty.md) et [**MFPKEY \_ dyn \_ VBR \_ RAVG**](mfpkey-dyn-vbr-ravgproperty.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
