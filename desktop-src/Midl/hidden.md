---
title: attribut masqué
description: L’attribut \ Hidden \ indique que l’élément existe, mais ne doit pas être affiché dans un navigateur orienté utilisateur.
ms.assetid: bf1f9270-fb93-4421-804e-d56e2c863bbd
keywords:
- MIDL d’attribut masqué
topic_type:
- apiref
api_name:
- hidden
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1718351ef84199b60ba720ed2f3569cfa78a0a50
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093538"
---
# <a name="hidden-attribute"></a>attribut masqué

L’attribut **\[ Hidden \]** indique que l’élément existe, mais ne doit pas être affiché dans un navigateur orienté utilisateur.

``` syntax
[
    other-attributes, 
    hidden
] 
element element-name
{
    definitions
}

[other-attributes, hidden] function-type function-name(optional-parameter-list);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*autres attributs* 
</dt> <dd>

Zéro, un ou plusieurs attributs MIDL facultatifs.

</dd> <dt>

*appartient* 
</dt> <dd>

L’une des directives suivantes : [**coclass**](coclass.md), [**dispinterface**](dispinterface.md), [**interface**](interface.md)ou [**Library**](library.md).

</dd> <dt>

*nom de l’élément* 
</dt> <dd>

Nom que d’autres composants logiciels peuvent utiliser pour décourber l’élément actuel.

</dd> <dt>

*Description* 
</dt> <dd>

Spécifie les instructions qui composent la définition de l’élément.

</dd> <dt>

*type de fonction* 
</dt> <dd>

Type de retour de la fonction.

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Nom utilisé pour appeler la fonction.

</dd> <dt>

*liste de paramètres facultatifs* 
</dt> <dd>

Zéro, un ou plusieurs paramètres de fonction.

</dd> </dl>

## <a name="remarks"></a>Notes

L’attribut **\[ Hidden \]** vous permet de supprimer des membres de votre interface (en les protégeant d’un autre usage) tout en conservant la compatibilité avec le code existant. Vous pouvez utiliser l' **\[ attribut \] Hidden** sur les propriétés, les méthodes et les instructions de [**coclasse**](coclass.md), [**dispinterface**](dispinterface.md), [**interface**](interface.md)et [**Library**](library.md) .

Lorsqu’il est spécifié pour une bibliothèque, l’attribut **\[ Hidden \]** empêche l’affichage de la totalité de la bibliothèque. Cette utilisation est destinée aux contrôles. Les hôtes doivent créer une bibliothèque de types qui encapsule le contrôle avec des propriétés étendues.

### <a name="flags"></a>Indicateurs

VARFLAG \_ FHIDDEN, FUNCFLAG \_ FHIDDEN, TYPEFLAG \_ FHIDDEN

## <a name="examples"></a>Exemples

``` syntax
[hidden, vararg] SAFEARRAY (int) SecretFunc(
    [in, out] SAFEARRAY (variant) *varP) ;

[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    hidden, 
    version (3.0)
] 
library HiddenLib 
{
    /* Library definition statements here. */
};
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**coclasse**](coclass.md)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[**Bibliothèque**](library.md)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> </dl>

 

 