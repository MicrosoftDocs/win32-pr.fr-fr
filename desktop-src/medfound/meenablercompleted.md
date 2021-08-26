---
description: Déclenché par un objet activateur de contenu lorsque les objets qui activent l’action sont terminés.
ms.assetid: 5162800c-9c55-40de-be66-a98765324f76
title: Événement MEEnablerCompleted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2983cbcf3927626da88432c0cc04f28e2fc5d3e866d161b514dcbe5108bcf92a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013799"
---
# <a name="meenablercompleted-event"></a>Événement MEEnablerCompleted

Déclenché par un objet activateur de contenu lorsque l’action d’activation de l’objet est terminée. Les objets qui exposent l’interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) peuvent déclencher cet événement. L’événement est déclenché si l’un des événements suivants se produit :

-   La méthode [**IMFContentEnabler :: AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) se termine de façon asynchrone.
-   L’application appelle [**IMFContentEnabler :: MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable), puis l’application termine la requête http après, comme décrit dans la méthode **MonitorEnable** .

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="remarks"></a>Remarques

Le code d’état de l’événement peut contenir l’une des valeurs suivantes.



| Valeur                                     | Description                                                                                                                                                                                |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_OK**                            | L’opération a réussi.                                                                                                                                                        |
| **\_NOTACQUIRED de \_ \_ licence DRM \_ E** | La licence DRM n’a pas été acquise. Si la tentative précédente a utilisé [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable), l’application doit essayer une acquisition non silencieuse. |
| **\_analyse DRM de NS S \_ \_ \_ annulée**   | L’opération [**MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) a été annulée.                                                                                            |



 

Pour recevoir cet événement, interrogez l’interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) pour l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . Appelez ensuite [**IMFMediaEventGenerator :: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), comme décrit dans la rubrique [Media Event Generators](media-event-generators.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[Générateurs d’événements de média](media-event-generators.md)
</dt> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




