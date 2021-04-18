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
ms.openlocfilehash: 21c710b21c31147f7208ddd1637426aeafb60234
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515952"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures vidéo Direct3D](direct3d-video-structures.md)
</dt> </dl>

 

 




