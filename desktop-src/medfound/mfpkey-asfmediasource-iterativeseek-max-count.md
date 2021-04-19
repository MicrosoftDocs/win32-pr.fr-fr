---
description: Définit le nombre maximal d’itérations de recherche que la source de média ASF utilisera lors de la recherche itérative.
ms.assetid: 5b596faf-1217-424d-ae16-8c9ec6f31af1
title: MFPKEY_ASFMediaSource_IterativeSeek_Max_Count, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfb9268f1def2ab0d489f58cafa0b1720196c7ac
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106523754"
---
# <a name="mfpkey_asfmediasource_iterativeseek_max_count-property"></a>\_Propriété MFPKEY ASFMediaSource \_ IterativeSeek \_ Max \_ Count

Définit le nombre maximal d’itérations de recherche que la source de média ASF utilisera lors de la recherche itérative.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**CORRESPONDANTE**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>Notes

Utilisez cette propriété pour configurer la source de média ASF. Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source. Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).

Cette propriété s’applique uniquement lorsque la recherche itérative est activée. Pour plus d’informations, consultez [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).

La plage valide de cette propriété est \[ 1-10 \] , inclus. Avec un nombre plus élevé, la recherche itérative a tendance à être plus précise, mais elle prend plus de temps.

La valeur par défaut est 5.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 7 \[ Desktop Apps \| UWP\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]<br/>                     |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




