---
title: Énumération DRM_ATTR_DATATYPE (wmdrmsdk. h)
description: L' \_ \_ énumération de type de données de l’attribut DRM définit les types de données utilisés pour les propriétés et les attributs DRM.
ms.assetid: ccad16e2-475d-4cc7-b773-f17038d2754a
keywords:
- Format Windows Media d’énumération DRM_ATTR_DATATYPE
- Format Windows Media d’énumération
topic_type:
- apiref
api_name:
- DRM_ATTR_DATATYPE
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09f55c3d218aa86c33f699d4cb762e752a0bf4e1029e8ca42eee797aaf8ac721
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110529"
---
# <a name="drm_attr_datatype-enumeration"></a>\_Énumération de type de données de l’attr DRM \_

L’énumération de **\_ \_ type** de données de l’attribut DRM définit les types de données utilisés pour les propriétés et les attributs DRM.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum DRM_ATTR_DATATYPE { 
  DRM_TYPE_DWORD   = 0,
  DRM_TYPE_STRING  = 1,
  DRM_TYPE_BINARY  = 2,
  DRM_TYPE_BOOL    = 3,
  DRM_TYPE_QWORD   = 4,
  DRM_TYPE_WORD    = 5,
  DRM_TYPE_GUID    = 6
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="DRM_TYPE_DWORD"></span><span id="drm_type_dword"></span>**\_type DRM \_ DWORD**
</dt> <dd>

La propriété est une valeur **DWORD** sur 4 octets.

</dd> <dt>

<span id="DRM_TYPE_STRING"></span><span id="drm_type_string"></span>**\_chaîne de type DRM \_**
</dt> <dd>

La propriété est une chaîne Unicode terminée par le caractère null.

</dd> <dt>

<span id="DRM_TYPE_BINARY"></span><span id="drm_type_binary"></span>**\_binaire de type DRM \_**
</dt> <dd>

La propriété est un tableau d’octets.

</dd> <dt>

<span id="DRM_TYPE_BOOL"></span><span id="drm_type_bool"></span>**\_type DRM \_ bool**
</dt> <dd>

La propriété est une valeur booléenne sur 4 octets.

</dd> <dt>

<span id="DRM_TYPE_QWORD"></span><span id="drm_type_qword"></span>**\_type DRM \_ QWord**
</dt> <dd>

La propriété est une valeur **QWord** sur 8 octets.

</dd> <dt>

<span id="DRM_TYPE_WORD"></span><span id="drm_type_word"></span>**\_mot de type DRM \_**
</dt> <dd>

La propriété est une valeur de **mot** de 2 octets.

</dd> <dt>

<span id="DRM_TYPE_GUID"></span><span id="drm_type_guid"></span>**\_GUID du type DRM \_**
</dt> <dd>

La propriété est une valeur GUID de 128 bits (6 octets).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Types énumération**](drm-enumeration-types.md)
</dt> </dl>

 

 





