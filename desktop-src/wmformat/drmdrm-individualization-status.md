---
title: Énumération DRM_INDIVIDUALIZATION_STATUS (wmdrmsdk. h)
description: Le \_ \_ type d’énumération de l’état de l’individualisation DRM définit les États valides pour l’individualisation DRM. | Énumération DRM_INDIVIDUALIZATION_STATUS (wmdrmsdk. h)
ms.assetid: 4e6712e2-3297-4636-9b0c-07269bd63d52
keywords:
- Format Windows Media d’énumération DRM_INDIVIDUALIZATION_STATUS
- Format Windows Media d’énumération
topic_type:
- apiref
api_name:
- DRM_INDIVIDUALIZATION_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b395d3ad4271ccef9964f0d39c74a1e0ba158257
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521703"
---
# <a name="drm_individualization_status-enumeration-wmdrmsdkh"></a><span data-ttu-id="682c3-106">Énumération DRM_INDIVIDUALIZATION_STATUS (wmdrmsdk. h)</span><span class="sxs-lookup"><span data-stu-id="682c3-106">DRM_INDIVIDUALIZATION_STATUS enumeration (Wmdrmsdk.h)</span></span>

<span data-ttu-id="682c3-107">Le type d’énumération de l’état de l' **\_ \_ individualisation DRM** définit les États valides pour l’individualisation DRM.</span><span class="sxs-lookup"><span data-stu-id="682c3-107">The **DRM\_INDIVIDUALIZATION\_STATUS** enumeration type defines the valid states for DRM individualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="682c3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="682c3-108">Syntax</span></span>


```C++
typedef enum DRM_INDIVIDUALIZATION_STATUS { 
  INDI_UNDEFINED  = 0x0000,
  INDI_BEGIN      = 0x0001,
  INDI_SUCCEED    = 0x0002,
  INDI_FAIL       = 0x0004,
  INDI_CANCEL     = 0x0008,
  INDI_DOWNLOAD   = 0x0010,
  INDI_INSTALL    = 0x0020
} ;
```



## <a name="constants"></a><span data-ttu-id="682c3-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="682c3-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="682c3-110"><span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**INDI \_ non défini**</span><span class="sxs-lookup"><span data-stu-id="682c3-110"><span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**INDI\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="682c3-111">Cette valeur est réservée à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="682c3-111">This value is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="682c3-112"><span id="INDI_BEGIN"></span><span id="indi_begin"></span>**INDI \_ Begin**</span><span class="sxs-lookup"><span data-stu-id="682c3-112"><span id="INDI_BEGIN"></span><span id="indi_begin"></span>**INDI\_BEGIN**</span></span>
</dt> <dd>

<span data-ttu-id="682c3-113">Indique le début du processus d’individualisation.</span><span class="sxs-lookup"><span data-stu-id="682c3-113">Indicates the start of the individualization process.</span></span>

</dd> <dt>

<span data-ttu-id="682c3-114"><span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**INDI \_ réussie**</span><span class="sxs-lookup"><span data-stu-id="682c3-114"><span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**INDI\_SUCCEED**</span></span>
</dt> <dd>

<span data-ttu-id="682c3-115">Indique que le processus d’individualisation est terminé.</span><span class="sxs-lookup"><span data-stu-id="682c3-115">Indicates that the individualization process has been completed.</span></span>

</dd> <dt>

<span data-ttu-id="682c3-116"><span id="INDI_FAIL"></span><span id="indi_fail"></span>**échec de INDI \_**</span><span class="sxs-lookup"><span data-stu-id="682c3-116"><span id="INDI_FAIL"></span><span id="indi_fail"></span>**INDI\_FAIL**</span></span>
</dt> <dd>

<span data-ttu-id="682c3-117">Indique que le processus d’individualisation a échoué.</span><span class="sxs-lookup"><span data-stu-id="682c3-117">Indicates that the individualization process failed.</span></span>

</dd> <dt>

<span data-ttu-id="682c3-118"><span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**INDI \_ Annuler**</span><span class="sxs-lookup"><span data-stu-id="682c3-118"><span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**INDI\_CANCEL**</span></span>
</dt> <dd>

<span data-ttu-id="682c3-119">Indique que le processus d’individualisation a été annulé par l’application.</span><span class="sxs-lookup"><span data-stu-id="682c3-119">Indicates that the individualization process was canceled by the application.</span></span>

</dd> <dt>

<span data-ttu-id="682c3-120"><span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**Téléchargement de INDI \_**</span><span class="sxs-lookup"><span data-stu-id="682c3-120"><span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**INDI\_DOWNLOAD**</span></span>
</dt> <dd>

<span data-ttu-id="682c3-121">Indique que la mise à niveau de sécurité est en cours de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="682c3-121">Indicates that the security upgrade is being downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="682c3-122"><span id="INDI_INSTALL"></span><span id="indi_install"></span>**installation de INDI \_**</span><span class="sxs-lookup"><span data-stu-id="682c3-122"><span id="INDI_INSTALL"></span><span id="indi_install"></span>**INDI\_INSTALL**</span></span>
</dt> <dd>

<span data-ttu-id="682c3-123">Indique que la mise à niveau de sécurité est en cours d’installation.</span><span class="sxs-lookup"><span data-stu-id="682c3-123">Indicates that the security upgrade is being installed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="682c3-124">Notes</span><span class="sxs-lookup"><span data-stu-id="682c3-124">Remarks</span></span>

<span data-ttu-id="682c3-125">Cette énumération est utilisée par la structure d' [**\_ \_ État**](drmwm-individualize-status.md) de l’énumération WM.</span><span class="sxs-lookup"><span data-stu-id="682c3-125">This enumeration is used by the [**WM\_INDIVIDUALIZE\_STATUS**](drmwm-individualize-status.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="682c3-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="682c3-126">Requirements</span></span>



| <span data-ttu-id="682c3-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="682c3-127">Requirement</span></span> | <span data-ttu-id="682c3-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="682c3-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="682c3-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="682c3-129">Header</span></span><br/> | <dl> <span data-ttu-id="682c3-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="682c3-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="682c3-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="682c3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="682c3-132">**Types énumération**</span><span class="sxs-lookup"><span data-stu-id="682c3-132">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





