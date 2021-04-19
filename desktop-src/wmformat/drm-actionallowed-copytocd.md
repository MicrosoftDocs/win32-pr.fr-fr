---
title: DRM_ActionAllowed_CopyToCD
description: L' \_ attribut DRM ActionAllowed \_ CopyToCD indique si le contenu peut être copié sur un CD.
ms.assetid: c650bb2e-6cec-404a-8ece-7a5687cda99f
keywords:
- Format Windows Media DRM_ActionAllowed_CopyToCD
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToCD
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ba214fb2f067ba523222f92211bf7a9412a1634
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106511473"
---
# <a name="drm_actionallowed_copytocd"></a>\_ACTIONALLOWED DRM \_ CopyToCD

L’attribut **DRM \_ ActionAllowed \_ CopyToCD** indique si le contenu peut être copié sur un CD.

## <a name="global-constant"></a>Constante globale

g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD

## <a name="data-type"></a>Type de données

**\_type WMT \_ bool**

## <a name="remarks"></a>Notes

Les licences Windows Media DRM 10 utilisent l’action copier pour limiter la copie sur CD. Vous devez vérifier la propriété de [**\_ \_ copie DRM ActionAllowed**](drm-actionallowed-copy.md) pour déterminer si la copie est autorisée.

Il s’agit d’une propriété en lecture seule qui est récupérée à l’aide de [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés DRM**](drm-properties.md)
</dt> </dl>

 

 




