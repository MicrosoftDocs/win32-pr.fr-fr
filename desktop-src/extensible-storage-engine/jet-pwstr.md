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
ms.openlocfilehash: 536ef3bba465f6d152e3483436c1dc1e82277339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518806"
---
# <a name="jet_pwstr"></a>JET_PWSTR


_**S’applique à :** Windows | Serveur Windows_

## <a name="jet_pwstr"></a>JET_PWSTR

Le type de données **JET_PWSTR** contient une chaîne **Unicode** terminée par le caractère null (char \* ).

**Windows Vista : JET_PWSTR** est introduite dans Windows Vista.

```cpp
    typedef __nullterminated WCHAR * JET_PWSTR;
```

### <a name="data-types"></a>Types de données

JET_PWSTR

Chaîne Unicode terminée par un caractère null (char \* ).

### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Nécessite Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
</tbody>
</table>

