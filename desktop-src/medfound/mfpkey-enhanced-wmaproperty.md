---
description: Spécifie si l’encodeur principal utilise la &\# 0034 ; Plus \# 0034&fonctionnalité.
ms.assetid: 1ace09da-7dee-469e-a533-63b40ac747ab
title: MFPKEY_ENHANCED_WMA, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df1c7ddc0e7bfb6d62d51e535f10b257eac6f2ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525664"
---
# <a name="mfpkey_enhanced_wma-property"></a>MFPKEY \_ , \_ propriété WMA améliorée

Spécifie si l’encodeur principal utilise la fonctionnalité « plus ».

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

**VT \_ UI4**

## <a name="default-value"></a>Valeur par défaut

0

## <a name="remarks"></a>Notes

Cette propriété n’est disponible que pour les Windows Media Audio sans perte.

Si vous laissez cette propriété à sa valeur par défaut égale à 0 ou si vous la définissez sur 1, l’encodeur principal détermine si la partie « plus » doit être utilisée. Si vous affectez à cette propriété la valeur 2, l’encodeur principal n’utilise pas la fonctionnalité « plus ».

Cette propriété modifie les types de médias énumérés. par conséquent, si vous la définissez, vous devez le faire avant de définir le type de sortie.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista ou Windows 7<br/>                                                   |
| En-tête<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
