---
title: Énumération WMDRMNET_POLICY_TYPE (wmdrmsdk. h)
description: Le \_ \_ type d’énumération de type de stratégie WMDRMNET répertorie les types de stratégies qui sont disponibles pour les opérations DRM Windows Media pour les périphériques réseau.
ms.assetid: 83e9e247-3bd8-4857-97b6-95b3cd5ad25c
keywords:
- Format Windows Media d’énumération WMDRMNET_POLICY_TYPE
- Format Windows Media d’énumération
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_TYPE
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 964a3e938caa312f02f21074f046f3cf88d72de6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539992"
---
# <a name="wmdrmnet_policy_type-enumeration"></a>\_Énumération des types de stratégie WMDRMNET \_

Le type d’énumération de **\_ \_ type de stratégie WMDRMNET** répertorie les types de stratégies qui sont disponibles pour les opérations DRM Windows Media pour les périphériques réseau.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum WMDRMNET_POLICY_TYPE { 
  WMDRMNET_POLICY_TYPE_UNDEFINED       = 0x0000,
  WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY  = 0x0001
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WMDRMNET_POLICY_TYPE_UNDEFINED"></span><span id="wmdrmnet_policy_type_undefined"></span>**\_type de stratégie WMDRMNET \_ \_ non défini**
</dt> <dd>

Les types de stratégie non définis ne sont pas pris en charge.

</dd> <dt>

<span id="WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY"></span><span id="wmdrmnet_policy_type_transcryptplay"></span>**WMDRMNET \_ type de stratégie \_ \_ TRANSCRYPTPLAY**
</dt> <dd>

La stratégie régit la possibilité de convertir le contenu protégé par Windows Media DRM en Windows Media DRM protégé pour les données des périphériques réseau et de le lire sur un appareil en réseau.

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
</dt> <dt>

[**\_stratégie WMDRMNET**](wmdrmnet-policy.md)
</dt> </dl>

 

 





