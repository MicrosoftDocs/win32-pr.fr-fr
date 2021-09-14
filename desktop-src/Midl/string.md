---
title: attribut de chaîne
description: L’attribut \ String \ indique que le tableau Char, WCHAR \_ t, Byte (ou équivalent) unidimensionnel ou le pointeur vers ce tableau doit être traité comme une chaîne.
ms.assetid: 379cd59e-7540-4188-9b5c-6c25a8928999
keywords:
- MIDL, attribut de chaîne
topic_type:
- apiref
api_name:
- string
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae2bd3c56bcf09d1c47343f903653e9d83113b1d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093177"
---
# <a name="string-attribute"></a>attribut de chaîne

L’attribut **\[ \] String** indique que le tableau [**char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Byte**](byte.md) (ou équivalent) unidimensionnel ou le pointeur vers ce tableau doit être traité comme une chaîne. La chaîne peut également être un tableau (ou un pointeur vers un tableau) de constructions dont les champs sont tous du type **Byte**.

``` syntax
typedef [ string [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef [ struct | union ] 
{
    [ string [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...
};

[ string [[ , function-attribute-list ]] ] type-specifier ptr-decl function-name(
  [[ [ parameter-attribute-list ] ]] type-specifier [[standard-declarator]]
  , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ string [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
  , ...);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*type-attribut-List* 
</dt> <dd>

Spécifie un ou plusieurs attributs qui s’appliquent à un type. Les attributs de type valides incluent **\[** [**handle**](handle.md) **\]** , **\[** [**\_ type de commutateur**](switch-type.md) **\]** , **\[** [**transmettre \_ en tant que**](transmit-as.md) **\]** ; l’attribut de pointeur **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** ; et les attributs d’utilisation **\[** [**\_ handle de contexte**](context-handle.md) **\]** , **\[ \] chaîne** et **\[** [**Ignorer**](ignore.md) **\]** . Séparez plusieurs attributs par des virgules.

</dd> <dt>

*spécificateur de type* 
</dt> <dd>

Spécifie un [type de base](midl-base-types.md), un type [**struct**](struct.md) ou un identificateur de type. Une spécification de stockage facultative peut précéder *le type-specifier*.

</dd> <dt>

*standard-déclarateur* 
</dt> <dd>

Spécifie un déclarateur C standard, tel qu’un identificateur, un déclarateur de pointeur ou un déclarateur de tableau. Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**tableaux**](arrays-1.md)et [pointeurs](/windows/desktop/Rpc/arrays-and-pointers).

</dd> <dt>

*déclarateur-liste* 
</dt> <dd>

Spécifie les déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau. Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**tableaux**](arrays-1.md)et [pointeurs](/windows/desktop/Rpc/arrays-and-pointers). La *liste déclarateur* se compose d’un ou de plusieurs déclarateurs séparés par des virgules. L’identificateur de nom de paramètre dans le déclarateur de fonction est facultatif.

</dd> <dt>

*Field-attribute-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs de champ qui s’appliquent à la structure, au membre d’Union ou au paramètre de fonction. Les deux attributs de champ valides sont **\[** [**Max \_**](max-is.md) **\]** et **\[** [**size \_ est**](size-is.md) **\]** ; les attributs d’utilisation **\[ String \]**, **\[ ignore \]** et **\[ Context \_ handle \]**, l’attribut de pointeur **\[** [**ref**](ref.md) **\]** , **\[ unique \]** ou **\[** [**ptr**](ptr.md) **\]** et le **\[ \_ type \] de commutateur** d’attribut Union. Séparez plusieurs attributs de champ par des virgules.

</dd> <dt>

*function-attribute-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs qui s’appliquent à la fonction. Les attributs de fonction valides sont **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md) **\]** , l’attribut de pointeur **\[ \] ref**, **\[ unique \]** ou **\[ ptr \]**; et les attributs d’utilisation **\[ chaîne \]**, **\[ Ignorer \]** et **\[ \_ \] handle de contexte**.

</dd> <dt>

*pointeur-decl* 
</dt> <dd>

Spécifie un déclarateur de pointeur facultatif auquel s’applique l’attribut de **\[ chaîne \]** . Un déclarateur de pointeur est le même que le déclarateur de pointeur utilisé dans C ; elle est construite à partir de l' \* indicateur, de modificateurs tels que **Far** et de l’identificateur [**const**](const.md).

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Spécifie le nom de la procédure distante.

</dd> <dt>

*Parameter-attribute-List* 
</dt> <dd>

Se compose de zéro, un ou plusieurs attributs appropriés pour le type de paramètre spécifié. Les attributs de paramètre peuvent accepter et **\[ sortir \]** les attributs directionnels ; les attributs **\[ de \]** champ **\[** [**Max \_ sont**](max-is.md) **\]** et **\[** [**size \_ est**](size-is.md) **\]** ; l’attribut de pointeur **\[ \] ref**, **\[ unique \]** ou **\[ ptr \]**; et les attributs d’utilisation **\[ \_ handle \] de contexte** et **\[ chaîne \]**. L’attribut d’utilisation **\[ ignore \]** ne peut pas être utilisé en tant qu’attribut de paramètre. Séparez plusieurs attributs par des virgules.

</dd> </dl>

## <a name="remarks"></a>Notes

Si l’attribut de **\[ chaîne \]** est utilisé avec un tableau dont les limites sont déterminées au moment de l’exécution, vous devez également spécifier **\[ \_ \] une taille** , ou l’attribut **\[ Max \_ est \]** un attribut, comme dans l’exemple suivant :

``` syntax
/* a string that can hold up to MAX_STRING_LENGTH characters */
typedef [string, max_is(MAX_STRING_LENGTH)] char line[];
```

L’attribut de **\[ chaîne \]** ne peut pas être utilisé avec des attributs qui spécifient la plage d’éléments transmis, par exemple **\[ First \_ est \]**, **\[ Last \_ is \]** et **\[ Length \_ est \]**.

Lorsqu’il est utilisé sur des tableaux multidimensionnels, l’attribut de **\[ chaîne \]** s’applique au tableau le plus à droite.

Pour définir une chaîne comptée, n’utilisez pas l’attribut de **\[ chaîne \]** . Utilisez un tableau de caractères ou un pointeur de type caractère tel que le suivant :

``` syntax
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
} counted_string;
```

L’attribut **\[ String \]** spécifie que le stub doit utiliser une méthode fournie par le langage pour déterminer la longueur des chaînes.

Lors de la déclaration de chaînes en C, vous devez allouer de l’espace pour un caractère supplémentaire qui marque la fin de la chaîne.

## <a name="examples"></a>Exemples

``` syntax
/* a string type that can hold up to 80 characters */ 
typedef [string] char line[81]; 
 
HRESULT Proc1([in, string] char * pszName);
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**tableaux**](arrays-1.md)
</dt> <dt>

[Types de base MIDL](midl-base-types.md)
</dt> <dt>

[**rappel**](callback.md)
</dt> <dt>

[**char**](char-idl.md)
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

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**la taille \_ est**](size-is.md)
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
</dt> <dt>

[**WCHAR \_ t**](wchar-t.md)
</dt> </dl>

 

 