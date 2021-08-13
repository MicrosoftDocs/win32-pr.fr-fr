---
title: Structure WINBIO_REGISTERED_FORMAT ( \_ types WINBIO. h)
description: Spécifie un format de données inscrit comme une paire propriétaire/format.
ms.assetid: a178840e-81cc-4dd3-9d80-a181fa7fa888
keywords:
- API de Windows Biometric Framework de structure de WINBIO_REGISTERED_FORMAT
- API du pointeur de structure PWINBIO_REGISTERED_FORMAT Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_REGISTERED_FORMAT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fcf871f3fc5f258de22e033e8a388968ab58c1a35e19829bf3d02a97ca60c53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909367"
---
# <a name="winbio_registered_format-structure"></a>\_Structure de format inscrite WINBIO \_

La structure de **\_ \_ format inscrite WINBIO** spécifie un format de données inscrit comme une paire propriétaire/format.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WINBIO_REGISTERED_FORMAT {
  USHORT Owner;
  USHORT Type;
} WINBIO_REGISTERED_FORMAT, *PWINBIO_REGISTERED_FORMAT;
```



## <a name="members"></a>Membres

<dl> <dt>

**Propriétaire**
</dt> <dd>

Valeur propriétaire assignée à IBIA (International Biometric Industry Association).

</dd> <dt>

**Type**
</dt> <dd>

Format assigné par le propriétaire.

</dd> </dl>

## <a name="remarks"></a>Remarques

étant donné que Windows prend actuellement en charge uniquement les lecteurs d’empreintes digitales, les valeurs suivantes doivent être utilisées dans la structure de **\_ \_ FORMAT inscrit WINBIO** .



| Constante                                    | Signification                                                                                                               |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| \_Propriétaire du \_ FORMAT ANSI 381 \_ \_ WINBIO<br/> | InterNational Committee for Information Technology Standards (INCITS) Technical Committee M1 (biométrique).<br/> |
| \_Type de \_ FORMAT ANSI 381 \_ \_ WINBIO<br/>  | Format d’échange de données basé sur l’image Finger ANSI INCITS 381.<br/>                                                |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (include WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’application cliente](client-application-structures.md)
</dt> <dt>

[**\_ \_ Constantes de FORMAT ANSI 381 WINBIO \_**](winbio-ansi-381-format-constants.md)
</dt> <dt>

[**WINBIO \_ BDB \_ ANSI \_ 381 \_ en-tête**](winbio-bdb-ansi-381-header.md)
</dt> <dt>

[**\_ \_ en-tête Bir WINBIO**](winbio-bir-header.md)
</dt> </dl>

 

 





