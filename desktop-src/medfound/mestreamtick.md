---
description: Signale qu’un flux multimédia n’a pas de données disponibles à une heure spécifiée.
ms.assetid: 1a00fff1-c3ab-4965-a663-3c15bb48ea98
title: Événement MEStreamTick (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27123569e991043a534883964ba94e4955d60a40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533751"
---
# <a name="mestreamtick-event"></a>Événement MEStreamTick

Signale qu’un flux multimédia n’a pas de données disponibles à une heure spécifiée.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE           | Description                                                                   |
|-------------------|-------------------------------------------------------------------------------|
| Le \_ i8 VT<br/> | Heure à laquelle l’intervalle se produit, en unités de 100 nanosecondes.<br/> <br/> |



## <a name="remarks"></a>Notes

Cet événement signale un écart dans les données. L’événement avertit les composants en aval qu’ils n’attendent aucune donnée à l’heure spécifiée.

L’événement doit être envoyé par l’objet qui génère les horodatages pour les échantillons de média dans le flux. Selon le format des données, il peut s’agir de l’une des deux opérations suivantes :

-   Le flux multimédia sur la source du média (interface [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) ), ou
-   Transformation de décodeur (interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) ).

Pendant ce laps de temps, l’objet doit envoyer l’événement sur aussi souvent qu’il produirait normalement des exemples. Pour la vidéo, envoyer un événement pour chaque frame manquant. Pour l’audio, envoyez l’événement au moins une fois par seconde pendant l’intervalle. La valeur de l’événement est l’horodatage de l’échantillon manquant. Envoyez autant d’événements MEStreamTick que nécessaire pour combler l’écart dans les données.

Si une source de média a plusieurs flux et qu’il y a un écart dans plusieurs flux, chaque flux doit envoyer des événements MEStreamTick. Par exemple, s’il existe un écart dans les données audio et vidéo, les deux flux envoient l’événement.

L’événement MEStreamTick ne termine pas une demande [**IMFMediaStream :: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) . La source du média doit toujours envoyer un événement [MEMediaSample](memediasample.md) pour chaque appel à **RequestSample**.

Les récepteurs multimédias ne peuvent pas utiliser cet événement directement. Pour signaler un intervalle dans le flux à un récepteur multimédia, appelez [**IMFStreamSink ::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) avec un marqueur de **\_ \_ graduation de marqueur MFSTREAMSINK** . Le pipeline Media Foundation convertit les événements MEStreamTick en marqueurs de **\_ \_ graduation MFSTREAMSINK** , si nécessaire.

Ne définissez pas l’attribut de [**\_ discontinuité MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) sur l’exemple de support suivant après un événement MEStreamTick. L’attribut de **\_ discontinuité MFSampleExtension** implique que l’horodatage est discontinu avec les horodatages précédents, tandis que MEStreamTick implique que les horodatages sont continus, mais que certaines données sont manquantes.

> [!Note]  
> Une version antérieure de la documentation indiquait de façon erronée que l’exemple après un événement MEStreamTick doit avoir l’attribut [**\_ discontinu MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) .

 

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

 

 




