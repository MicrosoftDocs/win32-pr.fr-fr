---
title: last_is (attribut)
description: L’attribut de champ \ Last \_ is \ spécifie l’index du dernier élément de tableau à transmettre. Lorsque l’index spécifié est égal à zéro ou négatif, aucun élément de tableau n’est transmis.
ms.assetid: 42a5cb0d-0887-4aa7-b34f-2fbad0f4c8ab
keywords:
- last_is MIDL de l’attribut
topic_type:
- apiref
api_name:
- last_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 453a51109452f3cdacb1a48e67b76ccbc9f2e257
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507906"
---
# <a name="last_is-attribute"></a>le dernier \_ attribut est

L’attribut Field **\[ Last \_ \]** spécifie l’index du dernier élément de tableau à transmettre. Lorsque l’index spécifié est égal à zéro ou négatif, aucun élément de tableau n’est transmis.

``` syntax
[last_is( limited-expression-list )]
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*Limited-expression-List* 
</dt> <dd>

Spécifie une ou plusieurs expressions en langage C. Chaque expression prend la valeur d’un entier qui représente l’index de tableau du dernier élément de tableau à transmettre. Le compilateur MIDL prend en charge les expressions conditionnelles, les expressions logiques, les expressions relationnelles et les expressions arithmétiques. MIDL n’autorise pas les appels de fonction dans les expressions et n’autorise pas les opérateurs d’incrémentation et de décrémentation. Séparez plusieurs expressions par des virgules.

</dd> </dl>

## <a name="remarks"></a>Notes

Le **\[ dernier \_ attribut \] est** détermine que la valeur de l’index de tableau correspondant à la **\[** [**\_**](length-is.md) **\]** **\[ \_ \]** longueur est attribut lorsque la longueur n’est pas spécifiée. La relation entre ces index de tableau est la suivante : longueur = Last-First + 1.

Si la valeur de l’index de tableau spécifié par la **\[** [**première \_ est**](first-is.md) supérieure **\]** à la valeur spécifiée par le **\[ dernier \_ \] est**, aucun élément n’est transmis.

Le **\[ dernier \_ attribut \] is** ne peut pas être utilisé en tant qu’attribut de champ en même temps que la **\[** [**longueur \_ est**](length-is.md) **\]** attribute ou l’attribut de **\[** [**chaîne**](string.md) **\]** .

L’utilisation d’une expression constante avec le **\[ dernier attribut \_ est \]** une utilisation inappropriée de l’attribut. Il est légal, mais inefficace, et se traduira par un code de marshaling plus lent.

Quand la valeur spécifiée par **\[** [**Max \_ est**](max-is.md) **\]** supérieure ou égale à zéro, la relation suivante doit être vraie : 0 <= Last \_ est <= Max \_ est.

## <a name="examples"></a>Exemples

``` syntax
proc1(
    [in] short Last,
    [in, last_is(Last)] short asNumbers[MAXSIZE]);
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Attributs de champ](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[**tout d’abord, \_**](first-is.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**la longueur \_ est**](length-is.md)
</dt> <dt>

[**le nombre maximal \_ est**](max-is.md)
</dt> <dt>

[**la taille \_ est**](size-is.md)
</dt> </dl>

 

 