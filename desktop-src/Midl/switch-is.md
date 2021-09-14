---
title: switch_is (attribut)
description: L’attribut \ Switch \_ est \ spécifie l’expression ou l’identificateur agissant comme le discriminante d’Union qui sélectionne le membre Union.
ms.assetid: 93552bdf-6a14-47ce-877e-32ed976bb895
keywords:
- switch_is MIDL de l’attribut
topic_type:
- apiref
api_name:
- switch_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c52661c4fa1ebce57011f4424901dd1ec18250f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093158"
---
# <a name="switch_is-attribute"></a>le commutateur \_ est un attribut

L’attribut **\[ Switch \_ is \]** spécifie l’expression ou l’identificateur agissant en tant que discriminante d’Union qui sélectionne le membre Union.

``` syntax
typedef struct [[ struct-tag ]] 
{
    [ switch_is(limited-expr) [[ , field-attr-list ]] ] union-type-specifier declarator;
    ...
}

[[ [function-attribute-list] ]] type-specifier [[pointer-declarator]] function-name(
    [ switch_is(limited-expr) [[ , param-attr-list ]] ] union-type [[declarator]]
    , ...);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*struct-tag* 
</dt> <dd>

Spécifie une balise facultative pour une structure.

</dd> <dt>

*Limited-expr* 
</dt> <dd>

Spécifie une expression de langage C prise en charge par MIDL. Presque toutes les expressions en langage C sont prises en charge. Le compilateur MIDL prend en charge les expressions conditionnelles, les expressions logiques, les expressions relationnelles et les expressions arithmétiques. MIDL n’autorise pas les appels de fonction dans les expressions et n’autorise pas les opérateurs de pré-et post-incrémentation et de prédécrémentation.

</dd> <dt>

*Field-attr-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs de champ qui s’appliquent à un membre Union. Les attributs de champ valides sont **\[** [**First \_**](first-is.md)is, **\]** **\[** [**Last \_ is**](last-is.md), **\]** **\[** [**Length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ is**](size-is.md) **\]** ; the usage Attributes **\[** [**String**](string.md) **\]** , **\[** [**ignore**](ignore.md) **\]** et **\[** [**Context \_ handle**](context-handle.md) **\]** ; The pointer **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** ; et pour les membres qui sont eux-mêmes unions, le **\[** [**\_ type de commutateur**](switch-type.md)d’attribut Union **\]** . Séparez plusieurs attributs de champ par des virgules.

</dd> <dt>

*type d’Union* 
</dt> <dd>

Spécifie l’identificateur de type d' [**Union**](union.md) . Une spécification de stockage facultative peut précéder *le type-specifier*.

</dd> <dt>

*déclarateur et déclarateur-liste* 
</dt> <dd>

Spécifie un déclarateur C standard, tel qu’un identificateur, un déclarateur de pointeur et un déclarateur de tableau. (Les déclarateurs de fonction et les déclarations de champ de bits ne sont pas autorisés dans les unions transmises dans les appels de procédure distante. Ces déclarateurs sont autorisés dans les unions qui ne sont pas transmises.) Séparez plusieurs déclarateurs par des virgules.

</dd> <dt>

*function-attribute-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs qui s’appliquent à la fonction. Les attributs de fonction valides sont **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md) **\]** , l’attribut de pointeur **\[ \] ref**, **\[ unique \]** ou **\[ ptr \]**; et les attributs d’utilisation **\[ chaîne \]**, **\[ Ignorer \]** et **\[ \_ \] handle de contexte**.

</dd> <dt>

*spécificateur de type* 
</dt> <dd>

Spécifie un [type de base](midl-base-types.md), un [**struct**](struct.md), une [**Union**](union.md), un type [**enum**](enum.md) ou un identificateur de type. Une spécification de stockage facultative peut précéder *le type-specifier*.

</dd> <dt>

*pointeur-déclarateur* 
</dt> <dd>

Spécifie zéro ou plusieurs déclarateurs de pointeur. Un déclarateur de pointeur est le même que le déclarateur de pointeur utilisé dans C ; elle est construite à partir de l' \* indicateur, de modificateurs tels que **Far** et de l’identificateur [**const**](const.md).

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Spécifie le nom de la procédure distante.

</dd> <dt>

*Param-attr-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs appropriés pour le type de paramètre spécifié. Les attributs de paramètres peuvent accepter et **\[ \] sortir** les attributs directionnels, les attributs **\[ \] de** **\[ \_ \]** **\[ \]** **\[ \_ \]** **\[ \_ \]** **\[ \]** **\[ \]** **\[ \_ \]** champ en **\[ premier \_ \]**,, le nom, la longueur, la valeur maximale, la taille et le **\[ \_ type \] de commutateur**, l’attribut de pointeur **\[ Ref \]**, unique ou PTR ; et le **\[ \_ handle \] de contexte** et la chaîne des attributs d’utilisation. L’attribut d’utilisation **\[ ignore \]** ne peut pas être utilisé en tant qu’attribut de paramètre. Séparez plusieurs attributs par des virgules.

</dd> <dt>

*type d’Union* 
</dt> <dd>

Identifie le spécificateur de type d' [**Union**](union.md) .

</dd> </dl>

## <a name="remarks"></a>Notes

Le discriminante associé au **\[ commutateur \_ est \]** l’attribut doit être défini au même niveau logique que l’Union :

-   Lorsque l’Union est un paramètre, l’Union discriminante doit être un autre paramètre.
-   Lorsque l’Union est un champ d’une structure, discriminante doit être un autre champ de la même structure.

La séquence dans une structure ou une liste de paramètres de fonction n’est pas significative. L’Union peut soit précéder ou suivre le discriminante.

Le **\[ commutateur \_ est \]** l’attribut peut apparaître en tant qu’attribut de champ ou en tant qu’attribut de paramètre.

## <a name="examples"></a>Exemples

``` syntax
typedef [switch_type(short)] union _WILLIE_UNION_TYPE 
{ 
    [case(24)] 
        float fMays; 
    [case(25)] 
        double dMcCovey; 
    [default] 
        ; 
} WILLIE_UNION_TYPE; 
 
typedef struct _WINNER_TYPE 
{ 
    [switch_is(sUniformNumber)] WILLIE_UNION_TYPE w; 
    short sUniformNumber; 
} WINNER_TYPE;
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types de base MIDL](midl-base-types.md)
</dt> <dt>

[**rappel**](callback.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**handle de contexte \_**](context-handle.md)
</dt> <dt>

[Unions encapsulées](encapsulated-unions.md)
</dt> <dt>

[**variables**](enum.md)
</dt> <dt>

[**tout d’abord, \_**](first-is.md)
</dt> <dt>

[**ignore**](ignore.md)
</dt> <dt>

[**la dernière \_ est**](last-is.md)
</dt> <dt>

[**la longueur \_ est**](length-is.md)
</dt> <dt>

[**localisé**](local.md)
</dt> <dt>

[**le nombre maximal \_ est**](max-is.md)
</dt> <dt>

[Unions qui ne sont pas encapsulées](nonencapsulated-unions.md)
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

 

 




