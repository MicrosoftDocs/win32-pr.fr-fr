---
description: 'TAGREF : contient l’index d’une entrée et ses informations de BALIse dans une base de données de shims.'
ms.assetid: e7d83dca-13a5-4396-b50b-0d068209c03c
title: TAGREF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34e27a60847630e7bbd8e07ccf005dfd7b474d7a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096627"
---
# <a name="tagref"></a>TAGREF

Contient l’index d’une entrée et ses informations sur les BALISes dans une base de données de shims.


```C++
typedef DWORD TAGREF;
```



## <a name="remarks"></a>Notes 

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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



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

 

 




