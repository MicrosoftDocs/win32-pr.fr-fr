---
description: 'TAGREF : contient l’index d’une entrée et ses informations de BALIse dans une base de données de shims.'
ms.assetid: e7d83dca-13a5-4396-b50b-0d068209c03c
title: TAGREF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bf5a9de8da025e8278ab0bca7ccbe16d70d16b782591181f6ce6ce74a010a39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075774"
---
# <a name="tagref"></a>TAGREF

Contient l’index d’une entrée et ses informations sur les BALISes dans une base de données de shims.


```C++
typedef DWORD TAGREF;
```



## <a name="remarks"></a>Remarques

Un **TAGREF** est spécifique à une base de données de shims et valide sur plusieurs bases de données. Il peut s’agir d’une valeur entière qui représente l’index ou de l’une des valeurs suivantes :

<dl> <dt>

<span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF \_ null (0)
</dt> <dd>

Le **TAGREF** n’existe pas. Cette valeur est retournée par une fonction lorsqu’elle ne peut pas retourner un **TAGREF** valide.

</dd> <dt>

<span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>\_Racine TAGREF (0)
</dt> <dd>

Indique une BALIse de liste racine qui peut être utilisée comme parent pour obtenir un **TAGREF** enfant.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbTagRefToTagID**](sdbtagreftotagid.md)
</dt> <dt>

[**Référence**](tag.md)
</dt> <dt>

[Types de BALISes](tag-types.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> </dl>

 

 




