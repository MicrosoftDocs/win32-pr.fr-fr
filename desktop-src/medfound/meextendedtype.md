---
description: Type d’événement personnalisé.
ms.assetid: a54a446c-0e96-467b-90f6-0f64a7c1727d
title: Événement MEExtendedType (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 520c0076365c4cea720b0fb04bab5f409206079e776da363d9a448ff5fd3eaa2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013599"
---
# <a name="meextendedtype-event"></a>Événement MEExtendedType

Type d’événement personnalisé. Vous pouvez utiliser ce type d’événement pour définir des événements personnalisés pour votre composant. Utilisez le type d’événement étendu pour identifier l’événement. Le type d’événement étendu est une valeur GUID associée à l’événement. Pour plus d’informations, consultez [**IMFMediaEvent :: GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |



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

 

 




