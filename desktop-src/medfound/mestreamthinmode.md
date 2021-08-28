---
description: Déclenché par un flux multimédia lorsqu’il démarre ou arrête l’affinage du flux. Pour plus d’informations sur la réduction, consultez à propos du contrôle du taux.
ms.assetid: 7de8cb64-122a-475f-990c-c19590a9d9d8
title: Événement MEStreamThinMode (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f13a9cc5b625a8b366bece1debc2017fce51e35d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479515"
---
# <a name="mestreamthinmode-event"></a>Événement MEStreamThinMode

Déclenché par un flux multimédia lorsqu’il démarre ou arrête l’affinage du flux. Pour plus d' *informations sur la réduction, consultez* [à propos du contrôle du taux](about-rate-control.md).

Cet événement peut être envoyé en réponse à la méthode [**IMFRateControl ::**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) seou à la méthode [**IMFQualityAdvise :: SetDropMode**](/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setdropmode) .

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.




| VARTYPE | Description | 
|---------|-------------|
| VT_BOOL<br /> | Indique si l’affinage a démarré ou s’est arrêté.<br /><ul><li>VARIANT_TRUE : les exemples fournis après cet événement sont éclaircis.</li><li>VARIANT_FALSE : les exemples fournis après cet événement ne sont pas éclaircis.</li></ul><br /> | 




## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




