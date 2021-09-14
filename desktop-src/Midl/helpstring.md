---
title: attribut HelpString
description: L’attribut \ HelpString \ spécifie une chaîne de caractères utilisée pour décrire l’élément auquel il s’applique.
ms.assetid: f05d3fdd-d975-4f0e-8181-07e16288ff48
keywords:
- attribut HelpString MIDL
topic_type:
- apiref
api_name:
- helpstring
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c58bbe61b10e2f223cf9f662f10d95ca72819b02
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093546"
---
# <a name="helpstring-attribute"></a>attribut HelpString

L’attribut **\[ helpString \]** spécifie une chaîne de caractères utilisée pour décrire l’élément auquel il s’applique. Vous pouvez appliquer l’attribut **\[ helpString \]** aux instructions Library, importlib, interface, dispinterface, module ou coclass, typedefs, propriétés et méthodes.

``` syntax
[
    helpstring(help-text-string)
    [, optional-attribute-list]
] 
element element-name
{
    definition
}

[idl-statement, helpstring(help-text-string)]
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*Help-Text-String* 
</dt> <dd>

Chaîne de caractères se terminant par zéro qui contient le texte d’aide.

</dd> <dt>

*Optional-attribute-List* 
</dt> <dd>

Zéro, une ou plusieurs instructions d’attribut MIDL.

</dd> <dt>

*appartient* 
</dt> <dd>

L’une des directives suivantes : [**Library**](library.md), **\[** [**importlib**](importlib.md) **\]** , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **Method**, **Property** ou [**coclass**](coclass.md).

</dd> <dt>

*nom de l’élément* 
</dt> <dd>

Nom que d’autres composants logiciels peuvent utiliser pour décourber l’élément actuel

</dd> <dt>

*définition* 
</dt> <dd>

Spécifie les instructions qui composent la définition de l’élément.

</dd> <dt>

*IDL-Statement* 
</dt> <dd>

Une instruction de définition d’interface MIDL telle que [**propget**](propget.md) ou [**propput**](propput.md).

</dd> </dl>

## <a name="remarks"></a>Notes

Utilisez les fonctions [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) dans les interfaces [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) et [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) pour récupérer la chaîne d’aide.

## <a name="examples"></a>Exemples

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("Lines 1.0 Type Library"),
    version(1.0)
]
library Lines
{
     [
         uuid(1e123456-1f3c-1069-996b-00dd010fe676), 
         helpstring("Line object."),
         oleautomation,
         dual
     ]
     interface ILine : IDispatch                         
     {
         [propget, helpstring("Returns and sets RGB color.")]
         HRESULT Color([out, retval] long* ReturnVal); 
         [propput, helpstring("Returns and sets RGB color.")]
         HRESULT Color([in] long rgb);
     }
};
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Bibliothèque**](library.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**modules**](module.md)
</dt> <dt>

[**coclasse**](coclass.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 