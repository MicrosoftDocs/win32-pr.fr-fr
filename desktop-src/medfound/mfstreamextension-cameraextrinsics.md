---
description: Contient le extrinsics d’appareil photo pour le flux.
ms.assetid: 2236C135-BA3D-4C1B-8A39-5E23EF67425A
title: Attribut MFStreamExtension_CameraExtrinsics (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a551aaaef48100d6104804e54f7e0ddfac3f5cb1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313730"
---
# <a name="mfstreamextension_cameraextrinsics-attribute"></a>\_Attribut MFStreamExtension CameraExtrinsics

Contient le extrinsics d’appareil photo pour le flux.

## <a name="data-type"></a>Type de données

Tableau d’octets

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFMediaSourceEx :: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes).

## <a name="remarks"></a>Notes

La valeur de l’attribut est un [**MFCameraExtrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




