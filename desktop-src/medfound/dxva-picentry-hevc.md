---
description: Spécifie une référence à une surface non compressée.
ms.assetid: 01F9C9F9-8EB4-49D5-91F0-89B4C40DDDC8
title: Structure DXVA_PicEntry_HEVC (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_PicEntry_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: a2c4856452d0f8010e8f97126b4e660557ea40ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515799"
---
# <a name="dxva_picentry_hevc-structure"></a>DXVA \_ PicEntry \_ HEVC, structure

Spécifie une référence à une surface non compressée.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _DXVA_PicEntry_HEVC {
  union {
    struct {
      UCHAR  Index7Bits  :7;
      UCHAR  AssociatedFlag   :1;
    };
    UCHAR  bPicEntry;
  };
} DXVA_PicEntry_HEVC, *PDXVA_PicEntry_HEVC;
```



## <a name="members"></a>Membres

<dl> <dt>

**Index7Bits**
</dt> <dd>

Index qui identifie une surface non compressée.

</dd> <dt>

**AssociatedFlag** 
</dt> <dd>

Indicateur 1 bit facultatif associé à la surface. La signification de l’indicateur dépend du contexte. Par exemple, il peut spécifier si le frame de référence est une référence à long terme ou une référence à long terme.

</dd> <dt>

**bPicEntry**
</dt> <dd>

Accède à la totalité des 8 bits de l’Union.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures de Media Foundation](media-foundation-structures.md)
</dt> </dl>

 

 




