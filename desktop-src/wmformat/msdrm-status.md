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
# <a name="msdrm_status-enumeration"></a>\_Énumération de l’État msdrm

Le type d’énumération d' **\_ État msdrm** définit des conditions d’État pour le sous-système DRM.

## <a name="syntax"></a>Syntaxe


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="DRM_ERROR"></span><span id="drm_error"></span>**\_erreur DRM**
</dt> <dd>

Spécifie qu’une erreur s’est produite.

</dd> <dt>

<span id="DRM_INFORMATION"></span><span id="drm_information"></span>**\_informations DRM**
</dt> <dd>

Spécifie qu’il existe des informations d’État supplémentaires.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_BEGIN"></span><span id="drm_backuprestore_begin"></span>**début de la \_ BACKUPRESTORE DRM \_**
</dt> <dd>

Spécifie qu’une opération de sauvegarde ou de restauration de licence a commencé.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_END"></span><span id="drm_backuprestore_end"></span>**\_fin de BACKUPRESTORE DRM \_**
</dt> <dd>

Spécifie qu’une opération de sauvegarde ou de restauration de licence s’est terminée.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_CONNECTING"></span><span id="drm_backuprestore_connecting"></span>**\_connexion DRM BACKUPRESTORE \_**
</dt> <dd>

Spécifie qu’une opération de sauvegarde ou de restauration de la licence est en cours et que l’ordinateur client se connecte au serveur de sauvegarde.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_DISCONNECTING"></span><span id="drm_backuprestore_disconnecting"></span>**déconnexion de DRM \_ BACKUPRESTORE \_**
</dt> <dd>

Spécifie qu’une opération de sauvegarde ou de restauration de la licence est en cours et que l’ordinateur client se déconnecte du serveur de sauvegarde.

</dd> <dt>

<span id="DRM_ERROR_WITHURL"></span><span id="drm_error_withurl"></span>**\_erreur DRM \_ WITHURL**
</dt> <dd>

Spécifie que l’opération DRM a rencontré une URL incorrecte.

</dd> <dt>

<span id="DRM_RESTRICTED_LICENSE"></span><span id="drm_restricted_license"></span>**\_licence DRM restreinte \_**
</dt> <dd>

Spécifie que l’opération DRM ne peut pas continuer, car aucune licence n’accordant le droit requis n’existe sur l’ordinateur client.

</dd> <dt>

<span id="DRM_NEEDS_INDIVIDUALIZATION"></span><span id="drm_needs_individualization"></span>**DRM \_ a besoin d’une \_ individualisation**
</dt> <dd>

Spécifie que l’opération DRM ne peut pas continuer, car le sous-système DRM doit être individualisé.

</dd> <dt>

<span id="DRM_PLAY_OPL_NOTIFICATION"></span><span id="drm_play_opl_notification"></span>**\_notification de lecture DRM \_ OPL \_**
</dt> <dd>

Spécifie qu’une opération de lecture ne peut pas être effectuée, car une exigence de niveau de protection de sortie n’a pas été satisfaite.

</dd> <dt>

<span id="DRM_COPY_OPL_NOTIFICATION"></span><span id="drm_copy_opl_notification"></span>**NOTIFICATION de OPL de la \_ copie DRM \_ \_**
</dt> <dd>

Spécifie qu’une opération de copie ne peut pas être effectuée, car une exigence de niveau de protection de sortie n’a pas été satisfaite.

</dd> <dt>

<span id="DRM_REFRESHCRL_COMPLETE"></span><span id="drm_refreshcrl_complete"></span>**\_REFRESHCRL DRM \_ terminé**
</dt> <dd>

Spécifie qu’un appel à [**IWMDRMSecurity ::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) a terminé l’actualisation d’une liste de révocation.

</dd> </dl>

## <a name="remarks"></a>Notes

Aucun.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Types énumération**](drm-enumeration-types.md)
</dt> </dl>

 

 





