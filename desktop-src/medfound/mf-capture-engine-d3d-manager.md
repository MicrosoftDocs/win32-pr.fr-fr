---
description: Définit un pointeur vers le Gestionnaire de périphériques DXGI sur le moteur de capture.
ms.assetid: 1DFDE7AB-7DFF-4C39-9460-E42E37649AAC
title: Attribut MF_CAPTURE_ENGINE_D3D_MANAGER (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3c5e87d4817f539f91ecd55aec10a2086afeaeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113683"
---
# <a name="mf_capture_engine_d3d_manager-attribute"></a>\_Attribut du \_ \_ Gestionnaire D3D du moteur de capture MF \_

Définit un pointeur vers le Gestionnaire de périphériques DXGI sur le moteur de capture.

## <a name="data-type"></a>Type de données

**IUnknown \** _

## <a name="remarks"></a>Notes

La valeur de cet attribut est un pointeur vers l’interface [_ *IMFDXGIDeviceManager* *](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) . Cet attribut permet au moteur de capture d’allouer des images vidéo à l’aide de surfaces DXGI et d’utiliser l’accélération matérielle pour le décodage et le traitement vidéo.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                   |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                         |
| En-tête<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du moteur de capture](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine :: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




