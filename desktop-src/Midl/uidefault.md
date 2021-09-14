---
title: uidefault (attribut)
description: L’attribut \ UIDefault \ indique que le membre des informations de type est le membre par défaut à afficher dans l’interface utilisateur.
ms.assetid: e789be38-a509-437d-89c9-ebbc830e5ae2
keywords:
- MIDL de l’attribut UIDefault
topic_type:
- apiref
api_name:
- uidefault
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcef39f36abad7c7cb5562b2d892761bd1bb7b5b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093101"
---
# <a name="uidefault-attribute"></a>uidefault (attribut)

L’attribut **\[ UIDefault \]** indique que le membre d’informations de type est le membre par défaut à afficher dans l’interface utilisateur.

``` syntax
[method-attribute-list, uidefault]return-type method-name(method-parameter-list)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*méthode-attribute-List* 
</dt> <dd>

Autres attributs qui s’appliquent à la méthode.

</dd> <dt>

*type de retour* 
</dt> <dd>

Type des données retournées par la méthode à la fin de l’exécution.

</dd> <dt>

*nom de méthode* 
</dt> <dd>

Nom de la méthode.

</dd> <dt>

*méthode-parameter-list* 
</dt> <dd>

Zéro, un ou plusieurs paramètres pour la méthode.

</dd> </dl>

## <a name="remarks"></a>Notes

l’application de l’attribut **\[ uidefault \]** à un membre d’une interface ou d’une dispinterface indique Visual Basic, au moment du design, d’afficher automatiquement cet événement ou cette propriété à l’utilisateur. cela signifie que lorsque l’utilisateur double-clique sur un objet, Visual Basic passe à l’événement dans l’interface source par défaut qui a l’attribut **\[ uidefault \]** . quand l’utilisateur sélectionne un objet, l’explorateur de propriétés de Visual Basic affiche la propriété dans l’interface source par défaut qui a cet attribut. si aucun événement ou propriété n’a l’attribut **\[ uidefault \]** , Visual Basic affiche le premier événement ou la première propriété figurant dans l’interface par défaut.

### <a name="typeflag-representation"></a>Représentation TYPEFLAG

Présence de FUNCFLAG \_ FUIDEFAULT ou VARFLAG \_ FUIDEFAULT

## <a name="examples"></a>Exemples

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IForm: IDispatch
{
    [propget]HRESULT Backcolor([out, retval] long *Value);
    [propput]HRESULT Backcolor([in] long Value);
    [propget, uidefault]HRESULT Name([out, retval] BSTR *Value);
    [propput, uidefault]HRESULT Name([in] BSTR Value);
}
[
    odl,
    dual,
    uuid(87654321-1234-1234-1234-123456789ABC),
    restricted
] 
interface IFormEvents: IDispatch
{
    [uidefault]HRESULT Click();
    HRESULT Resize();
}

[
    uuid(12345678-1234-1234-1234-987654321ABC)
]
coclass Form
{
    [default] interface IForm;
    [default, source] interface IFormEvents;
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 