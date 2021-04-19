---
description: 'Déclenché par la source de Sequencer lorsque la méthode IMFSequencerSource :: UpdateTopology se termine de façon asynchrone.'
ms.assetid: f573cbd0-689c-4bfe-846b-6fc8008101c8
title: Événement MESequencerSourceTopologyUpdated (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baaf03119832937a584178b9f5958b066046c633
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534421"
---
# <a name="mesequencersourcetopologyupdated-event"></a>Événement MESequencerSourceTopologyUpdated

Déclenché par la source de Sequencer lorsque la méthode [**IMFSequencerSource :: UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) se termine de façon asynchrone.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE            | Description                                                                                                                                                                                                                        |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| VT \_ UI4<br/> | Identificateur de l’élément de séquenceur de la topologie en cours de mise à jour. L’application spécifie cette valeur dans le paramètre *dwId* de la méthode [**UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) .<br/> <br/> |



## <a name="remarks"></a>Notes

Cet événement signale que la source de Sequencer a mis à jour la topologie, mais ne signifie pas que la topologie est prête pour la lecture. L’application doit attendre l’événement [MESessionTopologyStatus](mesessiontopologystatus.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> <dt>

[Source de Sequencer](sequencer-source.md)
</dt> </dl>

 

 




