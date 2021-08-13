---
title: propput (attribut)
description: L’attribut \ propput \ spécifie une fonction de définition de propriété. La propriété doit avoir le même nom que la fonction.
ms.assetid: ffd8af15-42a4-4852-a29b-1fc66f673978
keywords:
- propput, attribut MIDL
topic_type:
- apiref
api_name:
- propput
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f0e34d4826abfa2df6cd1262ccd4bcec04344f4500ddf5c146816d23f6261c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641932"
---
# <a name="propput-attribute"></a>propput (attribut)

L’attribut **\[ propput \]** spécifie une fonction de définition de propriété. La propriété doit avoir le même nom que la fonction *.*

``` syntax
[propput [,optional-property-attributes]] return-type function-name( parameters);
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

*function-name* 
</dt> <dd>

Nom de la procédure distante.

</dd> <dt>

*parameters* 
</dt> <dd>

Zéro, un ou plusieurs paramètres à la procédure distante.

</dd> </dl>

## <a name="remarks"></a>Remarques

Une fonction qui a l’attribut **\[ propput \]** doit également avoir, en tant que dernier paramètre, un paramètre qui a l' **\[** attribut [**in**](in.md) **\]** .

Au maximum, vous **\[** [](propget.md) **\]** pouvez spécifier un propget, **\[ propput \]** et **\[** [**PROPPUTREF**](propputref.md) **\]** pour une fonction.

Si l' **\[** attribut [**LCID**](lcid.md) **\]** est utilisé dans la liste des paramètres d’une fonction qui contient un paramètre avec l’attribut **\[ propput \]** , le paramètre **\[ LCID \]** doit être le dernier de la dernière.

### <a name="flags"></a>Indicateurs

APPELER \_ PROPERTYPUT

## <a name="examples"></a>Exemples

``` syntax
interface InMyFace : IDispatch                         
{
    [propget, 
     helpstring("A meaningful comment.")] HRESULT Method1(
         [out, retval] int* ReturnVal); 

    [propput, 
     helpstring("Another meaningful comment.")] HRESULT Method1(
         [in] int Value);
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Différences entre MIDL et MKTYPLIB](differences-between-midl-and-mktyplib.md)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 