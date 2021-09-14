---
title: defaultbind (attribut)
description: L’attribut \ defaultbind \ indique la propriété unique pouvant être liée qui représente le mieux l’objet.
ms.assetid: 8cf0922a-3d7c-404d-b4fd-edbd772987bf
keywords:
- MIDL de l’attribut defaultbind
topic_type:
- apiref
api_name:
- defaultbind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 518c11da8d5f9b0762843c5b69292562a94b80c4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093686"
---
# <a name="defaultbind-attribute"></a>defaultbind (attribut)

L’attribut **\[ defaultbind \]** indique la propriété unique pouvant être liée qui représente le mieux l’objet.

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, defaultbind [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*interface-attribut-List* 
</dt> <dd>

Spécifie une liste d’un ou plusieurs attributs qui s’appliquent à l’ensemble de l’interface. Lorsque deux attributs d’interface ou plus sont présents, ils doivent être séparés par des virgules.

</dd> <dt>

*nom de l’interface* 
</dt> <dd>

Spécifie le nom de l’interface.

</dd> <dt>

*liste d’attributs* 
</dt> <dd>

Spécifie une liste d’un ou plusieurs attributs qui s’appliquent à la fonction. Lorsque deux attributs d’interface ou plus sont présents, ils doivent être séparés par des virgules.

</dd> <dt>

*ReturnType* 
</dt> <dd>

Spécifie le type de retour de la fonction.

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Spécifie le nom de la fonction à laquelle l’attribut **\[ defaultbind \]** sera appliqué.

</dd> <dt>

*params* 
</dt> <dd>

Liste des paramètres de la fonction.

</dd> </dl>

## <a name="remarks"></a>Notes

Les propriétés qui ont l’attribut **\[ defaultbind \]** doivent également avoir l' **\[** attribut pouvant être [**lié**](bindable.md) **\]** . Une seule propriété dans une interface ou une dispinterface peut avoir l’attribut **\[ defaultbind \]** .

Cet attribut est utilisé par les conteneurs qui ont un modèle utilisateur impliquant la liaison à un objet plutôt que la liaison à une propriété d’un objet. Un objet peut prendre en charge la liaison de données mais ne pas avoir cet attribut.

### <a name="flags"></a>Indicateurs

FUNCFLAG \_ FDEFAULTBIND, VARFLAG \_ FDEFAULTBIND

## <a name="examples"></a>Exemples

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, 
         defaultbind, displaybind] long Size(void);

        [id(1), propput, bindable, 
         defaultbind, displaybind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 