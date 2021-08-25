---
title: unique (attribut)
description: L’attribut \ unique \ spécifie un pointeur unique.
ms.assetid: 0d668148-e65a-478f-9e47-2528d3caa84c
keywords:
- MIDL d’attribut unique
topic_type:
- apiref
api_name:
- unique
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57c176c9a246329b6193c97ca5ce356c2b433cb421b77b374e103778df1b79dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822029"
---
# <a name="unique-attribute"></a>unique (attribut)

L’attribut **\[ unique \]** spécifie un pointeur unique.

``` syntax
pointer_default(unique)

typedef [ unique [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef struct-or-union-declarator 
{
    [ unique [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...}

[ unique [[ , function-attribute-list ]] ] type-specifier ptr-decl function-name(
    [[ [ parameter-attribute-list ] ]] type-specifier [[declarator]]
    , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ unique [[ , parameter-attribute-list ]] ] type-specifier [[declarator]]
    , ...);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*type-attribut-List* 
</dt> <dd>

Spécifie un ou plusieurs attributs qui s’appliquent au type. Les attributs de type valides incluent **\[** [**handle**](handle.md) **\]** , **\[** [**\_ type de commutateur**](switch-type.md) **\]** , **\[** [**transmettre \_ en tant que**](transmit-as.md) **\]** ; l’attribut de pointeur **\[** [**ref**](ref.md) **\]** , **\[ \] unique** ou **\[** [**ptr**](ptr.md) **\]** ; et les attributs d’utilisation **\[** [**\_ handle de contexte**](context-handle.md) **\]** , **\[** [**chaîne**](string.md) **\]** et **\[** [**Ignorer**](ignore.md) **\]** . Séparez plusieurs attributs par des virgules.

</dd> <dt>

*spécificateur de type* 
</dt> <dd>

Spécifie un [type de base](midl-base-types.md), un [**struct**](struct.md), une [**Union**](union.md), un type [**enum**](enum.md) ou un identificateur de type. Une spécification de stockage facultative peut précéder *le type-specifier*.

</dd> <dt>

*déclarateur et déclarateur-liste* 
</dt> <dd>

Spécifie les déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau. Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**tableaux**](arrays-1.md)et [pointeurs](/windows/desktop/Rpc/arrays-and-pointers). La *liste déclarateur* se compose d’un ou de plusieurs déclarateurs séparés par des virgules. L’identificateur de nom de paramètre dans le déclarateur de fonction est facultatif.

</dd> <dt>

*struct-or-Union-declarator* 
</dt> <dd>

Spécifie un déclarateur de [**struct**](struct.md) ou d' [**Union**](union.md) MIDL.

</dd> <dt>

*Field-attribute-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs de champ qui s’appliquent au membre de structure, au membre d’Union ou au paramètre de fonction. Les attributs de champ valides sont **\[** [**First \_**](first-is.md)is, **\]** **\[** [**Last \_ is**](last-is.md), **\]** **\[** [**Length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ is**](size-is.md) **\]** ; the usage Attributes **\[ \] String**, **\[ ignore \]** et **\[ Context \_ \] handle**; the pointer **\[ Ref \]**, **\[ unique \]** ou **\[ ptr \]**; et le **\[ \_ type \] de commutateur** d’Union. Séparez plusieurs attributs de champ par des virgules.

</dd> <dt>

*function-attribute-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs qui s’appliquent à la fonction. Les attributs de fonction valides sont **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md) **\]** , l’attribut de pointeur **\[ \] ref**, **\[ unique \]** ou **\[ ptr \]**; et les attributs d’utilisation **\[ chaîne \]**, **\[ Ignorer \]** et **\[ \_ \] handle de contexte**.

</dd> <dt>

*pointeur-decl* 
</dt> <dd>

Spécifie au moins un déclarateur de pointeur auquel s’applique l’attribut **\[ unique \]** . Un déclarateur de pointeur est le même que le déclarateur de pointeur utilisé dans C ; elle est construite à partir de l' \* indicateur, de modificateurs tels que **Far** et de l’identificateur [**const**](const.md).

</dd> <dt>

*function-name* 
</dt> <dd>

Spécifie le nom de la procédure distante.

</dd> <dt>

*Parameter-attribute-List* 
</dt> <dd>

Se compose de zéro, un ou plusieurs attributs appropriés pour le type de paramètre spécifié. Les attributs de paramètre peuvent accepter et **\[ \] sortir** les attributs directionnels, les attributs **\[ de \]** **\[ \]**  **\[ \]** [](ptr.md) **\[ \_ \]** champ en **\[ premier \_ \]**,, le nom, la **\[ longueur \_ \]**, la valeur **\[ maximale \_ \]**, la **\[ taille \_ \]** et le **\[ \_ type \] de commutateur**; l’attribut de pointeur REF, unique ou PTR ; et le **\[ \_ handle \] de contexte** et la chaîne des attributs d’utilisation. L’attribut d’utilisation **\[ ignore \]** ne peut pas être utilisé en tant qu’attribut de paramètre. Séparez plusieurs attributs par des virgules.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les attributs de pointeur peuvent être appliqués en tant qu’attribut de type ; en tant qu’attribut de champ qui s’applique à un membre de structure, un membre d’Union ou un paramètre ; ou en tant qu’attribut de fonction qui s’applique au type de retour de la fonction. L’attribut de pointeur peut également apparaître avec le **\[** mot clé [**\_ default du pointeur**](pointer-default.md) **\]** .

Un pointeur unique présente les caractéristiques suivantes :

-   Peut avoir la valeur **null**.
-   Peut changer pendant un appel de **null** en non **null**, de non **null à** **null** ou d’une valeur non **null** à une autre.
-   Peut allouer une nouvelle mémoire sur le client. Lorsque le pointeur unique passe de **null** à non **null**, les données retournées à partir du serveur sont écrites dans un nouveau stockage.
-   Peut utiliser la mémoire existante sur le client sans allouer de nouvelle mémoire. Lorsqu’un pointeur unique change pendant un appel d’une valeur non **null** à une autre, le pointeur est supposé pointer vers un objet de données du même type. Les données retournées par le serveur sont écrites dans le stockage existant spécifié par la valeur du pointeur unique avant l’appel.
-   Peut disposer d’une mémoire orpheline sur le client. La mémoire référencée par un pointeur unique non **null** peut ne jamais être libérée si le pointeur unique devient **null** pendant un appel et que le client n’a pas d’autre moyen de déréférencer le stockage.
-   Ne provoque pas d’alias. À l’instar du stockage pointé par un pointeur de référence, le stockage désigné par un pointeur unique ne peut pas être atteint à partir d’un autre nom de la fonction.

Les stubs appellent les fonctions de gestion de mémoire fournies par l’utilisateur, [**MIDL \_ \_ allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function) et l' [**\_ utilisateur MIDL \_ Free**](/windows/desktop/Rpc/the-midl-user-free-function) pour allouer et libérer la mémoire requise pour les pointeurs uniques et leurs référents.

Les restrictions suivantes s’appliquent aux pointeurs uniques :

-   L’attribut **\[ unique \]** ne peut pas être appliqué aux paramètres de handle de liaison ( [**handle \_ t**](handle-t.md)) et aux paramètres de handle de contexte.
-   L’attribut **\[ \] unique** ne peut pas être appliqué aux paramètres de pointeur de **\[** [](out-idl.md) **\]** niveau supérieur uniquement (paramètres qui ont uniquement l’attribut directionnel **\[ out \]** ).
-   Par défaut, les pointeurs de niveau supérieur dans les listes de paramètres sont des **\[** [](ref.md) **\]** pointeurs de référence. Cela est vrai même si l’interface spécifie un **pointeur \_ par défaut (unique)**. Les paramètres de niveau supérieur dans les listes de paramètres doivent être spécifiés avec l’attribut **\[ unique \]** comme pointeur unique.
-   Les pointeurs uniques ne peuvent pas être utilisés pour décrire la taille d’un tableau ou d’un bras d’Union, car les pointeurs uniques peuvent avoir la valeur **null**. Cette restriction empêche l’erreur qui se produit si une valeur **null** est utilisée comme taille de tableau ou taille d’Union-ARM.

## <a name="examples"></a>Exemples

``` syntax
pointer_default(unique) 
 
typedef [unique, string] unsigned char * MY_STRING_TYPE; 
 
[unique] char * MyFunction([in, out, unique] long * plNumber);
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

[**handle \_ t**](handle-t.md)
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

[allouer un \_ utilisateur MIDL \_](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[\_utilisateur \_ gratuit MIDL](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[**à**](out-idl.md)
</dt> <dt>

[**pointeur \_ par défaut**](pointer-default.md)
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

[**transmettre \_ en tant que**](transmit-as.md)
</dt> <dt>

[**union**](union.md)
</dt> </dl>

 

 