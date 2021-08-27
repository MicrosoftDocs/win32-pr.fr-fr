---
description: Spécifie s’il faut utiliser un algorithme qui produit une vidéo de qualité supérieure, ou un algorithme plus rapide.
ms.assetid: a6760e7e-7c99-4412-bde5-05958fad89a1
title: MFPKEY_RESIZE_QUALITY, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e8aeb59935c8fc3462b713967ed2b14a0adfcf731fa1a71fec434b0e07d4309
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973408"
---
# <a name="mfpkey_resize_quality-property"></a>\_Propriété de qualité de REdimensionnement MFPKEY \_

Spécifie s’il faut utiliser un algorithme qui produit une vidéo de qualité supérieure, ou un algorithme plus rapide.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

VT \_ bool

## <a name="applies-to"></a>S'applique à

-   [Dimensionnement vidéo DSP](videoresizer.md)

## <a name="remarks"></a>Remarques

Utilisez l’une des valeurs suivantes :



| Valeur     | Description          |
|-----------|----------------------|
| VT \_ false | Algorithme plus rapide     |
| VT \_ vrai  | Vidéo de qualité supérieure |



 

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

 

 
