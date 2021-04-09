---
description: Signale la progression d’un objet activateur de contenu. Les objets qui exposent l’interface IMFContentEnabler peuvent déclencher cet événement pour avertir l’application de la progression des actions des activateurs du contenu.
ms.assetid: ec14ba9b-cfb6-4e32-870e-2436e11c308b
title: Événement MEEnablerProgress (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58303835113408a7fe09436967286d5ff988acdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202009"
---
# <a name="meenablerprogress-event"></a>Événement MEEnablerProgress

Signale la progression d’un objet activateur de contenu. Les objets qui exposent l’interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) peuvent déclencher cet événement pour avertir l’application de la progression des actions de l’activateur du contenu.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE               | Description                                                               |
|-----------------------|---------------------------------------------------------------------------|
| \_LPWStr VT<br/> | Chaîne de caractères larges qui décrit la progression.<br/> <br/> |



## <a name="remarks"></a>Notes

Pour recevoir cet événement, interrogez l’interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) pour l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . Appelez ensuite [**IMFMediaEventGenerator :: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), comme décrit dans la rubrique [Media Event Generators](media-event-generators.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[Générateurs d’événements de média](media-event-generators.md)
</dt> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




