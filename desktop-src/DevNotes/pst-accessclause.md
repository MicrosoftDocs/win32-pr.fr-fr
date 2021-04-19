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
ms.openlocfilehash: 3536b92bf1d014090f124976b8f4a16e25beb444
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528781"
---
# <a name="pst_accessclause-structure"></a>ACCESSCLAUSE PST ( \_ structure)

\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP. Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

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

 

 
