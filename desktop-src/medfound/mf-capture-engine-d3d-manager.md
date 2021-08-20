---
description: Définit un pointeur vers le Gestionnaire de périphériques DXGI sur le moteur de capture.
ms.assetid: 1DFDE7AB-7DFF-4C39-9460-E42E37649AAC
title: Attribut MF_CAPTURE_ENGINE_D3D_MANAGER (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dd8db74da2a55bba4eb0a50f48d80a31d3f75514f5f20b5d0d1329a63b71a7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061152"
---
# <a name="mf_capture_engine_d3d_manager-attribute"></a>\_Attribut du \_ \_ Gestionnaire D3D du moteur de capture MF \_

Définit un pointeur vers le Gestionnaire de périphériques DXGI sur le moteur de capture.

## <a name="data-type"></a>Type de données

**IUnknown\***

## <a name="remarks"></a>Remarques

La valeur de cet attribut est un pointeur vers l’interface [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) . Cet attribut permet au moteur de capture d’allouer des images vidéo à l’aide de surfaces DXGI et d’utiliser l’accélération matérielle pour le décodage et le traitement vidéo.

## <a name="requirements"></a>Conditions requises



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

 

 




