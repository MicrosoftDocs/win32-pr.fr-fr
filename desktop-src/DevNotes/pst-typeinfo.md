---
description: Décrit un type ou un sous-type.
ms.assetid: 4b6b77d9-54ea-4101-9c8b-e525f9aa3816
title: Structure PST_TYPEINFO (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_TYPEINFO
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: fc78d0570ff2e5cf66a9048d64143149564a51c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533188"
---
# <a name="pst_typeinfo-structure"></a>PST, \_ structure

\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP. Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Décrit un type ou un sous-type.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD  cbSize;
  LPWSTR szDisplayName;
} PST_TYPEINFO, *PPST_TYPEINFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**cbSize**
</dt> <dd>

La taille de cette structure.

</dd> <dt>

**szDisplayName**
</dt> <dd>

Pointeur vers une chaîne de caractères larges qui représente le nom complet du type.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Pstore. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CreateSubtype**](ipstore-createsubtype.md)
</dt> <dt>

[**CreateType**](ipstore-createtype.md)
</dt> <dt>

[**GetSubtypeInfo**](ipstore-getsubtypeinfo.md)
</dt> <dt>

[**GetTypeInfo**](ipstore-gettypeinfo.md)
</dt> </dl>

 

 
