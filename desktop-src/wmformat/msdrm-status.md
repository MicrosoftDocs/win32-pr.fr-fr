---
title: Énumération MSDRM_STATUS (wmdrmsdk. h)
description: Le \_ type d’énumération d’État msdrm définit des conditions d’État pour le sous-système DRM.
ms.assetid: b26600ea-2603-4fca-9408-2d5c88091dcc
keywords:
- Format Windows Media d’énumération MSDRM_STATUS
- Format Windows Media d’énumération
topic_type:
- apiref
api_name:
- MSDRM_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf2a73de9e33216e22a01966be8f2ed6a3185fdf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528079"
---
# <a name="msdrm_status-enumeration"></a><span data-ttu-id="72445-105">\_Énumération de l’État msdrm</span><span class="sxs-lookup"><span data-stu-id="72445-105">MSDRM\_STATUS enumeration</span></span>

<span data-ttu-id="72445-106">Le type d’énumération d' **\_ État msdrm** définit des conditions d’État pour le sous-système DRM.</span><span class="sxs-lookup"><span data-stu-id="72445-106">The **MSDRM\_STATUS** enumeration type defines status conditions for the DRM subsystem.</span></span>

## <a name="syntax"></a><span data-ttu-id="72445-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72445-107">Syntax</span></span>


```C++
typedef enum MSDRM_STATUS { 
  DRM_ERROR                        = 0,
  DRM_INFORMATION                  = 1,
  DRM_BACKUPRESTORE_BEGIN          = 2,
  DRM_BACKUPRESTORE_END            = 3,
  DRM_BACKUPRESTORE_CONNECTING     = 4,
  DRM_BACKUPRESTORE_DISCONNECTING  = 5,
  DRM_ERROR_WITHURL                = 6,
  DRM_RESTRICTED_LICENSE           = 7,
  DRM_NEEDS_INDIVIDUALIZATION      = 8,
  DRM_PLAY_OPL_NOTIFICATION        = 9,
  DRM_COPY_OPL_NOTIFICATION        = 10,
  DRM_REFRESHCRL_COMPLETE          = 11
} ;
```



## <a name="constants"></a><span data-ttu-id="72445-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="72445-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="72445-109"><span id="DRM_ERROR"></span><span id="drm_error"></span>**\_erreur DRM**</span><span class="sxs-lookup"><span data-stu-id="72445-109"><span id="DRM_ERROR"></span><span id="drm_error"></span>**DRM\_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="72445-110">Spécifie qu’une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="72445-110">Specifies that an error has occurred.</span></span>

</dd> <dt>

<span data-ttu-id="72445-111"><span id="DRM_INFORMATION"></span><span id="drm_information"></span>**\_informations DRM**</span><span class="sxs-lookup"><span data-stu-id="72445-111"><span id="DRM_INFORMATION"></span><span id="drm_information"></span>**DRM\_INFORMATION**</span></span>
</dt> <dd>

<span data-ttu-id="72445-112">Spécifie qu’il existe des informations d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="72445-112">Specifies that there is additional status information.</span></span>

</dd> <dt>

<span data-ttu-id="72445-113"><span id="DRM_BACKUPRESTORE_BEGIN"></span><span id="drm_backuprestore_begin"></span>**début de la \_ BACKUPRESTORE DRM \_**</span><span class="sxs-lookup"><span data-stu-id="72445-113"><span id="DRM_BACKUPRESTORE_BEGIN"></span><span id="drm_backuprestore_begin"></span>**DRM\_BACKUPRESTORE\_BEGIN**</span></span>
</dt> <dd>

<span data-ttu-id="72445-114">Spécifie qu’une opération de sauvegarde ou de restauration de licence a commencé.</span><span class="sxs-lookup"><span data-stu-id="72445-114">Specifies that a license backup or restore operation has begun.</span></span>

</dd> <dt>

<span data-ttu-id="72445-115"><span id="DRM_BACKUPRESTORE_END"></span><span id="drm_backuprestore_end"></span>**\_fin de BACKUPRESTORE DRM \_**</span><span class="sxs-lookup"><span data-stu-id="72445-115"><span id="DRM_BACKUPRESTORE_END"></span><span id="drm_backuprestore_end"></span>**DRM\_BACKUPRESTORE\_END**</span></span>
</dt> <dd>

<span data-ttu-id="72445-116">Spécifie qu’une opération de sauvegarde ou de restauration de licence s’est terminée.</span><span class="sxs-lookup"><span data-stu-id="72445-116">Specifies that a license backup or restore operation has ended.</span></span>

</dd> <dt>

<span data-ttu-id="72445-117"><span id="DRM_BACKUPRESTORE_CONNECTING"></span><span id="drm_backuprestore_connecting"></span>**\_connexion DRM BACKUPRESTORE \_**</span><span class="sxs-lookup"><span data-stu-id="72445-117"><span id="DRM_BACKUPRESTORE_CONNECTING"></span><span id="drm_backuprestore_connecting"></span>**DRM\_BACKUPRESTORE\_CONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="72445-118">Spécifie qu’une opération de sauvegarde ou de restauration de la licence est en cours et que l’ordinateur client se connecte au serveur de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="72445-118">Specifies that a license backup or restore operation is in progress and that the client computer is connecting with the backup server.</span></span>

</dd> <dt>

<span data-ttu-id="72445-119"><span id="DRM_BACKUPRESTORE_DISCONNECTING"></span><span id="drm_backuprestore_disconnecting"></span>**déconnexion de DRM \_ BACKUPRESTORE \_**</span><span class="sxs-lookup"><span data-stu-id="72445-119"><span id="DRM_BACKUPRESTORE_DISCONNECTING"></span><span id="drm_backuprestore_disconnecting"></span>**DRM\_BACKUPRESTORE\_DISCONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="72445-120">Spécifie qu’une opération de sauvegarde ou de restauration de la licence est en cours et que l’ordinateur client se déconnecte du serveur de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="72445-120">Specifies that a license backup or restore operation is in progress and that the client computer is disconnecting from the backup server.</span></span>

</dd> <dt>

<span data-ttu-id="72445-121"><span id="DRM_ERROR_WITHURL"></span><span id="drm_error_withurl"></span>**\_erreur DRM \_ WITHURL**</span><span class="sxs-lookup"><span data-stu-id="72445-121"><span id="DRM_ERROR_WITHURL"></span><span id="drm_error_withurl"></span>**DRM\_ERROR\_WITHURL**</span></span>
</dt> <dd>

<span data-ttu-id="72445-122">Spécifie que l’opération DRM a rencontré une URL incorrecte.</span><span class="sxs-lookup"><span data-stu-id="72445-122">Specifies that the DRM operation has encountered a bad URL.</span></span>

</dd> <dt>

<span data-ttu-id="72445-123"><span id="DRM_RESTRICTED_LICENSE"></span><span id="drm_restricted_license"></span>**\_licence DRM restreinte \_**</span><span class="sxs-lookup"><span data-stu-id="72445-123"><span id="DRM_RESTRICTED_LICENSE"></span><span id="drm_restricted_license"></span>**DRM\_RESTRICTED\_LICENSE**</span></span>
</dt> <dd>

<span data-ttu-id="72445-124">Spécifie que l’opération DRM ne peut pas continuer, car aucune licence n’accordant le droit requis n’existe sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="72445-124">Specifies that the DRM operation cannot continue because no license granting the required right exists on the client computer.</span></span>

</dd> <dt>

<span data-ttu-id="72445-125"><span id="DRM_NEEDS_INDIVIDUALIZATION"></span><span id="drm_needs_individualization"></span>**DRM \_ a besoin d’une \_ individualisation**</span><span class="sxs-lookup"><span data-stu-id="72445-125"><span id="DRM_NEEDS_INDIVIDUALIZATION"></span><span id="drm_needs_individualization"></span>**DRM\_NEEDS\_INDIVIDUALIZATION**</span></span>
</dt> <dd>

<span data-ttu-id="72445-126">Spécifie que l’opération DRM ne peut pas continuer, car le sous-système DRM doit être individualisé.</span><span class="sxs-lookup"><span data-stu-id="72445-126">Specifies that the DRM operation cannot continue because the DRM subsystem needs to be individualized.</span></span>

</dd> <dt>

<span data-ttu-id="72445-127"><span id="DRM_PLAY_OPL_NOTIFICATION"></span><span id="drm_play_opl_notification"></span>**\_notification de lecture DRM \_ OPL \_**</span><span class="sxs-lookup"><span data-stu-id="72445-127"><span id="DRM_PLAY_OPL_NOTIFICATION"></span><span id="drm_play_opl_notification"></span>**DRM\_PLAY\_OPL\_NOTIFICATION**</span></span>
</dt> <dd>

<span data-ttu-id="72445-128">Spécifie qu’une opération de lecture ne peut pas être effectuée, car une exigence de niveau de protection de sortie n’a pas été satisfaite.</span><span class="sxs-lookup"><span data-stu-id="72445-128">Specifies that a playback operation cannot be completed because an output protection level requirement has not been met.</span></span>

</dd> <dt>

<span data-ttu-id="72445-129"><span id="DRM_COPY_OPL_NOTIFICATION"></span><span id="drm_copy_opl_notification"></span>**NOTIFICATION de OPL de la \_ copie DRM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="72445-129"><span id="DRM_COPY_OPL_NOTIFICATION"></span><span id="drm_copy_opl_notification"></span>**DRM\_COPY\_OPL\_NOTIFICATION**</span></span>
</dt> <dd>

<span data-ttu-id="72445-130">Spécifie qu’une opération de copie ne peut pas être effectuée, car une exigence de niveau de protection de sortie n’a pas été satisfaite.</span><span class="sxs-lookup"><span data-stu-id="72445-130">Specifies that a copy operation cannot be completed because an output protection level requirement has not been met.</span></span>

</dd> <dt>

<span data-ttu-id="72445-131"><span id="DRM_REFRESHCRL_COMPLETE"></span><span id="drm_refreshcrl_complete"></span>**\_REFRESHCRL DRM \_ terminé**</span><span class="sxs-lookup"><span data-stu-id="72445-131"><span id="DRM_REFRESHCRL_COMPLETE"></span><span id="drm_refreshcrl_complete"></span>**DRM\_REFRESHCRL\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="72445-132">Spécifie qu’un appel à [**IWMDRMSecurity ::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) a terminé l’actualisation d’une liste de révocation.</span><span class="sxs-lookup"><span data-stu-id="72445-132">Specifies that a call to [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) has completed refreshing a revocation list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72445-133">Notes</span><span class="sxs-lookup"><span data-stu-id="72445-133">Remarks</span></span>

<span data-ttu-id="72445-134">Aucun.</span><span class="sxs-lookup"><span data-stu-id="72445-134">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="72445-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72445-135">Requirements</span></span>



| <span data-ttu-id="72445-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72445-136">Requirement</span></span> | <span data-ttu-id="72445-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="72445-137">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="72445-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="72445-138">Header</span></span><br/> | <dl> <span data-ttu-id="72445-139"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="72445-139"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72445-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72445-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72445-141">**Types énumération**</span><span class="sxs-lookup"><span data-stu-id="72445-141">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





