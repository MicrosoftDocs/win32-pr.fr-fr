---
description: Contient un pointeur vers le Gestionnaire de périphériques Microsoft Direct3D pour le lecteur source.
ms.assetid: 507d350e-da0c-42d0-8a8d-77618ee5a1dd
title: Attribut MF_SOURCE_READER_D3D_MANAGER (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43bf0d49bb2744ff8219f8d15a6316f11875455c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865578"
---
# <a name="mf_source_reader_d3d_manager-attribute"></a>\_Attribut du \_ \_ Gestionnaire D3D du lecteur source MF \_

Contient un pointeur vers le [Gestionnaire de périphériques Microsoft Direct3D](direct3d-device-manager.md) pour le [lecteur source](source-reader.md).

## <a name="data-type"></a>Type de données

**IDirect3DDeviceManager9 \* ou IMFDXGIDeviceManager \*** stocké sous la forme **IUnknown \** _

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [_ *IMFAttributes :: GetUnknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Pour définir cet attribut, appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Notes

La valeur de cet attribut peut être un pointeur vers l’interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) ou un [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager).

Utilisez cet attribut pour fournir un appareil Direct3D pour tous les décodeurs vidéo chargés par le lecteur source. Si vous définissez cet attribut et que le décodeur prend en charge l’accélération vidéo Microsoft DirectX (DXVA), le lecteur source utilise le périphérique Direct3D pour allouer des mémoires tampons vidéo. Ces mémoires tampons sont compatibles avec le processeur vidéo DXVA 2. (Voir [traitement vidéo DXVA](dxva-video-processing.md).)

Utilisez cet attribut avec les fonctions suivantes :

-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

En général, vous définissez cet attribut si vous utilisez le lecteur source pour obtenir des trames vidéo décodées et que vous utilisez Direct3D pour afficher les frames. La définition de cet attribut permet au décodeur d’utiliser DXVA.

Vous ne définissez pas cet attribut si :

-   Vous utilisez le lecteur source pour traiter uniquement les données audio et non vidéo.
-   Vous obtenez une vidéo compressée à partir du lecteur source. Dans ce cas, le lecteur source ne crée pas de décodeur.

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

 

 




