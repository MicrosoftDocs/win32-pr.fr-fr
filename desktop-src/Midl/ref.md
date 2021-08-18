---
title: ref (attribut)
description: L’attribut \ Ref \ identifie un pointeur de référence. Il est utilisé simplement pour représenter un niveau d’indirection.
ms.assetid: db4ff938-0f38-4f77-bb65-f728ffd609e0
keywords:
- MIDL (MIDL), attribut de référence
topic_type:
- apiref
api_name:
- ref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 916556bdee83817f512c2d86eef2d768c3f6dbddf06b39408da5c25a2ba10ed2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013667"
---
# <a name="ref-attribute"></a>ref (attribut)

L’attribut **\[ Ref \]** identifie un pointeur de référence. Il est utilisé simplement pour représenter un niveau d’indirection.

``` syntax
pointer_default(ref)

typedef [ ref [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef [ struct | union ] 
{
    [ ref [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...}

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ ref [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
    , ...);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*type-attribut-List* 
</dt> <dd>

Spécifie un ou plusieurs attributs qui s’appliquent au type. Les attributs de type valides incluent **\[** [**handle**](handle.md) **\]** , **\[** [**\_ type de commutateur**](switch-type.md) **\]** , **\[** [**transmettre \_ en tant que**](transmit-as.md) **\]** ; les attributs de pointeur **\[ Ref \]**, **\[** [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** ; et les attributs d’utilisation **\[** [**\_ handle de contexte**](context-handle.md) **\]** , **\[** [**chaîne**](string.md) **\]** et **\[** [**Ignorer**](ignore.md) **\]** . Séparez plusieurs attributs par des virgules.

</dd> <dt>

*spécificateur de type* 
</dt> <dd>

Spécifie un type de [base](midl-base-types.md), un [**struct**](struct.md), une [**Union**](union.md)ou un type [**enum**](enum.md) ou un identificateur de type. Une spécification de stockage facultative peut précéder *le type-specifier*.

</dd> <dt>

*standard-déclarateur* 
</dt> <dd>

Spécifie un déclarateur C standard, tel qu’un identificateur, un déclarateur de pointeur ou un déclarateur de tableau. Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**tableaux**](arrays-1.md), tableaux [et pointeurs](/windows/desktop/Rpc/arrays-and-pointers).

</dd> <dt>

*déclarateur-liste* 
</dt> <dd>

Spécifie les déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau. Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**tableaux**](arrays-1.md), tableaux [et pointeurs](/windows/desktop/Rpc/arrays-and-pointers). La *liste déclarateur* se compose d’un ou de plusieurs déclarateurs séparés par des virgules. L’identificateur de nom de paramètre dans le déclarateur de fonction est facultatif.

</dd> <dt>

*Field-attribute-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs de champ qui s’appliquent à la structure, au membre d’Union ou au paramètre de fonction. Les attributs de champ valides sont **\[** [**First \_**](first-is.md)is, **\]** **\[** [**Last \_ is**](last-is.md), **\]** **\[** [**Length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ is**](size-is.md) **\]** ; the usage Attributes **\[** [**String**](string.md) **\]** , **\[** [**ignore**](ignore.md) **\]** et **\[** [**Context \_ handle**](context-handle.md) **\]** ; The pointer **\[ \] ref**, **\[** [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** ; et le **\[** [**\_ type de commutateur**](switch-type.md)d’Union **\]** . Séparez plusieurs attributs de champ par des virgules.

</dd> <dt>

*function-attribute-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs qui s’appliquent à la fonction. Les attributs de fonction valides sont **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** l’attribut de pointeur **\[ Ref \]**, **\[** [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** ; et les attributs d’utilisation **\[** [**chaîne**](string.md) **\]** , **\[** [**Ignorer**](ignore.md) **\]** et **\[** [**\_ handle de contexte**](context-handle.md) **\]** .

</dd> <dt>

*pointeur-decl* 
</dt> <dd>

Spécifie au moins un déclarateur de pointeur auquel s’applique l’attribut **\[ Ref \]** . Un déclarateur de pointeur est le même que le déclarateur de pointeur utilisé dans C ; elle est construite à partir de l' \* indicateur, de modificateurs tels que **Far** et de l’identificateur [**const**](const.md).

</dd> <dt>

*function-name* 
</dt> <dd>

Spécifie le nom de la procédure distante.

</dd> <dt>

*Parameter-attribute-List* 
</dt> <dd>

Se compose de zéro, un ou plusieurs attributs appropriés pour le type de paramètre spécifié. Les attributs de paramètre peuvent accepter et sortir les attributs directionnels, **\[** les attributs [**de champ en**](in.md) premier,, le **\]** **\[** [](out-idl.md) **\]** **\[** [**\_**](first-is.md) **\]** nom, la longueur, la valeur maximale, la **\[** [**\_**](last-is.md) **\]** **\[** [**\_**](length-is.md) **\]** **\[** [**\_**](max-is.md) **\]** **\[** [**taille \_**](size-is.md) **\]** et le **\[** [**\_ type de commutateur**](switch-type.md) **\]** ; l’attribut de pointeur **\[ Ref \]**, **\[** [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** ; et le **\[** [**\_ handle de contexte**](context-handle.md) et la chaîne des attributs d’utilisation **\]** **\[** [](string.md) **\]** . L’attribut d’utilisation **\[** [**ignore**](ignore.md) **\]** ne peut pas être utilisé en tant qu’attribut de paramètre. Séparez plusieurs attributs par des virgules.

</dd> </dl>

## <a name="remarks"></a>Remarques

Un attribut de pointeur peut être appliqué comme un attribut de type, comme un attribut de champ qui s’applique à un membre de structure, un membre d’Union ou un paramètre ; ou en tant qu’attribut de fonction qui s’applique au type de retour de la fonction. L’attribut de pointeur peut également apparaître avec le **\[** mot clé [**\_ default du pointeur**](pointer-default.md) **\]** .

Un pointeur de référence présente les caractéristiques suivantes :

-   Pointe toujours vers un stockage valide ; n’a jamais la valeur **null**. Un pointeur de référence peut toujours être déréférencé.
-   Jamais modifié pendant un appel. Un pointeur de référence pointe toujours vers le même stockage sur le client avant et après l’appel.
-   N’alloue pas de nouvelle mémoire sur le client. Les données retournées à partir du serveur sont écrites dans le stockage existant spécifié par la valeur du pointeur de référence avant l’appel.
-   Ne provoque pas d’alias. Stockage pointée par un pointeur de référence ne peut pas être atteint à partir d’un autre nom dans la fonction.

Un pointeur de référence ne peut pas être utilisé en tant que type d’un pointeur retourné par une fonction.

Si aucun attribut n’est spécifié pour un paramètre de pointeur de niveau supérieur, il est traité comme un pointeur de référence.

## <a name="examples"></a>Exemples

``` syntax
[unique] char * GetFirstName( 
    [in, ref] char * pszFullName);
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**tableaux**](arrays-1.md)
</dt> <dt>

[Tableaux et pointeurs](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Attributs de tableau et de Sized-Pointer](array-and-sized-pointer-attributes.md)
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

[**traitée**](handle.md)
</dt> <dt>

[**tenir**](ignore.md)
</dt> <dt>

[**la dernière \_ est**](last-is.md)
</dt> <dt>

[**la longueur \_ est**](length-is.md)
</dt> <dt>

[**local**](local.md)
</dt> <dt>

[**le nombre maximal \_ est**](max-is.md)
</dt> <dt>

[**à**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**la taille \_ est**](size-is.md)
</dt> <dt>

[**chaîne**](string.md)
</dt> <dt>

[**modélis**](struct.md)
</dt> <dt>

[**type de commutateur \_**](switch-type.md)
</dt> <dt>

[**transmettre \_ en tant que**](transmit-as.md)
</dt> <dt>

[**union**](union.md)
</dt> <dt>

[**unique**](unique.md)
</dt> </dl>

 

 