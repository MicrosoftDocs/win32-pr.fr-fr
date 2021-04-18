---
description: Fournit des commentaires à Quality Manager sur la qualité de la lecture.
ms.assetid: 1b4b6a2d-411e-42d1-a44b-bb1928e1c063
title: Événement MEQualityNotify (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d8f486bfebfd137ba341176af0fdad257776df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528270"
---
# <a name="mequalitynotify-event"></a>Événement MEQualityNotify

Fournit des commentaires à Quality Manager sur la qualité de la lecture.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE           | Description                         |
|-------------------|-------------------------------------|
| Le \_ i8 VT<br/> | Consultez la section Notes.<br/> <br/> |



## <a name="remarks"></a>Notes

Cet événement est déclenché par certains composants de pipeline. La session multimédia transfère l’événement au gestionnaire de qualité en appelant la méthode [**IMFQualityManager :: NotifyQualityEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyqualityevent) .

Le type étendu de l’événement indique la signification des données d’événement.



| Type étendu                            | Données d’événement                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_latence du \_ traitement des notifications de qualité MF \_ \_ | Latence de traitement approximative introduite par le composant, en unités de 100 nanosecondes.<br/> La latence de traitement est la quantité de latence introduite par un composant dans le pipeline en traitant un exemple. Dans certains cas, la latence ne peut pas être dérivée simplement en examinant les appels à [**IMFQualityManager :: NotifyProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) et [**IMFQualityManager :: NotifyProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput). Par exemple, il se peut qu’il n’y ait pas de correspondance un-à-un entre les exemples d’entrée et les exemples de sortie. Dans ce cas, le composant peut envoyer un événement MEQualityNotify avec la latence de traitement. Si la latence de traitement change, le composant peut envoyer un nouvel événement à tout moment pendant la diffusion en continu.<br/> |
| retard de l’exemple de notification de \_ qualité MF \_ \_ \_         | Délai d’attente de l’échantillon, en unités de 100 nanosecondes. Si la valeur est positive, l’échantillon était en retard. Si la valeur est négative, l’échantillon était tôt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Pour récupérer le type étendu, appelez [**IMFMediaEvent :: GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).

Les composants de pipeline ne sont pas requis pour envoyer cet événement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)
</dt> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




