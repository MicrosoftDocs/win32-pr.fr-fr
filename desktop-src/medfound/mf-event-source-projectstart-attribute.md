---
description: Spécifie l’heure de début d’une topologie de segment.
ms.assetid: d8902fb6-c758-4d3d-9230-e918948bda19
title: Attribut MF_EVENT_SOURCE_PROJECTSTART (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75e3d386b90a45d1ba06d0d0c1641b97544ca1d2422dd1d2d6f7762f93cf4ee4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118060695"
---
# <a name="mf_event_source_projectstart-attribute"></a>\_Attribut PROJECTSTART de la source d’événement MF \_ \_

Spécifie l’heure de début d’une topologie de segment.

## <a name="data-type"></a>Type de données

**UINT64**

Traiter en tant que valeur **LongLong** .

## <a name="remarks"></a>Remarques

Cet attribut est utilisé avec l’événement [MESourceStarted](mesourcestarted.md) . La source de Sequencer définit cet attribut lorsque la topologie de segment actuelle a l' [**attribut \_ \_ PROJECTSTART de topologie MF**](mf-topology-projectstart-attribute.md) . Les deux attributs ont la même valeur.

Cet attribut est une valeur signée, bien qu’il soit stocké en tant que **UINT64**.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Conditions requises



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

 

 




