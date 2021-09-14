---
description: Spécifie si le lecteur source arrête la source du média.
ms.assetid: c85f5994-8005-48c9-8a05-0316f48f4142
title: Attribut MF_SOURCE_READER_DISCONNECT_MEDIASOURCE_ON_SHUTDOWN (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a9474e7fb19bb6531baf31a97238bbe6b10e46
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231761"
---
# <a name="mf_source_reader_disconnect_mediasource_on_shutdown-attribute"></a>\_Lecteur source \_ MF \_ Disconnect \_ MEDIASOURCE \_ sur l' \_ attribut Shutdown

Spécifie si le [lecteur source](source-reader.md) arrête la source du média.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Notes

Cet attribut s’applique uniquement lorsque l’application crée le lecteur source à partir d’un objet source multimédia existant, en appelant [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource) ou en appelant [**IMFReadWriteClassFactory :: CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject).

Par défaut, lorsque l’application libère le lecteur source, le lecteur source arrête la source du média en appelant [**IMFMediaSource :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) sur la source du média. À ce stade, l’application ne peut plus utiliser la source du média.

Toutefois, si le \_ lecteur source \_ MF \_ Disconnect \_ MEDIASOURCE \_ sur \_ l’attribut Shutdown a la **valeur true**, le lecteur source n’arrête pas la source du média. Cela signifie que l’application peut toujours utiliser la source du média après que l’application a libéré le lecteur source. Cela signifie également que l’application est responsable de l’appel de [**IMFMediaSource :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) sur la source du média.

Si l’application crée le lecteur source à partir d’une URL ou d’un flux d’octets, le lecteur source arrête toujours la source du média. Le \_ lecteur source \_ MF \_ Disconnect \_ MEDIASOURCE \_ sur l' \_ attribut Shutdown est ignoré dans ce cas.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Applications du serveur 2008 R2 \[ Desktop Apps \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lecteur source](source-reader.md)
</dt> <dt>

[Attributs du lecteur source](source-reader-attributes.md)
</dt> </dl>

 

 




