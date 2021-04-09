---
description: Spécifie l’heure de début d’une topologie de segment.
ms.assetid: d8902fb6-c758-4d3d-9230-e918948bda19
title: Attribut MF_EVENT_SOURCE_PROJECTSTART (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 512e2129c3104d9e7160163f03a9c28b2716273e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869117"
---
# <a name="mf_event_source_projectstart-attribute"></a>\_Attribut PROJECTSTART de la source d’événement MF \_ \_

Spécifie l’heure de début d’une topologie de segment.

## <a name="data-type"></a>Type de données

**UINT64**

Traiter en tant que valeur **LongLong** .

## <a name="remarks"></a>Notes

Cet attribut est utilisé avec l’événement [MESourceStarted](mesourcestarted.md) . La source de Sequencer définit cet attribut lorsque la topologie de segment actuelle a l' [**attribut \_ \_ PROJECTSTART de topologie MF**](mf-topology-projectstart-attribute.md) . Les deux attributs ont la même valeur.

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

 

 




