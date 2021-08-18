---
description: Définit le format de la cible de rendu pour le moteur multimédia.
ms.assetid: 70FFDD44-9FDE-4D86-AD65-60019AC4A2BC
title: Attribut MF_MEDIA_ENGINE_VIDEO_OUTPUT_FORMAT (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaa0dab3c3ea1c9ce23d767458df0b68a9b3c787f80ca1af786061536343a356
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973728"
---
# <a name="mf_media_engine_video_output_format-attribute"></a>\_Attribut de \_ \_ format de \_ sortie vidéo de Media Engine MF \_

Définit le format de la cible de rendu pour le moteur multimédia.

## <a name="data-type"></a>Type de données

**Dxgi \_ FORMAT** stocké comme **UInt32**

## <a name="remarks"></a>Remarques

Définissez cet attribut si vous créez le moteur multimédia en mode serveur de trame. Pour plus d’informations, consultez [**IMFMediaEngineClassFactory :: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance). La valeur de l’attribut est une valeur de [ \_ format dxgi](../direct3d9/d3dformat.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Mfmediaengine. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
