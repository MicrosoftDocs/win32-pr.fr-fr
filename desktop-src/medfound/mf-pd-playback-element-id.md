---
description: Contient l’identificateur de l’élément de sélection dans la présentation.
ms.assetid: 355818cf-1e00-46ad-9ce1-ab3a178164f9
title: Attribut MF_PD_PLAYBACK_ELEMENT_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 744a1d164c71cbd7eb8bb47ef12be68d47b8351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529445"
---
# <a name="mf_pd_playback_element_id-attribute"></a>\_Attribut d' \_ ID d’élément de lecture MF PD \_ \_

Contient l’identificateur de l’élément de sélection dans la présentation.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>S’applique à

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Notes

Les sources multimédias qui fournissent des sélections peuvent éventuellement définir cet attribut sur leurs descripteurs de présentation.

Lorsqu’une source de média remet une sélection, elle envoie un événement [MENewPresentation](menewpresentation.md) pour chaque élément de sélection après le premier. Cet événement contient un descripteur de présentation pour le nouvel élément playlist. La source du média peut affecter des identificateurs aux éléments en définissant l' \_ attribut d’ID d’élément de lecture MF PD \_ \_ \_ sur chaque descripteur de présentation, y compris celui créé par [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).

Une source de média peut également envoyer l’événement [MENewPresentation](menewpresentation.md) en raison d’un changement de flux dynamique ou d’une modification du nombre de flux. Dans ce cas, la valeur de l' \_ ID d’élément de lecture MF PD \_ \_ \_ doit rester la même dans les deux présentations, pour indiquer que les deux présentations représentent le même élément de sélection. Si deux présentations consécutives ont la même valeur pour cet attribut, le pipeline Microsoft Media Foundation s’attend à ce que les horodatages restent continus au sein de la transition. Par conséquent, la source du média ne doit pas utiliser l’attribut de [ \_ \_ \_ \_ début réel](mf-event-source-actual-start-attribute.md) de la source de l’événement MF lorsqu’elle passe à la présentation suivante.

Les sources multimédias qui implémentent [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) doivent utiliser l’attribut d' [ \_ \_ \_ ELEMENTID de séquence TOPONODE MF](mf-toponode-sequence-elementid-attribute.md) plutôt que l' \_ attribut d’ID d’élément de lecture MF PD \_ \_ \_ .

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 7 \[ Desktop Apps \| UWP\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]<br/>                     |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du descripteur de présentation](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




