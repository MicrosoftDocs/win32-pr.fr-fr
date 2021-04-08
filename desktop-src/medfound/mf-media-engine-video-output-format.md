---
description: Définit le format de la cible de rendu pour le moteur multimédia.
ms.assetid: 70FFDD44-9FDE-4D86-AD65-60019AC4A2BC
title: Attribut MF_MEDIA_ENGINE_VIDEO_OUTPUT_FORMAT (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 004025da1ad5258e5b04a3afba4a359f50f7444c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761384"
---
# <a name="mf_media_engine_video_output_format-attribute"></a>\_Attribut de \_ \_ format de \_ sortie vidéo de Media Engine MF \_

Définit le format de la cible de rendu pour le moteur multimédia.

## <a name="data-type"></a>Type de données

**Dxgi \_ FORMAT** stocké comme **UInt32**

## <a name="remarks"></a>Notes

Définissez cet attribut si vous créez le moteur multimédia en mode serveur de trame. Pour plus d’informations, consultez [**IMFMediaEngineClassFactory :: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance). La valeur de l’attribut est une valeur de [ \_ format dxgi](../direct3d9/d3dformat.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 8 \[ Desktop Apps \| UWP\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ \| apps UWP\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Mfmediaengine. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
