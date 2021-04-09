---
title: attribut source
description: L’attribut \ source \ indique qu’un membre d’une coclasse, d’une propriété ou d’une méthode est une source d’événements. Pour un membre d’une coclasse, cet attribut signifie que le membre est appelé au lieu d’être implémenté.
ms.assetid: fbd5411a-e614-4643-810a-f3765e7ec16d
keywords:
- MIDL de l’attribut source
topic_type:
- apiref
api_name:
- source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 621e97fd20b6b96d275044dc7cbe701faee29712
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940866"
---
# <a name="source-attribute"></a>attribut source

L’attribut **\[ source \]** indique qu’un membre d’une [**coclasse**](coclass.md), d’une propriété ou d’une méthode est une source d’événements. Pour un membre d’une **coclasse**, cet attribut signifie que le membre est appelé au lieu d’être implémenté.

``` syntax
[
    coclass-attributes
]
coclass coclass-name
{
    [source [, optional-attributes] ] statement-type statement-name; 
  [, ...]
}

[source] object-type function-name(optional-parameter-list);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*coclasse-attributs* 
</dt> <dd>

Zéro, un ou plusieurs attributs qui seront appliqués à la [**coclasse**](coclass.md).

</dd> <dt>

*nom de la coclasse* 
</dt> <dd>

Identificateur de nom de la [**coclasse**](coclass.md).

</dd> <dt>

*attributs facultatifs* 
</dt> <dd>

Zéro, un ou plusieurs attributs MIDL.

</dd> <dt>

*type d’instruction* 
</dt> <dd>

Peut être [**interface**](interface.md) ou [**dispinterface**](dispinterface.md).

</dd> <dt>

*nom de l’instruction* 
</dt> <dd>

Nom de l' [**interface**](interface.md) ou [**dispinterface**](dispinterface.md).

</dd> <dt>

*type d’objet* 
</dt> <dd>

Type de l’objet retourné par la méthode. Cet objet est une source d’événements.

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Nom d’une méthode dans une [**interface**](interface.md) ou une [**dispinterface**](dispinterface.md).

</dd> <dt>

*liste de paramètres facultatifs* 
</dt> <dd>

Zéro, un ou plusieurs paramètres de méthode.

</dd> </dl>

## <a name="remarks"></a>Notes

Sur une propriété ou une méthode, l’attribut **\[ source \]** indique que le membre retourne un objet ou un variant qui est une source d’événements. L’objet implémente **IConnectionPointContainer**.

### <a name="flags"></a>Indicateurs

IMPLTYPEFLAG \_ FSOURCE, \_ source VARFLAG, FUNCFLAG \_ source

## <a name="examples"></a>Exemples

``` syntax
[default, source] dispinterface DIMyFaceAdviseSink;
[source]interface IMyFaceAdviseSink;
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**coclasse**](coclass.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 