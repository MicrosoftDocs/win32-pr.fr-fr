---
description: Ajuste la saturation.
ms.assetid: bd71f542-36d9-4dfc-b402-35ee8e574731
title: MFPKEY_COLOR_SATURATION, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b357521327bc913a0ace6b630cb9f2a27b553c3dfc8303e1a6bd9af218c5b743
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954399"
---
# <a name="mfpkey_color_saturation-property"></a>\_ \_ Propriété saturation de la couleur MFPKEY

Ajuste la saturation.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

0

## <a name="applies-to"></a>S'applique à

-   [Transformation de contrôle de couleur DSP](colorcontroltransform.md)

## <a name="remarks"></a>Remarques

L’ajustement de saturation s’effectue en multipliant les valeurs CB et CR par une constante.

Cette propriété a une plage comprise entre-127 et 127. La valeur zéro indique qu’aucune modification n’est apportée à la saturation.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
