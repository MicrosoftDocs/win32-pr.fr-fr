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
ms.openlocfilehash: 852d44a4c812aed0d2f188b5ab18e9b74a1813bd9605bf348ca23b96b72f7d2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809409"
---
# <a name="drm_actionallowed_copytocd"></a>\_ACTIONALLOWED DRM \_ CopyToCD

L’attribut **DRM \_ ActionAllowed \_ CopyToCD** indique si le contenu peut être copié sur un CD.

## <a name="global-constant"></a>Constante globale

g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD

## <a name="data-type"></a>Type de données

**\_type WMT \_ bool**

## <a name="remarks"></a>Remarques

Windows Les licences Media DRM 10 utilisent l’action de copie pour limiter la copie sur CD. Vous devez vérifier la propriété de [**\_ \_ copie DRM ActionAllowed**](drm-actionallowed-copy.md) pour déterminer si la copie est autorisée.

Il s’agit d’une propriété en lecture seule qui est récupérée à l’aide de [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés DRM**](drm-properties.md)
</dt> </dl>

 

 




