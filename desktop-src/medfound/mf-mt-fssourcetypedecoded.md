---
description: 'MF_MT_FSSourceTypeDecoded attribute : spécifie si un décodeur peut utiliser des horodatages de décodage lors de la définition d’horodatages.'
title: MF_MT_FSSourceTypeDecoded
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3799c11e3b921427ff4a3b05aa3d7f47e297ba14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093087"
---
# <a name="mf_mt_fssourcetypedecoded-attribute"></a>\_ \_ Attribut FSSourceTypeDecoded MF MT

Spécifie qu’un type de média est décodé automatiquement.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**


## <a name="remarks"></a>Notes 
Un type de média est marqué comme un attribut pour indiquer qu’il n’existe pas sur la source physique et est synthétisé par le pipeline. La valeur 1 (TRUE) indique que le type de média est synthétisé. La valeur 0 (FALSe), ou la valeur qui n’est pas présente, indique qu’elle ne l’est pas.

Dans la version actuelle, cet attribut doit être spécifié à l’aide de la valeur GUID suivante au lieu de la constante MD_MT_FSSourceTypeDecoded :

```ea031a62-8bbb-43c5-b5c4-572d2d231c18```


## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 8 \[ Desktop Apps \| UWP\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ \| apps UWP\]<br/>                        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




