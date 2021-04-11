---
description: Déclenché par un récepteur de flux lorsque le type de média récepteur n’est plus valide.
ms.assetid: 9eeb4262-1593-4c5f-9341-ebd328b586e7
title: Événement MEStreamSinkFormatChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e04c62072f69425079753ef4d0a56edcf8d65d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201996"
---
# <a name="mestreamsinkformatchanged-event"></a>Événement MEStreamSinkFormatChanged

Déclenché par un récepteur de flux lorsque le type de média du récepteur n’est plus valide.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="remarks"></a>Notes

Un récepteur de flux peut déclencher cela même si un événement invalide le type de média du récepteur de flux. Par exemple, le convertisseur vidéo amélioré (EVR) envoie cet événement lorsque l’affichage change.

La valeur **HRESULT** récupérée par [**IMFMediaEvent :: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) peut indiquer la raison pour laquelle le type de média n’est plus valide.

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

 

 




