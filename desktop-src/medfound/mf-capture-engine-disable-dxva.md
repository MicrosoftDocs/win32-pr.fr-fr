---
description: Spécifie si le moteur de capture utilise l’accélération vidéo DirectX (DXVA) pour le décodage vidéo.
ms.assetid: 9F677E6E-0DCD-456F-8A00-1C11011BAA13
title: Attribut MF_CAPTURE_ENGINE_DISABLE_DXVA (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d2ce31ed55e151e7254168e5e6bcce0c5460e88
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531261"
---
# <a name="mf_capture_engine_disable_dxva-attribute"></a>\_Désactiver l' \_ \_ \_ attribut DXVA du moteur de capture MF

Spécifie si le moteur de capture utilise l’accélération vidéo DirectX (DXVA) pour le décodage vidéo.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="remarks"></a>Notes

Cet attribut s’applique si les conditions suivantes sont vraies :

-   Le moteur de capture décode un flux vidéo compressé à partir du périphérique de capture (par exemple, si l’appareil de capture émet une vidéo H. 264).
-   Le décodeur vidéo prend en charge le décodage accéléré par le matériel à l’aide d’DXVA.
-   L’application utilise l’attribut de [ \_ \_ \_ \_ Gestionnaire D3D du moteur de capture MF](mf-capture-engine-d3d-manager.md) pour définir le gestionnaire de périphériques dxgi sur le moteur de capture.

Dans le cas contraire, cet attribut est ignoré.

Cet attribut permet à l’application de désactiver DXVA tout en décodant toujours les surfaces Direct3D.

La valeur par défaut de cet attribut est **false**, ce qui signifie que le décodage DXVA est activé lorsqu’il est disponible.

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

 

 




