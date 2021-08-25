---
description: 'Signale une erreur grave. Tout composant Media Foundation peut envoyer cet événement à tout moment. Appelez IMFMediaEvent :: GetStatus pour recevoir le code d’erreur de l’opération qui a échoué.'
ms.assetid: bff80041-77d8-43b1-a410-9cefaf45eb2c
title: Événement MEError (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd012bf7fbb7f21f37201a67f5c203f5981be6aa16795e2a3c37d16ea268f67c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941469"
---
# <a name="meerror-event"></a>Événement MEError

Signale une erreur grave. Tout composant Media Foundation peut envoyer cet événement à tout moment. Appelez [**IMFMediaEvent :: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) pour recevoir le code d’erreur de l’opération qui a échoué.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="remarks"></a>Remarques

Cet événement doit être utilisé uniquement pour les erreurs inattendues. N’envoyez pas cet événement pour signaler qu’une méthode asynchrone a échoué. Si une méthode asynchrone échoue, le code d’erreur est retourné dans l’événement normal pour cette méthode.

Si une erreur récupérable se produit pendant la diffusion en continu, envoyez l’événement [MENonFatalError](menonfatalerror.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




