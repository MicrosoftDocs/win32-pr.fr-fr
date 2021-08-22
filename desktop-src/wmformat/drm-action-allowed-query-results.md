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
ms.openlocfilehash: d66973838bb6d9cf745ae30b885acccf7b4b311834bbe827d96ccbeea501bd17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547809"
---
# <a name="drm_action_allowed_query_results-enumeration"></a>\_ \_ \_ Énumération des résultats de requête autorisés par l’action DRM \_

Le type d’énumération des **\_ \_ \_ \_ résultats de requête autorisés par l’action DRM** est utilisé par l’interface [**IWMDRMLicenseQuery :: QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) pour spécifier la raison pour laquelle une action n’est pas autorisée.

## <a name="syntax"></a>Syntaxe


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED"></span><span id="drm_action_allowed_query_not_enabled"></span>**\_requête autorisée d’action DRM \_ \_ \_ non \_ activée**
</dt> <dd>

Spécifie que l’action requêtes n’est pas autorisée. Pour les actions qui ne sont pas autorisées, la valeur retournée est cette valeur combinée à l’aide d’une opération de bits or avec une ou plusieurs autres valeurs de cette énumération.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE"></span><span id="drm_action_allowed_query_not_enabled_no_license"></span>**\_requête autorisée d’action DRM \_ \_ \_ non \_ activée \_ aucune \_ licence**
</dt> <dd>

Spécifie qu’il n’existe aucune licence pour le contenu demandé.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT"></span><span id="drm_action_allowed_query_not_enabled_no_right"></span>**la \_ requête autorisée de l’action DRM \_ n’est \_ \_ pas \_ activée \_ \_**
</dt> <dd>

Spécifie qu’une licence existe pour le contenu, mais que le droit demandé n’est pas autorisé.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED"></span><span id="drm_action_allowed_query_not_enabled_exhausted"></span>**\_requête autorisée d’action DRM \_ \_ \_ non \_ activée \_ épuisée**
</dt> <dd>

Spécifie que le droit interrogé est limité par un nombre et qu’il n’y a plus d’autres utilisations.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED"></span><span id="drm_action_allowed_query_not_enabled_expired"></span>**la \_ requête autorisée de l’action DRM \_ \_ \_ n’a pas été \_ activée \_ .**
</dt> <dd>

Spécifie que le droit interrogé est limité avec une date d’expiration antérieure à la date actuelle.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED"></span><span id="drm_action_allowed_query_not_enabled_not_started"></span>**la \_ requête autorisée de l’action DRM \_ \_ \_ n' \_ a pas \_ \_ été activée.**
</dt> <dd>

Spécifie que le droit interrogé est limité par une date de début postérieure à la date actuelle.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_appsec_too_low"></span>**la \_ requête autorisée de l’action DRM \_ n’est \_ \_ pas \_ activée \_ APPSEC \_ trop \_ faible**
</dt> <dd>

Spécifie qu’une licence existe pour le contenu et que la licence autorise le droit de requête, mais que le niveau de sécurité de l’application appelante n’est pas assez élevé.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV"></span><span id="drm_action_allowed_query_not_enabled_req_indiv"></span>**\_demande d’action DRM \_ autorisée \_ \_ non \_ activée \_ \_ indiv**
</dt> <dd>

Spécifie qu’une licence existe pour le contenu et que la licence autorise le droit de requête, mais que le sous-système DRM doit être individualisé.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_too_low"></span>**\_requête autorisée d’action DRM \_ \_ \_ non \_ activée \_ copie \_ OPL \_ trop \_ faible**
</dt> <dd>

Spécifie que le niveau de protection de sortie du client est trop faible.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_excluded"></span>**\_requête autorisée de l’action DRM \_ \_ \_ non \_ activée \_ copie \_ OPL \_ exclue**
</dt> <dd>

Spécifie que le niveau de protection de sortie du client se trouve dans la liste d’exclusion.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_clock_support"></span>**la \_ requête de l’action DRM \_ autorisée n’est \_ \_ pas activée. \_ \_ aucune \_ horloge \_**
</dt> <dd>

Spécifie que la licence requiert une prise en charge de l’horloge sécurisée et que le client ne la fournit pas.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_metering_support"></span>**la \_ requête autorisée de l’action DRM \_ n’est \_ \_ pas \_ activée. \_ aucune \_ \_ prise en charge du contrôle**
</dt> <dd>

Spécifie que l’action interrogée est autorisée par une licence, mais que ce contrôle est requis et que le client ne prend pas en charge le contrôle.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH"></span><span id="drm_action_allowed_query_not_enabled_chain_depth_too_high"></span>**\_ \_ \_ \_ \_ une profondeur de chaîne non activée \_ pour \_ \_ l’action DRM est trop \_ élevée**
</dt> <dd>

Spécifie que les droits de l’action interrogée ne peuvent pas être déterminés, car le contenu est couvert par une licence chaînée et la licence feuille est manquante.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les valeurs de ce type d’énumération indiquent qu’une action n’est pas autorisée. La valeur zéro indique que l’action est autorisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Types énumération**](drm-enumeration-types.md)
</dt> </dl>

 

 





