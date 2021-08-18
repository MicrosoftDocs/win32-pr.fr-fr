---
description: Spécifie si la topologie du segment actuel est vide.
ms.assetid: efd497dc-affc-4453-975c-09c5dca06374
title: Attribut MF_EVENT_SOURCE_FAKE_START (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b026811330443a3fb5e7c9671a7f6a3de8580985b6be4c6ba149a2d4dc196325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973768"
---
# <a name="mf_event_source_fake_start-attribute"></a>\_Attribut de \_ \_ début factice de source d’événement MF \_

Spécifie si la topologie du segment actuel est vide.

## <a name="data-type"></a>Type de données

**UINT32**

Traiter en tant que valeur booléenne.

## <a name="remarks"></a>Remarques

Cet attribut est utilisé avec l’événement [MESourceStarted](mesourcestarted.md) .

La source de Sequencer affecte la **valeur true** à cet attribut si la topologie du segment actuel est vide. Si cet attribut a la **valeur true**, la lecture n’a pas encore démarré. La valeur par défaut de cet attribut est **false**.

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

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




