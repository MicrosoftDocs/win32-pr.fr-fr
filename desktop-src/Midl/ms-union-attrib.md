---
title: ms_union (attribut)
description: Le mot clé \ MS \_ Union \ est utilisé pour contrôler l’alignement du rapport de non-remise des unions non encapsulées.
ms.assetid: 20ac2985-4552-4224-b03b-07378a2c0cdf
keywords:
- ms_union MIDL de l’attribut
topic_type:
- apiref
api_name:
- ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7ad9b750027163aef806f5a66e51f87874a0ad2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093386"
---
# <a name="ms_union-attribute"></a>\_attribut ms Union

Le mot clé \[ **MS \_ Union** \] est utilisé pour contrôler l’alignement du rapport de non-remise des unions non encapsulées.

``` syntax
[
    ms_union,
    ...
]
interface interface-name 
{
    ...
}

[ms_union] procedure-type procedure-name(param-list);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom de l’interface* 
</dt> <dd>

Spécifie le nom de l’interface.

</dd> <dt>

*type de procédure* 
</dt> <dd>

Spécifie le type de retour de la procédure à laquelle l’attribut est appliqué.

</dd> <dt>

*nom de la procédure* 
</dt> <dd>

Spécifie le nom de la procédure.

</dd> <dt>

*Param-liste* 
</dt> <dd>

Spécifie la liste de paramètres de la procédure, qui peut être vide.

</dd> </dl>

## <a name="remarks"></a>Notes

N’utilisez jamais ce commutateur ou cet attribut avec les nouvelles interfaces. Il s’agit uniquement d’une fonctionnalité de compatibilité descendante. Le compilateur MIDL dans cette version de Microsoft RPC reflète le comportement du compilateur de l’IDL ETCD OSF pour les unions qui ne sont pas encapsulées. Toutefois, étant donné que les versions antérieures du compilateur MIDL ne l’ont pas fait, le commutateur d' [**\_ Union/ms.**](-ms-union.md) fournit la compatibilité avec les interfaces générées sur les versions précédentes du compilateur MIDL.

La fonctionnalité **MS \_ Union** peut être utilisée en tant qu’attribut d’interface IDL, en tant qu’attribut de type IDL ou en tant que commutateur de ligne de commande ( [**/ms. \_ Union**](-ms-union.md)).

## <a name="examples"></a>Exemples

``` syntax
[ms_union] long procedure (...);
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**/ms. \_ Union**](-ms-union.md)
</dt> </dl>

 

 




