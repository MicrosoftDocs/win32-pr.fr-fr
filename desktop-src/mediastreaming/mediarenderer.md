---
title: MediaRenderer, classe
description: Implémente l’interface IMediaRenderer qui représente un appareil de convertisseur de médias numériques DLNA (DMR).
ms.assetid: bac7898f-1334-4e28-92c7-6de464884eaf
keywords:
- API de diffusion multimédia en continu de la classe MediaRenderer
- API de diffusion multimédia en continu de la classe MediaRenderer, décrite
topic_type:
- apiref
api_name:
- MediaRenderer
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d14cdea89535fc680874905a9fb2b3358595baab
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507882"
---
# <a name="mediarenderer-class"></a>MediaRenderer, classe

Implémente l’interface [**IMediaRenderer**](imediarenderer.md) qui représente un appareil de convertisseur de médias numériques DLNA (DMR).

**MediaRenderer** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MediaRenderer** possède ces méthodes.



| Méthode                                                                                       | Description                                                                                                                                                                                                                                                                                                                                                               |
|:---------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ajouter \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/legacy/hh828962(v=vs.85))        | Inscrit un gestionnaire d’événements pour l’événement [**RenderingParametersUpdate**](renderingparametersupdate.md) .<br/>                                                                                                                                                                                                                                                       |
| [**Ajouter \_ TransportParametersUpdate**](/previous-versions/windows/desktop/legacy/hh828963(v=vs.85))        | Inscrit un gestionnaire d’événements pour l’événement [**TransportParametersUpdate**](transportparametersupdate.md) .<br/>                                                                                                                                                                                                                                                       |
| [**GetMuteAsync**](/previous-versions/windows/desktop/legacy/hh828964(v=vs.85))                                           | Interroge de manière asynchrone le DMR pour déterminer si le son est actuellement muet ou non.<br/>                                                                                                                                                                                                                                                                            |
| [**GetPositionInformationAsync**](/previous-versions/windows/desktop/legacy/hh828965(v=vs.85))             | Interroge de manière asynchrone le DMR pour récupérer les informations de position.<br/>                                                                                                                                                                                                                                                                                               |
| [**GetTransportInformationAsync**](/previous-versions/windows/desktop/legacy/hh828966(v=vs.85))           | Interroge de manière asynchrone le DMR pour récupérer les informations de transport.<br/>                                                                                                                                                                                                                                                                                              |
| [**GetVolumeAsync**](/previous-versions/windows/desktop/legacy/hh828967(v=vs.85))                                       | Interroge le DMR de manière asynchrone pour son niveau de volume audio actuel.<br/>                                                                                                                                                                                                                                                                                             |
| [**PauseAsync**](mediarenderer-pauseasync.md)                                               | Ordonne à DMR de suspendre de manière asynchrone la diffusion du contenu actuel.<br/>                                                                                                                                                                                                                                                                                         |
| [**PlayAsync**](/previous-versions/windows/desktop/legacy/hh828972(v=vs.85))                                                 | Ordonne à DMR de lire de façon asynchrone le contenu spécifié en appelant la méthode [**SetSourceFromUriAsync**](/previous-versions/windows/desktop/legacy/hh828983(v=vs.85)), [**SetSourceFromStreamAsync**](/previous-versions/windows/desktop/legacy/hh828982(v=vs.85))ou [**SetSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/legacy/hh828981(v=vs.85)) .<br/>                       |
| [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/legacy/hh828973(v=vs.85))                                   | Ordonne à DMR de lire de façon asynchrone le contenu spécifié en appelant la méthode [**SetSourceFromUriAsync**](/previous-versions/windows/desktop/legacy/hh828983(v=vs.85)), [**SetSourceFromStreamAsync**](/previous-versions/windows/desktop/legacy/hh828982(v=vs.85))ou [**SetSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/legacy/hh828981(v=vs.85)) au taux spécifié.<br/> |
| [**supprimer \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/legacy/hh828974(v=vs.85))  | Annule l’inscription d’un gestionnaire d’événements pour l’événement [**RenderingParametersUpdate**](renderingparametersupdate.md) .<br/>                                                                                                                                                                                                                                                     |
| [**supprimer \_ TransportParametersUpdate**](/previous-versions/windows/desktop/legacy/hh828975(v=vs.85))  | Annule l’inscription d’un gestionnaire d’événements pour l’événement [**TransportParametersUpdate**](transportparametersupdate.md) .<br/>                                                                                                                                                                                                                                                     |
| [**SeekAsync**](/previous-versions/windows/desktop/legacy/hh828976(v=vs.85))                                                 | Ordonne à DMR de rechercher de manière asynchrone un décalage de temps particulier.<br/>                                                                                                                                                                                                                                                                                          |
| [**SetMuteAsync**](/previous-versions/windows/desktop/legacy/hh828977(v=vs.85))                                           | Indique à DMR de manière asynchrone d’activer ou de désactiver le son.<br/>                                                                                                                                                                                                                                                                                           |
| [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/legacy/hh828978(v=vs.85)) | Ordonne à la DMR de manière asynchrone de préparer le contenu spécifié en vue de sa diffusion une fois que le contenu actuel est terminé.<br/>                                                                                                                                                                                                                                   |
| [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/legacy/hh828979(v=vs.85))           | Fait en sorte que le DMR de manière asynchrone prépare le flux multimédia spécifié en vue de sa diffusion une fois que le contenu actuel est terminé.<br/>                                                                                                                                                                                                                              |
| [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/legacy/hh828980(v=vs.85))                 | Fait en sorte que le DMR de manière asynchrone prépare le contenu identifié par l’URI spécifié pour être lu une fois que le contenu actuel est terminé.<br/>                                                                                                                                                                                                             |
| [**SetSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/legacy/hh828981(v=vs.85))         | Fait en sorte que le DMR de manière asynchrone prépare le contenu spécifié en vue de sa diffusion.<br/>                                                                                                                                                                                                                                                                                 |
| [**SetSourceFromStreamAsync**](/previous-versions/windows/desktop/legacy/hh828982(v=vs.85))                   | Fait en sorte que le DMR de manière asynchrone prépare le flux multimédia spécifié en vue de sa diffusion une fois que le contenu actuel est terminé.<br/>                                                                                                                                                                                                                              |
| [**SetSourceFromUriAsync**](/previous-versions/windows/desktop/legacy/hh828983(v=vs.85))                         | Fait en sorte que le DMR de manière asynchrone prépare le contenu identifié par l’URI spécifié pour sa diffusion.<br/>                                                                                                                                                                                                                                                           |
| [**SetVolumeAsync**](/previous-versions/windows/desktop/legacy/hh828984(v=vs.85))                                       | Définit de manière asynchrone le niveau du volume audio sur le DMR à la valeur spécifiée.<br/>                                                                                                                                                                                                                                                                                  |
| [**StopAsync**](mediarenderer-stopasync.md)                                                 | Fait en sorte que le DMR de manière asynchrone arrête la diffusion du contenu actuel.<br/>                                                                                                                                                                                                                                                                                          |



 

### <a name="properties"></a>Propriétés

La classe **MediaRenderer** possède les propriétés suivantes.



| Propriété                                                                | Type d’accès          | Description                                                                                 |
|:------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------|
| [**ActionInformation**](mediarenderer-actioninformation.md)<br/> | Lecture seule<br/> | Obtient des informations sur les méthodes qui peuvent être appelées actuellement sur la DMR.<br/>        |
| [**IsAudioSupported**](mediarenderer-isaudiosupported.md)<br/>   | Lecture seule<br/> | Obtient une valeur qui indique si DMR est capable de diffuser du contenu audio.<br/> |
| [**IsImageSupported**](mediarenderer-isimagesupported.md)<br/>   | Lecture seule<br/> | Obtient une valeur qui indique si la DMR est capable d’afficher des images.<br/>     |
| [**IsVideoSupported**](mediarenderer-isvideosupported.md)<br/>   | Lecture seule<br/> | Obtient une valeur qui indique si DMR est capable de regarder du contenu vidéo.<br/> |



 

 

