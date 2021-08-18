---
description: Contient l’heure de début à laquelle une source du média redémarre à partir de sa position actuelle.
ms.assetid: b598b4d1-40e1-4282-b312-5aa6ca3a6733
title: Attribut MF_EVENT_SOURCE_ACTUAL_START (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46ce39e8a9f90ad0cd7f0cbd590b32719ab10dbd8e498c396e86772ce333e94c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104835"
---
# <a name="mf_event_source_actual_start-attribute"></a>\_Attribut de \_ \_ début réel \_ de la source de l’événement MF

Contient l’heure de début à laquelle une source du média redémarre à partir de sa position actuelle.

## <a name="data-type"></a>Type de données

**UINT64**

Traiter en tant que valeur **LongLong** .

## <a name="remarks"></a>Remarques

Cet attribut est utilisé avec l’événement [MESourceStarted](mesourcestarted.md) . L’attribut est pertinent lorsque les données d’événement sont vides (**VT \_ vide**), ce qui indique que la source du média a démarré à partir de la position de lecture actuelle. Dans ce cas, l’attribut de **\_ \_ \_ \_ début réel de la source d’événements MF** spécifie l’heure de début réelle. Si les données d’événement sont des données **VT \_ vides** et que cet attribut n’est pas défini, l’heure de début est supposée être égale à zéro.

Lorsque les données d’événement [MESourceStarted](mesourcestarted.md) contiennent l’heure de début (**VT \_ i8**), cet attribut ne doit pas être défini.

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

 

 




