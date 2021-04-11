---
description: Spécifie si le lecteur source active DirectX Video Acceleration (DXVA) sur le décodeur vidéo.
ms.assetid: ec539038-3fd3-41b7-a0e6-e75e3f2828a7
title: Attribut MF_SOURCE_READER_DISABLE_DXVA (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9362f067d1d6ceae426e9ee6530e08b95837595f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320470"
---
# <a name="mf_source_reader_disable_dxva-attribute"></a>\_ \_ \_ Attribut DXVA de désactivation de lecteur source \_ MF

Spécifie si le [lecteur source](source-reader.md) active DirectX Video Acceleration (DXVA) sur le décodeur vidéo.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Notes

Cet attribut s’applique si les conditions suivantes sont vraies :

-   Le lecteur source décode un flux vidéo.
-   Le décodeur vidéo prend en charge le décodage DXVA.
-   L’application utilise l’attribut du [ \_ \_ \_ \_ Gestionnaire D3D du lecteur source MF](mf-source-reader-d3d-manager.md) pour définir le [Gestionnaire de périphériques Direct3D](direct3d-device-manager.md) sur le lecteur source.

Cet attribut permet à l’application de désactiver DXVA tout en décodant toujours les surfaces Direct3D.

Par défaut, le lecteur source utilise le [Gestionnaire de périphériques Direct3D](direct3d-device-manager.md) pour deux raisons :

-   Pour activer le décodage DXVA dans le décodeur vidéo.
-   Pour allouer des surfaces Direct3D pour les exemples vidéo.

Si la valeur de l' \_ \_ \_ attribut DXVA de désactivation de l' \_ attribut DXVA est **true**, le lecteur source désactive le décodage DXVA, bien qu’il utilise toujours le [Gestionnaire de périphériques Direct3D](direct3d-device-manager.md) pour allouer des surfaces Direct3D.

Si l’attribut du [ \_ \_ \_ \_ Gestionnaire D3D du lecteur source MF](mf-source-reader-d3d-manager.md) n’est pas défini, l' \_ attribut DXVA du lecteur source MF de \_ \_ désactivation \_ est ignoré.

La valeur par défaut de cet attribut est **false**, ce qui signifie que le décodage DXVA est activé lorsqu’il est disponible.

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

 

 




