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
# <a name="drm_individualization_status-enumeration-wmdrmsdkh"></a>Énumération DRM_INDIVIDUALIZATION_STATUS (wmdrmsdk. h)

Le type d’énumération de l’état de l' **\_ \_ individualisation DRM** définit les États valides pour l’individualisation DRM.

## <a name="syntax"></a>Syntaxe


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**INDI \_ non défini**
</dt> <dd>

Cette valeur est réservée à une utilisation ultérieure.

</dd> <dt>

<span id="INDI_BEGIN"></span><span id="indi_begin"></span>**INDI \_ Begin**
</dt> <dd>

Indique le début du processus d’individualisation.

</dd> <dt>

<span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**INDI \_ réussie**
</dt> <dd>

Indique que le processus d’individualisation est terminé.

</dd> <dt>

<span id="INDI_FAIL"></span><span id="indi_fail"></span>**échec de INDI \_**
</dt> <dd>

Indique que le processus d’individualisation a échoué.

</dd> <dt>

<span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**INDI \_ Annuler**
</dt> <dd>

Indique que le processus d’individualisation a été annulé par l’application.

</dd> <dt>

<span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**Téléchargement de INDI \_**
</dt> <dd>

Indique que la mise à niveau de sécurité est en cours de téléchargement.

</dd> <dt>

<span id="INDI_INSTALL"></span><span id="indi_install"></span>**installation de INDI \_**
</dt> <dd>

Indique que la mise à niveau de sécurité est en cours d’installation.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette énumération est utilisée par la structure d' [**\_ \_ État**](drmwm-individualize-status.md) de l’énumération WM.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Types énumération**](drm-enumeration-types.md)
</dt> </dl>

 

 





