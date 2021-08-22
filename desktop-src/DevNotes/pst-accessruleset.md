---
description: Identifie l’ensemble de règles d’accès pour les données de stockage protégées.
ms.assetid: 0eee34c2-b832-41b3-80f5-b03fdddf75cc
title: Structure PST_ACCESSRULESET (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSRULESET
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 9695af01c6f0ffb33fe20a112659444011ad9c18812b8d2fd885641635c6b4c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666975"
---
# <a name="pst_accessruleset-structure"></a>ACCESSRULESET PST ( \_ structure)

\[le Stockage protégé (Pstore) peut être utilisé dans Windows Server 2003 et Windows XP. elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Identifie l’ensemble de règles d’accès pour les données de stockage protégées.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD          cbSize;
  DWORD          cRules;
  PST_ACCESSRULE *rgRules;
} PST_ACCESSRULESET, *PPST_ACCESSRULESET;
```



## <a name="members"></a>Membres

<dl> <dt>

**cbSize**
</dt> <dd>

La taille de cette structure.

</dd> <dt>

**cRules**
</dt> <dd>

Nombre de règles dans le tableau **rgRules** .

</dd> <dt>

**rgRules**
</dt> <dd>

Pointeur vers un tableau de structures [**\_ ACCESSRULE PST**](pst-accessrule.md) .

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Pstore. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_ACCESSRULE PST**](pst-accessrule.md)
</dt> <dt>

[**CreateSubtype**](ipstore-createsubtype.md)
</dt> </dl>

 

 
