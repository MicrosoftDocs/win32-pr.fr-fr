---
description: Spécifie si l’encodeur est limité par une latence maximale.
ms.assetid: 8148ae1e-239e-40fa-a88d-810a1d93d8e9
title: MFPKEY_CONSTRAINENCLATENCY, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f880006bf2aba04196547a79e74f94a7210edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543492"
---
# <a name="mfpkey_constrainenclatency-property"></a>MFPKEY \_ propriété CONSTRAINENCLATENCY

Spécifie si l’encodeur est limité par une latence maximale.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

**VT \_ bool**

## <a name="default-value"></a>Valeur par défaut

**VARIANTE \_ false**

## <a name="remarks"></a>Notes

Si vous laissez cette propriété à sa valeur par défaut **Variant \_ false**, l’encodeur énumère un ensemble de modes par défaut qui ont environ 2000 millisecondes de latence de l’encodeur. Si vous affectez à cette propriété la **\_ valeur variant true**, vous devez également spécifier une latence maximale de l’encodeur en définissant la propriété [**MFPKEY \_ MAXENCLATENCYMS**](mfpkey-maxenclatencymsproperty.md) . Dans ce cas, l’encodeur crée des modes qui répondent aux exigences de latence et énumère uniquement ces modes. L’encodeur garantit un échantillon de sortie dès que l’encodeur a reçu une entrée pour une période de temps égale à **MFPKEY \_ MAXENCLATENCYMS**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
