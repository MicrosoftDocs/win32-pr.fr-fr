---
description: Spécifie le nombre d’échantillons par défaut par image.
ms.assetid: ad629dbd-49d8-43d0-95a8-03f2043e397e
title: MFPKEY_PREFERRED_FRAMESIZE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe04ad37c6cd684e3179cbd16328346fd6f11dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526874"
---
# <a name="mfpkey_preferred_framesize-property"></a>\_Propriété de \_ trame préférée MFPKEY

Spécifie le nombre d’échantillons par défaut par image.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

**VT \_ UI4**

## <a name="remarks"></a>Notes

Pour spécifier une taille de cadre préférée, définissez les propriétés suivantes.

-   Affectez à MFPKEY une **\_ valeur variant** pour une propriété de [**\_ \_ \_ trame**](mfpkey-requesting-a-framesizeproperty.md) .
-   Définissez le cadre **MFPKEY \_ préféré \_** sur le nombre d’échantillons souhaité dans chaque image.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista ou Windows 7<br/>                                                   |
| En-tête<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
