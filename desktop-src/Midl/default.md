---
title: attribut par défaut
description: L’attribut \ default \ indique que l’interface ou dispinterface, définie dans une coclasse, représente l’interface de programmabilité par défaut. Cet attribut est destiné à être utilisé par les langages de macro.
ms.assetid: 66769dff-60a0-4e6e-9357-c4339c0bfa3f
keywords:
- MIDL d’attribut par défaut
topic_type:
- apiref
api_name:
- default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2171515bffc41abf2b5fe9a25826c2a71d3939c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093685"
---
# <a name="default-attribute"></a>attribut par défaut

L’attribut **\[ par \] défaut** indique que l' [**interface**](interface.md) ou la [**dispinterface**](dispinterface.md), définie dans une [**coclasse**](coclass.md), représente l’interface de programmabilité par défaut. Cet attribut est destiné à être utilisé par les langages de macro.

``` syntax
[
    uuid(uuid-number) 
    [, attribute-list]
] 
coclass coclass-name
{
    [ default [, optional-interface-attribute] ]; 
    interface | dispinterface interface-name;
}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*UUID-Number* 
</dt> <dd>

Spécifie un numéro d’identification unique universel pour la [**coclasse**](coclass.md).

</dd> <dt>

*liste d’attributs* 
</dt> <dd>

Spécifie d’autres attributs de [**coclasse**](coclass.md) . Séparez plusieurs attributs par des virgules.

</dd> <dt>

*nom de la coclasse* 
</dt> <dd>

Spécifie le nom par lequel d’autres composants logiciels peuvent référencer cette [**coclasse**](coclass.md).

</dd> <dt>

*Optional-interface-Attribute* 
</dt> <dd>

L' **\[** [](source.md) **\]** attribut source, qui spécifie qu’une interface ou une dispinterface est sortante, est le seul autre attribut qui peut être utilisé ici.

</dd> <dt>

*nom de l’interface* 
</dt> <dd>

Spécifie le nom de l’interface.

</dd> </dl>

## <a name="remarks"></a>Notes

Une [**coclasse**](coclass.md) peut avoir au plus deux membres **\[ par défaut \]** . L’une représente l’interface sortante (source) ou dispinterface, tandis que l’autre représente l’interface entrante (sink) ou dispinterface. Si l’attribut **\[ par \] défaut** n’est spécifié pour aucun membre de la **coclasse** ou du **cotype**, les premiers membres sortants et entrants qui n’ont pas l' **\[** attribut [**Restricted**](restricted.md) **\]** sont traités comme des valeurs par défaut.

### <a name="flags"></a>Indicateurs

IMPLTYPEFLAG \_ FDEFAULT

## <a name="examples"></a>Exemples

``` syntax
[ 
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("Hello Class"),appobject
]  
coclass Hello
{
    [default] interface IHello:IUnknown;
    interface IDispatch;
};
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**coclasse**](coclass.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**sensible**](restricted.md)
</dt> <dt>

[**code**](source.md)
</dt> </dl>

 

 