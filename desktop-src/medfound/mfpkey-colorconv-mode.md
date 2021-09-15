---
description: MFPKEY_COLORCONV_MODE propriété-spécifie si le flux d’entrée est entrelacé.
ms.assetid: d0d93151-5b0d-44a7-8497-f11b3e23a031
title: MFPKEY_COLORCONV_MODE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8c3f2d6256c4d7a9410264fb18703eea251e9c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525717"
---
# <a name="mfpkey_colorconv_mode-property"></a>MFPKEY \_ \_ propriété mode COLORCONV

Spécifie si le flux d’entrée est entrelacé.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

Calculé par le DSP à partir de la vidéo source.

## <a name="applies-to"></a>S'applique à

-   [Convertisseur de couleurs DSP](colorconverter.md)

## <a name="remarks"></a>Notes

Utilisez l’une des valeurs suivantes.



| Valeur | Description |
|-------|-------------|
| 0     | Progressif |
| 2     | Interlaced  |



 

Si cette propriété n’est pas définie, le DSP utilise le type de média d’entrée pour déterminer si la vidéo est entrelacée. Vous pouvez définir cette propriété pour remplacer le paramètre de type de média.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
