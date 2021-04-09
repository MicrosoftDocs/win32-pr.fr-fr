---
title: DRM_ActionAllowed_CopyToNonSDMIDevice
description: L' \_ attribut DRM ActionAllowed \_ CopyToNonSDMIDevice indique si le contenu peut être copié sur un appareil non-SDMI.
ms.assetid: 517ceeb5-4979-4667-ba54-8b9b1c6069f2
keywords:
- Format Windows Media DRM_ActionAllowed_CopyToNonSDMIDevice
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToNonSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8043c6384fbe0ce57ba56fc9799810d7b6a126b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030832"
---
# <a name="drm_actionallowed_copytononsdmidevice"></a>\_ACTIONALLOWED DRM \_ CopyToNonSDMIDevice

L’attribut **DRM \_ ActionAllowed \_ CopyToNonSDMIDevice** indique si le contenu peut être copié sur un appareil non-SDMI

## <a name="global-constant"></a>Constante globale

g \_ wszWMDRM \_ ActionAllowed \_ CopyToNonSDMIDevice

## <a name="data-type"></a>Type de données

**\_type WMT \_ bool**

## <a name="remarks"></a>Notes

Les licences Windows Media DRM 10 utilisent l’action de copie pour limiter la copie sur les appareils. Vous devez vérifier la propriété de [**\_ \_ copie DRM ActionAllowed**](drm-actionallowed-copy.md) pour déterminer si la copie est autorisée.

Il s’agit d’une propriété en lecture seule qui est récupérée à l’aide de [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés DRM**](drm-properties.md)
</dt> </dl>

 

 




