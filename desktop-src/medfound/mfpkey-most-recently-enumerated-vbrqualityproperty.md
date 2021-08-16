---
description: Spécifie le niveau de qualité VBR du type de sortie énuméré le plus récemment.
ms.assetid: 7d67e41f-060b-49a1-9e17-5db081ef4210
title: MFPKEY_MOST_RECENT_ENUMERATED_VBRQUALITY, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68e609f8dc7b95eb9cfd4bf537af47d1a11cb4ba625f0bbc65897b008ff03a31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117689793"
---
# <a name="mfpkey_most_recent_enumerated_vbrquality-property"></a>MFPKEY \_ \_ \_ propriété VBRQUALITY énumérée la plus récente \_

Spécifie le niveau de qualité VBR du type de sortie énuméré le plus récemment. Lecture seule.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

**VT \_ UI4**

## <a name="remarks"></a>Remarques

Lorsque l’encodeur agit comme une Media Foundation transformation (MFT) et qu’il énumère un type de sortie sur un appel à [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype), vous pouvez interroger la table MFT pour obtenir la propriété **\_ \_ \_ \_ VBRQUALITY énumérée la plus récente de MFPKEY** . La valeur retournée indique la qualité VBR du type de média de sortie retourné le plus récemment. Vous pouvez ensuite utiliser cette valeur pour définir la propriété [**MFPKEY \_ souhaitée \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) de l’encodeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista ou Windows 7<br/>                                                   |
| En-tête<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md)
</dt> <dt>

[**MFPKEY de \_ contrainte \_ énumérée \_ VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
