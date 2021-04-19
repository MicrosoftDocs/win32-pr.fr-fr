---
description: Déclenché par les récepteurs de flux du convertisseur vidéo amélioré (EVR) si le périphérique vidéo change.
ms.assetid: 5b663d6b-5df8-4321-a6a5-a21b9810065a
title: Événement MEStreamSinkDeviceChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 651fc34a56ca52cfb9e0b3f20e6e4d6b5366f541
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516917"
---
# <a name="mestreamsinkdevicechanged-event"></a>Événement MEStreamSinkDeviceChanged

Déclenché par les récepteurs de flux du convertisseur vidéo amélioré (EVR) si le périphérique vidéo change. Par exemple, le EVR déclenche cet événement lorsqu’il reçoit un événement de [**\_ \_ modification d’affichage EC**](../directshow/ec-display-changed.md) .

Le pipeline Media Foundation répond à cet événement en renvoyant tous les exemples de demandes qui ont échoué pendant la modification de l’appareil.

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

 

 
