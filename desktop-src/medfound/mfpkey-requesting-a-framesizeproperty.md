---
description: Spécifie si l’encodeur doit utiliser une taille de trame préférée donnée dans le nombre d’échantillons par image.
ms.assetid: c9baeff7-53fb-425f-b07b-4066a705ca54
title: MFPKEY_REQUESTING_A_FRAMESIZE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c39d1d9ecdba27e46a1e49949f1607fc60d53501d321e49c4899f9b8928ccf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555429"
---
# <a name="mfpkey_requesting_a_framesize-property"></a>MFPKEY \_ demandant \_ une \_ propriété de trame

Spécifie si l’encodeur doit utiliser une taille de trame préférée donnée dans le nombre d’échantillons par image.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

**VT \_ bool**

## <a name="remarks"></a>Remarques

Pour spécifier une taille de cadre préférée, définissez les propriétés suivantes.

-   Affectez à MFPKEY une valeur VARIANT pour une propriété de **\_ \_ \_ trame** \_ .
-   Définissez le cadre [**MFPKEY \_ préféré \_**](mfpkey-preferred-framesizeproperty.md) sur le nombre d’échantillons souhaité dans chaque image.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista ou Windows 7<br/>                                                   |
| En-tête<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
