---
title: Attribut ContentDistributorDuration
description: L’attribut ContentDistributorDuration est la durée de l’exécution de l’élément, en secondes.
ms.assetid: c64cb4ca-b0bc-4beb-b2ae-ddd0c5fcd35c
keywords:
- Attribut ContentDistributorDuration lecteur Windows Media
topic_type:
- apiref
api_name:
- ContentDistributorDuration
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9f17bad8ef5dd1ab4b0a3d1c7b5becec6fd34a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521662"
---
# <a name="contentdistributorduration-attribute"></a>Attribut ContentDistributorDuration

L’attribut **ContentDistributorDuration** est la durée de l’exécution de l’élément, en secondes.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [Autres éléments](other-item-attributes.md)

## <a name="remarks"></a>Notes

Si l’attribut de **durée** normale n’est pas défini (null) ou 0, la valeur de cet attribut est retournée à la place.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------|
| Version<br/> | Lecteur Windows Media 11<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> <dt>

[**Attribut Duration**](duration-attribute.md)
</dt> </dl>

 

 





