---
description: Déclenché par la session multimédia lorsque le format change sur un récepteur multimédia.
ms.assetid: f56419f8-7f50-4eda-bf4a-fcdbbe46e180
title: Événement MESessionStreamSinkFormatChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f08d086d5966e0fc1f6ce4b4b3d639b40d795a4e05799f3928f61afa9abddf4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119268589"
---
# <a name="mesessionstreamsinkformatchanged-event"></a>Événement MESessionStreamSinkFormatChanged

Déclenché par la session multimédia lorsque le format change sur un récepteur multimédia.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="attributes"></a>Attributs

Les attributs suivants sont définis pour cet événement.



| Attribut                                                                    | Description                                                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**\_ \_ nœud sortie de l’événement MF \_**](mf-event-output-node-attribute.md)<br/> | Identifie le nœud de topologie du récepteur multimédia dont le format a été modifié.<br/> <br/> |



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

 

 




