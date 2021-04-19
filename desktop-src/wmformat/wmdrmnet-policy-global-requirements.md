---
title: Structure WMDRMNET_POLICY_GLOBAL_REQUIREMENTS (wmdrmsdk. h)
description: La \_ structure des \_ exigences globales de la stratégie WMDRMNET \_ contient des exigences globales pour Windows Media DRM pour les périphériques réseau.
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
ms.openlocfilehash: 0ccf13c881c9696d970a00ac902f3f8d08f13c58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542243"
---
# <a name="wmdrmnet_policy_global_requirements-structure"></a>\_Structure des \_ exigences globales de la stratégie WMDRMNET \_

La structure des **\_ \_ \_ exigences globales de la stratégie WMDRMNET** contient des exigences globales pour Windows Media DRM pour les périphériques réseau.

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

[**WMDRMNET \_ Structure \_ d' \_ environnement minimale**](wmdrmnet-policy-minimum-environment.md) de la stratégie contenant les exigences de sécurité minimales pour Windows Media DRM pour les périphériques réseau.

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

 

 





