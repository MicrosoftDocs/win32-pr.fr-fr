---
description: Permet au moteur multimédia de lire du contenu protégé.
ms.assetid: F6F17EC7-6553-4127-B691-C20C945DD4D8
title: Attribut MF_MEDIA_ENGINE_CONTENT_PROTECTION_MANAGER (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe80e619f3b256f6aa587f32d9ee5b6f43cd2978a5dfb043c62536ff5315bacb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244688"
---
# <a name="mf_media_engine_content_protection_manager-attribute"></a>\_Attribut Media \_ Engine \_ Content \_ protection \_ Manager MF

Permet au moteur multimédia de lire du contenu protégé.

## <a name="data-type"></a>Type de données

**IUnknown\***

## <a name="remarks"></a>Notes

La valeur de cet attribut est un pointeur vers l’interface [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) . L’appelant doit implémenter l’interface.

Cet attribut peut être l’un des attributs passés à [**IMFMediaEngineClassFactory :: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance). Il est obligatoire si le contenu protégé doit être lu.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Mfmediaengine. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFMediaEngineClassFactory :: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




