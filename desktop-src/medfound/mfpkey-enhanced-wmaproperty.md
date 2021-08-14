---
description: Spécifie si l’encodeur principal utilise la &\# 0034 ; Plus \# 0034&fonctionnalité.
ms.assetid: 1ace09da-7dee-469e-a533-63b40ac747ab
title: MFPKEY_ENHANCED_WMA, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab3fdcd3087773ea760615224b148bd497c1f89114c0f761a7d2f90fb0b5a8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738016"
---
# <a name="mfpkey_enhanced_wma-property"></a>MFPKEY \_ , \_ propriété WMA améliorée

Spécifie si l’encodeur principal utilise la fonctionnalité « plus ».

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

**VT \_ UI4**

## <a name="default-value"></a>Valeur par défaut

0

## <a name="remarks"></a>Remarques

cette propriété n’est disponible que pour les Windows Media Audio sans perte.

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

 

 
