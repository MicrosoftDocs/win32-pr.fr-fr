---
title: attribut en lecture seule
description: L’attribut \ ReadOnly \ interdit l’assignation à une variable.
ms.assetid: b81064e6-e788-48d1-9958-203f1e3c7e4d
keywords:
- MIDL d’attribut ReadOnly
topic_type:
- apiref
api_name:
- readonly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b4ef4ca5f32b96146ed5ab0ec085d32b24dca3a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093233"
---
# <a name="readonly-attribute"></a>attribut en lecture seule

L’attribut **\[ ReadOnly \]** interdit l’assignation à une variable.

``` syntax
[readonly [, optional-attributes]] data-type identifier
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*attributs facultatifs* 
</dt> <dd>

Zéro, un ou plusieurs attributs MIDL.

</dd> <dt>

*type de données* 
</dt> <dd>

Type des données contenues par l' *identificateur*.

</dd> <dt>

*identifier* 
</dt> <dd>

Nom par lequel le logiciel peut faire référence à l’emplacement de stockage des données.

</dd> </dl>

## <a name="remarks"></a>Notes

L’attribut **\[ ReadOnly \]** interdit l’assignation à une variable. la **\[ lecture \]** seule est prise en charge uniquement au niveau du paramètre, et non au niveau de la méthode.

### <a name="flags"></a>Indicateurs

VARFLAG \_ FREADONLY

## <a name="examples"></a>Exemples

``` syntax
HRESULT Method3([in, readonly] int iMmutable);
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 