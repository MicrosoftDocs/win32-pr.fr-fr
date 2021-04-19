---
description: Déclenché par une source de média lorsque les caractéristiques des sources changent.
ms.assetid: df7bb9a3-5949-4a4a-8835-c5b1d01b5cb3
title: Événement MESourceCharacteristicsChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659e9eea0352d131aac4959b2952e8426ae408a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534163"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




