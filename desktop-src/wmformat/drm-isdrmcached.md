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
ms.openlocfilehash: 185a8b2c94ca5ec517eb1a781262e3f988001a01
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106545736"
---
# <a name="drm_isdrmcached"></a>\_ISDRMCACHED DRM

La propriété **DRM \_ IsDRMCached** indique si les informations de licence DRM version 1 ont été stockées sur l’ordinateur local.

## <a name="global-constant"></a>Constante globale

g \_ wszWMDRM \_ IsDRMCached

## <a name="data-type"></a>Type de données

**\_type WMT \_ bool**

## <a name="remarks"></a>Notes

Il s’agit d’une propriété en lecture seule qui est récupérée à l’aide de [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Cela est **vrai** lorsque l’URL d’acquisition de licence correspond à l’une des deux URL connues utilisées pour l’acquisition de licences locales dans DRM version 1.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés DRM**](drm-properties.md)
</dt> </dl>

 

 




