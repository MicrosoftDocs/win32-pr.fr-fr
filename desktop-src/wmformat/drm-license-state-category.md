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
# <a name="drm_license_state_category-enumeration-drmexternalsh"></a><span data-ttu-id="8f233-105">Énumération DRM_LICENSE_STATE_CATEGORY (Drmexternals. h)</span><span class="sxs-lookup"><span data-stu-id="8f233-105">DRM_LICENSE_STATE_CATEGORY enumeration (Drmexternals.h)</span></span>

<span data-ttu-id="8f233-106">Le type d’énumération de **catégorie d' \_ État de licence \_ \_ DRM** définit les catégories pour les chaînes de [*licence*](wmformat-glossary.md) DRM qui sont affichées à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8f233-106">The **DRM\_LICENSE\_STATE\_CATEGORY** enumeration type defines the categories for DRM [*license*](wmformat-glossary.md) strings that are displayed to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f233-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8f233-107">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="8f233-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="8f233-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8f233-109"><span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**État de la \_ licence WM DRM \_ \_ \_ noright**</span><span class="sxs-lookup"><span data-stu-id="8f233-109"><span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**WM\_DRM\_LICENSE\_STATE\_NORIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="8f233-110">Indique que la chaîne prendra la forme « lecture non autorisée ».</span><span class="sxs-lookup"><span data-stu-id="8f233-110">Indicates the string will take the form "Playback not permitted."</span></span>

</dd> <dt>

<span data-ttu-id="8f233-111"><span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**État de la \_ licence WM DRM \_ \_ \_ UNLIM**</span><span class="sxs-lookup"><span data-stu-id="8f233-111"><span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**WM\_DRM\_LICENSE\_STATE\_UNLIM**</span></span>
</dt> <dd>

<span data-ttu-id="8f233-112">Indique que la chaîne prendra la forme « lecture illimitée ».</span><span class="sxs-lookup"><span data-stu-id="8f233-112">Indicates the string will take the form "Playback unlimited."</span></span>

</dd> <dt>

<span data-ttu-id="8f233-113"><span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**\_nombre d' \_ États de licence WM DRM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8f233-113"><span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT**</span></span>
</dt> <dd>

<span data-ttu-id="8f233-114">Indique que la chaîne prendra la forme « lecture valide 5 fois ».</span><span class="sxs-lookup"><span data-stu-id="8f233-114">Indicates the string will take the form "Playback valid 5 times."</span></span>

</dd> <dt>

<span data-ttu-id="8f233-115"><span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**\_ \_ État de la licence WM DRM \_ \_ de**</span><span class="sxs-lookup"><span data-stu-id="8f233-115"><span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**WM\_DRM\_LICENSE\_STATE\_FROM**</span></span>
</dt> <dd>

<span data-ttu-id="8f233-116">Indique que la chaîne prendra la forme « lecture valide à partir de 7/12/00 ».</span><span class="sxs-lookup"><span data-stu-id="8f233-116">Indicates the string will take the form "Playback valid from 7/12/00."</span></span>

</dd> <dt>

<span data-ttu-id="8f233-117"><span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**État de la \_ licence WM DRM \_ \_ \_ jusqu’au**</span><span class="sxs-lookup"><span data-stu-id="8f233-117"><span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**WM\_DRM\_LICENSE\_STATE\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="8f233-118">Indique que la chaîne prendra la forme « lecture valide jusqu’au 7/12/00 ».</span><span class="sxs-lookup"><span data-stu-id="8f233-118">Indicates the string will take the form "Playback valid until 7/12/00."</span></span>

</dd> <dt>

<span data-ttu-id="8f233-119"><span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**\_ \_ État de la licence WM DRM \_ \_ de \_ jusqu’au**</span><span class="sxs-lookup"><span data-stu-id="8f233-119"><span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**WM\_DRM\_LICENSE\_STATE\_FROM\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="8f233-120">Indique que la chaîne prendra la forme « lecture valide du 5/12 au 9/12 ».</span><span class="sxs-lookup"><span data-stu-id="8f233-120">Indicates the string will take the form "Playback valid from 5/12 to 9/12."</span></span>

</dd> <dt>

<span data-ttu-id="8f233-121"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**\_ \_ \_ nombre d’États de licence WM DRM \_ \_ de**</span><span class="sxs-lookup"><span data-stu-id="8f233-121"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM**</span></span>
</dt> <dd>

<span data-ttu-id="8f233-122">Indique que la chaîne prendra la forme « lecture valide 5 fois de 5/12 à 9/12 ».</span><span class="sxs-lookup"><span data-stu-id="8f233-122">Indicates the string will take the form "Playback valid 5 times from 5/12 to 9/12."</span></span>

</dd> <dt>

<span data-ttu-id="8f233-123"><span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**\_nombre d’États de licence WM DRM \_ \_ \_ \_ jusqu’au**</span><span class="sxs-lookup"><span data-stu-id="8f233-123"><span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="8f233-124">Indique que la chaîne prendra la forme « lecture valide 5 fois jusqu’au 7/12/00 ».</span><span class="sxs-lookup"><span data-stu-id="8f233-124">Indicates the string will take the form "Playback valid 5 times until 7/12/00."</span></span>

</dd> <dt>

<span data-ttu-id="8f233-125"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**\_ \_ \_ nombre d’États de licence WM DRM \_ \_ depuis \_ jusqu’à**</span><span class="sxs-lookup"><span data-stu-id="8f233-125"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="8f233-126">Indique que la chaîne prendra la forme « lecture valide 5 fois de 5/12 à 9/12 ».</span><span class="sxs-lookup"><span data-stu-id="8f233-126">Indicates the string will take the form "Playback valid 5 times from 5/12 to 9/12."</span></span>

</dd> <dt>

<span data-ttu-id="8f233-127"><span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**EXPIRATION de l’état de la \_ licence WM DRM \_ \_ \_ \_ après \_ FIRSTUSE**</span><span class="sxs-lookup"><span data-stu-id="8f233-127"><span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**WM\_DRM\_LICENSE\_STATE\_EXPIRATION\_AFTER\_FIRSTUSE**</span></span>
</dt> <dd>

<span data-ttu-id="8f233-128">Indique que la chaîne prendra la forme « lecture valide pendant 24 heures à partir de la première utilisation ».</span><span class="sxs-lookup"><span data-stu-id="8f233-128">Indicates the string will take the form "Playback valid for 24 hours from first use."</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f233-129">Notes</span><span class="sxs-lookup"><span data-stu-id="8f233-129">Remarks</span></span>

<span data-ttu-id="8f233-130">Cette énumération indique la catégorie de chaque chaîne de sortie possible à afficher.</span><span class="sxs-lookup"><span data-stu-id="8f233-130">This enumeration indicates the category for each possible output string to be displayed.</span></span> <span data-ttu-id="8f233-131">Il est membre de la structure de données de l' [**\_ État de licence \_ \_ DRM**](drm-license-state-data.md) .</span><span class="sxs-lookup"><span data-stu-id="8f233-131">It is a member of the [**DRM\_LICENSE\_STATE\_DATA**](drm-license-state-data.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f233-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f233-132">Requirements</span></span>



| <span data-ttu-id="8f233-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f233-133">Requirement</span></span> | <span data-ttu-id="8f233-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f233-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f233-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f233-135">Minimum supported client</span></span><br/> | <span data-ttu-id="8f233-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f233-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8f233-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f233-137">Minimum supported server</span></span><br/> | <span data-ttu-id="8f233-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f233-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8f233-139">Version</span><span class="sxs-lookup"><span data-stu-id="8f233-139">Version</span></span><br/>                  | <span data-ttu-id="8f233-140">SDK Windows Media Format 7 ou versions ultérieures du kit de développement logiciel (SDK)</span><span class="sxs-lookup"><span data-stu-id="8f233-140">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="8f233-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="8f233-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f233-142"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f233-142"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f233-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f233-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f233-144">**Types énumération**</span><span class="sxs-lookup"><span data-stu-id="8f233-144">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





