---
description: La structure DATATYPEs \_ info \_ 1 contient des informations sur le type de données utilisé pour enregistrer un travail d’impression.
ms.assetid: 6169006c-12d4-4608-865c-732f04107f9f
title: Structure DATATYPES_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DATATYPES_INFO_1
- _DATATYPES_INFO_1A
- _DATATYPES_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 05defe3d8cc6cd66b15b2cacdd3d3d1d56c348e4946a43700278f100ea17da5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119719669"
---
# <a name="datatypes_info_1-structure"></a>Structure des informations de type de données \_ \_ 1

La structure **DataTypes \_ info \_ 1** contient des informations sur le type de données utilisé pour enregistrer un travail d’impression.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _DATATYPES_INFO_1 {
  LPTSTR pName;
} DATATYPES_INFO_1, *PDATATYPES_INFO_1;
```



## <a name="members"></a>Membres

<dl> <dt>

**pName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui identifie le type de données utilisé pour enregistrer un travail d’impression.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ DataTypes \_ info \_ 1s** (Unicode) et **\_ DataTypes \_ info \_ 1a** (ANSI)<br/>                       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md)
</dt> </dl>

 

 




