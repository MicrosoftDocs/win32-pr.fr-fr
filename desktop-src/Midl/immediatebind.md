---
title: immediatebind (attribut)
description: L’attribut \ immediatebind \ indique que la base de données sera immédiatement notifiée de toutes les modifications apportées à la propriété d’un objet lié aux données.
ms.assetid: 1c08ddca-e273-43b3-a8f6-ed7f552e4e0e
keywords:
- MIDL de l’attribut immediatebind
topic_type:
- apiref
api_name:
- immediatebind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8a797514c15f8d4c46bb6161946d5d0b6bd10b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093518"
---
# <a name="immediatebind-attribute"></a>immediatebind (attribut)

L’attribut **\[ immediatebind \]** indique que la base de données sera immédiatement notifiée de toutes les modifications apportées à la propriété d’un objet lié aux données.

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, immediatebind[, optional-attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*interface-attribut-List* 
</dt> <dd>

Spécifie une liste d’un ou plusieurs attributs qui s’appliquent à l’ensemble de l’interface.

</dd> <dt>

*nom de l’interface* 
</dt> <dd>

Spécifie le nom de l' [**interface**](interface.md) ou de [**dispinterface**](dispinterface.md).

</dd> <dt>

*Optional-attribute-List* 
</dt> <dd>

Zéro, un ou plusieurs attributs de fonction.

</dd> <dt>

*ReturnType* 
</dt> <dd>

Spécifie le type de retour de la fonction.

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Spécifie le nom de la fonction dans le fichier IDL.

</dd> <dt>

*params* 
</dt> <dd>

Zéro, un ou plusieurs paramètres de fonction.

</dd> </dl>

## <a name="remarks"></a>Notes

L’attribut **\[ immediatebind \]** permet aux contrôles de faire la différence entre les propriétés qui doivent notifier la base de données de chaque modification et celles qui ne le font pas. Par exemple, chaque modification apportée à un contrôle de case à cocher doit être envoyée immédiatement à la base de données sous-jacente, même si le contrôle n’a pas perdu le focus. Toutefois, pour un contrôle ListBox, une modification se produit chaque fois qu’une sélection différente est mise en surbrillance. Notifier la base de données d’une modification avant que le contrôle ne perde le focus n’est pas efficace et inutile. L’attribut **\[ immediatebind \]** vous permet de spécifier, en définissant le bit immediatebind, des propriétés individuelles sur un formulaire dont les modifications doivent être signalées immédiatement.

Les propriétés qui ont l’attribut **\[ immediatebind \]** doivent également avoir l' **\[** attribut pouvant être [**lié**](bindable.md) **\]** .

### <a name="flags"></a>Indicateurs

FUNCFLAG \_ FIMMEDIATEBIND, VARFLAG \_ FIMMEDIATEBIND

## <a name="examples"></a>Exemples

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, immediatebind] long Size(void);

        [id(1), propput, bindable, 
         immediatebind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 