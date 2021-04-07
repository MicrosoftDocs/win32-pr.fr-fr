---
description: Contient un pointeur vers l’interface de rappel des applications pour le writer du récepteur.
ms.assetid: 22df1fa0-469d-4501-aaf0-a0379b7ed096
title: Attribut MF_SINK_WRITER_ASYNC_CALLBACK (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f11bed051df9107ca3a2247b6c3d0cf2058224c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759568"
---
# <a name="mf_sink_writer_async_callback-attribute"></a>\_Attribut de \_ \_ rappel asynchrone du writer de récepteur MF \_

Contient un pointeur vers l’interface de rappel de l’application pour le writer du récepteur.

## <a name="data-type"></a>Type de données

**[](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) IMFSinkWriterCallback \** _ stocké en tant que _*IUnknown \**_

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [_ *IMFAttributes :: GetUnknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Pour définir cet attribut, appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Notes

La valeur de cet attribut est un pointeur vers l’interface [**IMFSinkWriterCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) de l’application.

Utilisez cet attribut avec les fonctions suivantes :

-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

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

[Attributs du writer du récepteur](sink-writer-attributes.md)
</dt> </dl>

 

 




