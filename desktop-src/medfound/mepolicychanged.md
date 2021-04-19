---
description: Déclenché par un composant de pipeline lorsque la stratégie de sortie du flux change. Cet événement s’applique uniquement au contenu protégé.
ms.assetid: 9dc78dc6-3fc2-4a81-ad41-45ff3fdbdade
title: Événement MEPolicyChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b6827c44958e2df016365a8caa9a66f1aad9a30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544251"
---
# <a name="mepolicychanged-event"></a>Événement MEPolicyChanged

Déclenché par un composant de pipeline lorsque la stratégie de sortie du flux change. Cet événement s’applique uniquement au contenu protégé.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE                | Description                                                                                                                  |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| VT \_ inconnu<br/> | Pointeur vers l’interface [**IMFOutputPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy) de la nouvelle stratégie pour le flux.<br/> <br/> |



## <a name="remarks"></a>Notes

Toutes les sorties approuvées doivent gérer cet événement. Les transformations de Media Foundation (MFTs) reçoivent cet événement via la méthode [**IMFTransform ::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) . Les récepteurs multimédias reçoivent cet événement par le biais de la méthode [**IMFStreamSink ::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) .

La sortie approuvée doit appliquer la nouvelle stratégie ou retourner le code d’erreur MF \_ E \_ stratégie \_ non prise en charge.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows Vista- \[ \| applications UWP\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ \| apps UWP\]<br/>                                              |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




