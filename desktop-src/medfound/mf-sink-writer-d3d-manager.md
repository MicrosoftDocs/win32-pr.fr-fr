---
description: Contient un pointeur vers le Gestionnaire de périphériques DXGI pour le writer du récepteur.
ms.assetid: 0328FC02-2D32-480B-BB03-9C78BF317AF5
title: Attribut MF_SINK_WRITER_D3D_MANAGER (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23dea964be1a0ff726a974deaf1949863331df1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544317"
---
# <a name="mf_sink_writer_d3d_manager-attribute"></a>\_Attribut du \_ \_ Gestionnaire D3D \_ de l’enregistreur du récepteur MF

Contient un pointeur vers le Gestionnaire de périphériques DXGI pour le [writer du récepteur](sink-writer.md).

## <a name="data-type"></a>Type de données

**IMFDXGIDeviceManager \** _ stocké en tant que _*IUnknown \**_

## <a name="remarks"></a>Notes

La valeur de cet attribut est un pointeur vers l’interface [_ *IMFDXGIDeviceManager* *](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .

Utilisez cet attribut pour fournir un appareil Direct3D pour tous les encodeurs vidéo ou récepteurs multimédias chargés par le writer du récepteur.

Utilisez cet attribut avec les fonctions suivantes :

-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 8 \[ Desktop Apps \| UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ \| apps UWP\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Enregistreur du récepteur](sink-writer.md)
</dt> </dl>

 

 




