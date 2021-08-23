---
description: Type d’événement inconnu. Vous pouvez utiliser cette valeur pour initialiser des variables de type MediaEventType, mais un composant ne doit jamais déclencher l’événement MEUnknown.
ms.assetid: 786b69f4-8713-41db-829a-c13512baa3f1
title: Événement MEUnknown (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5abfd3d0616b435d3e31eb6c08a38fbee41377a493b21ad0494bdd2d367fc93f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714992"
---
# <a name="meunknown-event"></a>Événement MEUnknown

Type d’événement inconnu. Vous pouvez utiliser cette valeur pour initialiser des variables de type **MediaEventType**, mais un composant ne doit jamais déclencher l’événement MEUnknown

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

 

 




