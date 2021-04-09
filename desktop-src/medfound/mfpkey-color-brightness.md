---
description: Ajuste la luminosité.
ms.assetid: 1b3f56eb-3f22-4120-ba6c-331eccd5d303
title: MFPKEY_COLOR_BRIGHTNESS, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 685ab934a91f1843183fcfa88bb94c83e602db27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864774"
---
# <a name="mfpkey_color_brightness-property"></a>Propriété de luminosité des \_ couleurs MFPKEY \_

Ajuste la luminosité.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

0

## <a name="applies-to"></a>S'applique à

-   [Transformation de contrôle de couleur DSP](colorcontroltransform.md)

## <a name="remarks"></a>Notes

L’ajustement de la luminosité s’effectue en ajoutant une valeur au canal de luminance.

Cette propriété a une plage comprise entre-127 et 127. La valeur zéro indique qu’aucune modification n’est apportée à la luminosité.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
