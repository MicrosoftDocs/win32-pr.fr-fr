---
description: Le flux de médias utilise cet événement pour envoyer des métadonnées spécifiques du système de protection au décodeur.
ms.assetid: 249446CA-AEF7-41A1-98EB-0B9392AE4AD8
title: Événement MEContentProtectionMetadata (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd72289a900b9c9b96fe9a64d427dab13110d66
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530792"
---
# <a name="mecontentprotectionmetadata-event"></a>Événement MEContentProtectionMetadata

Le flux de médias utilise cet événement pour envoyer des métadonnées spécifiques du système de protection au décodeur.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="attributes"></a>Attributs

Les attributs suivants sont définis pour cet événement.



| Attribut                                                                                              | Description                                                                                         |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [\_keyData \_ de \_ métadonnées de flux d’événements MF \_](mf-event-stream-metadata-keydata.md)<br/>                | Il s’agit d’un attribut facultatif. Données spécifiques au système de protection.<br/> <br/>              |
| [\_contenu des \_ métadonnées du flux d’événements MF \_ \_ \_ KEYIDS](mf-event-stream-metadata-content-keyids.md)<br/> | ID de la clé de contenu à laquelle l’événement est associé.<br/> <br/>                          |
| [\_métadonnées de flux d’événements MF \_ \_ \_ SYSTEMID](mf-event-stream-metadata-systemid.md)<br/>              | Il s’agit d’un attribut facultatif. ID système pour lequel les données de clé sont destinées.<br/> <br/> |



## <a name="remarks"></a>Notes

Cet événement est utilisé, par exemple, pour l’événement de rotation de clé communiquant. Dans ce cas, il doit être envoyé le plus tôt possible pour permettre au décodeur de se préparer avant même que les échantillons chiffrés avec le nouvel ID de clé commencent à arriver.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




