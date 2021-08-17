---
description: MFPKEY_RESIZE_INTERLACE propriété-spécifie si le flux d’entrée est entrelacé.
ms.assetid: 01ee0766-06ed-4255-9057-2fe033a772cd
title: MFPKEY_RESIZE_INTERLACE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c614865d0c8a49238b9c8d6f7714787bb22aaadaa317a8a3a0405a7f51c87be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117873033"
---
# <a name="mfpkey_resize_interlace-property"></a>\_Propriété entrelacé de REdimensionnement MFPKEY \_

Spécifie si le flux d’entrée est entrelacé.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

VT \_ bool

## <a name="applies-to"></a>S'applique à

-   [Dimensionnement vidéo DSP](videoresizer.md)

## <a name="remarks"></a>Remarques

Utilisez l’une des valeurs suivantes :



| Valeur     | Description |
|-----------|-------------|
| VT \_ false | Progressif |
| VT \_ vrai  | Interlaced  |



 

Si cette propriété n’est pas définie, le DSP utilise le type de média d’entrée pour déterminer si la vidéo est entrelacée. Vous pouvez définir cette propriété pour remplacer le paramètre de type de média.

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

 

 
