---
description: Contient un tableau d’objets BLOB.
ms.assetid: e87f493b-f160-4316-b369-75d20c735213
title: Structure de BLOB_TABLE (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BLOB_TABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 32bacc925381f1c7ed30aa66247671b67e31b7e4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110382"
---
# <a name="blob_table-structure"></a>Structure de table d’objets BLOB \_

La structure de la **\_ table d’objets BLOB** contient un tableau d’objets BLOB.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD dwNumBlobs;
  HBLOB hBlobs[];
} BLOB_TABLE, *PBLOB_TABLE;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwNumBlobs**
</dt> <dd>

Indicateur que de nombreux objets BLOB suivent.

</dd> <dt>

**hBlobs**
</dt> <dd>

Handle vers le tableau d’objets BLOB.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




