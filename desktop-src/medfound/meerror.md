---
description: 'Signale une erreur grave. Tout composant Media Foundation peut envoyer cet événement à tout moment. Appelez IMFMediaEvent :: GetStatus pour recevoir le code d’erreur de l’opération qui a échoué.'
ms.assetid: bff80041-77d8-43b1-a410-9cefaf45eb2c
title: Événement MEError (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0eb557dffb2c73a63031a193c331edabe470db7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534164"
---
# <a name="meerror-event"></a>Événement MEError

Signale une erreur grave. Tout composant Media Foundation peut envoyer cet événement à tout moment. Appelez [**IMFMediaEvent :: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) pour recevoir le code d’erreur de l’opération qui a échoué.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="remarks"></a>Notes

Cet événement doit être utilisé uniquement pour les erreurs inattendues. N’envoyez pas cet événement pour signaler qu’une méthode asynchrone a échoué. Si une méthode asynchrone échoue, le code d’erreur est retourné dans l’événement normal pour cette méthode.

Si une erreur récupérable se produit pendant la diffusion en continu, envoyez l’événement [MENonFatalError](menonfatalerror.md) .

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

 

 




