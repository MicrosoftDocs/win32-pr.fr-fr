---
description: Spécifie si les modes énumérés par l’encodeur sont Limeted à ceux qui répondent à une exigence de qualité donnée par MFPKEY \_ souhaité \_ VBRQUALITY.
ms.assetid: b2f1d5c5-d2bb-4a8a-94ea-fd969e07bb0e
title: MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb9e63ab955bbe7726ab67bdab057fe2d397942
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127227603"
---
# <a name="mfpkey_constrain_enumerated_vbrquality-property"></a>MFPKEY \_ contraindre la \_ \_ propriété VBRQUALITY énumérée

Spécifie si les modes énumérés par l’encodeur sont Limeted à ceux qui répondent à une exigence de qualité donnée par [**MFPKEY \_ souhaité \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md).

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

**VT \_ bool**

## <a name="default-value"></a>Valeur par défaut

**VARIANTE \_ false**

## <a name="remarks"></a>Notes

Pour énumérer les modes VBR qui répondent à un certain besoin de qualité, définissez les propriétés suivantes de l’encodeur.

-   Affectez à [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) la **\_ valeur variant true**.
-   Affectez à **MFPKEY la \_ contrainte \_ énumérée \_ VBRQUALITY** la **\_ valeur variant true**.
-   Définissez [**MFPKEY \_ \_ VBRQUALITY souhaité**](mfpkey-desired-vbrqualityproperty.md) sur la qualité souhaitée. Pour les modes sans perte, définissez la qualité souhaitée sur 100.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista ou Windows 7<br/>                                                   |
| En-tête<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
