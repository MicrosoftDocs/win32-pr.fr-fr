---
description: 'En savoir plus sur : JET_PSTR'
title: JET_PSTR
TOCTitle: JET_PSTR
ms:assetid: acb1143f-a5ee-4088-9f05-cc2aeef23442
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294056(v=EXCHG.10)
ms:contentKeyID: 32765667
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
ms.openlocfilehash: c791b7e8ff070338f6c23b3b3f126e14aab38c4039faa8e9e2e16fd64a4d7080
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120093489"
---
# <a name="jet_pstr"></a>JET_PSTR


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_pstr"></a>JET_PSTR

Le type de données JET_PSTR contient une chaîne ASCII terminée par le caractère null (char \* ).

**Windows vista : JET_PSTR** est introduite dans Windows vista.

```cpp
    typedef __nullterminated char *  JET_PSTR;
```

### <a name="data-types"></a>Types de données

JET_PSTR

Chaîne ASCII terminée par un caractère null (char \* ).

### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>requiert Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>requiert Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
</tbody>
</table>

