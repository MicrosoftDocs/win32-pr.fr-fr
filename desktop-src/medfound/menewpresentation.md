---
description: Déclenché par une source de média qui fournit des topologies par le biais de l’interface IMFMediaSourceTopologyProvider, telle que la source de Sequencer. La source déclenche l’événement lorsqu’elle a une nouvelle présentation. La session multimédia transmet cet événement à l’application.
ms.assetid: c669b2c9-5ece-4045-b691-8a71bbf491e1
title: Événement MENewPresentation (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa2adec5b3dbb8544e537bdcc8f5c724130175b3167f9c51dc005112fdbd9a0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119228879"
---
# <a name="menewpresentation-event"></a>Événement MENewPresentation

Déclenché par une source de média qui fournit des topologies par le biais de l’interface [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) , telle que la source de Sequencer. La source déclenche l’événement lorsqu’elle a une nouvelle présentation. La session multimédia transmet cet événement à l’application.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE                | Description                                                                                                                                                             |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| VT \_ inconnu<br/> | Pointeur vers l’interface [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) du descripteur de présentation pour la nouvelle présentation.<br/> <br/> |



## <a name="remarks"></a>Remarques

L’application peut récupérer la topologie qui correspond au descripteur de présentation en appelant [**IMFMediaSourceTopologyProvider :: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) sur la source du média. L’application peut ensuite faire la file d’attente de la nouvelle topologie sur la session multimédia en appelant [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> <dt>

[Source de Sequencer](sequencer-source.md)
</dt> </dl>

 

 




