---
title: Énumération DRM_ACTION_ALLOWED_QUERY_RESULTS (wmdrmsdk. h)
description: Le \_ type d' \_ \_ énumération des résultats de requête autorisés \_ par l’action DRM est utilisé par l’interface IWMDRMLicenseQuery QueryActionAllowed pour spécifier la raison pour laquelle une action n’est pas autorisée.
ms.assetid: dc784cdf-6efe-415b-ba72-eb8fc50bef10
keywords:
- Format Windows Media d’énumération DRM_ACTION_ALLOWED_QUERY_RESULTS
- Format Windows Media d’énumération
topic_type:
- apiref
api_name:
- DRM_ACTION_ALLOWED_QUERY_RESULTS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d1e328acb915bd32547f3455e8556e4caba2360
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526846"
---
# <a name="drm_action_allowed_query_results-enumeration"></a><span data-ttu-id="efe71-105">\_ \_ \_ Énumération des résultats de requête autorisés par l’action DRM \_</span><span class="sxs-lookup"><span data-stu-id="efe71-105">DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS enumeration</span></span>

<span data-ttu-id="efe71-106">Le type d’énumération des **\_ \_ \_ \_ résultats de requête autorisés par l’action DRM** est utilisé par l’interface [**IWMDRMLicenseQuery :: QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) pour spécifier la raison pour laquelle une action n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="efe71-106">The **DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS** enumeration type is used by the [**IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) interface to specify the reason an action is not allowed.</span></span>

## <a name="syntax"></a><span data-ttu-id="efe71-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="efe71-107">Syntax</span></span>


```C++
typedef enum DRM_ACTION_ALLOWED_QUERY_RESULTS { 
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED                       = 0x00000001,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE            = 0x00000002,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT              = 0x00000004,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED             = 0x00000008,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED               = 0x00000010,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED           = 0x00000020,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW        = 0x00000040,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV             = 0x00000080,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW      = 0x00000100,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED     = 0x00000200,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT      = 0x00000400,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT   = 0x00000800,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH  = 0x00001000
} ;
```



## <a name="constants"></a><span data-ttu-id="efe71-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="efe71-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="efe71-109"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED"></span><span id="drm_action_allowed_query_not_enabled"></span>**\_requête autorisée d’action DRM \_ \_ \_ non \_ activée**</span><span class="sxs-lookup"><span data-stu-id="efe71-109"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED"></span><span id="drm_action_allowed_query_not_enabled"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED**</span></span>
</dt> <dd>

<span data-ttu-id="efe71-110">Spécifie que l’action requêtes n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="efe71-110">Specifies that the queries action is not allowed.</span></span> <span data-ttu-id="efe71-111">Pour les actions qui ne sont pas autorisées, la valeur retournée est cette valeur combinée à l’aide d’une opération de bits or avec une ou plusieurs autres valeurs de cette énumération.</span><span class="sxs-lookup"><span data-stu-id="efe71-111">For actions that are not allowed, the returned value is this value combined by using a bitwise OR with one or more of the other values in this enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="efe71-112"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE"></span><span id="drm_action_allowed_query_not_enabled_no_license"></span>**\_requête autorisée d’action DRM \_ \_ \_ non \_ activée \_ aucune \_ licence**</span><span class="sxs-lookup"><span data-stu-id="efe71-112"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE"></span><span id="drm_action_allowed_query_not_enabled_no_license"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NO\_LICENSE**</span></span>
</dt> <dd>

<span data-ttu-id="efe71-113">Spécifie qu’il n’existe aucune licence pour le contenu demandé.</span><span class="sxs-lookup"><span data-stu-id="efe71-113">Specifies that a license does not exist for the requested content.</span></span>

</dd> <dt>

<span data-ttu-id="efe71-114"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT"></span><span id="drm_action_allowed_query_not_enabled_no_right"></span>**la \_ requête autorisée de l’action DRM \_ n’est \_ \_ pas \_ activée \_ \_**</span><span class="sxs-lookup"><span data-stu-id="efe71-114"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT"></span><span id="drm_action_allowed_query_not_enabled_no_right"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NO\_RIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="efe71-115">Spécifie qu’une licence existe pour le contenu, mais que le droit demandé n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="efe71-115">Specifies that a license exists for the content, but that the queried right is not allowed.</span></span>

</dd> <dt>

<span data-ttu-id="efe71-116"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED"></span><span id="drm_action_allowed_query_not_enabled_exhausted"></span>**\_requête autorisée d’action DRM \_ \_ \_ non \_ activée \_ épuisée**</span><span class="sxs-lookup"><span data-stu-id="efe71-116"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED"></span><span id="drm_action_allowed_query_not_enabled_exhausted"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_EXHAUSTED**</span></span>
</dt> <dd>

<span data-ttu-id="efe71-117">Spécifie que le droit interrogé est limité par un nombre et qu’il n’y a plus d’autres utilisations.</span><span class="sxs-lookup"><span data-stu-id="efe71-117">Specifies that the queried right is restricted by a count, and that no more uses remain.</span></span>

</dd> <dt>

<span data-ttu-id="efe71-118"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED"></span><span id="drm_action_allowed_query_not_enabled_expired"></span>**la \_ requête autorisée de l’action DRM \_ \_ \_ n’a pas été \_ activée \_ .**</span><span class="sxs-lookup"><span data-stu-id="efe71-118"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED"></span><span id="drm_action_allowed_query_not_enabled_expired"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_EXPIRED**</span></span>
</dt> <dd>

<span data-ttu-id="efe71-119">Spécifie que le droit interrogé est limité avec une date d’expiration antérieure à la date actuelle.</span><span class="sxs-lookup"><span data-stu-id="efe71-119">Specifies that the queried right is restricted with an expiration date that is earlier than the current date.</span></span>

</dd> <dt>

<span data-ttu-id="efe71-120"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED"></span><span id="drm_action_allowed_query_not_enabled_not_started"></span>**la \_ requête autorisée de l’action DRM \_ \_ \_ n' \_ a pas \_ \_ été activée.**</span><span class="sxs-lookup"><span data-stu-id="efe71-120"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED"></span><span id="drm_action_allowed_query_not_enabled_not_started"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NOT\_STARTED**</span></span>
</dt> <dd>

<span data-ttu-id="efe71-121">Spécifie que le droit interrogé est limité par une date de début postérieure à la date actuelle.</span><span class="sxs-lookup"><span data-stu-id="efe71-121">Specifies that the queried right is restricted with a start date that is later than the current date.</span></span>

</dd> <dt>

<span data-ttu-id="efe71-122"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_appsec_too_low"></span>**la \_ requête autorisée de l’action DRM \_ n’est \_ \_ pas \_ activée \_ APPSEC \_ trop \_ faible**</span><span class="sxs-lookup"><span data-stu-id="efe71-122"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_appsec_too_low"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_APPSEC\_TOO\_LOW**</span></span>
</dt> <dd>

<span data-ttu-id="efe71-123">Spécifie qu’une licence existe pour le contenu et que la licence autorise le droit de requête, mais que le niveau de sécurité de l’application appelante n’est pas assez élevé.</span><span class="sxs-lookup"><span data-stu-id="efe71-123">Specifies that a license exists for the content and that the license allows the queried right, but that the security level of the calling application is not high enough.</span></span>

</dd> <dt>

<span data-ttu-id="efe71-124"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV"></span><span id="drm_action_allowed_query_not_enabled_req_indiv"></span>**\_demande d’action DRM \_ autorisée \_ \_ non \_ activée \_ \_ indiv**</span><span class="sxs-lookup"><span data-stu-id="efe71-124"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV"></span><span id="drm_action_allowed_query_not_enabled_req_indiv"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_REQ\_INDIV**</span></span>
</dt> <dd>

<span data-ttu-id="efe71-125">Spécifie qu’une licence existe pour le contenu et que la licence autorise le droit de requête, mais que le sous-système DRM doit être individualisé.</span><span class="sxs-lookup"><span data-stu-id="efe71-125">Specifies that a license exists for the content and that the license allows the queried right, but that the DRM subsystem must be individualized.</span></span>

</dd> <dt>

<span data-ttu-id="efe71-126"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_too_low"></span>**\_requête autorisée d’action DRM \_ \_ \_ non \_ activée \_ copie \_ OPL \_ trop \_ faible**</span><span class="sxs-lookup"><span data-stu-id="efe71-126"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_too_low"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_COPY\_OPL\_TOO\_LOW**</span></span>
</dt> <dd>

<span data-ttu-id="efe71-127">Spécifie que le niveau de protection de sortie du client est trop faible.</span><span class="sxs-lookup"><span data-stu-id="efe71-127">Specifies that the output protection level of the client is too low.</span></span>

</dd> <dt>

<span data-ttu-id="efe71-128"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_excluded"></span>**\_requête autorisée de l’action DRM \_ \_ \_ non \_ activée \_ copie \_ OPL \_ exclue**</span><span class="sxs-lookup"><span data-stu-id="efe71-128"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_excluded"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_COPY\_OPL\_EXCLUDED**</span></span>
</dt> <dd>

<span data-ttu-id="efe71-129">Spécifie que le niveau de protection de sortie du client se trouve dans la liste d’exclusion.</span><span class="sxs-lookup"><span data-stu-id="efe71-129">Specifies that the output protection level of the client is on the exclusion list.</span></span>

</dd> <dt>

<span data-ttu-id="efe71-130"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_clock_support"></span>**la \_ requête de l’action DRM \_ autorisée n’est \_ \_ pas activée. \_ \_ aucune \_ horloge \_**</span><span class="sxs-lookup"><span data-stu-id="efe71-130"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_clock_support"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NO\_CLOCK\_SUPPORT**</span></span>
</dt> <dd>

<span data-ttu-id="efe71-131">Spécifie que la licence requiert une prise en charge de l’horloge sécurisée et que le client ne la fournit pas.</span><span class="sxs-lookup"><span data-stu-id="efe71-131">Specifies that the license requires secure clock support and that the client does not provide it.</span></span>

</dd> <dt>

<span data-ttu-id="efe71-132"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_metering_support"></span>**la \_ requête autorisée de l’action DRM \_ n’est \_ \_ pas \_ activée. \_ aucune \_ \_ prise en charge du contrôle**</span><span class="sxs-lookup"><span data-stu-id="efe71-132"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_metering_support"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NO\_METERING\_SUPPORT**</span></span>
</dt> <dd>

<span data-ttu-id="efe71-133">Spécifie que l’action interrogée est autorisée par une licence, mais que ce contrôle est requis et que le client ne prend pas en charge le contrôle.</span><span class="sxs-lookup"><span data-stu-id="efe71-133">Specifies that the queried action is allowed by a license, but that metering is required and the client does not support metering.</span></span>

</dd> <dt>

<span data-ttu-id="efe71-134"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH"></span><span id="drm_action_allowed_query_not_enabled_chain_depth_too_high"></span>**\_ \_ \_ \_ \_ une profondeur de chaîne non activée \_ pour \_ \_ l’action DRM est trop \_ élevée**</span><span class="sxs-lookup"><span data-stu-id="efe71-134"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH"></span><span id="drm_action_allowed_query_not_enabled_chain_depth_too_high"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_CHAIN\_DEPTH\_TOO\_HIGH**</span></span>
</dt> <dd>

<span data-ttu-id="efe71-135">Spécifie que les droits de l’action interrogée ne peuvent pas être déterminés, car le contenu est couvert par une licence chaînée et la licence feuille est manquante.</span><span class="sxs-lookup"><span data-stu-id="efe71-135">Specifies that the rights for the queried action cannot be determined because the content is covered by a chained license and the leaf license is missing.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="efe71-136">Notes</span><span class="sxs-lookup"><span data-stu-id="efe71-136">Remarks</span></span>

<span data-ttu-id="efe71-137">Les valeurs de ce type d’énumération indiquent qu’une action n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="efe71-137">The values of this enumeration type indicate that an action is not allowed.</span></span> <span data-ttu-id="efe71-138">La valeur zéro indique que l’action est autorisée.</span><span class="sxs-lookup"><span data-stu-id="efe71-138">A value of zero indicates that the action is allowed.</span></span>

## <a name="requirements"></a><span data-ttu-id="efe71-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="efe71-139">Requirements</span></span>



| <span data-ttu-id="efe71-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="efe71-140">Requirement</span></span> | <span data-ttu-id="efe71-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="efe71-141">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="efe71-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="efe71-142">Header</span></span><br/> | <dl> <span data-ttu-id="efe71-143"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="efe71-143"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efe71-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efe71-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efe71-145">**Types énumération**</span><span class="sxs-lookup"><span data-stu-id="efe71-145">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





