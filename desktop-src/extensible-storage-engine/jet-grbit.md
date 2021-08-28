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
ms.openlocfilehash: 7aa3a0331244aa1f5dd07794204d5a94d57aeadb
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984172"
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


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)
