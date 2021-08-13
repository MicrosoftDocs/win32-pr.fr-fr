---
title: max_is (attribut)
description: L’attribut \ Max \_ is \ désigne la valeur maximale d’un index de tableau valide.
ms.assetid: 8d09f610-cae6-45f6-815c-5ba916d8a5e7
keywords:
- max_is MIDL de l’attribut
topic_type:
- apiref
api_name:
- max_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7dfa7e8cdc5b1df752a3a6eb442524157228d354079f262a27a5514860e335
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642965"
---
# <a name="max_is-attribute"></a>Max \_ is (attribut)

L’attribut **\[ Max \_ is \]** désigne la valeur maximale d’un index de tableau valide.

``` syntax
[max_is(limited-expression-list )]
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*Limited-expression-List* 
</dt> <dd>

Spécifie une ou plusieurs expressions en langage C. Chaque expression prend la valeur d’un entier qui représente l’index de tableau valide le plus élevé. Le compilateur MIDL prend en charge les expressions conditionnelles, les expressions logiques, les expressions relationnelles et les expressions arithmétiques. MIDL n’autorise pas les appels de fonction dans les expressions et n’autorise pas les opérateurs d’incrémentation et de décrémentation. Séparez plusieurs expressions par des virgules.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’attribut **\[ Max \_ is \]** ne correspond pas nécessairement au nombre d’éléments du tableau. Pour un tableau de taille *n* en C, où le premier élément du tableau est l’élément numéro zéro, la valeur maximale pour un index de tableau valide est *n*– 1.

L’attribut **\[ Max \_ is \]** ne peut pas être utilisé en tant qu’attribut de champ en même temps que la **\[** [**taille \_ est**](size-is.md) un **\]** attribut.

Bien qu’il soit légal d’utiliser l’attribut **\[ Max \_ is \]** avec une expression constante, cette opération est inefficace et inutile. Par exemple, utilisez un tableau de taille fixe :

``` syntax
/* transmits values of a[0]... a[MAX_SIZE-1] */ 
HRESULT Proc3([in] short Arr[MAX_SIZE]); 
```

plutôt que :

``` syntax
/* legal but marshaling code is much slower */ 
HRESULT Proc3([in max_is(MAX_SIZE-1)] short Arr[] );
```

## <a name="examples"></a>Exemples

``` syntax
/* if m = 10, there are 11 transmitted elements (a[0]...a[10])*/ 
HRESULT Proc1( 
    [in] short m, 
    [in, max_is(m)] short a[]);  
 
/* if m = 10, the valid range for b is b[0...10][20] */ 
HRESULT Proc2( 
    [in] short m, 
    [in, max_is(m)] short b[][20];
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Attributs de champ](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**min \_ est**](min-is.md)
</dt> <dt>

[**la taille \_ est**](size-is.md)
</dt> </dl>

 

 