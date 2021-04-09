---
description: Identificateur de l’index à accéder dans une base de données.
ms.assetid: 559e73bf-91c2-4dbf-a667-e5c0431aaffa
title: INDEXID contient
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b6ef6b79dd19183f575930e9793a6ab2f1f5cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111138"
---
# <a name="indexid"></a>INDEXID contient

Identificateur de l’index à accéder dans une base de données.


```C++
typedef DWORD INDEXID;
```



## <a name="remarks"></a>Notes

Un **IndexID contient** peut être une valeur entière qui représente l’index ou la valeur suivante :

<dl> <dt>

<span id="INDEXID_NULL___INDEXID_-1_"></span><span id="indexid_null___indexid_-1_"></span>INDEXID contient \_ null ((IndexID contient)-1)
</dt> <dd>

**IndexID contient** non valide.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbDeclareIndex**](sdbdeclareindex.md)
</dt> <dt>

[**SdbStartIndexing**](sdbstartindexing.md)
</dt> <dt>

[**SdbStopIndexing**](sdbstopindexing.md)
</dt> </dl>

 

 




