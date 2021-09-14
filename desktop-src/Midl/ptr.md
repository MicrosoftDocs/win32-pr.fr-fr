---
title: ptr (attribut)
description: L’attribut \ PTR \ désigne un pointeur comme un pointeur complet.
ms.assetid: a1233a25-b651-4a01-8abf-a64dc9ee168e
keywords:
- pointeur MIDL de l’attribut PTR
topic_type:
- apiref
api_name:
- ptr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2d8b2ee2e3ea4daccd1c4fa37ff1c1f1899dd3c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093237"
---
# <a name="ptr-attribute"></a>ptr (attribut)

L’attribut **\[ ptr \]** désigne un pointeur comme un pointeur complet.

``` syntax
pointer_default(ptr)

typedef [ ptr [ , type-attribute-list ] ] type-specifier declarator-list; 

typedef [ struct | union ]
{
    [ ptr [ , field-attribute-list ] ] type-specifier declarator-list;
    ...
}

[ ptr [ , function-attribute-list ] ] type-specifier ptr-decl function-name(
    [ [ parameter-attribute-list ] ] type-specifier [standard-declarator]
    , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ ptr [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
    , ...);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*type-attribut-List* 
</dt> <dd>

Spécifie un ou plusieurs attributs qui s’appliquent au type. Les attributs de type valides incluent **\[** [**handle**](handle.md) **\]** , **\[** [**\_ type de commutateur**](switch-type.md) **\]** , **\[** [**transmettre \_ en tant que**](transmit-as.md) **\]** ; l’attribut de pointeur **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md)ou **\[ ptr \]**; et les attributs d’utilisation **\[** [**\_ handle de contexte**](context-handle.md) **\]** , **\[** [**chaîne**](string.md) **\]** et **\[** [**Ignorer**](ignore.md) **\]** . Séparez plusieurs attributs par des virgules.

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

Spécifie zéro, un ou plusieurs attributs de champ qui s’appliquent au membre de structure ou d’Union ou au paramètre de fonction. Les attributs de champ valides sont **\[** [**First \_**](first-is.md)is, **\]** **\[** [**Last \_ is**](last-is.md), **\]** **\[** [**Length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ is**](size-is.md) **\]** ; the usage Attributes **\[** [**String**](string.md) **\]** , **\[** [**ignore**](ignore.md) **\]** et **\[** [**Context \_ handle**](context-handle.md) **\]** ; The pointer **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** ou **\[ ptr \]**; et le **\[** [**\_ type de commutateur**](switch-type.md)d’Union **\]** . Séparez plusieurs attributs de champ par des virgules.

</dd> <dt>

*function-attribute-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs qui s’appliquent à la fonction. Les attributs de fonction valides sont **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** l’attribut de pointeur **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** ou **\[ \] ptr**; et les attributs d’utilisation **\[** [**chaîne**](string.md) **\]** , **\[** [**Ignorer**](ignore.md) **\]** et **\[** [**\_ handle de contexte**](context-handle.md) **\]** .

</dd> <dt>

*pointeur-decl* 
</dt> <dd>

Spécifie au moins un déclarateur de pointeur auquel s’applique l’attribut **\[ ptr \]** . Un déclarateur de pointeur est le même que le déclarateur de pointeur utilisé dans C ; elle est construite à partir de l' \* indicateur, de modificateurs tels que **Far** et de l’identificateur [**const**](const.md).

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Spécifie le nom de la procédure distante.

</dd> <dt>

*Parameter-attribute-List* 
</dt> <dd>

Se compose de zéro, un ou plusieurs attributs appropriés pour le type de paramètre spécifié. Les attributs [**de**](in.md) paramètre peuvent prendre les attributs directionnels et les [**éliminer**](out-idl.md). les attributs de [**champ \_ sont en premier**](first-is.md), la [**longueur \_ est**](length-is.md), le [**nombre maximal \_**](max-is.md), la taille et le [**\_ type de commutateur**](switch-type.md); l’attribut de pointeur [**ref**](ref.md), [**unique**](unique.md)ou **\[ ptr \]**; et le [**\_ handle de contexte**](context-handle.md) et la [**chaîne**](string.md)des attributs d’utilisation. [**\_**](last-is.md) [**\_**](size-is.md) L’attribut d’utilisation [**ignore**](ignore.md) ne peut pas être utilisé en tant qu’attribut de paramètre. Séparez plusieurs attributs par des virgules.

</dd> </dl>

## <a name="remarks"></a>Notes

Le pointeur complet désigné par l’attribut **\[ ptr \]** approche les fonctionnalités complètes du pointeur du langage C. Le pointeur complet peut avoir la valeur **null** et peut changer pendant l’appel de **null** en non **null**. les Stockage pointées par les pointeurs complets peuvent être atteintes par d’autres noms dans l’application prenant en charge les alias et les cycles. Cette fonctionnalité nécessite une plus grande surcharge au cours d’un appel de procédure distante pour identifier les données référencées par le pointeur, déterminer si la valeur est **null** et pour déterminer si deux pointeurs pointent vers les mêmes données.

Utiliser des pointeurs complets pour :

-   Valeurs de retour distantes.
-   Pointeurs doubles, lorsque la taille d’un paramètre de sortie n’est pas connue.
-   Pointeurs **null** .

Les pointeurs complets (et uniques) ne peuvent pas être utilisés pour décrire la taille d’un tableau ou d’une Union, car ces pointeurs peuvent avoir la valeur **null**. Cette restriction par MIDL empêche une erreur qui peut se produire lorsqu’une valeur **null** est utilisée comme taille.

Les pointeurs de référence et uniques sont supposés ne pas générer d’alias de données. Un graphique dirigé obtenu en démarrant à partir d’un pointeur unique ou de référence et suivant uniquement les pointeurs unique ou de référence ne contient ni reconvergence, ni cycles.

Pour éviter les alias, toutes les valeurs de pointeur doivent être obtenues à partir d’un pointeur d’entrée de la même classe de pointeur. Si plusieurs pointeurs pointent vers le même emplacement de mémoire, tous ces pointeurs doivent être des pointeurs complets.

Dans certains cas, des pointeurs complets et uniques peuvent être mélangés. La valeur d’un pointeur unique peut être assignée à un pointeur complet, à condition que l’assignation ne viole pas les restrictions de modification de la valeur d’un pointeur unique. Toutefois, lorsque vous affectez à un pointeur unique la valeur d’un pointeur complet, vous pouvez créer un alias.

Le mélange de pointeurs complets et uniques peut entraîner des alias, comme illustré dans l’exemple suivant :

``` syntax
typedef struct 
{ 
    [ptr] short * pdata;          // full pointer  
} GRAPH_NODE_TYPE; 
 
typedef struct 
{ 
    [unique] graph_node * left;   // unique pointer  
    [unique] graph_node * right;  // unique pointer 
} TREE_NODE_TYPE; 
 
// application code: 
short a = 5; 
TREE_NODE_TYPE * t; 
GRAPH_NODE_TYPE g, h; 
 
g.pdata = h.pdata = &a; 
t->left = &g; 
t->right = &h; 
// t->left->pdata == t->right->pdata == &a
```

Bien que les points « t->Left » et « t->Right » pointent vers des emplacements de mémoire uniques, les « t->à gauche >pData » et le « t->>pData » sont des alias. Pour cette raison, les algorithmes de prise en charge d’alias doivent suivre tous les pointeurs (y compris les pointeurs uniques et de référence) qui peuvent finir par atteindre un pointeur complet.

## <a name="examples"></a>Exemples

``` syntax
pointer_default(ptr) 
 
typedef [ptr, string] unsigned char * MY_STRING_TYPE; 
 
[ptr] char * MyFunction([in, out, unique] long * plNumber);
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

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
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

[**pointeur \_ par défaut**](pointer-default.md)
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
</dt> <dt>

[**unique**](unique.md)
</dt> </dl>

 

 