---
title: Structure DRM_OUTPUT_PROTECTION_EX (wmdrmsdk. h)
description: La \_ structure de protection de sortie DRM \_ \_ ex contient des informations sur une technologie de protection de sortie. Cette structure étend \_ \_ la protection de la sortie DRM en ajoutant un numéro de version.
ms.assetid: eeebf5da-172b-4781-8c44-00504a6961bf
keywords:
- Structure DRM_OUTPUT_PROTECTION_EX format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- DRM_OUTPUT_PROTECTION_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeadbb845dc115b1faff858fe3a6ba0064eb425e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533455"
---
# <a name="drm_output_protection_ex-structure"></a>\_Protection de sortie DRM \_ \_ ex structure

La structure de **\_ protection de sortie DRM \_ \_ ex** contient des informations sur une technologie de protection de sortie. Cette structure étend **la \_ \_ protection de la sortie DRM** en ajoutant un numéro de version.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct DRM_OUTPUT_PROTECTION_EX {
  DWORD dwVersion;
  GUID  guidId;
  DWORD dwConfigData;
} ;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwVersion**
</dt> <dd>

Numéro de version.

</dd> <dt>

**Guidid ne**
</dt> <dd>

GUID identifiant la technologie de protection de sortie.

</dd> <dt>

**dwConfigData**
</dt> <dd>

Données de configuration pour la technologie.

</dd> </dl>

## <a name="remarks"></a>Notes

**DRM \_ La protection de sortie AUDIO par \_ \_ \_ exemple** et la **\_ \_ protection de sortie vidéo \_ \_ DRM** , par exemple, sont définies comme **\_ \_ protection de sortie DRM** dans les instructions **typedef** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_protection de sortie DRM \_**](drm-output-protection.md)
</dt> <dt>

[**Structures**](drm-structures.md)
</dt> </dl>

 

 





