---
title: defaultcollelem (attribut)
description: L’attribut \ defaultcollelem \ signale une propriété comme fonction d’accesseur pour un élément de la collection par défaut.
ms.assetid: e409f845-3f26-4551-abda-86c4776160aa
keywords:
- MIDL de l’attribut defaultcollelem
topic_type:
- apiref
api_name:
- defaultcollelem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45fdbd59ca954d955fc5598b2bc2dc7a39ee14b2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031186"
---
# <a name="defaultcollelem-attribute"></a>defaultcollelem (attribut)

L’attribut **\[ defaultcollelem \]** signale une propriété comme fonction d’accesseur pour un élément de la collection par défaut.

``` syntax
[property-attribute-list, defaultcollelem] return-type property-name(prop-param-list)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*property-attribute-List* 
</dt> <dd>

Autres attributs qui s’appliquent à la propriété.

</dd> <dt>

*type de retour* 
</dt> <dd>

Spécifie le type de retour de la fonction.

</dd> <dt>

*nom de la propriété* 
</dt> <dd>

Nom de la propriété.

</dd> <dt>

*prop-param-List* 
</dt> <dd>

Liste de zéro ou plusieurs paramètres associés à la propriété.

</dd> </dl>

## <a name="remarks"></a>Notes

L’attribut **\[ defaultcollelem \]** est utilisé pour l’optimisation du code® Visual BasicÂ. Si un membre d’une interface ou d’une dispinterface est marqué comme fonction d’accesseur, l’appel passera directement à ce membre.

L’utilisation de **\[ defaultcollelem \]** doit être cohérente pour une propriété. Par exemple, si vous utilisez l’attribut sur une propriété *obtenir* , il doit également être présent sur une propriété *Let* .

### <a name="typeflags-representation"></a>Représentation TYPEFLAGS

Présence de FUNCFLAG \_ FDEFAULTCOLLELEM ou VARFLAG \_ FDEFAULTCOLLELEM.

## <a name="examples"></a>Exemples

``` syntax
//A form has a button on it named Button1. 
//To enable use of the property syntax and efficient use of the !
//syntax, the form describes itself in type info this way.
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("This is IForm"),
    restricted
]
interface IForm1: IForm
{
    [propget, defaultcollelem] HRESULT Button1(
        [out, retval] Button *Value);
}

//User code may access the button using property syntax or ! syntax.

Sub Test()
Dim f as Form1
Dim b1 As Button
Dim b2 As Button

Set f = Form1

Set b1 = f.Button1        ' Property syntax
Set b = f!Button1        ' ! syntax
End Sub
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 