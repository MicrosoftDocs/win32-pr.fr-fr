---
title: Structure WMDRMNET_POLICY (wmdrmsdk. h)
description: La structure de la \_ stratégie WMDRMNET contient la stratégie à utiliser pour les opérations DRM Windows Media pour les périphériques réseau.
ms.assetid: 11eaaeb2-3470-4f58-ae1c-53ee0f60bdce
keywords:
- Structure WMDRMNET_POLICY format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574e37a8c5ee7f68291012b86cda3a89e25949ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540941"
---
# <a name="wmdrmnet_policy-structure"></a>Structure de la \_ stratégie WMDRMNET

La structure de la **\_ stratégie WMDRMNET** contient la stratégie à utiliser pour les opérations DRM Windows Media pour les périphériques réseau.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct WMDRMNET_POLICY {
  WMDRMNET_POLICY_TYPE ePolicyType;
  BYTE                 *pbPolicy;
} ;
```



## <a name="members"></a>Membres

<dl> <dt>

**ePolicyType**
</dt> <dd>

Membre de l’énumération de [**\_ \_ type de stratégie WMDRMNET**](wmdrmnet-policy-type.md) qui spécifie le type de stratégie.

</dd> <dt>

**pbPolicy**
</dt> <dd>

Mémoire tampon contenant la stratégie. Le seul type de stratégie actuellement pris en charge est le **\_ type de stratégie WMDRMNET \_ \_ TRANSCRYPTPLAY**. Ce membre est un pointeur vers une structure de **\_ \_ TRANSCRYPTPLAY de stratégie WMDRMNET** .

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure est utilisée en tant que paramètre pour la méthode [**IWMDRMNetTransmitter :: GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures**](drm-structures.md)
</dt> <dt>

[**\_ \_ exigences globales de la stratégie WMDRMNET \_**](wmdrmnet-policy-global-requirements.md)
</dt> <dt>

[**\_ \_ environnement minimal de la stratégie WMDRMNET \_**](wmdrmnet-policy-minimum-environment.md)
</dt> <dt>

[**\_stratégie WMDRMNET \_ TRANSCRYPTPLAY**](wmdrmnet-policy-transcryptplay.md)
</dt> <dt>

[**\_type de stratégie WMDRMNET \_**](wmdrmnet-policy-type.md)
</dt> </dl>

 

 





