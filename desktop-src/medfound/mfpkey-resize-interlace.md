---
description: MFPKEY_RESIZE_INTERLACE propriété-spécifie si le flux d’entrée est entrelacé.
ms.assetid: 01ee0766-06ed-4255-9057-2fe033a772cd
title: MFPKEY_RESIZE_INTERLACE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45d0efe93901a08322a05dbed2515f76b04a214b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092877"
---
# <a name="mfpkey_resize_interlace-property"></a>\_Propriété entrelacé de REdimensionnement MFPKEY \_

Spécifie si le flux d’entrée est entrelacé.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

VT \_ bool

## <a name="applies-to"></a>S'applique à

-   [Dimensionnement vidéo DSP](videoresizer.md)

## <a name="remarks"></a>Notes 

Utilisez l’une des valeurs suivantes :



| Valeur     | Description |
|-----------|-------------|
| VT \_ false | Progressif |
| VT \_ vrai  | Interlaced  |



 

Si cette propriété n’est pas définie, le DSP utilise le type de média d’entrée pour déterminer si la vidéo est entrelacée. Vous pouvez définir cette propriété pour remplacer le paramètre de type de média.

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

 

 
