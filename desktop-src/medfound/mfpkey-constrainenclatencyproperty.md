---
description: Spécifie si l’encodeur est limité par une latence maximale.
ms.assetid: 8148ae1e-239e-40fa-a88d-810a1d93d8e9
title: MFPKEY_CONSTRAINENCLATENCY, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8172b92b0b4d39602f0535b8bf1ef4456a896972e56c6da10f6585e5221fa7e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113419"
---
# <a name="mfpkey_constrainenclatency-property"></a>MFPKEY \_ propriété CONSTRAINENCLATENCY

Spécifie si l’encodeur est limité par une latence maximale.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

**VT \_ bool**

## <a name="default-value"></a>Valeur par défaut

**VARIANTE \_ false**

## <a name="remarks"></a>Remarques

Si vous laissez cette propriété à sa valeur par défaut **Variant \_ false**, l’encodeur énumère un ensemble de modes par défaut qui ont environ 2000 millisecondes de latence de l’encodeur. Si vous affectez à cette propriété la **\_ valeur variant true**, vous devez également spécifier une latence maximale de l’encodeur en définissant la propriété [**MFPKEY \_ MAXENCLATENCYMS**](mfpkey-maxenclatencymsproperty.md) . Dans ce cas, l’encodeur crée des modes qui répondent aux exigences de latence et énumère uniquement ces modes. L’encodeur garantit un échantillon de sortie dès que l’encodeur a reçu une entrée pour une période de temps égale à **MFPKEY \_ MAXENCLATENCYMS**.

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

 

 
