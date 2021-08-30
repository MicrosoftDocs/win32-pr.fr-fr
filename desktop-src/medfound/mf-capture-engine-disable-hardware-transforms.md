---
description: Désactive l’utilisation des transformations de Media Foundation basées sur le matériel (MFTs) dans le moteur de capture.
ms.assetid: 1C687FEC-276D-4759-A3B8-9A2A31CB0DE1
title: Attribut MF_CAPTURE_ENGINE_DISABLE_HARDWARE_TRANSFORMS (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7818e79a78ab346ffb8a1967569fdd8711e2b948e0eb656f032770487d8820ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956809"
---
# <a name="mf_capture_engine_disable_hardware_transforms-attribute"></a>\_Attribut de \_ \_ désactivation \_ des \_ transformations matérielles du moteur de capture MF

Désactive l’utilisation des transformations de Media Foundation basées sur le matériel (MFTs) dans le moteur de capture.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="remarks"></a>Remarques

Par défaut, le moteur de capture utilise des décodeurs ou des encodeurs matériels. Pour désactiver l’utilisation du matériel MFTs, affectez la valeur **true** à cet attribut lorsque vous créez le moteur de capture.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                         |
| En-tête<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du moteur de capture](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine :: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




