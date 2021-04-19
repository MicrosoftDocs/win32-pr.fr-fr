---
description: Les GUID suivants sont utilisés pour le suivi d’événements dans DirectShow.
ms.assetid: 438938fe-37e7-45d6-b49a-d96698307f25
title: GUID de trace (PerfStruct. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_AUDIOBREAK
- GUID_DSHOW_CTL
- GUID_STREAMTRACE
- GUID_VIDEOREND
api_type:
- HeaderDef
api_location:
- PerfStruct.h
ms.openlocfilehash: 4b2f2a6a678c029d01d9bf55481837d81d48557e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534828"
---
# <a name="trace-guids"></a>GUID de trace

Les GUID suivants sont utilisés pour le suivi d’événements dans DirectShow.



| GUID                                                                                                                                                                   | Description                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AUDIOBREAK"></span><span id="guid_audiobreak"></span><dl> <dt>**GUID \_ AUDIOBREAK**</dt> </dl>    | Événement d’arrêt audio. Les événements de ce type utilisent la structure [**PERFINFO \_ DShow \_ AUDIOBREAK**](perfinfo-dshow-audiobreak.md) pour les données d’événement.<br/>         |
| <span id="GUID_DSHOW_CTL"></span><span id="guid_dshow_ctl"></span><dl> <dt>**GUID de la \_ \_ liste CTL DShow**</dt> </dl>      | Fournisseur d’événements DirectShow.<br/>                                                                                                                        |
| <span id="GUID_STREAMTRACE"></span><span id="guid_streamtrace"></span><dl> <dt>**GUID \_ STREAMTRACE**</dt> </dl> | Événement de diffusion générale. Les événements de ce type utilisent la structure [**PERFINFO \_ DShow \_ STREAMTRACE**](perfinfo-dshow-streamtrace.md) pour les données d’événement.<br/> |
| <span id="GUID_VIDEOREND"></span><span id="guid_videorend"></span><dl> <dt>**GUID \_ VIDEOREND**</dt> </dl>       | Événement de rendu vidéo. Les événements de ce type utilisent la structure [**PERFINFO \_ DShow \_ AVREND**](perfinfo-dshow-avrend.md) pour les données d’événement.<br/>             |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PerfStruct. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Suivi d’événements dans DirectShow](event-tracing-in-directshow.md)
</dt> </dl>

 

 




