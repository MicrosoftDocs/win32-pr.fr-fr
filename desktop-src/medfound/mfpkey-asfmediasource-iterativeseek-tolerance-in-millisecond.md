---
description: Définit la tolérance, en millisecondes, utilisée lorsque la source de média ASF effectue une recherche itérative.
ms.assetid: 3ee4410f-857c-4978-a308-87decfba0e2f
title: MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8cfc1ef656e1cff3da4bb33f19a3c2176729035f94a194a4ede21354f5dbc54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874130"
---
# <a name="mfpkey_asfmediasource_iterativeseek_tolerance_in_millisecond-property"></a>MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Tolerance \_ en \_ millisecondes

Définit la tolérance, en millisecondes, utilisée lorsque la source de média ASF effectue une recherche itérative.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**ULONG**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>Remarques

Utilisez cette propriété pour configurer la source de média ASF. Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source. Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).

Cette propriété s’applique uniquement lorsque la recherche itérative est activée. Pour plus d’informations, consultez [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).

L’algorithme de recherche itérative s’arrête s’il trouve un paquet dont la distance par rapport à l’heure de recherche est comprise dans la tolérance spécifiée. La valeur par défaut est 8000 millisecondes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Applications du serveur 2008 R2 \[ Desktop Apps \| UWP\]<br/>                     |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




