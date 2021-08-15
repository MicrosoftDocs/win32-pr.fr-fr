---
title: appobject (attribut)
description: L’attribut \ AppObject \ identifie la coclasse comme un objet application, qui est associé à une application EXE complète.
ms.assetid: f4fcdf55-7431-4d66-8a46-f741c52fbe56
keywords:
- MIDL de l’attribut AppObject
topic_type:
- apiref
api_name:
- appobject
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f54cbe8d5c1c7a573216ae9cb55075ba3b3766d0d8c7898233be9364488131e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808331"
---
# <a name="appobject-attribute"></a>appobject (attribut)

L’attribut **\[ AppObject \]** identifie la [**coclasse**](coclass.md) comme un objet application, qui est associé à une application exe complète.

``` syntax
[
    uuid(uuid-number), 
    appobject 
  [, coclass-attribute-list]
]
coclass classname 
{ 
    [coclass definition]
}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*UUID-Number* 
</dt> <dd>

Spécifie un numéro d’identification unique universel pour la [**coclasse**](coclass.md).

</dd> <dt>

*coclass-attribute-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs qui s’appliquent à l’instruction [**coclass**](coclass.md) . Les attributs **de coclasse** autorisés sont [**\[ helpString \]**](helpstring.md), [**\[ HelpContext \]**](helpcontext.md), [**\[ Licensed \]**](licensed.md), [**\[ version \]**](version.md), [**\[ Control \]**](control.md)et [**\[ Hidden \]**](hidden.md).

</dd> <dt>

*NomClasse* 
</dt> <dd>

Spécifie le nom par lequel l’objet composant est connu dans la bibliothèque de types.

</dd> <dt>

*définition de coclasse* 
</dt> <dd>

Spécifie les instructions qui composent la définition de [**coclasse**](coclass.md) .

</dd> </dl>

## <a name="remarks"></a>Remarques

L’attribut **\[ AppObject \]** indique également que les fonctions et les propriétés de la [**coclasse**](coclass.md) sont globalement disponibles dans la bibliothèque de types actuelle.

La représentation TYPEFLAG de cet attribut est TYPEFLAG \_ FAPPOBJECT

## <a name="examples"></a>Exemples

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("Hello Class"),
    appobject
] 
coclass Hello
{
    [default] interface IHello : IUnknown;
    interface IDispatch;
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**coclasse**](coclass.md)
</dt> <dt>

[**régulation**](control.md)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**masquer**](hidden.md)
</dt> <dt>

[**licensed**](licensed.md)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Version**](version.md)
</dt> </dl>

 

 