---
description: Contient un pointeur vers le Gestionnaire de périphériques DXGI pour le writer du récepteur.
ms.assetid: 0328FC02-2D32-480B-BB03-9C78BF317AF5
title: Attribut MF_SINK_WRITER_D3D_MANAGER (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 706287b6001ba52c8bf5ba8a19326948afcf4f7f7569c606507115f484c46f10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714309"
---
# <a name="mf_sink_writer_d3d_manager-attribute"></a>\_Attribut du \_ \_ Gestionnaire D3D \_ de l’enregistreur du récepteur MF

Contient un pointeur vers le Gestionnaire de périphériques DXGI pour le [writer du récepteur](sink-writer.md).

## <a name="data-type"></a>Type de données

**IMFDXGIDeviceManager \* *_ stocké en tant que _* IUnknown\***

## <a name="remarks"></a>Remarques

La valeur de cet attribut est un pointeur vers l’interface [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .

Utilisez cet attribut pour fournir un appareil Direct3D pour tous les encodeurs vidéo ou récepteurs multimédias chargés par le writer du récepteur.

Utilisez cet attribut avec les fonctions suivantes :

-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Enregistreur du récepteur](sink-writer.md)
</dt> </dl>

 

 




