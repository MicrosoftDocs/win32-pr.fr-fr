---
description: Spécifie si l’encodeur est limité par une latence maximale de décodeur.
ms.assetid: 054e445e-fc71-4d4f-9e9f-f5ff71f0b4ee
title: MFPKEY_CONSTRAINDECLATENCY, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 343bcc9bd365b9f1321b200baa203fc27784594c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127227597"
---
# <a name="mfpkey_constraindeclatency-property"></a>MFPKEY \_ propriété CONSTRAINDECLATENCY

Spécifie si l’encodeur est limité par une latence maximale de décodeur.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

**VT \_ bool**

## <a name="default-value"></a>Valeur par défaut

**VARIANTE \_ false**

## <a name="remarks"></a>Notes

Si vous laissez cette propriété à sa valeur par défaut **Variant \_ false**, l’encodeur énumère un ensemble de modes par défaut qui ont environ 1500 millisecondes de latence de décodeur. Si vous affectez à cette propriété la **\_ valeur variant true**, vous devez également spécifier une latence maximale de décodeur en définissant la propriété [**MFPKEY \_ MAXDECLATENCYMS**](mfpkey-maxdeclatencymsproperty.md) . Dans ce cas, l’encodeur crée des modes qui répondent aux exigences de latence et énumère uniquement ces modes. L’encodeur garantit que les spécifications de la préroll (taille de mémoire tampon du décodeur) sont inférieures ou égales à **MFPKEY \_ MAXDECLATENCYMS**.

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

 

 
