---
description: Décrit une règle d’accès aux éléments stockés dans le stockage protégé.
ms.assetid: 22aebac3-46e9-4c66-bfaf-e82cf9d494cb
title: Structure PST_ACCESSRULE (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSRULE
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 26b4df38c5e5599c13cc52a75c58ea019d786eaa971c8ac3a67a7a8c15651075
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667055"
---
# <a name="pst_accessrule-structure"></a>ACCESSRULE PST ( \_ structure)

\[le Stockage protégé (Pstore) peut être utilisé dans Windows Server 2003 et Windows XP. elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Décrit une règle d’accès aux éléments stockés dans le stockage protégé.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD            cbSize;
  PST_ACCESSMODE   AccessModeFlags;
  DWORD            cClauses;
  PST_ACCESSCLAUSE *rgClauses;
} PST_ACCESSRULE, *PPST_ACCESSRULE;
```



## <a name="members"></a>Membres

<dl> <dt>

**cbSize**
</dt> <dd>

La taille de cette structure.

</dd> <dt>

**AccessModeFlags**
</dt> <dd>

Modes d’accès auxquels un ensemble spécifié de clauses d’accès appartient.



| Valeur                                                                                                                                                                                                         | Signification                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <dt>**Fichier PST \_ LIRE**</dt> <dt>0x0001</dt> </dl>    | Mode d’accès en lecture.<br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <dt>**Fichier PST \_ ÉCRIRE**</dt> <dt>0x0002</dt> </dl> | Mode d’accès en écriture.<br/> |



 

</dd> <dt>

**cClauses**
</dt> <dd>

Nombre de structures dans le tableau **rgClauses** .

</dd> <dt>

**rgClauses**
</dt> <dd>

Pointeur vers un tableau de structures [**\_ ACCESSCLAUSE PST**](pst-accessclause.md) .

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Pstore. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_ACCESSCLAUSE PST**](pst-accessclause.md)
</dt> <dt>

[**\_ACCESSRULESET PST**](pst-accessruleset.md)
</dt> </dl>

 

 
