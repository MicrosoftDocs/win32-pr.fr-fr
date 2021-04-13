---
description: Déclenché quand une source de média démarre sans rechercher.
ms.assetid: a52d8ee1-cb46-487d-a744-fca6db7c2353
title: Événement MESourceStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c17ba7898a8bf33df4a3508afee9b7c0c9bc81c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528263"
---
# <a name="mesourcestarted-event"></a>Événement MESourceStarted

Déclenché quand une source de média démarre sans rechercher.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement. L’heure de début était à partir de la position actuelle.<br/> <br/>                            |
| Le \_ i8 VT<br/>    | Heure de début, en unités de 100 nanosecondes, par rapport aux horodatages sur les échantillons.<br/> <br/> |



## <a name="attributes"></a>Attributs

Les attributs suivants sont définis pour cet événement.



| Attribut                                                                                     | Description                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ \_ début réel de la source de l’événement MF \_**](mf-event-source-actual-start-attribute.md)<br/> | Heure de début La source du média définit cet attribut si elle redémarre à partir de sa position actuelle.<br/> <br/>                     |
| [**début du substitut de la \_ source d’événement MF \_ \_ \_**](mf-event-source-fake-start-attribute.md)<br/>     | Spécifie si la topologie du segment actuel est vide. La source Sequencer définit cet attribut.<br/> <br/>             |
| [**\_ \_ PROJECTSTART source de l’événement MF \_**](mf-event-source-projectstart-attribute.md)<br/>  | Heure de début d’un segment, par rapport au début de la présentation. La source Sequencer définit cet attribut.<br/> <br/> |



## <a name="remarks"></a>Notes

Une source de média déclenche cet événement lorsqu’elle démarre à partir de l’état arrêté ou qu’elle commence à partir d’un état suspendu à la même position dans la source. L’événement est déclenché si la méthode [**IMFMediaSource :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) retourne S \_ OK.

Si la source du média démarre à partir de la position actuelle et que l’état précédent de la source était en cours d’exécution ou suspendu, les données d’événement peuvent être vides (VT \_ vide). Si les données d’événement sont des données VT \_ vides, la source du média peut définir l’attribut de [**\_ \_ \_ \_ démarrage réel**](mf-event-source-actual-start-attribute.md) de la source de l’événement MF avec l’heure de début réelle.

Si la source du média démarre à partir d’une nouvelle position, ou si l’état précédent de la source a été arrêté, les données d’événement doivent être l’heure de début (VT \_ I8).

Si la méthode [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) provoque une recherche, la source du média envoie l’événement [MESourceSeeked](mesourceseeked.md) au lieu de MESourceStarted.

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

 

 




