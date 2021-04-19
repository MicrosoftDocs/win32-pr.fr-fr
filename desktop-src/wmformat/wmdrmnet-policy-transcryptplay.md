---
title: Structure WMDRMNET_POLICY_TRANSCRYPTPLAY (wmdrmsdk. h)
description: La \_ structure TRANSCRYPTPLAY de la stratégie WMDRMNET \_ contient les informations de stratégie pour la diffusion de contenu à l’aide de Windows Media DRM pour les périphériques réseau.
ms.assetid: 95671c58-a593-40bb-856e-28ad1cba340e
keywords:
- Structure WMDRMNET_POLICY_TRANSCRYPTPLAY format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_TRANSCRYPTPLAY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0681251428b87b323c9ad3e73277ec8cdd2b95f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528393"
---
# <a name="wmdrmnet_policy_transcryptplay-structure"></a>\_ \_ Structure TRANSCRYPTPLAY de la stratégie WMDRMNET

La **structure \_ \_ TRANSCRYPTPLAY de la stratégie WMDRMNET** contient les informations de stratégie pour la diffusion de contenu à l’aide de Windows Media DRM pour les périphériques réseau.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct WMDRMNET_POLICY_TRANSCRYPTPLAY {
  WMDRMNET_POLICY_GLOBAL_REQUIREMENTS globals;
  WMDRMNET_POLICY_PLAY_OPL            playOPLs;
} ;
```



## <a name="members"></a>Membres

<dl> <dt>

**Globals**
</dt> <dd>

Structure de stratégie globale.

</dd> <dt>

**playOPLs**
</dt> <dd>

Niveaux de protection de sortie pour la lecture. **WMDRMNET \_ La \_ lecture \_ de la stratégie OPL** est un type défini comme [**DRM \_ Play \_ OPL \_ ex**](drm-play-opl-ex.md).

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

 

 





