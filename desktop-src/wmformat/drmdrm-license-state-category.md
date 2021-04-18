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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543274"
---
# <a name="drm_license_state_category-enumeration-wmdrmsdkh"></a><span data-ttu-id="434ed-104">Énumération DRM_LICENSE_STATE_CATEGORY (wmdrmsdk. h)</span><span class="sxs-lookup"><span data-stu-id="434ed-104">DRM_LICENSE_STATE_CATEGORY enumeration (Wmdrmsdk.h)</span></span>

<span data-ttu-id="434ed-105">Le type d’énumération de la **\_ catégorie d' \_ état \_ de licence DRM** spécifie le type de restriction de licence qui est décrit par une structure de [**données d' \_ État de licence \_ \_ DRM**](drmdrm-license-state-data.md) .</span><span class="sxs-lookup"><span data-stu-id="434ed-105">The **DRM\_LICENSE\_STATE\_CATEGORY** enumeration type specifies the type of license restriction that is described by a [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="434ed-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="434ed-106">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="434ed-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="434ed-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="434ed-108"><span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**État de la \_ licence WM DRM \_ \_ \_ noright**</span><span class="sxs-lookup"><span data-stu-id="434ed-108"><span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**WM\_DRM\_LICENSE\_STATE\_NORIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="434ed-109">Spécifie que l’action pour laquelle **les \_ \_ \_ données d’état de licence DRM** ont été reçues n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="434ed-109">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is not allowed.</span></span>

</dd> <dt>

<span data-ttu-id="434ed-110"><span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**État de la \_ licence WM DRM \_ \_ \_ UNLIM**</span><span class="sxs-lookup"><span data-stu-id="434ed-110"><span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**WM\_DRM\_LICENSE\_STATE\_UNLIM**</span></span>
</dt> <dd>

<span data-ttu-id="434ed-111">Spécifie que l’action pour laquelle **les \_ \_ \_ données d’état de licence DRM** ont été reçues est autorisée sans restriction.</span><span class="sxs-lookup"><span data-stu-id="434ed-111">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed without restriction.</span></span>

</dd> <dt>

<span data-ttu-id="434ed-112"><span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**\_nombre d' \_ États de licence WM DRM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="434ed-112"><span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT**</span></span>
</dt> <dd>

<span data-ttu-id="434ed-113">Spécifie que l’action pour laquelle **les \_ \_ \_ données d’état de licence DRM** ont été reçues est autorisée, mais uniquement un nombre défini de fois.</span><span class="sxs-lookup"><span data-stu-id="434ed-113">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed, but only a set number of times.</span></span>

</dd> <dt>

<span data-ttu-id="434ed-114"><span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**\_ \_ État de la licence WM DRM \_ \_ de**</span><span class="sxs-lookup"><span data-stu-id="434ed-114"><span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**WM\_DRM\_LICENSE\_STATE\_FROM**</span></span>
</dt> <dd>

<span data-ttu-id="434ed-115">Spécifie que l’action pour laquelle **les \_ \_ \_ données d’état de licence DRM** ont été reçues est autorisée après une date définie.</span><span class="sxs-lookup"><span data-stu-id="434ed-115">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed after a set date.</span></span>

</dd> <dt>

<span data-ttu-id="434ed-116"><span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**État de la \_ licence WM DRM \_ \_ \_ jusqu’au**</span><span class="sxs-lookup"><span data-stu-id="434ed-116"><span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**WM\_DRM\_LICENSE\_STATE\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="434ed-117">Spécifie que l’action pour laquelle **les \_ \_ \_ données d’état de licence DRM** ont été reçues est autorisée jusqu’à une date définie.</span><span class="sxs-lookup"><span data-stu-id="434ed-117">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed until a set date.</span></span>

</dd> <dt>

<span data-ttu-id="434ed-118"><span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**\_ \_ État de la licence WM DRM \_ \_ de \_ jusqu’au**</span><span class="sxs-lookup"><span data-stu-id="434ed-118"><span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**WM\_DRM\_LICENSE\_STATE\_FROM\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="434ed-119">Spécifie que l’action pour laquelle **les \_ \_ \_ données d’état de licence DRM** ont été reçues est autorisée entre deux dates définies.</span><span class="sxs-lookup"><span data-stu-id="434ed-119">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed between two set dates.</span></span>

</dd> <dt>

<span data-ttu-id="434ed-120"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**\_ \_ \_ nombre d’États de licence WM DRM \_ \_ de**</span><span class="sxs-lookup"><span data-stu-id="434ed-120"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM**</span></span>
</dt> <dd>

<span data-ttu-id="434ed-121">Spécifie que l’action pour laquelle **les \_ \_ \_ données d’état de licence DRM** ont été reçues est autorisée, mais uniquement un nombre défini de fois après une date définie.</span><span class="sxs-lookup"><span data-stu-id="434ed-121">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed, but only a set number of times after a set date.</span></span>

</dd> <dt>

<span data-ttu-id="434ed-122"><span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**\_nombre d’États de licence WM DRM \_ \_ \_ \_ jusqu’au**</span><span class="sxs-lookup"><span data-stu-id="434ed-122"><span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="434ed-123">Spécifie que l’action pour laquelle **les \_ \_ \_ données d’état de licence DRM** ont été reçues est autorisée, mais uniquement un nombre défini de fois jusqu’à une date définie.</span><span class="sxs-lookup"><span data-stu-id="434ed-123">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed, but only a set number of times until a set date.</span></span>

</dd> <dt>

<span data-ttu-id="434ed-124"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**\_ \_ \_ nombre d’États de licence WM DRM \_ \_ depuis \_ jusqu’à**</span><span class="sxs-lookup"><span data-stu-id="434ed-124"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="434ed-125">Spécifie que l’action pour laquelle **les \_ \_ \_ données d’état de licence DRM** ont été reçues est autorisée, mais uniquement un nombre défini de fois entre deux dates définies.</span><span class="sxs-lookup"><span data-stu-id="434ed-125">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed, but only a set number of times between two set dates.</span></span>

</dd> <dt>

<span data-ttu-id="434ed-126"><span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**EXPIRATION de l’état de la \_ licence WM DRM \_ \_ \_ \_ après \_ FIRSTUSE**</span><span class="sxs-lookup"><span data-stu-id="434ed-126"><span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**WM\_DRM\_LICENSE\_STATE\_EXPIRATION\_AFTER\_FIRSTUSE**</span></span>
</dt> <dd>

<span data-ttu-id="434ed-127">Spécifie que l’action pour laquelle **les \_ \_ \_ données d’état de licence DRM** ont été reçues est autorisée pendant un laps de temps défini à partir de la première utilisation de l’action.</span><span class="sxs-lookup"><span data-stu-id="434ed-127">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed for a set amount of time beginning with the first use of the action.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="434ed-128">Notes</span><span class="sxs-lookup"><span data-stu-id="434ed-128">Remarks</span></span>

<span data-ttu-id="434ed-129">Aucun.</span><span class="sxs-lookup"><span data-stu-id="434ed-129">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="434ed-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="434ed-130">Requirements</span></span>



| <span data-ttu-id="434ed-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="434ed-131">Requirement</span></span> | <span data-ttu-id="434ed-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="434ed-132">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="434ed-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="434ed-133">Header</span></span><br/> | <dl> <span data-ttu-id="434ed-134"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="434ed-134"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="434ed-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="434ed-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="434ed-136">**Types énumération**</span><span class="sxs-lookup"><span data-stu-id="434ed-136">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





