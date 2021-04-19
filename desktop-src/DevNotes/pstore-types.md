---
description: Types de données pour les méthodes de stockage protégées.
ms.assetid: 4d494326-6d0f-4a12-83a2-3c3dd3ca9c1b
title: Types PStore (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f1c93af4ae6756a6489b828c50bac505241bdd3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541121"
---
# <a name="pstore-types"></a>Types PStore

\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP. Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Types de données pour les méthodes de stockage protégées.


```C++
typedef DWORD PST_ACCESSMODE;
typedef DWORD PST_ACCESSCLAUSETYPE;
typedef DWORD PST_KEY;
```



<dl> <dt>

**\_ACCESSMODE PST**
</dt> <dd>

Définit le mode de lecture ou d’écriture de la règle d’accès.

</dd> <dt>

**\_ACCESSCLAUSETYPE PST**
</dt> <dd>

Définit le type de clause de la règle d’accès.

</dd> <dt>

**\_clé PST**
</dt> <dd>

Définit la clé pour l’élément stocké.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Pstore. h</dt> </dl> |



 

 
