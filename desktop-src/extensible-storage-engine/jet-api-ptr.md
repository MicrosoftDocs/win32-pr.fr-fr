---
description: 'En savoir plus sur : JET_API_PTR'
title: JET_API_PTR
TOCTitle: JET_API_PTR
ms:assetid: 27b1eeec-1707-4edb-a4b2-2619190c21e7
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269209(v=EXCHG.10)
ms:contentKeyID: 32765512
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ddf50b5bb5e65ca60677f5578170b84f744016e9
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985302"
---
# <a name="jet_api_ptr"></a>JET_API_PTR


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_api_ptr"></a>JET_API_PTR

Le type de données **JET_API_PTR** contient un entier ou une valeur de pointeur.

```cpp
    #if defined(_WIN64)
        typedef unsigned __int64 JET_API_PTR;
    #elif !defined(__midl) && (defined(_X86_) || defined(_M_IX86)) && _MSC_VER >= 1300
        typedef __w64 unsigned long JET_API_PTR;
    #else
        typedef unsigned long JET_API_PTR;
    #endif
```

### <a name="data-types"></a>Types de données

JET_API_PTR

À l’instar d’un type de données **DWORD_PTR** , le type de données **JET_API_PTR** est défini sur 4 octets sur un ordinateur 32 bits et sur 8 octets sur un ordinateur 64 bits.

### <a name="remarks"></a>Remarques

Le type de données **JET_API_PTR** est utilisé pour définir les types de données suivants :

  - [JET_HANDLE](./jet-handle.md)

  - [JET_INSTANCE](./jet-instance.md)

  - [JET_SESID](./jet-sesid.md)

  - [JET_TABLEID](./jet-tableid.md)

  - [JET_LS](./jet-ls.md)

### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 

