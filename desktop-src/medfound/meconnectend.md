---
description: Déclenché par la source réseau à la fin de l’ouverture d’une URL.
ms.assetid: 737aec32-24f4-4825-ad34-8d2fc889bc09
title: Événement MEConnectEnd (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9801b1af38f7bf0a0107680d77a399b3927a616e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530801"
---
# <a name="meconnectend-event"></a>Événement MEConnectEnd

Déclenché par la source réseau à la fin de l’ouverture d’une URL.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="remarks"></a>Notes

La source réseau envoie cet événement directement à l’application par le biais de la méthode [**IMFSourceOpenMonitor :: OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) de l’application, et non par le biais de l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) habituelle.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor)
</dt> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




