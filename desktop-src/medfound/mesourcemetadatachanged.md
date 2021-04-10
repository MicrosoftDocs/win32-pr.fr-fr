---
description: Déclenché par une source de média lors de la mise à jour de ses métadonnées.
ms.assetid: 6818b0c9-9628-41e6-8dc6-dff26f4fcfd2
title: Événement MESourceMetadataChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b72463d145d7b4b4b14ac3c321f19a7f9a4c2178
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951300"
---
# <a name="mesourcemetadatachanged-event"></a>Événement MESourceMetadataChanged

Déclenché par une source de média lors de la mise à jour de ses métadonnées.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="remarks"></a>Notes

Si la source du média ne peut pas fournir toutes les métadonnées lorsque la source est créée pour la première fois, elle doit déclencher cet événement une fois que les métadonnées sont disponibles.

La source du média doit créer un nouveau descripteur de présentation et copier tous les attributs du descripteur de présentation (PD) vers l’objet d’événement. L’application peut utiliser l’objet d’événement pour énumérer les nouveaux attributs PD. En particulier, les valeurs pour [MF \_ PD \_ Duration](mf-pd-duration-attribute.md) et [MF \_ PD \_ total \_ file \_ Size](mf-pd-total-file-size-attribute.md) peuvent être inconnues jusqu’à ce que le fichier soit complètement téléchargé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> <dt>

[Attributs du descripteur de présentation](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




