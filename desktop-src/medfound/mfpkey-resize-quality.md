---
description: Spécifie s’il faut utiliser un algorithme qui produit une vidéo de qualité supérieure, ou un algorithme plus rapide.
ms.assetid: a6760e7e-7c99-4412-bde5-05958fad89a1
title: MFPKEY_RESIZE_QUALITY, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e79ae1cac78b4d836261905afdacaf14fc227fc4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530680"
---
# <a name="mfpkey_resize_quality-property"></a>\_Propriété de qualité de REdimensionnement MFPKEY \_

Spécifie s’il faut utiliser un algorithme qui produit une vidéo de qualité supérieure, ou un algorithme plus rapide.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

VT \_ bool

## <a name="applies-to"></a>S'applique à

-   [Dimensionnement vidéo DSP](videoresizer.md)

## <a name="remarks"></a>Notes

Utilisez l’une des valeurs suivantes :



| Valeur     | Description          |
|-----------|----------------------|
| VT \_ false | Algorithme plus rapide     |
| VT \_ vrai  | Vidéo de qualité supérieure |



 

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

 

 
