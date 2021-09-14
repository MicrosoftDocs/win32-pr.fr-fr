---
description: Contient les intrinsèques de l’appareil photo Pinhole pour le flux.
ms.assetid: 7E5E7C60-9C3F-406B-A7DD-A953181CD314
title: Attribut MFStreamExtension_PinholeCameraIntrinsics (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ee9ad848f0b8cc12c2496544d98b4ef17332151
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235914"
---
# <a name="mfstreamextension_pinholecameraintrinsics-attribute"></a>\_Attribut MFStreamExtension PinholeCameraIntrinsics

Contient les intrinsèques de l’appareil photo Pinhole pour le flux.

## <a name="data-type"></a>Type de données

Tableau d’octets

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFMediaSourceEx :: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes).

## <a name="remarks"></a>Notes

La valeur de l’attribut est un [**MFPinholeCameraIntrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




