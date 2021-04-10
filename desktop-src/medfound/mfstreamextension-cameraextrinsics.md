---
description: Contient le extrinsics d’appareil photo pour le flux.
ms.assetid: 2236C135-BA3D-4C1B-8A39-5E23EF67425A
title: Attribut MFStreamExtension_CameraExtrinsics (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a551aaaef48100d6104804e54f7e0ddfac3f5cb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114402"
---
# <a name="mfstreamextension_cameraextrinsics-attribute"></a>\_Attribut MFStreamExtension CameraExtrinsics

Contient le extrinsics d’appareil photo pour le flux.

## <a name="data-type"></a>Type de données

Tableau d’octets

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFMediaSourceEx :: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes).

## <a name="remarks"></a>Notes

La valeur de l’attribut est un [**MFCameraExtrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




