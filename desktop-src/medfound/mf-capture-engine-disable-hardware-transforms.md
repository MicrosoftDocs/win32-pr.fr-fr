---
description: Désactive l’utilisation des transformations de Media Foundation basées sur le matériel (MFTs) dans le moteur de capture.
ms.assetid: 1C687FEC-276D-4759-A3B8-9A2A31CB0DE1
title: Attribut MF_CAPTURE_ENGINE_DISABLE_HARDWARE_TRANSFORMS (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9631804c61fab953793c3f89d1eac3dc2e8f4dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531260"
---
# <a name="mf_capture_engine_disable_hardware_transforms-attribute"></a>\_Attribut de \_ \_ désactivation \_ des \_ transformations matérielles du moteur de capture MF

Désactive l’utilisation des transformations de Media Foundation basées sur le matériel (MFTs) dans le moteur de capture.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="remarks"></a>Notes

Par défaut, le moteur de capture utilise des décodeurs ou des encodeurs matériels. Pour désactiver l’utilisation du matériel MFTs, affectez la valeur **true** à cet attribut lorsque vous créez le moteur de capture.

## <a name="requirements"></a>Spécifications



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

 

 




