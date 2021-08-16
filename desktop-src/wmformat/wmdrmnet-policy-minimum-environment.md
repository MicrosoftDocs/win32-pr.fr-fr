---
title: Structure WMDRMNET_POLICY_MINIMUM_ENVIRONMENT (wmdrmsdk. h)
description: la \_ \_ \_ structure d’environnement minimale de la stratégie WMDRMNET contient les exigences de sécurité minimales pour Windows DRM pour les périphériques réseau.
ms.assetid: b1bc9a8d-197e-45fe-a152-0b81add977eb
keywords:
- Structure WMDRMNET_POLICY_MINIMUM_ENVIRONMENT format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_MINIMUM_ENVIRONMENT
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26c11cf02d7cfcd2e3ab62c4e6b110e2c20b77cf6f79251a23f642b38d4df553
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118027460"
---
# <a name="wmdrmnet_policy_minimum_environment-structure"></a>\_Structure d' \_ \_ environnement minimale de la stratégie WMDRMNET

la structure d' **\_ \_ \_ environnement minimale de la stratégie WMDRMNET** contient les exigences de sécurité minimales pour Windows DRM pour les périphériques réseau.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct WMDRMNET_POLICY_MINIMUM_ENVIRONMENT {
  WORD  wMinimumSecurityLevel;
  DWORD dwMinimumAppRevocationListVersion;
  DWORD dwMinimumDeviceRevocationListVersion;
} ;
```



## <a name="members"></a>Membres

<dl> <dt>

**wMinimumSecurityLevel**
</dt> <dd>

Niveau de sécurité d’application minimal requis.

</dd> <dt>

**dwMinimumAppRevocationListVersion**
</dt> <dd>

Version minimale de la liste de révocation des certificats d’application requise.

</dd> <dt>

**dwMinimumDeviceRevocationListVersion**
</dt> <dd>

Configuration minimale requise pour la liste de révocation des certificats d’appareil.

</dd> </dl>

## <a name="remarks"></a>Notes

Aucun.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures**](drm-structures.md)
</dt> <dt>

[**\_stratégie WMDRMNET**](wmdrmnet-policy.md)
</dt> </dl>

 

 





