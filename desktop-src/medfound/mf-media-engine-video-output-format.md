---
description: Définit le format de la cible de rendu pour le moteur multimédia.
ms.assetid: 70FFDD44-9FDE-4D86-AD65-60019AC4A2BC
title: Attribut MF_MEDIA_ENGINE_VIDEO_OUTPUT_FORMAT (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 004025da1ad5258e5b04a3afba4a359f50f7444c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414172"
---
# <a name="mf_media_engine_video_output_format-attribute"></a>\_Attribut de \_ \_ format de \_ sortie vidéo de Media Engine MF \_

Définit le format de la cible de rendu pour le moteur multimédia.

## <a name="data-type"></a>Type de données

**Dxgi \_ FORMAT** stocké comme **UInt32**

## <a name="remarks"></a>Notes

Définissez cet attribut si vous créez le moteur multimédia en mode serveur de trame. Pour plus d’informations, consultez [**IMFMediaEngineClassFactory :: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance). La valeur de l’attribut est une valeur de [ \_ format dxgi](../direct3d9/d3dformat.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Mfmediaengine. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
