---
title: Structure WMDRMNET_POLICY_GLOBAL_REQUIREMENTS (wmdrmsdk. h)
description: la \_ \_ structure des exigences globales de la stratégie WMDRMNET \_ contient des exigences globales pour la gestion DRM des médias Windows pour les périphériques réseau.
ms.assetid: 140b3a6f-ccba-4735-b48a-2e990f5ec570
keywords:
- Structure WMDRMNET_POLICY_GLOBAL_REQUIREMENTS format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_GLOBAL_REQUIREMENTS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e2a8dc7be95638e171126eb4a55c50744ee3e5126d3e0b49eb8f229ec0257e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843970"
---
# <a name="wmdrmnet_policy_global_requirements-structure"></a>\_Structure des \_ exigences globales de la stratégie WMDRMNET \_

la structure des **\_ \_ \_ exigences globales de la stratégie WMDRMNET** contient des exigences globales pour la gestion DRM des médias Windows pour les périphériques réseau.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct WMDRMNET_POLICY_GLOBAL_REQUIREMENTS {
  WMDRMNET_POLICY_MINIMUM_ENVIRONMENT MinimumEnvironment;
} ;
```



## <a name="members"></a>Membres

<dl> <dt>

**MinimumEnvironment**
</dt> <dd>

[**WMDRMNET \_ structure \_ d' \_ environnement minimale**](wmdrmnet-policy-minimum-environment.md) de la stratégie contenant les exigences de sécurité minimales pour Windows DRM pour les périphériques réseau.

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

 

 





