---
title: attribut sous licence
description: L’attribut \ Licensed indique que la coclasse à laquelle elle s’applique est concédée sous licence et doit être instanciée à l’aide de IClassFactory2.
ms.assetid: c4789ea2-8ff6-423e-8b69-22a7a5392854
keywords:
- MIDL d’attribut sous licence
topic_type:
- apiref
api_name:
- licensed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b4320157216db18f595d67e172bc49de2d6050551732265060cb5a21339c908
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067203"
---
# <a name="licensed-attribute"></a>attribut sous licence

L’attribut **\[ Licensed \]** indique que la [**coclasse**](coclass.md) à laquelle elle s’applique est concédée sous licence et doit être instanciée à l’aide de [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2).

``` syntax
[
    licensed
    [ , attribute-list ] 
]
coclass classname 
{
  coclass-definition
};
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*liste d’attributs* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs qui s’appliquent à l’instruction [**coclass**](coclass.md) . Les attributs de **coclasse** autorisés sont **\[** [**helpString**](helpstring.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[ Licensed \]**, **\[** [**version**](version.md) **\]** , **\[** [**Control**](control.md) **\]** et **\[** [**Hidden**](hidden.md) **\]** .

</dd> <dt>

*NomClasse* 
</dt> <dd>

Spécifie le nom par lequel l’objet composant est connu dans la bibliothèque de types.

</dd> <dt>

*coclasse-définition* 
</dt> <dd>

Spécifie les instructions qui composent la définition de [**coclasse**](coclass.md) .

</dd> </dl>

## <a name="remarks"></a>Remarques

La gestion des licences est une fonctionnalité de COM qui permet de contrôler la création d’objets. Les objets sous licence ne peuvent être créés que par des clients autorisés à les utiliser. La gestion des licences est implémentée dans COM par le biais de l’interface [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2) et par la prise en charge d’une clé de licence qui peut être transmise au moment de l’exécution.

### <a name="flags"></a>Indicateurs

TYPEFLAG \_ FLICENSED

## <a name="examples"></a>Exemples

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    licensed, 
    helpstring("A meaningfulcomment"
]
coclass MyClass
{
    // coclass definition statements
};
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**coclasse**](coclass.md)
</dt> <dt>

[Contenu d’une bibliothèque de types](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
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

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Version**](version.md)
</dt> </dl>

 

 