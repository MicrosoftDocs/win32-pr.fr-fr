---
title: Array, attribut
description: Les tableaux sont des collections homogènes de données accessibles par un numéro d’index ou d’élément.
ms.assetid: 375fb795-8f18-45b7-898c-99f1273746d8
keywords:
- attribut de tableau MIDL
topic_type:
- apiref
api_name:
- arrays
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e189eb1784a4ff24b799c7a4d4482d0f56b20e3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106527141"
---
# <a name="arrays-attribute"></a>Array, attribut

Les tableaux sont des collections homogènes de données accessibles par un numéro d’index ou d’élément.

``` syntax
typedef [ [type-attr-list] ] type-specifier [pointer-decl] array-declarator;

typedef [ [type-attr-list] ] struct [ tag ] 
{
    [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
    ...
};

typedef [ [type-attr-list] ] union [ tag ] 
{
    [ case (limited-expression [ , ... ] ) ]
  [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
  [ [ default ]
  [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
  ]
};

[[ [function-attribute-list] ]] type-specifier [[pointer-decl]] function-name(
        [[ [param-attr-list] ]] type-specifier [[pointer-decl]] array-declarator
        , ...);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*type-attr-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs qui s’appliquent au type. Les attributs de type valides incluent [**\[ \] handle**](handle.md), [**\[ \_ \] type de commutateur**](switch-type.md), [**\[ transmettre \_ en tant que \]**](transmit-as.md); l’attribut de pointeur [**\[ Ref \]**](ref.md), [**\[ unique \]**](unique.md)ou [**\[ ptr \]**](ptr.md); et les attributs d’utilisation [**\[ \_ handle \] de contexte**](context-handle.md), [**\[ chaîne \]**](string.md)et [**\[ Ignorer \]**](ignore.md). Séparez plusieurs attributs par des virgules.

</dd> <dt>

*spécificateur de type* 
</dt> <dd>

Spécifie l’identificateur de type, le type de base, le [**struct**](struct.md), l' [**Union**](union.md)ou le type [**enum**](enum.md) . La spécification de type peut inclure une spécification de stockage facultative.

</dd> <dt>

*pointeur-decl* 
</dt> <dd>

Spécifie zéro ou plusieurs déclarateurs de pointeur. Un déclarateur de pointeur est le même que le déclarateur de pointeur utilisé en C, construit à partir de l' **\*** indicateur, modificateurs tels que **Far** et le qualificateur [**const**](const.md).

</dd> <dt>

*déclarateur de tableau* 
</dt> <dd>

Spécifie le nom du tableau, suivi de l’une des constructions suivantes pour chaque dimension du tableau : «**\[ \]**», « **\[\*\]** », «**\[ ***Const1*** \]**» ou «**\[ ***Lower...*** Upper \]**», où *Lower* et *Upper* sont des valeurs constantes qui représentent les limites inférieure et supérieure. La constante *inférieure* doit être égale à zéro.

</dd> <dt>

*tag* 
</dt> <dd>

Spécifie une balise facultative pour la structure ou l’Union.

</dd> <dt>

*Field-attribute-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs de champ qui s’appliquent à la structure, au membre d’Union ou au paramètre de fonction. Les attributs de champ valides sont [**\[ First \_ \]**](first-is.md)is, [**\[ Last \_ is \]**](last-is.md), [**\[ Length \_ \]**](length-is.md)is, [**\[ Max \_ is \]**](max-is.md), [**\[ size \_ is \]**](size-is.md), the usage Attributes [**\[ String \]**](string.md)et [**\[ ignore \]**](ignore.md); les attributs de pointeur [**\[ Ref \]**](ref.md), [**\[ unique \]**](unique.md)et [**\[ ptr \]**](ptr.md); et le [**\[ \_ type \] de commutateur**](switch-type.md)d’Union. Séparez plusieurs attributs de champ par des virgules. Notez que les attributs répertoriés ci-dessus, le **\[ premier \_ \]** est, le **\[ dernier \_ est \]**, et [**\[ Ignorer \]**](ignore.md) ne sont pas valides pour les unions.

</dd> <dt>

*Limited-expression* 
</dt> <dd>

Spécifie une expression de langage C. Le compilateur MIDL prend en charge les expressions conditionnelles, les expressions logiques, les expressions relationnelles et les expressions arithmétiques. MIDL n’autorise pas les appels de fonction dans les expressions et n’autorise pas les opérateurs d’incrémentation et de décrémentation.

</dd> <dt>

*function-attribute-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs qui s’appliquent à la fonction. Les attributs de fonction valides sont [**\[ callback \]**](callback.md), [**\[ \] local**](local.md), l’attribut de pointeur [**\[ Ref \]**](ref.md), [**\[ unique \]**](unique.md)ou [**\[ ptr \]**](ptr.md); et la [**\[ chaîne \]**](string.md)d’attributs d’utilisation et le [**\[ \_ handle \] de contexte**](context-handle.md).

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Spécifie le nom de la procédure distante.

</dd> <dt>

*Param-attr-List* 
</dt> <dd>

Spécifie les attributs directionnels et un ou plusieurs attributs de champ facultatifs qui s’appliquent au paramètre de tableau. Les attributs de champ valides incluent [**\[ Max \_ is \]**](max-is.md), [**\[ size \_ \] is**](size-is.md), [**\[ Length \_ is \]**](length-is.md), [**\[ First \_ is \]**](first-is.md)et [**\[ Last \_ is \]**](last-is.md).

</dd> </dl>

## <a name="remarks"></a>Notes

Les tableaux dans MIDL utilisent un style semblable à, mais pas exactement identiques à C et C++. Pour plus d’informations, consultez [tableaux MIDL](midl-arrays.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

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

[**tenir**](ignore.md)
</dt> <dt>

[**la dernière \_ est**](last-is.md)
</dt> <dt>

[**la longueur \_ est**](length-is.md)
</dt> <dt>

[**localisé**](local.md)
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

[**transmettre \_ en tant que**](transmit-as.md)
</dt> <dt>

[**UE**](union.md)
</dt> <dt>

[**unique**](unique.md)
</dt> </dl>

 

 




