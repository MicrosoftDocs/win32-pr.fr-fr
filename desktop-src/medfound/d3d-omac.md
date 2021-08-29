---
description: Contient un code d’authentification de message (MAC).
ms.assetid: be5515fd-1936-46b8-9fc8-8d1f87048c38
title: Structure D3D_OMAC (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3D_OMAC
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 05cf39bccc33eb1f993b0e86cfa89fc290832b422129441d99f028f3d826c3fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449542"
---
# <a name="d3d_omac-structure"></a>D3D \_ OMAC, structure

Contient un code d’authentification de message (MAC).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3D_OMAC {
  BYTE Omac[D3D_OMAC_SIZE];
} D3D_OMAC;
```



## <a name="members"></a>Membres

<dl> <dt>

**Omac**
</dt> <dd>

Tableau d’octets qui contient la valeur MAC de chiffrement du message.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures vidéo Direct3D](direct3d-video-structures.md)
</dt> </dl>

 

 




