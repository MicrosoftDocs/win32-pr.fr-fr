---
description: Contient le GUID de catégorie pour une transformation de Media Foundation (MFT).
ms.assetid: 3c0948fc-42ea-4e43-a312-c98038020214
title: MFPKEY_CATEGORY, propriété (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bbb83ab2c824ff9a4510e520b13c49ae5b3a52a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865577"
---
# <a name="mfpkey_category-property"></a>\_Propriété de catégorie MFPKEY

Contient le GUID de catégorie pour une transformation de Media Foundation (MFT).



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**GUID** (**CLSID** \* )

\_CLSID VT

**puuid**



## <a name="remarks"></a>Notes

La valeur de cette propriété est un GUID qui identifie la catégorie MFT. Pour obtenir la liste des catégories, consultez [**MFT \_ Category**](mft-category.md).

Cette propriété est facultative et est à titre d’information uniquement. Une table MFT peut utiliser cette propriété pour signaler la catégorie sous laquelle elle est inscrite. Pour obtenir cette propriété, interrogez la table MFT pour l’interface **IPropertyStore** .

Pour énumérer une catégorie MFT, appelez la fonction [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) . Il n’existe pas de lien direct entre la fonction **MFTEnum** et cette propriété.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Transformations de Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 




