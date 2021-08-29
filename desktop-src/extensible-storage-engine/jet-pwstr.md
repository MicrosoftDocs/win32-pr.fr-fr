---
description: 'En savoir plus sur : JET_PWSTR'
title: JET_PWSTR
TOCTitle: JET_PWSTR
ms:assetid: 6575f0f0-d022-4e70-9f17-c1d884d9e226
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269271(v=EXCHG.10)
ms:contentKeyID: 32765573
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
ms.openlocfilehash: adfa30d90087113f14b684440c21d6246fdc1f64
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987842"
---
# <a name="jet_pwstr"></a>JET_PWSTR


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_pwstr"></a>JET_PWSTR

Le type de données **JET_PWSTR** contient une chaîne **Unicode** terminée par le caractère null (char \* ).

**Windows vista : JET_PWSTR** est introduite dans Windows vista.

```cpp
    typedef __nullterminated WCHAR * JET_PWSTR;
```

### <a name="data-types"></a>Types de données

JET_PWSTR

Chaîne Unicode terminée par un caractère null (char \* ).

### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows Server 2008.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 


