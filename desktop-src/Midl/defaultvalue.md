---
title: defaultvalue (attribut)
description: L’attribut \ DefaultValue \ vous permet de spécifier une valeur par défaut pour un paramètre facultatif typé.
ms.assetid: a974a0f7-7b08-4f17-bb28-0e23e6aa97db
keywords:
- MIDL d’attribut DefaultValue
topic_type:
- apiref
api_name:
- defaultvalue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04f4efaac16325ec77721665a4dee14c9514a192
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093678"
---
# <a name="defaultvalue-attribute"></a>defaultvalue (attribut)

L’attribut **\[ DefaultValue \]** vous permet de spécifier une valeur par défaut pour un paramètre facultatif typé.

``` syntax
interface interface-name
{
  return-type function-name(
        mandatory-param-list, 
        [[attribute-list,] defaultvalue(value)] param-type param-name
        [ , optional-param-list]);
}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom de l’interface* 
</dt> <dd>

Spécifie le nom de l’interface.

</dd> <dt>

*type de retour* 
</dt> <dd>

Spécifie le type de retour de la fonction.

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Spécifie le nom de la fonction à laquelle l’attribut **\[ DefaultValue \]** sera appliqué.

</dd> <dt>

*obligatoire-param-List* 
</dt> <dd>

Spécifie un ou plusieurs paramètres obligatoires.

</dd> <dt>

*liste d’attributs* 
</dt> <dd>

Spécifie une liste d’un ou plusieurs attributs, séparés par des virgules, qui s’appliquent au paramètre.

</dd> <dt>

*Param-type* 
</dt> <dd>

Indique le type du paramètre facultatif.

</dd> <dt>

*nom du paramètre* 
</dt> <dd>

Spécifie le nom du paramètre facultatif.

</dd> <dt>

*Liste facultative-param* 
</dt> <dd>

Spécifie zéro, un ou plusieurs paramètres supplémentaires, chacun d’entre eux devant avoir une valeur par défaut.

</dd> </dl>

## <a name="remarks"></a>Notes

La valeur par défaut que vous spécifiez pour le paramètre peut être n’importe quelle constante, ou une expression qui correspond à une constante, qui peut être représentée par un **Variant**. Plus précisément, vous ne pouvez pas appliquer l’attribut **\[ \] DefaultValue** à un paramètre qui est une structure, un tableau ou un type **SAFEARRAY** .

Le compilateur MIDL accepte l’ordonnancement des paramètres suivant (de gauche à droite) :

1.  Paramètres obligatoires (paramètres qui n’ont pas les attributs **\[ DefaultValue \]** ou **\[** [**facultatifs**](optional.md) **\]** )
2.  paramètres facultatifs avec ou sans l’attribut **\[ DefaultValue \]** ,
3.  paramètres avec l’attribut **\[ facultatif \]** et sans l’attribut **\[ DefaultValue \]** ,
4.  **\[** paramètre [**LCID**](lcid.md) **\]** , le cas échéant,
5.  **\[**[**retVal**](retval.md) **\]** paramètre

## <a name="examples"></a>Exemples

``` syntax
interface IFace : IUnknown
{
    HRESULT Ex1([defaultvalue(44)] LONG i);
    HRESULT Ex2([defaultvalue(44)] SHORT i);
...
};

interface QueryDef : IUnknown
{
    HRESULT OpenRecordset( [in, defaultvalue(DBOPENTABLE)]
    LONG Type,
    [out,retval] Recordset **pprst);
}
//  Type is now known to be a LONG type (good for browser in VBA and
//  good for a C/C++ programmer) and has a default value of
//  DBOPENTABLE
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[**LCID**](lcid.md)
</dt> <dt>

[**facultatif**](optional.md)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**retval**](retval.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 