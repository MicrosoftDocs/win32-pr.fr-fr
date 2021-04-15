---
description: Déclenché par une source de média lors du redémarrage ou de la recherche d’un flux déjà actif.
ms.assetid: 2d91a267-e109-45f5-886b-11b883cc5509
title: Événement MEUpdatedStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e3b2e6fdc5928a08306b344c02b5eaafc37e957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529602"
---
# <a name="meupdatedstream-event"></a>Événement MEUpdatedStream

Déclenché par une source de média lors du redémarrage ou de la recherche d’un flux déjà actif.

Quand la méthode [**IMFMediaSource :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) est appelée sur une source de média, la source du média envoie un événement pour chaque flux sélectionné :

-   La source envoie l’événement [MENewStream](menewstream.md) si le flux n’a pas été sélectionné dans l’appel précédent à [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), ou il s’agit du tout premier appel à **Start** sur cette source de média.

-   La source envoie l’événement MEUpdatedStream si le flux a déjà été sélectionné dans l’appel précédent à [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).

Aucun événement n’est envoyé pour les flux non sélectionnés.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE                | Description                                                                                        |
|------------------------|----------------------------------------------------------------------------------------------------|
| VT \_ inconnu<br/> | Pointeur vers l’interface [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) du flux.<br/> <br/> |



## <a name="remarks"></a>Notes

Lors du premier appel à [**Démarrer**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) dans lequel un flux devient actif, la source du média envoie un événement [MENewStream](menewstream.md) pour le flux. Lors des appels suivants à **Start**, la source du média envoie un événement MEUpdatedStream, jusqu’à ce que le flux soit désélectionné.

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

 

 




