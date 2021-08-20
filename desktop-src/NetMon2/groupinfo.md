---
description: Associe un nom de groupe et son descripteur.
ms.assetid: 76f3fe37-cf85-42ab-8f9e-3ab2c6053dcd
title: GROUPINFO, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GROUPINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 333584e0ecc7a7ec9f5606891ee729eb7d925a01ea190960ff4444c1f7b8ae82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117981654"
---
# <a name="groupinfo-structure"></a>GROUPINFO, structure

La structure **GROUPINFO** associe un nom de groupe et son descripteur.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  char   szGroupName[EXPERTGROUPNAMELENGTH+1];
  HGROUP hGroup;
} GROUPINFO, *PGROUPINFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**szGroupName**
</dt> <dd>

Valeur incrémentée d’un tableau dans la structure **GroupName** .

</dd> <dt>

**hGroup**
</dt> <dd>

Handle vers un groupe.

</dd> </dl>

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




