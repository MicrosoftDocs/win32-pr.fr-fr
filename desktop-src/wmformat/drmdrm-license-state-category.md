---
title: Énumération DRM_LICENSE_STATE_CATEGORY (wmdrmsdk. h)
description: Le \_ \_ \_ type d’énumération de la catégorie d’état de licence DRM spécifie le type de restriction de licence qui est décrit par une \_ structure de données d’état de licence DRM \_ \_ .
ms.assetid: 51258be9-2f4d-4f25-97f7-2cac6c155ade
keywords:
- Format Windows Media d’énumération DRM_LICENSE_STATE_CATEGORY
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_CATEGORY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e928a95a71d9636f88bc3c79ac36168072527040
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127230993"
---
# <a name="drm_license_state_category-enumeration-wmdrmsdkh"></a>Énumération DRM_LICENSE_STATE_CATEGORY (wmdrmsdk. h)

Le type d’énumération de la **\_ catégorie d' \_ état \_ de licence DRM** spécifie le type de restriction de licence qui est décrit par une structure de [**données d' \_ État de licence \_ \_ DRM**](drmdrm-license-state-data.md) .

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
} DRM_LICENSE_STATE_CATEGORY;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**État de la \_ licence WM DRM \_ \_ \_ noright**
</dt> <dd>

Spécifie que l’action pour laquelle **les \_ \_ \_ données d’état de licence DRM** ont été reçues n’est pas autorisée.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**État de la \_ licence WM DRM \_ \_ \_ UNLIM**
</dt> <dd>

Spécifie que l’action pour laquelle **les \_ \_ \_ données d’état de licence DRM** ont été reçues est autorisée sans restriction.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**\_nombre d' \_ États de licence WM DRM \_ \_**
</dt> <dd>

Spécifie que l’action pour laquelle **les \_ \_ \_ données d’état de licence DRM** ont été reçues est autorisée, mais uniquement un nombre défini de fois.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**\_ \_ État de la licence WM DRM \_ \_ de**
</dt> <dd>

Spécifie que l’action pour laquelle **les \_ \_ \_ données d’état de licence DRM** ont été reçues est autorisée après une date définie.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**État de la \_ licence WM DRM \_ \_ \_ jusqu’au**
</dt> <dd>

Spécifie que l’action pour laquelle **les \_ \_ \_ données d’état de licence DRM** ont été reçues est autorisée jusqu’à une date définie.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**\_ \_ État de la licence WM DRM \_ \_ de \_ jusqu’au**
</dt> <dd>

Spécifie que l’action pour laquelle **les \_ \_ \_ données d’état de licence DRM** ont été reçues est autorisée entre deux dates définies.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**\_ \_ \_ nombre d’États de licence WM DRM \_ \_ de**
</dt> <dd>

Spécifie que l’action pour laquelle **les \_ \_ \_ données d’état de licence DRM** ont été reçues est autorisée, mais uniquement un nombre défini de fois après une date définie.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**\_nombre d’États de licence WM DRM \_ \_ \_ \_ jusqu’au**
</dt> <dd>

Spécifie que l’action pour laquelle **les \_ \_ \_ données d’état de licence DRM** ont été reçues est autorisée, mais uniquement un nombre défini de fois jusqu’à une date définie.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**\_ \_ \_ nombre d’États de licence WM DRM \_ \_ depuis \_ jusqu’à**
</dt> <dd>

Spécifie que l’action pour laquelle **les \_ \_ \_ données d’état de licence DRM** ont été reçues est autorisée, mais uniquement un nombre défini de fois entre deux dates définies.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**EXPIRATION de l’état de la \_ licence WM DRM \_ \_ \_ \_ après \_ FIRSTUSE**
</dt> <dd>

Spécifie que l’action pour laquelle **les \_ \_ \_ données d’état de licence DRM** ont été reçues est autorisée pendant un laps de temps défini à partir de la première utilisation de l’action.

</dd> </dl>

## <a name="remarks"></a>Notes

Aucun.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Types énumération**](drm-enumeration-types.md)
</dt> </dl>

 

 





