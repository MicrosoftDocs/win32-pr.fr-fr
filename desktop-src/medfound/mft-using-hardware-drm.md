---
description: Spécifie si le IMFTransform utilise le matériel DRM.
title: MFT_USING_HARDWARE_DRM (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e6dbacedbf5fd9298e4da5154bd82fcc9f39bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485345"
---
# <a name="mft_using_hardware_drm-attribute"></a>MFT \_ utilisant \_ l' \_ attribut DRM matériel

Spécifie si le IMFTransform utilise le matériel DRM.

## <a name="data-type"></a>Type de données

**UInt32** (traité comme **bool**)

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>S’applique à

[**IMTransfrom**](/windows/win32/api/mftransform/nn-mftransform-imftransform)

## <a name="remarks"></a>Notes

Si un Decrypter MFT spécifie que cet attribut a la valeur 1, il utilise le service DRM matériel. Si un Decrypter MFT spécifie que cet attribut a la valeur 0, il n’utilise pas de DRM matériel. Si un Decrypter MFT ne spécifie pas cet attribut ou le spécifie avec une valeur différente, alors il n’est pas (ou n’est pas possible) d’indiquer s’il utilise la DRM matérielle.


La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Mise à jour 2020 de Windows 10 avril   <br/>                                       |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[Attributs de transformation](transform-attributes.md)
</dt> </dl>

 

 




