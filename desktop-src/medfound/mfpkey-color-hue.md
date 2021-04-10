---
description: Ajuste la teinte.
ms.assetid: 8dc3c888-5ab8-40a1-8768-bec58b62eaf0
title: MFPKEY_COLOR_HUE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b3ddf0109090bfb56102560dc06a853c970e7ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115135"
---
# <a name="mfpkey_color_hue-property"></a>\_ \_ Propriété teinte de couleur MFPKEY

Ajuste la teinte.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

0

## <a name="applies-to"></a>S'applique à

-   [Transformation de contrôle de couleur DSP](colorcontroltransform.md)

## <a name="remarks"></a>Notes

L’ajustement de la teinte est effectué en combinant les valeurs CB et CR. (Si CB et CR sont tracés dans un espace à deux dimensions, l’ajustement de la teinte est effectué en faisant tourner l’origine.)

Cette propriété a une plage comprise entre-127 et 127. La valeur zéro indique qu’il n’y a aucune modification de la teinte.

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

 

 
