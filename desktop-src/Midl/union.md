---
title: attribut Union
description: Le mot clé Union apparaît dans les fonctions qui se rapportent aux unions discriminées.
ms.assetid: 135a6581-e03e-4b90-9fd8-15690820dbd0
keywords:
- MIDL (MIDL), attribut d’Union
topic_type:
- apiref
api_name:
- union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc683472d67775c4a2900695246d5f9ca920ca32
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093098"
---
# <a name="union-attribute"></a>attribut Union

Le mot clé **Union** apparaît dans les fonctions qui se rapportent aux unions discriminées.

``` syntax
/* Encapsulated union*/
typedef [[ [type-attribute-list] ]] union [[ struct-name ]] switch (switch-type switch-name) [[ union-name ]] 
{
  C-style-case-list 
  [[ [ field-attribute-list <> ] ]] type-specifier <> declarator-list <>;

        ...
}

/* Non-encapsulated union*/
typedef [switch_type(switch-type) [[ , type-attr-list ]] ] union [[ tag ]] 
{ 
    [ case ( limited-expr-list) ]
  [[ [ field-attribute-list ] ]] type-specifier declarator-list;
  [[ [ default ]
  [[ [ field-attribute-list ] ]] type-specifier declarator-list;
  ]]
}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*type-attribut-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs qui s’appliquent au type d’Union. Les attributs de type valides incluent **\[** [**handle**](handle.md) **\]** , **\[** [**transmettre \_ en tant que**](transmit-as.md) **\]** ; attribut de pointeur **\[** [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** ; et les attributs d’utilisation **\[** [**\_ handle de contexte**](context-handle.md) **\]** et **\[** [**Ignorer**](ignore.md) **\]** . Les unions encapsulées peuvent également avoir l' **\[** [](ref.md) **\]** attribut de type de pointeur Ref. Séparez plusieurs attributs par des virgules.

</dd> <dt>

*nom du struct* 
</dt> <dd>

Spécifie une balise facultative qui nomme la structure générée par le compilateur MIDL.

</dd> <dt>

*type de commutateur* 
</dt> <dd>

Spécifie un type [**int**](int.md), [**char**](char-idl.md), [**enum**](enum.md) ou un identificateur qui correspond à l’un de ces types.

</dd> <dt>

*nom du commutateur* 
</dt> <dd>

Spécifie le nom de la variable de type *switch-type* qui agit en tant que discriminante d’Union.

</dd> <dt>

*nom d’Union* 
</dt> <dd>

Spécifie un identificateur facultatif qui nomme l’Union dans la structure, générée par le compilateur MIDL, qui contient l’Union et le discriminante.

</dd> <dt>

*C-style-case-liste* 
</dt> <dd>

Liste de «**case** *const-expr* : »

</dd> <dt>

*Limited-expression-List* 
</dt> <dd>

Spécifie une ou plusieurs expressions en langage C. Le compilateur MIDL prend en charge les expressions conditionnelles, les expressions logiques, les expressions relationnelles et les expressions arithmétiques. MIDL n’autorise pas les appels de fonction dans les expressions et n’autorise pas les opérateurs d’incrémentation et de décrémentation. Les expressions individuelles de la liste doivent être séparées par une virgule.

</dd> <dt>

*Field-attribute-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs de champ qui s’appliquent au membre Union. Les attributs de champ valides sont **\[** [**First \_**](first-is.md)is, **\]** **\[** [**Last \_ is**](last-is.md), **\]** **\[** [**Length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ is**](size-is.md) **\]** ; the usage Attributes **\[** [**String**](string.md) **\]** , **\[** [**ignore**](ignore.md) **\]** et **\[** [**Context \_ handle**](context-handle.md) **\]** ; l’attribut de pointeur **\[** [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** ; et, pour les membres qui sont des unions non encapsulées, le **\[** [**\_ type de commutateur**](switch-type.md)d’attribut Union **\]** . Les unions sans encapsulées peuvent également utiliser l’attribut de champ de pointeur de **\[** [**référence**](ref.md) **\]** . Séparez plusieurs attributs de champ par des virgules.

</dd> <dt>

*spécificateur de type* 
</dt> <dd>

Spécifie un [type de base](midl-base-types.md), un [**struct**](struct.md), une **Union**, un type [**enum**](enum.md) ou un identificateur de type. Une spécification de stockage facultative peut précéder *le type-specifier*.

</dd> <dt>

*déclarateur-liste* 
</dt> <dd>

Un ou plusieurs déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau. (Les déclarateurs de fonction et les déclarations de champ de bits ne sont pas autorisés dans les unions transmises dans les appels de procédure distante. Sauf quand vous utilisez le commutateur de compilateur MIDL [**/OSF**](-osf.md), ces déclarateurs sont autorisés dans les unions qui ne sont pas transmises. Séparez plusieurs déclarateurs par des virgules.

</dd> <dt>

*étiquette* 
</dt> <dd>

Spécifie une balise facultative.

</dd> </dl>

## <a name="remarks"></a>Notes

MIDL prend en charge deux types d’unions discriminées : les [unions encapsulées](encapsulated-unions.md) et les unions qui ne sont pas [encapsulées](nonencapsulated-unions.md). L’Union encapsulée est compatible avec les implémentations précédentes de RPC (NCA version 1). L’Union non encapsulée élimine certaines des restrictions de l’Union encapsulée et fournit un discriminante plus visible que l’Union encapsulée.

L’Union encapsulée est identifiée par le mot clé [**switch**](switch.md) et l’absence d’autres mots clés liés à l’Union.

L’Union non encapsulée, également appelée « Union », est identifiée par la présence du **\[** [**commutateur \_**](switch-is.md) **\]** et les **\[** Mots clés de [**\_ type de commutateur**](switch-type.md) **\]** , qui identifient le discriminante et son type.

Quand vous utilisez **\[** [**dans**](in.md), [**les**](out-idl.md) **\]** unions out, sachez que la modification de la valeur du commutateur d’Union au cours de l’appel peut faire en sorte que l’appel distant se comporte différemment d’un appel local. Au retour, les stubs copient le paramètre **\[ in**, **out \]** dans la mémoire déjà présente sur le client. Lorsque la procédure distante modifie la valeur du commutateur d’Union et modifie donc la taille de l’objet de données, les stubs peuvent remplacer la mémoire valide par la valeur **\[ out \]** . Quand le commutateur d’Union modifie l’objet de données d’un type de base en un type pointeur, les stubs peuvent remplacer la mémoire valide lorsqu’ils copient le référent du pointeur dans l’emplacement de mémoire indiqué par la valeur de **\[ dans \]** un type de base.

La forme des unions doit être identique sur les plateformes pour garantir l’interconnexion.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Unions encapsulées](encapsulated-unions.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**dans**](in.md)
</dt> <dt>

[Unions qui ne sont pas encapsulées](nonencapsulated-unions.md)
</dt> <dt>

[**à**](out-idl.md)
</dt> <dt>

[**le commutateur \_ est**](switch-is.md)
</dt> <dt>

[**type de commutateur \_**](switch-type.md)
</dt> </dl>

 

 




