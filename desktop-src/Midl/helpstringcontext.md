---
title: attribut helpstringcontext
description: L’attribut \ helpstringcontext \ spécifie un identificateur de contexte d’aide 32 bits dans le fichier d’aide. Vous pouvez appliquer l’attribut \ helpstringcontext \ à la bibliothèque, à l’interface, à dispinterface, au module, à la coclasse, aux instructions typedef, aux propriétés, aux paramètres et aux méthodes.
ms.assetid: 0ac41bd9-ccc6-4b5c-b925-63bff9254eed
keywords:
- MIDL de l’attribut helpstringcontext
topic_type:
- apiref
api_name:
- helpstringcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64e97ea0d7b41d87ef1d535d562f3b515dda4f59a67f6d5e35f97bed8b1f9ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807234"
---
# <a name="helpstringcontext-attribute"></a>attribut helpstringcontext

L’attribut **\[ helpstringcontext \]** spécifie un identificateur de contexte d’aide 32 bits dans le fichier d’aide. Vous pouvez appliquer l’attribut **\[ helpstringcontext \]** à la [**bibliothèque**](library.md), à l' [**interface**](interface.md), à [**dispinterface**](dispinterface.md), au [**module**](module.md), à la [**coclasse**](coclass.md), aux instructions [**typedef**](typedef.md) , aux propriétés, aux paramètres et aux méthodes.

``` syntax
[  helpstringcontext(contextid)[, optional-attribute-list]] idl-statement
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*ContextId* 
</dt> <dd>

Entier unique qui identifie le texte d’aide associé à l’instruction MIDL actuelle.

</dd> <dt>

*Optional-attribute-List* 
</dt> <dd>

Zéro, un ou plusieurs attributs MIDL.

</dd> <dt>

*IDL-Statement* 
</dt> <dd>

Instruction MIDL à laquelle l’attribut **\[ helpstringcontext \]** sera appliqué.

</dd> </dl>

## <a name="remarks"></a>Remarques

Utilisez les fonctions **GetDocumentation2** dans les interfaces **ITypeLib2** et **ITypeInfo2** pour récupérer la chaîne d’aide.

## <a name="examples"></a>Exemples

``` syntax
[
    uuid(. . .),
    helpstringcontext(103),
    version(1.0)
]
library Lines
{
    [
        uuid(. . .), 
        helpstringcontext(102),
        oleautomation,
        dual
    ]
    interface ILine : IDispatch
    {
        [propget, helpstringcontext(100)] HRESULT Color([out, retval] long* ReturnVal); 
        [propput, helpstringcontext(101)] HRESULT Color([in] long rgb);
    }
};
```

 

 




