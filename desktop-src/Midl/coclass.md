---
title: coclass (attribut)
description: L’instruction coclass fournit une liste des interfaces prises en charge pour un objet composant.
ms.assetid: 2c636327-ad18-4087-b495-d1aa84a07f48
keywords:
- attribut de coclasse MIDL
topic_type:
- apiref
api_name:
- coclass
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba95b38675869637c679a2409a82fb812709ec8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093726"
---
# <a name="coclass-attribute"></a>coclass (attribut)

L’instruction **coclass** fournit une liste des interfaces prises en charge pour un objet composant.

``` syntax
[
    coclass-attribute-list
]
coclass classname
{
    [
        interface-attributes
    ] 
    [interface | dispinterface] interfacename 
    {
  . . . 
    }
}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*coclass-attribute-List* 
</dt> <dd>

L' **\[** attribut [**UUID**](uuid.md) **\]** est requis sur une **coclasse**. Il s’agit du même **\[ UUID \]** qui est inscrit en tant que CLSID dans la base de données d’inscription du système. Les **\[** [](helpstring.md) **\]** attributs HelpString, **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**Licensed**](licensed.md), **\]** **\[** [**version**](version.md) **\]** , **\[** [**Control**](control.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** et **\[** [**AppObject**](appobject.md) **\]** sont acceptés, mais pas obligatoires, avant une définition de **coclasse** .

</dd> <dt>

*NomClasse* 
</dt> <dd>

Nom par lequel l’objet commun est connu dans la bibliothèque de types.

</dd> <dt>

*interface-attributs* 
</dt> <dd>

Attributs facultatifs pour l’interface ou dispinterface. Les **\[** attributs [**source**](source.md) **\]** , **\[** [**default**](default.md) **\]** et **\[** [**Restricted**](restricted.md) **\]** sont acceptés sur une interface ou dispinterface dans une **coclasse**.

</dd> <dt>

*InterfaceName* 
</dt> <dd>

Soit une interface déclarée avec le mot clé [**interface**](interface.md) , soit une dispinterface déclarée avec le mot clé [**dispinterface**](dispinterface.md) .

</dd> </dl>

## <a name="remarks"></a>Notes

Le modèle d’objet de composant Microsoft définit une classe en tant qu’implémentation de qui autorise **QueryInterface** entre un ensemble d’interfaces.

## <a name="examples"></a>Exemples

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    version(1.0), 
    helpstring("A class"), 
    helpcontext(2481), appobject
] 
coclass myapp 
{ 
    [source] interface IMydocfuncs : IUnknown; 
    dispinterface DMydocfuncs; 
}; 
 
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
coclass mycoclass 
{ 
    [restricted] interface iface1; 
    interface iface2; 
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**appobject**](appobject.md)
</dt> <dt>

[**régulation**](control.md)
</dt> <dt>

[**valeurs**](default.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**masquer**](hidden.md)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[**licensed**](licensed.md)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**sensible**](restricted.md)
</dt> <dt>

[**code**](source.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**uuid**](uuid.md)
</dt> <dt>

[**Version**](version.md)
</dt> </dl>

 

 