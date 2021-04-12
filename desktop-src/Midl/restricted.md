---
title: restricted (attribut)
description: L’attribut \ Restricted \ spécifie qu’une bibliothèque, ou un membre d’un module, d’une interface ou d’une dispinterface ne peut pas être appelé arbitrairement.
ms.assetid: ad1ae84f-77f4-4028-bd71-ff01414e474e
keywords:
- MIDL d’attribut limité
topic_type:
- apiref
api_name:
- restricted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca610c0dcf29ebc3a767005b4c22e3231947e88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381889"
---
# <a name="restricted-attribute"></a>restricted (attribut)

L’attribut **\[ Restricted \]** spécifie qu’une bibliothèque, ou un membre d’un module, d’une interface ou d’une dispinterface ne peut pas être appelé arbitrairement.

``` syntax
[
    restricted
    [, other-attributes]
] 
statement-type statement-name 
{
    definitions
};
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*autres attributs* 
</dt> <dd>

Zéro, un ou plusieurs attributs MIDL.

</dd> <dt>

*type d’instruction* 
</dt> <dd>

Une des valeurs suivantes : [**Library**](library.md), [**module**](module.md), [**interface**](interface.md), [**dispinterface**](dispinterface.md).

</dd> <dt>

*nom de l’instruction* 
</dt> <dd>

Identificateur par lequel le logiciel fait référence à cette instruction.

</dd> <dt>

*Description* 
</dt> <dd>

Éléments de langage MIDL qui définissent le contenu de cette instruction.

</dd> </dl>

## <a name="remarks"></a>Notes

Cet attribut vous permet de contrôler l’accès aux éléments des interfaces, bibliothèques, modules et dispinterfaces. Par exemple, il peut empêcher l’utilisation d’un élément de données par un programmeur de macro. Vous pouvez appliquer cet attribut à un membre d’une [**coclasse**](coclass.md), indépendamment du fait que le membre est une dispinterface ou une interface, et indépendamment du fait que le membre soit un récepteur (entrant) ou une source (sortante). Un membre d’une **coclasse** ne peut pas avoir à la fois les attributs **\[ Restricted \]** et **\[ default \]** .

### <a name="flags"></a>Indicateurs

IMPLTYPEFLAG \_ FRESTRICTED, FUNCFLAG \_ FRESTRICTED

## <a name="examples"></a>Exemples

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version (1.0), 
    restricted
] 
library MyLibrary
{
    // Library definition statements.
};

[propget, restricted] HRESULT MyProc(void);
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Bibliothèque**](library.md)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**modules**](module.md)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 