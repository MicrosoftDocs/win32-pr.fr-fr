---
description: 'En savoir plus sur : JET_GRBIT'
title: JET_GRBIT
TOCTitle: JET_GRBIT
ms:assetid: b72548cf-3ca2-4ba5-b07a-35eb7e85ed2b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294066(v=EXCHG.10)
ms:contentKeyID: 32765681
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
ms.openlocfilehash: 2b54ed8a95d81c148b68727384dd76fba3d2dc8b1f9d6452c2105bc45f015646
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119362279"
---
# <a name="jet_grbit"></a>JET_GRBIT


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_grbit"></a>JET_GRBIT

Le type de données **JET_GRBIT** est un groupe de bits qui contiennent des constantes spécifiques aux fonctions et structures dans lesquelles il est utilisé.

```cpp
typedef unsigned long JET_GRBIT;
```

### <a name="data-types"></a>Types de données

JET_GRBIT

En général, les constantes utilisées comme valeurs pour ce type de données reflètent le nom de l’élément API dans lequel elles sont utilisées. Par exemple, toutes les constantes transmises à [JetRetrieveColumn](./jetretrievecolumn-function.md) commencent par « JET_bitRetrieve ». De même, toutes les constantes transmises à [JetSetColumn](./jetsetcolumn-function.md) commencent par « JET_bitSet ».

La valeur zéro provoque l’ignorance du paramètre.

### <a name="remarks"></a>Remarques

Pour plus d’informations, consultez la fonction ou la structure spécifique. Les options sont généralement transmises sous la forme d’un ensemble d’indicateurs qui peuvent être combinés.

### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Voir aussi

[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)
