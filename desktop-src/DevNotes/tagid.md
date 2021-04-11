---
description: Contient l’index d’une entrée et ses informations sur les BALISes dans une base de données de shims.
ms.assetid: 2ff58e01-cc47-4612-a3bc-a87ccb343bd2
title: TAGID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e7d8b8a25633d3505936d105b0eef7ed38746ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950501"
---
# <a name="tagid"></a>TAGID

Contient l’index d’une entrée et ses informations sur les BALISes dans une base de données de shims.


```C++
typedef DWORD TAGID;
```



## <a name="remarks"></a>Notes

Un **TagId** est spécifique à une base de données. Il peut s’agir d’une valeur entière qui représente l’index ou de l’une des valeurs suivantes :

<dl> <dt>

<span id="TAGID_NULL__0_"></span><span id="tagid_null__0_"></span>TAGID \_ null (0)
</dt> <dd>

Le **TagId** n’existe pas. Cette valeur est retournée par une fonction lorsqu’elle ne peut pas retourner un **TagId** valide.

</dd> <dt>

<span id="TAGID_ROOT__0_"></span><span id="tagid_root__0_"></span>\_Racine TagId (0)
</dt> <dd>

Indique une BALIse de liste racine qui peut être utilisée comme parent pour obtenir un **TagId** enfant.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence**](tag.md)
</dt> <dt>

[Types de BALISes](tag-types.md)
</dt> <dt>

[**TAGREF**](tagref.md)
</dt> </dl>

 

 




