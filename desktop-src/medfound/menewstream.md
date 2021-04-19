---
description: Déclenché par une source de média lorsqu’elle démarre un nouveau flux.
ms.assetid: 1bc8b265-b7a1-4068-89f7-c0da03dfb874
title: Événement MENewStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60394d442b24dcdc234ada2dd3fd418e6ab7b54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524964"
---
# <a name="menewstream-event"></a>Événement MENewStream

Déclenché par une source de média lorsqu’elle démarre un nouveau flux.

Quand la méthode [**IMFMediaSource :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) est appelée sur une source de média, la source du média envoie un événement pour chaque flux sélectionné :

-   La source envoie l’événement MENewStream si le flux n’a pas été sélectionné dans l’appel précédent à [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), ou il s’agit du tout premier appel à **Start** sur cette source de média.

-   La source envoie l’événement [MEUpdatedStream](meupdatedstream.md) si le flux a déjà été sélectionné dans l’appel précédent à [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).

Aucun événement n’est envoyé pour les flux non sélectionnés.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE                | Description                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------|
| VT \_ inconnu<br/> | Contient un pointeur vers l’interface [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) du flux.<br/> <br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




