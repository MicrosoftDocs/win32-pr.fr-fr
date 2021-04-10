---
title: propget (attribut)
description: L’attribut \ propget \ spécifie une fonction d’accesseur de propriété. La propriété doit avoir le même nom que la fonction.
ms.assetid: 0b76ece3-e19b-4c80-883c-ff414bc2e435
keywords:
- attribut propget MIDL
topic_type:
- apiref
api_name:
- propget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6337409e021670c282400d38b97543687fa81c2a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031084"
---
# <a name="propget-attribute"></a>propget (attribut)

L’attribut **\[ propget \]** spécifie une fonction d’accesseur de propriété. La propriété doit avoir le même nom que la fonction.

``` syntax
[propget [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*attributs facultatifs* 
</dt> <dd>

Zéro, un ou plusieurs attributs de propriété.

</dd> <dt>

*type de retour* 
</dt> <dd>

Type des données retournées par la procédure distante.

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Nom de la procédure distante.

</dd> <dt>

*parameters* 
</dt> <dd>

Zéro, un ou plusieurs paramètres à la procédure distante.

</dd> </dl>

## <a name="remarks"></a>Notes

Une fonction qui a l’attribut propget doit également avoir, en tant que dernier paramètre, un type pointeur avec les **\[** attributs [**out**](out-idl.md) **\]** et **\[** [**retVal**](retval.md) **\]** . Si le dernier paramètre n’a pas les \[ attributs out, retval \] , la valeur de retour de la fonction est traitée comme un \[ paramètre out, retval \] . Par exemple, une fonction avec le prototype

``` syntax
[propget] short MyFunction([in] long aLongValue);
```

est traité comme

``` syntax
[propget] HRESULT MyFunction([in] long aLongValue, [out,retval] short *outValue);
```

Au maximum, vous pouvez spécifier un **\[ propget \]**, **\[** [**propput**](propput.md) **\]** et **\[** [**PROPPUTREF**](propputref.md) **\]** pour une fonction.

Si l' **\[** attribut [**LCID**](lcid.md) **\]** est utilisé dans la liste des paramètres d’une fonction qui contient un paramètre avec l' **\[** attribut [**propput**](propput.md) **\]** , le paramètre **\[ LCID \]** doit être le dernier de la dernière.

### <a name="flags"></a>Indicateurs

APPELER \_ PropertyGet (

## <a name="examples"></a>Exemples

``` syntax
interface MyInterface : IDispatch                         
{                
    [propget, 
     helpstring("A meaningful comment.")] HRESULT Method1(
         [out, retval] int* ReturnVal); 

    [propput, 
     helpstring("Another meaningful comment.")] HRESULT Method1(
         [in] int Value);
        
    [propget, 
     helpstring("A meaningful comment."), id(1)] HRESULT Method2(
         [out, retval] YourInterface** ReturnVal); 

    [propputref, 
     helpstring("Another meaningful comment."), 
     id(1)] HRESULT Method2([in] YourPoint* Point);
}                 
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**à**](out-idl.md)
</dt> <dt>

[**retval**](retval.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 