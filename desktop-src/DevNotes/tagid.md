---
description: Contient l’index d’une entrée et ses informations sur les BALISes dans une base de données de shims.
ms.assetid: 2ff58e01-cc47-4612-a3bc-a87ccb343bd2
title: TAGID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4c65183170c7304bf05a670b1eadb3a5953d6f33b1f6415210f12db8898760
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075782"
---
# <a name="tagid"></a>TAGID

Contient l’index d’une entrée et ses informations sur les BALISes dans une base de données de shims.


```C++
typedef DWORD TAGID;
```



## <a name="remarks"></a>Remarques

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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence**](tag.md)
</dt> <dt>

[Types de BALISes](tag-types.md)
</dt> <dt>

[**TAGREF**](tagref.md)
</dt> </dl>

 

 




