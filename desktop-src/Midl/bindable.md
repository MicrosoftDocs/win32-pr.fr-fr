---
title: bindable (attribut)
description: L’attribut \ Binder \ indique que la propriété prend en charge la liaison de données.
ms.assetid: ba09096d-a2f7-4958-827c-0fba19ded26f
keywords:
- MIDL d’attribut pouvant être lié
topic_type:
- apiref
api_name:
- bindable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33911ba5ff55ef5e3dd377613dd98532ecd97486
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106509649"
---
# <a name="bindable-attribute"></a>bindable (attribut)

L’attribut **\[ pouvant \] être lié** indique que la propriété prend en charge la liaison de données.

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable[, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*interface-attribut-List* 
</dt> <dd>

Spécifie une liste de zéro ou plusieurs attributs IDL qui s’appliquent à l’ensemble de l’interface. Lorsque deux attributs d’interface ou plus sont présents, ils doivent être séparés par des virgules.

</dd> <dt>

*nom de l’interface* 
</dt> <dd>

Spécifie le nom de l’interface.

</dd> <dt>

*liste d’attributs* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs qui s’appliquent au prototype de fonction pour une propriété ou une méthode dans une [**interface**](interface.md) ou une [**dispinterface**](dispinterface.md). Les attributs suivants sont valides : [**\[ \] helpString**](helpstring.md), [**\[ \] HelpContext**](helpcontext.md), [**\[ String \]**](string.md), [**\[ defaultbind \]**](defaultbind.md), [**\[ displaybind \]**](displaybind.md), [**\[ immediatebind \]**](immediatebind.md), [**\[ propget \]**](propget.md), [**\[ propput \]**](propput.md), [**\[ PROPPUTREF \]**](propputref.md)et [**\[ vararg \]**](vararg.md). Si **vararg** est spécifié, le dernier paramètre doit être un tableau sécurisé de type Variant. Séparez plusieurs attributs par des virgules.

</dd> <dt>

*ReturnType* 
</dt> <dd>

Spécifie le type de retour de la fonction.

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Spécifie le nom de la fonction à laquelle l’attribut **\[ pouvant être lié \]** sera appliqué.

</dd> <dt>

*params* 
</dt> <dd>

Liste des paramètres de la fonction.

</dd> </dl>

## <a name="remarks"></a>Notes

En prenant en charge la liaison de données, l’attribut **\[ pouvant être lié \]** permet au client d’être averti chaque fois qu’une propriété a une valeur modifiée. (Si vous souhaitez que le client soit averti des modifications imminentes apportées à une propriété, utilisez l’attribut [**\[ modification \]**](requestedit.md) .)

Étant donné que l’attribut **\[ pouvant être lié \]** fait référence à la propriété dans son ensemble, il doit être spécifié partout où la propriété est définie. Par conséquent, vous devez spécifier l’attribut à la fois sur la fonction d’accès à la propriété et la fonction de définition de propriété.

### <a name="flags"></a>Indicateurs

FUNCFLAG \_ FBINDABLE, VARFLAG \_ FBINDABLE

## <a name="examples"></a>Exemples

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676)
]
dispinterface MyObject 
{ 
    properties: 
    methods: 
        [id(1), propget, bindable, defaultbind, displaybind] long x(); 
        [id(1), propput, bindable, 
        defaultbind, displaybind] HRESULT x(long rhs); 
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**defaultbind**](defaultbind.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**displaybind**](displaybind.md)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**immediatebind**](immediatebind.md)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**requestedit**](requestedit.md)
</dt> <dt>

[**chaîne**](string.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**vararg**](vararg.md)
</dt> </dl>

 

 