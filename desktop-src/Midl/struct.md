---
title: struct (attribut)
description: Le mot clé struct est utilisé dans un spécificateur de type structure.
ms.assetid: 89e18f0e-185a-408e-812d-3d11f228b473
keywords:
- MIDL, attribut de struct
topic_type:
- apiref
api_name:
- struct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5c97ca9a2dbbfeddc5416b517e85e0926434c5d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106511282"
---
# <a name="struct-attribute"></a>struct (attribut)

Le mot clé **struct** est utilisé dans un spécificateur de type structure.

``` syntax
struct [[ struct-tag ]] 
{
  [[ [ field-attribute-list ] ]] type-specifier declarator-list;
    ...
};
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*struct-tag* 
</dt> <dd>

Spécifie une balise facultative pour la structure.

</dd> <dt>

*Field-attribute-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs de champ qui s’appliquent au membre de la structure. Les attributs de champ valides sont **\[** [**First \_**](first-is.md)is, **\]** **\[** [**Last \_ is**](last-is.md), **\]** **\[** [**Length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** et **\[** [**size \_ is**](size-is.md) **\]** ; les attributs d’utilisation **\[** [**String**](string.md) **\]** et **\[** [**ignore**](ignore.md) **\]** ; l’attribut de pointeur **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** ; et le **\[** [**\_ type de commutateur**](switch-type.md)d’attribut Union **\]** . Séparez plusieurs attributs de champ par des virgules.

</dd> <dt>

*spécificateur de type* 
</dt> <dd>

Spécifie un type de [base](midl-base-types.md), un **struct**, une [**Union**](union.md)ou un type [**enum**](enum.md) ou un identificateur de type. Une spécification de stockage facultative peut précéder *le type-specifier*.

</dd> <dt>

*déclarateur-liste* 
</dt> <dd>

Spécifie un ou plusieurs déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau. (Les déclarateurs de fonction et les déclarations de champ de bits ne sont pas autorisés dans les structures transmises dans les appels de procédure distante. Ces déclarateurs sont autorisés dans les structures qui ne sont pas transmises.) Séparez plusieurs déclarateurs par des virgules.

</dd> </dl>

## <a name="remarks"></a>Notes

Le spécificateur de type de structure IDL, **struct**, diffère du spécificateur de type C standard de la manière suivante :

-   Chaque membre de structure peut être associé à des attributs de champ facultatifs qui décrivent les caractéristiques de ce membre de structure dans le cadre d’un appel de procédure distante.
-   Les champs de bits et les déclarateurs de fonction ne sont pas autorisés dans les structures utilisées dans les appels de procédure distante. Ces constructions de déclarateur C standard ne peuvent être utilisées que si la structure n’est pas transmise sur le réseau.

La forme des structures doit être la même sur toutes les plateformes pour garantir l’interconnexion.

## <a name="examples"></a>Exemples

``` syntax
typedef struct _PITCHER_RECORD_TYPE 
{ 
    short flag; 
    [switch_is(flag)] union PITCHER_STATISTICS_TYPE p; 
} PITCHER_RECORD_TYPE;
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

[**/c \_ ext**](-c-ext.md)
</dt> <dt>

[**handle de contexte \_**](context-handle.md)
</dt> <dt>

[**variables**](enum.md)
</dt> <dt>

[**tout d’abord, \_**](first-is.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**tenir**](ignore.md)
</dt> <dt>

[**la dernière \_ est**](last-is.md)
</dt> <dt>

[**la longueur \_ est**](length-is.md)
</dt> <dt>

[**le nombre maximal \_ est**](max-is.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**la taille \_ est**](size-is.md)
</dt> <dt>

[**chaîne**](string.md)
</dt> <dt>

[**type de commutateur \_**](switch-type.md)
</dt> <dt>

[**UE**](union.md)
</dt> <dt>

[**unique**](unique.md)
</dt> </dl>

 

 