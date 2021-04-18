---
title: Constantes TS_SS_ (Textstor. h)
description: Les \_ \_ constantes TS SS \, définies avant l’exécution dans la \_ structure d’État TS, décrivent les États des documents statiques.
ms.assetid: 17264527-946a-4648-a4eb-30db751602ab
topic_type:
- apiref
api_name:
- TS_SS_DISJOINTSEL
- TS_SS_REGIONS
- TS_SS_TRANSITORY
- TS_SS_NOHIDDENTEXT
- TS_SS_TKBAUTOCORRECTENABLE
- TS_SS_TKBPREDICTIONENABLE
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 773645b8a75b7e8eeafa40ed9fa95067743628d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512545"
---
# <a name="ts_ss_-constants"></a>\_ \_ \* Constantes TS SS

Les \_ \_ \* constantes TS SS, définies avant l’exécution dans la structure d' [**\_ État TS**](/windows/desktop/api/Textstor/ns-textstor-ts_status) , décrivent les États des documents statiques.



| Constante/valeur                                                                                                                                                                                                                                                      | Description                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TS_SS_DISJOINTSEL"></span><span id="ts_ss_disjointsel"></span><dl> <dt>**TS \_ SS \_ DISJOINTSEL**</dt> <dt>(0x1)</dt> </dl>                             | Le document prend en charge les sélections multiples.<br/>                                                          |
| <span id="TS_SS_REGIONS"></span><span id="ts_ss_regions"></span><dl> <dt>**TS \_ \_Zones SS**</dt> <dt>(0X2)</dt> </dl>                                         | Le document peut contenir plusieurs régions.<br/>                                                          |
| <span id="TS_SS_TRANSITORY"></span><span id="ts_ss_transitory"></span><dl> <dt>**TS \_ SS \_ transitoire**</dt> <dt>(0x4)</dt> </dl>                                | Le document est supposé avoir un cycle d’utilisation courts.<br/>                                               |
| <span id="TS_SS_NOHIDDENTEXT"></span><span id="ts_ss_nohiddentext"></span><dl> <dt>**TS \_ SS \_ NOHIDDENTEXT**</dt> <dt>(0x8)</dt> </dl>                          | Le document ne contient jamais de texte masqué.<br/>                                                        |
| <span id="TS_SS_TKBAUTOCORRECTENABLE"></span><span id="ts_ss_tkbautocorrectenable"></span><dl> <dt>**TS \_ SS \_ TKBAUTOCORRECTENABLE**</dt> <dt>(0x10)</dt> </dl> | **À compter de Windows 8 :** Le document prend en charge la correction automatique fournie par le clavier tactile.<br/>   |
| <span id="TS_SS_TKBPREDICTIONENABLE"></span><span id="ts_ss_tkbpredictionenable"></span><dl> <dt>**TS \_ SS \_ TKBPREDICTIONENABLE**</dt> <dt>(0x20)</dt> </dl>    | **À compter de Windows 8 :** Le document prend en charge les suggestions de texte fournies par le clavier tactile.<br/> |



## <a name="remarks"></a>Notes

Le membre **dwStaticFlags** de la structure d' **\_ État TS** utilise ces constantes.

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

[**\_statut TS**](/windows/desktop/api/Textstor/ns-textstor-ts_status)
</dt> <dt>

[**\_État TF**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))
</dt> </dl>

 

