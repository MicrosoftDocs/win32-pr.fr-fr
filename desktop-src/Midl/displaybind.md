---
title: displaybind (attribut)
description: L’attribut \ displaybind \ indique une propriété qui doit être affichée à l’utilisateur comme pouvant être liée.
ms.assetid: 047a58b2-3ae2-437a-992f-a9d1541decbe
keywords:
- MIDL de l’attribut DisplayBind
topic_type:
- apiref
api_name:
- displaybind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f015954a7b1fe07d4ecf61e9a4ba4da4c932e65c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725436"
---
# <a name="displaybind-attribute"></a>displaybind (attribut)

L’attribut **\[ displaybind \]** indique une propriété qui doit être affichée à l’utilisateur comme pouvant être liée.

``` syntax
[
  [interface-attribute-list]
]
interface | dispinterface interface-name
{
    [bindable, displaybind [ , attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*interface-attribut-List* 
</dt> <dd>

Spécifie une liste facultative d’attributs d’interface.

</dd> <dt>

*nom de l’interface* 
</dt> <dd>

Nom de l’interface.

</dd> <dt>

*liste d’attributs* 
</dt> <dd>

Spécifie une liste d’un ou plusieurs attributs, séparés par des virgules, qui s’appliquent au type de retour de fonction.

</dd> <dt>

*ReturnType* 
</dt> <dd>

Spécifie le type de retour de la fonction.

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Spécifie le nom de la fonction à laquelle l’attribut **\[ displaybind \]** sera appliqué.

</dd> <dt>

*params* 
</dt> <dd>

Liste des paramètres de la fonction.

</dd> </dl>

## <a name="remarks"></a>Notes

Les propriétés qui ont l’attribut **\[ displaybind \]** doivent également avoir l' **\[** attribut pouvant être [**lié**](bindable.md) **\]** . Un objet peut prendre en charge la liaison de données mais ne pas avoir cet attribut.

### <a name="flags"></a>Indicateurs

FUNCFLAG \_ FDISPLAYBIND, VARFLAG \_ FDISPLAYBIND

## <a name="examples"></a>Exemples

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, defaultbind, 
         displaybind] long Size(void);

        [id(1), propput, bindable, defaultbind, 
         displaybind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 