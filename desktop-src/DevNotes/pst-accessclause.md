---
description: Contient des informations sur la clause d’accès pour le stockage protégé.
ms.assetid: 59634ada-4879-4ae7-b757-dfa6a88549af
title: Structure PST_ACCESSCLAUSE (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSCLAUSE
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: e5933b762ac19ac188e2d7253e86482caae968abd58ecb02087c32657d250216
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386179"
---
# <a name="pst_accessclause-structure"></a>ACCESSCLAUSE PST ( \_ structure)

\[le Stockage protégé (Pstore) peut être utilisé dans Windows Server 2003 et Windows XP. elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Contient des informations sur la clause d’accès pour le stockage protégé.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD                cbSize;
  PST_ACCESSCLAUSETYPE ClauseType;
  DWORD                cbClauseData;
  BYTE                 *pbClauseData;
} PST_ACCESSCLAUSE, *PPST_ACCESSCLAUSE;
```



## <a name="members"></a>Membres

<dl> <dt>

**cbSize**
</dt> <dd>

La taille de cette structure.

</dd> <dt>

**ClauseType**
</dt> <dd>

Type de données vers lequel pointe le membre **pbClauseData** . Pour plus d’informations, consultez [**types Pstore**](pstore-types.md).

</dd> <dt>

**cbClauseData**
</dt> <dd>

Taille des données vers lesquelles pointe le membre **pbClauseData** .

</dd> <dt>

**pbClauseData**
</dt> <dd>

Pointeur vers les données de la clause d’accès.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Pstore. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_ACCESSRULE PST**](pst-accessrule.md)
</dt> </dl>

 

 
