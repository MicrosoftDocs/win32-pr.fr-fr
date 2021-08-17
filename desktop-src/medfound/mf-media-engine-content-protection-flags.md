---
description: Spécifie si le moteur multimédia doit lire du contenu protégé.
ms.assetid: 2A593499-BF40-440E-AF1D-3B0E7732489A
title: Attribut MF_MEDIA_ENGINE_CONTENT_PROTECTION_FLAGS (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1cb6b9c9a49c690af84678435ac2bb4fdab76a2fb13c95fecd9ddc33771d7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956439"
---
# <a name="mf_media_engine_content_protection_flags-attribute"></a>\_ \_ \_ \_ Attribut indicateurs de protection du contenu Media Engine MF \_

Spécifie si le moteur multimédia doit lire du contenu protégé.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

La valeur de cet attribut est **une opération or au niveau du bit** des indicateurs de l’énumération des [**indicateurs de protection du \_ moteur de Media \_ \_ \_ MF**](/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_protection_flags) . Pour activer la lecture de contenu protégé, définissez l’indicateur **\_ Media \_ Engine \_ Enable \_ protected \_ content** .

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

[Attributs du moteur multimédia](media-engine-attributes.md)
</dt> <dt>

[**IMFMediaEngineClassFactory :: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




