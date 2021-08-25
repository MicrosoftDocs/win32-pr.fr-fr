---
description: Déclenché par un composant de pipeline lorsque la stratégie de sortie du flux change. Cet événement s’applique uniquement au contenu protégé.
ms.assetid: 9dc78dc6-3fc2-4a81-ad41-45ff3fdbdade
title: Événement MEPolicyChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ac87d3dae63b20d19c91f0fdef5471060753152901d9096b1be315cd76e9974
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957409"
---
# <a name="mepolicychanged-event"></a>Événement MEPolicyChanged

Déclenché par un composant de pipeline lorsque la stratégie de sortie du flux change. Cet événement s’applique uniquement au contenu protégé.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE                | Description                                                                                                                  |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| VT \_ inconnu<br/> | Pointeur vers l’interface [**IMFOutputPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy) de la nouvelle stratégie pour le flux.<br/> <br/> |



## <a name="remarks"></a>Remarques

Toutes les sorties approuvées doivent gérer cet événement. Les transformations de Media Foundation (MFTs) reçoivent cet événement via la méthode [**IMFTransform ::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) . Les récepteurs multimédias reçoivent cet événement par le biais de la méthode [**IMFStreamSink ::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) .

La sortie approuvée doit appliquer la nouvelle stratégie ou retourner le code d’erreur MF \_ E \_ stratégie \_ non prise en charge.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications UWP pour applications de bureau Vista \|\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows Applications de bureau du serveur 2008 \[ \| applications UWP\]<br/>                                              |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




