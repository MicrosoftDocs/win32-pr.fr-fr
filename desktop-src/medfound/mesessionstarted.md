---
description: 'Déclenché lorsque la méthode IMFMediaSession :: Start se termine de façon asynchrone.'
ms.assetid: 28ed32f0-9b23-4da1-9587-15f490da7bf9
title: Événement MESessionStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24cf1b461017ce9cdcbaeb57e7c327a7b12b80a63c181dbe1f50f223977c5095
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061719"
---
# <a name="mesessionstarted-event"></a>Événement MESessionStarted

Déclenché lorsque la méthode [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) se termine de façon asynchrone.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="attributes"></a>Attributs

Les attributs suivants sont définis pour cet événement.



| Attribut                                                                                               | Description                                                                                     |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**décalage de l’heure de présentation de l' \_ événement MF \_ \_ \_**](mf-event-presentation-time-offset-attribute.md)<br/> | Décalage entre l’heure de présentation et les horodatages de la source du média.<br/> <br/> |



## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




