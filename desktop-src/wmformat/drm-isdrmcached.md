---
title: DRM_IsDRMCached
description: La \_ propriété DRM IsDRMCached indique si les informations de licence DRM version 1 ont été stockées sur l’ordinateur local.
ms.assetid: 868e3ada-d608-41d6-93d7-0b7930cbf2f9
keywords:
- Format Windows Media DRM_IsDRMCached
topic_type:
- apiref
api_name:
- DRM_IsDRMCached
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9b5bbcf7e4e1c11c8ae992156b7541ac66c7a9d43f2cb1d52878d1ee6762d6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709039"
---
# <a name="drm_isdrmcached"></a>\_ISDRMCACHED DRM

La propriété **DRM \_ IsDRMCached** indique si les informations de licence DRM version 1 ont été stockées sur l’ordinateur local.

## <a name="global-constant"></a>Constante globale

g \_ wszWMDRM \_ IsDRMCached

## <a name="data-type"></a>Type de données

**\_type WMT \_ bool**

## <a name="remarks"></a>Remarques

Il s’agit d’une propriété en lecture seule qui est récupérée à l’aide de [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Cela est **vrai** lorsque l’URL d’acquisition de licence correspond à l’une des deux URL connues utilisées pour l’acquisition de licences locales dans DRM version 1.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés DRM**](drm-properties.md)
</dt> </dl>

 

 




