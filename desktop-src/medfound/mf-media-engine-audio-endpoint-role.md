---
description: Spécifie le rôle d’appareil pour le flux audio.
ms.assetid: E4B7660D-5F41-495A-B77D-94B7981F4C2C
title: Attribut MF_MEDIA_ENGINE_AUDIO_ENDPOINT_ROLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a15a973aef342e3d37cde3e6d9f3dd7d61c553fecaa943215dbcc77a319950
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104775"
---
# <a name="mf_media_engine_audio_endpoint_role-attribute"></a>\_Attribut de \_ rôle de \_ point de terminaison audio du moteur multimédia \_ MF \_

Spécifie le rôle d’appareil pour le flux audio.

## <a name="data-type"></a>Type de données

**[**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)** stocké en tant que **UInt32**

## <a name="remarks"></a>Remarques

La valeur de cet attribut est un membre de l’énumération [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) .

Cet attribut est utilisé avec la méthode [**IMFMediaEngineClassFactory :: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) pour initialiser le moteur multimédia. L’attribut est facultatif.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
