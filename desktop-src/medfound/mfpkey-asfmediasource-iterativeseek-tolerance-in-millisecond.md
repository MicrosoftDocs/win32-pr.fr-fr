---
description: Définit la tolérance, en millisecondes, utilisée lorsque la source de média ASF effectue une recherche itérative.
ms.assetid: 3ee4410f-857c-4978-a308-87decfba0e2f
title: MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4190d9f87d906a701908dfc17b61633204fe8a2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106523752"
---
# <a name="mfpkey_asfmediasource_iterativeseek_tolerance_in_millisecond-property"></a>MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Tolerance \_ en \_ millisecondes

Définit la tolérance, en millisecondes, utilisée lorsque la source de média ASF effectue une recherche itérative.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**CORRESPONDANTE**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>Notes

Utilisez cette propriété pour configurer la source de média ASF. Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source. Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).

Cette propriété s’applique uniquement lorsque la recherche itérative est activée. Pour plus d’informations, consultez [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).

L’algorithme de recherche itérative s’arrête s’il trouve un paquet dont la distance par rapport à l’heure de recherche est comprise dans la tolérance spécifiée. La valeur par défaut est 8000 millisecondes.

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

 

 




