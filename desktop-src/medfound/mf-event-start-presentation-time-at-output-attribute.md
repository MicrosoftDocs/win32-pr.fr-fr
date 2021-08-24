---
description: Heure de présentation à laquelle les récepteurs multimédia affichent le premier exemple de la nouvelle topologie.
ms.assetid: 02a8c542-b519-495e-9fb2-8db2f5384db7
title: Attribut MF_EVENT_START_PRESENTATION_TIME_AT_OUTPUT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bd5949a73244eec26fb0390805c11f630291a470b2016b5a3575311261b72a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723179"
---
# <a name="mf_event_start_presentation_time_at_output-attribute"></a>\_ \_ \_ Heure de présentation du démarrage de l’événement MF \_ \_ au niveau de l' \_ attribut de sortie

Heure de présentation à laquelle les récepteurs multimédia affichent le premier exemple de la nouvelle topologie.

## <a name="data-type"></a>Type de données

**UINT64**

Traiter en tant que valeur **LongLong** .

## <a name="remarks"></a>Remarques

Si des objets de pipeline dans la topologie précédente présentent des données mises en mémoire tampon, cette valeur sera légèrement inférieure à la valeur de l’attribut de décalage de l’heure de présentation de l' [**\_ événement \_ \_ \_ MF**](mf-event-presentation-time-offset-attribute.md) , car les récepteurs doivent restituer les données mises en mémoire tampon.

Cet attribut est une valeur signée, bien qu’il soit stocké en tant que **UINT64**.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs d'événement](event-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




