---
title: Constantes TS_SHIFT_ (Textstor. h)
description: Les \_ \_ constantes TS Shift \ sont utilisées par l’interface IAnchor pour la manipulation du texte masqué et du comptage des caractères.
ms.assetid: 93329238-f6e8-432e-9167-550a02b33b46
topic_type:
- apiref
api_name:
- TS_SHIFT_COUNT_HIDDEN
- TS_SHIFT_HALT_HIDDEN
- TS_SHIFT_HALT_VISIBLE
- TS_SHIFT_COUNT_ONLY
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f3a11463aea1633079d771bf6a8b333475865e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384695"
---
# <a name="ts_shift_-constants"></a>\_Constantes de décalage TS \_ \*

Les \_ \_ \* constantes de décalage TS sont utilisées par l’interface **IAnchor** pour la manipulation du texte masqué et du comptage de caractères.



| Constante/valeur                                                                                                                                                                                                                                       | Description                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_SHIFT_COUNT_HIDDEN"></span><span id="ts_shift_count_hidden"></span><dl> <dt>**TS \_ Nombre de DÉCALAGEs \_ \_ masqué**</dt> <dt>(0x1)</dt> </dl> | Spécifie que l’ancre sera déplacée vers la limite de région suivante, y compris la limite d’une zone de texte masqué. S’il n’est pas défini, le point d’ancrage est déplacé au-delà du texte masqué adjacent jusqu’à ce qu’une région de texte visible soit trouvée.<br/> |
| <span id="TS_SHIFT_HALT_HIDDEN"></span><span id="ts_shift_halt_hidden"></span><dl> <dt>**TS \_ Arrêt du décalage \_ \_ masqué**</dt> <dt>(0X2)</dt> </dl>    | Non utilisé.<br/>                                                                                                                                                                                                                            |
| <span id="TS_SHIFT_HALT_VISIBLE"></span><span id="ts_shift_halt_visible"></span><dl> <dt>**TS \_ Arrêt du décalage \_ \_ visible**</dt> <dt>(0x4)</dt> </dl> | Non utilisé.<br/>                                                                                                                                                                                                                            |
| <span id="TS_SHIFT_COUNT_ONLY"></span><span id="ts_shift_count_only"></span><dl> <dt>**TS \_ Nombre de DÉCALAGEs \_ \_ uniquement**</dt> <dt>(0x8)</dt> </dl>       | Le point d’ancrage n’est pas décalé.<br/>                                                                                                                                                                                                           |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 professionnel<br/>                                         |
| En-tête<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IAnchor::ShiftRegion](/windows/desktop/api/Textstor/nf-textstor-ianchor-shiftregion)
</dt> </dl>

 

 





