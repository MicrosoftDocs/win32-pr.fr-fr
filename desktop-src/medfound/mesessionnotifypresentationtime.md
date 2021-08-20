---
description: Déclenché par la session multimédia au démarrage d’une nouvelle présentation. Cet événement indique la date de début de la présentation et le décalage entre l’heure de la présentation et l’heure de la source.
ms.assetid: 67c7d5f3-ffaf-4359-a59c-bb26b992b6cd
title: Événement MESessionNotifyPresentationTime (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d10c1b1e443bd2c6a56a926d5355de5606bf2f2e25618269f8d4ed735538d92f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061763"
---
# <a name="mesessionnotifypresentationtime-event"></a>Événement MESessionNotifyPresentationTime

Déclenché par la session multimédia au démarrage d’une nouvelle présentation. Cet événement indique la date de début de la présentation et le décalage entre l’heure de la présentation et l’heure de la source.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="attributes"></a>Attributs

Les attributs suivants sont définis pour cet événement.



| Attribut                                                                                                                   | Description                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**heure de la présentation du démarrage de l' \_ événement MF \_ \_ \_**](mf-event-start-presentation-time-attribute.md)<br/>                       | Heure de début de la présentation.<br/> <br/>                                                      |
| [**décalage de l’heure de présentation de l' \_ événement MF \_ \_ \_**](mf-event-presentation-time-offset-attribute.md)<br/>                     | Décalage entre l’heure de présentation et les horodatages de la source du média.<br/> <br/>                 |
| [**\_ \_ \_ heure de début de la présentation de l’événement MF \_ \_ à la \_ sortie**](mf-event-start-presentation-time-at-output-attribute.md)<br/> | Heure de présentation à laquelle les récepteurs multimédia affichent le premier exemple de la nouvelle topologie.<br/> <br/> |



## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
</dt> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




