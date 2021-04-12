---
description: Contient un pointeur vers l’interface de rappel des applications pour le lecteur source.
ms.assetid: de226a5a-03c0-4bfe-bb20-8969ce43cf53
title: Attribut MF_SOURCE_READER_ASYNC_CALLBACK (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66542a155fbb6fa3e56958733626b1d0b750ab9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203714"
---
# <a name="mf_source_reader_async_callback-attribute"></a>\_Attribut de \_ \_ rappel asynchrone du lecteur source MF \_

Contient un pointeur vers l’interface de rappel de l’application pour le [lecteur source](source-reader.md).

## <a name="data-type"></a>Type de données

**IMFSourceReaderCallback \** _ stocké en tant que _*IUnknown \**_

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [_ *IMFAttributes :: GetUnknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Pour définir cet attribut, appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Notes

La valeur de cet attribut est un pointeur vers l’interface [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) de l’application.

Utilisez cet attribut avec les fonctions suivantes :

-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 7 \[ Desktop Apps \| UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lecteur source](source-reader.md)
</dt> <dt>

[Attributs du lecteur source](source-reader-attributes.md)
</dt> </dl>

 

 




