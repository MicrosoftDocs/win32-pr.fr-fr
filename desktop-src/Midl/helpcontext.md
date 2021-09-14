---
title: helpcontext (attribut)
description: L’attribut \ HelpContext \ spécifie un identificateur de contexte qui permet à l’utilisateur d’afficher des informations sur cet élément dans le fichier d’aide.
ms.assetid: 44a60c75-be69-4cd9-afb0-5eb988830e6c
keywords:
- l’attribut HelpContext MIDL
topic_type:
- apiref
api_name:
- helpcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75a8811a73515528981a8214caba3fe2778e2ea9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093558"
---
# <a name="helpcontext-attribute"></a>helpcontext (attribut)

L' \[ attribut **HelpContext** \] spécifie un identificateur de contexte qui permet à l’utilisateur d’afficher des informations sur cet élément dans le fichier d’aide.

``` syntax
[
    uuid(uuid-number), 
    helpcontext(helpcontext-value)
    [, attribute-list]
] 
element element-name
{
    definitions
}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*UUID-Number* 
</dt> <dd>

Spécifie un numéro d’identification unique universel pour la [**bibliothèque**](library.md), \[ [**importlib**](importlib.md) \] , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **Methods**, **\[ Property \]** ou [**coclass**](coclass.md).

</dd> <dt>

*HelpContext-valeur* 
</dt> <dd>

Entier unique qui identifie le texte d’aide associé à l’élément MIDL actuel.

</dd> <dt>

*liste d’attributs* 
</dt> <dd>

Spécifie une liste d’un ou plusieurs attributs qui s’appliquent à l’élément MIDL dans son ensemble.

</dd> <dt>

*appartient* 
</dt> <dd>

L’une des directives suivantes : [**Library**](library.md), \[ [**importlib**](importlib.md) \] , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **Method**, **Property** ou [**coclass**](coclass.md).

</dd> <dt>

*nom de l’élément* 
</dt> <dd>

Nom que d’autres composants logiciels peuvent utiliser pour décourber l’élément actuel.

</dd> <dt>

*Description* 
</dt> <dd>

Spécifie les instructions qui composent la définition de l’élément.

</dd> </dl>

## <a name="remarks"></a>Notes

L' \[ **attribut HelpContext** \] peut être appliqué aux éléments suivants : [**Library**](library.md), \[ [**importlib**](importlib.md) \] , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **Method**, **Property** ou [**coclass**](coclass.md).

La *valeur HelpContext* est un identificateur de contexte 32 bits dans le fichier d’aide qui peut être récupéré avec les fonctions [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) dans les interfaces [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) et [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) .

## <a name="examples"></a>Exemples

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpcontext(7035943),
    helpstring("Hello Class"),
    appobject
] 
coclass Hello
{
    [default, helpcontext(3914972)] interface IHello : IUnknown;
    interface IDispatch;
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**coclasse**](coclass.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[**Bibliothèque**](library.md)
</dt> <dt>

[**modules**](module.md)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 