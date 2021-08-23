---
title: out (attribut)
description: L’attribut \ out \ identifie les paramètres de pointeur retournés de la procédure appelée à la procédure appelante (du serveur au client).
ms.assetid: f92ef78a-321b-460e-a18a-b63a5e199ad0
keywords:
- MIDL, attribut de sortie
topic_type:
- apiref
api_name:
- out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32bdbd18c6412f943a124a62badb9c154fa9aeb64573919970ffc1dc4af17798
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066799"
---
# <a name="out-attribute"></a>out (attribut)

L' \[ attribut **out** \] identifie les paramètres de pointeur retournés de la procédure appelée à la procédure appelante (du serveur au client).

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ out [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*function-attribute-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs qui s’appliquent à la fonction. Les attributs de fonction valides sont \[ [**callback**](callback.md) \] , \[ [**local**](local.md), \] l’attribut de pointeur \[ [**ref**](ref.md) \] , \[ [**unique**](unique.md) \] ou \[ [**ptr**](ptr.md) \] ; et les attributs d’utilisation \[ [**chaîne**](string.md) \] , \[ [**Ignorer**](ignore.md) \] et \[ [**\_ handle de contexte**](context-handle.md) \] .

</dd> <dt>

*spécificateur de type* 
</dt> <dd>

Spécifie un type de [base \_](midl-base-types.md), un [**struct**](struct.md), une [**Union**](union.md)ou un type [**enum**](enum.md) ou un identificateur de type. Une spécification de stockage facultative peut précéder *le type-specifier*.

</dd> <dt>

*pointeur-déclarateur* 
</dt> <dd>

Spécifie zéro ou plusieurs déclarateurs de pointeur. Un déclarateur de pointeur est le même que le déclarateur de pointeur utilisé dans C ; elle est construite à partir de l' \* indicateur, de modificateurs tels que **Far** et de l’identificateur [**const**](const.md).

</dd> <dt>

*function-name* 
</dt> <dd>

Spécifie le nom de la procédure distante.

</dd> <dt>

*Parameter-attribute-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs appropriés pour un type de paramètre spécifié. Les attributs de paramètre avec l' \[  \] attribut out peuvent également prendre l’attribut directionnel \[  \] . les attributs de champ \[ [**\_ sont**](first-is.md) \] , \[ [**Last \_ is**](last-is.md), \] \[ [**Length \_ is**](length-is.md) \] , \[ [**Max \_ is**](max-is.md), \] \[ [**size \_ is**](size-is.md) \] et \[ [**\_ type de commutateur**](switch-type.md) \] ; le pointeur attribute \[ [**ref**](ref.md) \] , \[ [**unique**](unique.md) \] ou \[ [**ptr**](ptr.md) \] ; et les attributs d’utilisation \[ [**\_ handle de contexte**](context-handle.md) \] et \[ [**String**](string.md) \] . L’attribut d’utilisation \[ [**ignore**](ignore.md) \] ne peut pas être utilisé en tant qu’attribut de paramètre. Séparez plusieurs attributs par des virgules.

</dd> <dt>

*declarator* 
</dt> <dd>

Spécifie les déclarateurs standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau. Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**tableaux**](arrays-1.md), tableaux [et pointeurs](/windows/desktop/Rpc/arrays-and-pointers). Le déclarateur de paramètre dans le déclarateur de fonction, tel que le nom du paramètre, est facultatif.

</dd> </dl>

## <a name="remarks"></a>Remarques

L' \[ attribut **out** \] indique qu’un paramètre qui agit comme un pointeur et ses données associées en mémoire doit être repassé de la procédure appelée à la procédure d’appel.

L' \[ attribut **out** \] doit être un pointeur. Les compilateurs IDL DCE nécessitent la présence d’un Explicit \* comme déclarateur de pointeur dans la déclaration du paramètre. Microsoft IDL offre une extension qui supprime cette exigence et autorise un tableau ou un type de pointeur défini précédemment.

Un attribut associé, \[ [**dans**](in.md) \] , indique que le paramètre est passé de la procédure appelante à la procédure appelée. Les \[  \] attributs in et \[ **out** \] spécifient la direction dans laquelle les paramètres sont passés. Un paramètre peut être défini en tant que \[ **en** \] seule, en \[ **sortie** seule \] ou \[ **en** **sortie** \] .

Un \[ paramètre en **sortie** \] seule est supposé être non défini lorsque la procédure distante est appelée et que la mémoire de l’objet est allouée par le serveur. Étant donné que les curseurs/paramètres de niveau supérieur doivent toujours pointer vers un stockage valide, et ne peuvent donc pas avoir la **valeur null**, \[ **out** \] ne peut pas être appliqué aux \[ [](unique.md) \] pointeurs uniques ou \[ [**ptr**](ptr.md) de niveau supérieur \] . Les paramètres qui sont \[ **uniques** \] ou les \[  \] pointeurs PTR doivent être \[ [**dans**](in.md) \] ou \[ **dans**, paramètres de **sortie** \] .

## <a name="examples"></a>Exemples

``` syntax
HRESULT MyFunction([out] short * pcount);
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**tableaux**](arrays-1.md)
</dt> <dt>

[Types de base MIDL](midl-base-types.md)
</dt> <dt>

[**rappel**](callback.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**handle de contexte \_**](context-handle.md)
</dt> <dt>

[**variables**](enum.md)
</dt> <dt>

[**tout d’abord, \_**](first-is.md)
</dt> <dt>

[**tenir**](ignore.md)
</dt> <dt>

[**dans**](in.md)
</dt> <dt>

[**la dernière \_ est**](last-is.md)
</dt> <dt>

[**la longueur \_ est**](length-is.md)
</dt> <dt>

[**local**](local.md)
</dt> <dt>

[**le nombre maximal \_ est**](max-is.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**la taille \_ est**](size-is.md)
</dt> <dt>

[**chaîne**](string.md)
</dt> <dt>

[**modélis**](struct.md)
</dt> <dt>

[**type de commutateur \_**](switch-type.md)
</dt> <dt>

[**union**](union.md)
</dt> <dt>

[**unique**](unique.md)
</dt> </dl>

 

 