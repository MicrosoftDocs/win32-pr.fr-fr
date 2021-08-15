---
description: Déclenché par une source de média lorsque les caractéristiques des sources changent.
ms.assetid: df7bb9a3-5949-4a4a-8835-c5b1d01b5cb3
title: Événement MESourceCharacteristicsChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd69be00727ec3f1f635b82fb6c8e29c4016959ced480be4e9de6b8a83cfe8cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877367"
---
# <a name="mesourcecharacteristicschanged-event"></a>Événement MESourceCharacteristicsChanged

Déclenché par une source de média lorsque les caractéristiques de la source changent.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="attributes"></a>Attributs

Les attributs suivants sont définis pour cet événement.



| Attribut                                                                                                   | Description                                                          |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**caractéristiques de la \_ source d’événements MF \_ \_**](mf-event-source-characteristics-attribute.md)<br/>          | Nouvelles caractéristiques de la source du média.<br/> <br/>      |
| [**caractéristiques de la \_ source d’événements MF \_ \_ \_ Old**](mf-event-source-characteristics-old-attribute.md)<br/> | Caractéristiques précédentes de la source du média.<br/> <br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




