---
description: Spécifie le rôle d’appareil pour le flux audio.
ms.assetid: E4B7660D-5F41-495A-B77D-94B7981F4C2C
title: Attribut MF_MEDIA_ENGINE_AUDIO_ENDPOINT_ROLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b1b00115a28592140e41463cf296acf54ad7cde
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106535737"
---
# <a name="mf_media_engine_audio_endpoint_role-attribute"></a>\_Attribut de \_ rôle de \_ point de terminaison audio du moteur multimédia \_ MF \_

Spécifie le rôle d’appareil pour le flux audio.

## <a name="data-type"></a>Type de données

**[**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)** stocké en tant que **UInt32**

## <a name="remarks"></a>Notes

La valeur de cet attribut est un membre de l’énumération [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) .

Cet attribut est utilisé avec la méthode [**IMFMediaEngineClassFactory :: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) pour initialiser le moteur multimédia. L’attribut est facultatif.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 8 \[ Desktop Apps \| UWP\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ \| apps UWP\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
