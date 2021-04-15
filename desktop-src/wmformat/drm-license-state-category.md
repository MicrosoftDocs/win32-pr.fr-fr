---
title: Énumération DRM_LICENSE_STATE_CATEGORY (Drmexternals. h)
description: Le \_ \_ \_ type d’énumération de catégorie d’état de licence DRM définit les catégories pour les chaînes de licence DRM qui sont affichées à l’utilisateur.
ms.assetid: f5c5aa78-84f9-4ee4-b551-05bf864243ab
keywords:
- Format Windows Media d’énumération DRM_LICENSE_STATE_CATEGORY
- Format Windows Media d’énumération
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_CATEGORY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40763ec7f610073784e3bd1516d4c955abcd65b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466126"
---
# <a name="drm_license_state_category-enumeration-drmexternalsh"></a>Énumération DRM_LICENSE_STATE_CATEGORY (Drmexternals. h)

Le type d’énumération de **catégorie d' \_ État de licence \_ \_ DRM** définit les catégories pour les chaînes de [*licence*](wmformat-glossary.md) DRM qui sont affichées à l’utilisateur.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum DRM_LICENSE_STATE_CATEGORY { 
  WM_DRM_LICENSE_STATE_NORIGHT                    = 0,
  WM_DRM_LICENSE_STATE_UNLIM,
  WM_DRM_LICENSE_STATE_COUNT,
  WM_DRM_LICENSE_STATE_FROM,
  WM_DRM_LICENSE_STATE_UNTIL,
  WM_DRM_LICENSE_STATE_FROM_UNTIL,
  WM_DRM_LICENSE_STATE_COUNT_FROM,
  WM_DRM_LICENSE_STATE_COUNT_UNTIL,
  WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL,
  WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**État de la \_ licence WM DRM \_ \_ \_ noright**
</dt> <dd>

Indique que la chaîne prendra la forme « lecture non autorisée ».

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**État de la \_ licence WM DRM \_ \_ \_ UNLIM**
</dt> <dd>

Indique que la chaîne prendra la forme « lecture illimitée ».

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**\_nombre d' \_ États de licence WM DRM \_ \_**
</dt> <dd>

Indique que la chaîne prendra la forme « lecture valide 5 fois ».

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**\_ \_ État de la licence WM DRM \_ \_ de**
</dt> <dd>

Indique que la chaîne prendra la forme « lecture valide à partir de 7/12/00 ».

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**État de la \_ licence WM DRM \_ \_ \_ jusqu’au**
</dt> <dd>

Indique que la chaîne prendra la forme « lecture valide jusqu’au 7/12/00 ».

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**\_ \_ État de la licence WM DRM \_ \_ de \_ jusqu’au**
</dt> <dd>

Indique que la chaîne prendra la forme « lecture valide du 5/12 au 9/12 ».

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**\_ \_ \_ nombre d’États de licence WM DRM \_ \_ de**
</dt> <dd>

Indique que la chaîne prendra la forme « lecture valide 5 fois de 5/12 à 9/12 ».

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**\_nombre d’États de licence WM DRM \_ \_ \_ \_ jusqu’au**
</dt> <dd>

Indique que la chaîne prendra la forme « lecture valide 5 fois jusqu’au 7/12/00 ».

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**\_ \_ \_ nombre d’États de licence WM DRM \_ \_ depuis \_ jusqu’à**
</dt> <dd>

Indique que la chaîne prendra la forme « lecture valide 5 fois de 5/12 à 9/12 ».

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**EXPIRATION de l’état de la \_ licence WM DRM \_ \_ \_ \_ après \_ FIRSTUSE**
</dt> <dd>

Indique que la chaîne prendra la forme « lecture valide pendant 24 heures à partir de la première utilisation ».

</dd> </dl>

## <a name="remarks"></a>Notes

Cette énumération indique la catégorie de chaque chaîne de sortie possible à afficher. Il est membre de la structure de données de l' [**\_ État de licence \_ \_ DRM**](drm-license-state-data.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                      |
| Version<br/>                  | SDK Windows Media Format 7 ou versions ultérieures du kit de développement logiciel (SDK)<br/>                       |
| En-tête<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Types énumération**](enumeration-types.md)
</dt> </dl>

 

 





