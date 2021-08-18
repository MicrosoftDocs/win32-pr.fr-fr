---
title: first_is (attribut)
description: L’attribut \ First \_ is \ spécifie l’index du premier élément de tableau à transmettre.
ms.assetid: 1de7821c-19e7-4b2c-98fc-2fae3563831c
keywords:
- first_is MIDL de l’attribut
topic_type:
- apiref
api_name:
- first_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d08be3ce14074c126a35272ede1b670121634f75d0b3d6cfb0db34e4f305760
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067279"
---
# <a name="first_is-attribute"></a>First \_ est l’attribut

Le \[ **premier attribut \_ est** \] spécifie l’index du premier élément de tableau à transmettre.

``` syntax
first_is(limited-expression-list)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*Limited-expression-List* 
</dt> <dd>

Spécifie une ou plusieurs expressions en langage C. Chaque expression prend la valeur d’un entier qui représente l’index de tableau du premier élément de tableau à transmettre. Le compilateur MIDL prend en charge les expressions conditionnelles, les expressions logiques, les expressions relationnelles et les expressions arithmétiques. MIDL n’autorise pas les appels de fonction dans les expressions et n’autorise pas les opérateurs d’incrémentation et de décrémentation. Séparez plusieurs expressions par des virgules.

</dd> </dl>

## <a name="remarks"></a>Remarques

Si le **\[ premier \_ est \]** un attribut n’est pas présent, ou si l’index spécifié est un nombre négatif, l’élément de tableau zéro est le premier élément transmis.

La **\[ première \_ est \]** l’attribut peut également aider à déterminer les valeurs des index de tableau correspondant au **\[** [**dernier \_ is**](last-is.md) **\]** ou **\[** [**Length \_ est**](length-is.md) **\]** attribute quand ces attributs ne sont pas spécifiés. La relation entre ces index de tableau est la suivante :

``` syntax
length = last - first + 1
```

La relation suivante doit également contenir les éléments suivants :

``` syntax
0 <= first_is <= max_is
```

La relation suivante doit contenir lorsque **\[** [**Max \_ est**](max-is.md) **\] <= 0 :**

``` syntax
first_is == 0
```

La **\[ première \_ est \]** l’attribut ne peut pas être utilisé en même temps que l’attribut de **\[** [**chaîne**](string.md) **\]** .

L’utilisation d’une expression constante avec la **\[ première \_ est \]** l’attribut est une utilisation inappropriée de l’attribut. Il est légal, mais inefficace, et se traduira par un code de marshaling plus lent.

## <a name="examples"></a>Exemples

``` syntax
HRESULT Proc1(
    [in] short First,
    [first_is(First)] Arr[10]);
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[attributs de champ \_](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**la dernière \_ est**](last-is.md)
</dt> <dt>

[**la longueur \_ est**](length-is.md)
</dt> <dt>

[**le nombre maximal \_ est**](max-is.md)
</dt> <dt>

[**min \_ est**](min-is.md)
</dt> <dt>

[**la taille \_ est**](size-is.md)
</dt> <dt>

[**chaîne**](string.md)
</dt> </dl>

 

 