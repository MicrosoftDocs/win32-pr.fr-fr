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
ms.openlocfilehash: e0615ad9c11657a47d9eaa87035207cb499634cd4ded6ae484d6f5d256c23e15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144342"
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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




