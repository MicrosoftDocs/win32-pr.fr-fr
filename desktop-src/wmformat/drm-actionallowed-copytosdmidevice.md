---
title: DRM_ActionAllowed_CopyToSDMIDevice
description: L' \_ attribut DRM ActionAllowed \_ CopyToSDMIDevice indique si le contenu peut être copié sur un appareil SDMI.
ms.assetid: 3ffb9c8f-5640-4ab5-9939-f9525ab960c6
keywords:
- Format Windows Media DRM_ActionAllowed_CopyToSDMIDevice
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a868eab52d354672802ef1f736bbc2754af605371708247415cbe78a42442e1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809419"
---
# <a name="drm_actionallowed_copytosdmidevice"></a>\_ACTIONALLOWED DRM \_ CopyToSDMIDevice

L’attribut **DRM \_ ActionAllowed \_ CopyToSDMIDevice** indique si le contenu peut être copié sur un appareil SDMI.

## <a name="global-constant"></a>Constante globale

g \_ wszWMDRM \_ ActionAllowed \_ CopyToSDMIDevice

## <a name="data-type"></a>Type de données

**\_type WMT \_ bool**

## <a name="remarks"></a>Remarques

Windows Les licences Media DRM 10 utilisent l’action de copie pour limiter la copie sur les appareils. Vous devez vérifier la propriété de [**\_ \_ copie DRM ActionAllowed**](drm-actionallowed-copy.md) pour déterminer si la copie est autorisée.

Il s’agit d’une propriété en lecture seule qui est récupérée à l’aide de [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés DRM**](drm-properties.md)
</dt> </dl>

 

 




