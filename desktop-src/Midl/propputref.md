---
title: propputref (attribut)
description: L’attribut \ propputref \ spécifie une fonction de définition de propriété qui utilise une référence au lieu d’une valeur.
ms.assetid: 84f1cd08-3c42-4a6d-bb1d-0bfd3f4c33f2
keywords:
- propputref, attribut MIDL
topic_type:
- apiref
api_name:
- propputref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead5ccf7f9dc6a59580b7c3e3576f3c7503ccafc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093246"
---
# <a name="propputref-attribute"></a>propputref (attribut)

L’attribut **\[ PROPPUTREF \]** spécifie une fonction de définition de propriété qui utilise une référence au lieu d’une valeur.

``` syntax
[propputref [,optional-property-attributes]] return-type function-name( parameters);
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

Une fonction qui a l’attribut **\[ PROPPUTREF \]** doit également avoir, en tant que dernier paramètre, un pointeur qui a l' **\[** attribut [**in**](in.md) **\]** .

La propriété doit avoir le même nom que la fonction. Au maximum, l’un des **\[** attributs [**propget**](propget.md) **\]** , **\[** [**propput**](propput.md) **\]** et **\[ PROPPUTREF \]** peut être spécifié pour une fonction.

### <a name="flags"></a>Indicateurs

APPELER \_ PROPERTYPUTREF

## <a name="examples"></a>Exemples

``` syntax
interface InMyFace : IDispatch 
{
    [propget, 
     helpstring("A meaningful comment."), 
     id(1)] HRESULT Method2([out, retval] YourInterface** ReturnVal); 
    [propputref, 
     helpstring("Another meaningful comment."), 
     id(1)] HRESULT Method2([in] YourPoint* Point);
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**dans**](in.md)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 