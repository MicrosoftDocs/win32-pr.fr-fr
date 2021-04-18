---
description: Déclenché par un récepteur de flux lorsqu’il termine la transition à l’État en cours d’exécution.
ms.assetid: 95ac658b-bec0-442d-85ef-61966b40a2f2
title: Événement MEStreamSinkStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 407ab885da04746034b7126a8d9bb9389d2928f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533801"
---
# <a name="mestreamsinkstarted-event"></a>Événement MEStreamSinkStarted

Déclenché par un récepteur de flux lorsqu’il termine la transition à l’État en cours d’exécution. La transition vers l’exécution se produit lorsque la méthode [**IMFPresentationClock :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start) est appelée sur l’horloge de présentation du récepteur. Le récepteur multimédia reçoit la notification par le biais de sa méthode [**IMFClockStateSink :: OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) ou [**IMFClockStateSink :: OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) .

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |



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

[Récepteurs de médias](media-sinks.md)
</dt> </dl>

 

 




