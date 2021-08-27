---
description: 'MF_MT_FSSourceTypeDecoded attribute : spécifie si un décodeur peut utiliser des horodatages de décodage lors de la définition d’horodatages.'
title: MF_MT_FSSourceTypeDecoded
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ae25fce343d0c24f7b0a79e2623e7c3e2d0f9272b2f95a825860860ff6f88c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113759"
---
# <a name="mf_mt_fssourcetypedecoded-attribute"></a>\_ \_ Attribut FSSourceTypeDecoded MF MT

Spécifie qu’un type de média est décodé automatiquement.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**


## <a name="remarks"></a>Remarques
Un type de média est marqué comme un attribut pour indiquer qu’il n’existe pas sur la source physique et est synthétisé par le pipeline. La valeur 1 (TRUE) indique que le type de média est synthétisé. La valeur 0 (FALSe), ou la valeur qui n’est pas présente, indique qu’elle ne l’est pas.

Dans la version actuelle, cet attribut doit être spécifié à l’aide de la valeur GUID suivante au lieu de la constante MD_MT_FSSourceTypeDecoded :

```ea031a62-8bbb-43c5-b5c4-572d2d231c18```


## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




