---
description: Heure de présentation à laquelle les récepteurs multimédia affichent le premier exemple de la nouvelle topologie.
ms.assetid: 02a8c542-b519-495e-9fb2-8db2f5384db7
title: Attribut MF_EVENT_START_PRESENTATION_TIME_AT_OUTPUT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a588bc6604deed6c6865cd8283390d28e3ffd49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866189"
---
# <a name="mf_event_start_presentation_time_at_output-attribute"></a>\_ \_ \_ Heure de présentation du démarrage de l’événement MF \_ \_ au niveau de l' \_ attribut de sortie

Heure de présentation à laquelle les récepteurs multimédia affichent le premier exemple de la nouvelle topologie.

## <a name="data-type"></a>Type de données

**UINT64**

Traiter en tant que valeur **LongLong** .

## <a name="remarks"></a>Notes

Si des objets de pipeline dans la topologie précédente présentent des données mises en mémoire tampon, cette valeur sera légèrement inférieure à la valeur de l’attribut de décalage de l’heure de présentation de l' [**\_ événement \_ \_ \_ MF**](mf-event-presentation-time-offset-attribute.md) , car les récepteurs doivent restituer les données mises en mémoire tampon.

Cet attribut est une valeur signée, bien qu’il soit stocké en tant que **UINT64**.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
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

 

 




