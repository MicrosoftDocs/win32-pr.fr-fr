---
title: nonextensible, attribut
description: L’attribut \ non extensible \ spécifie que l’implémentation IDispatch comprend uniquement les propriétés et les méthodes listées dans la description de l’interface et ne peut pas être étendue avec des membres supplémentaires au moment de l’exécution.
ms.assetid: 5fcffa65-4f0c-4180-a6c2-f68d63ff99ae
keywords:
- MIDL d’attribut unextensible
topic_type:
- apiref
api_name:
- nonextensible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96c4e55cf5cf2c05ff9c3619b19e7a9b0582f3cf64bc0f9a711fb1af274bfb9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066877"
---
# <a name="nonextensible-attribute"></a>nonextensible, attribut

L’attribut non **\[ \] extensible** spécifie que l’implémentation [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) comprend uniquement les propriétés et les méthodes listées dans la description de l’interface et ne peut pas être étendue avec des membres supplémentaires au moment de l’exécution. (Par défaut, Automation suppose que les interfaces peuvent ajouter des membres au moment de l’exécution ; autrement dit, elles sont extensibles.)

``` syntax
[
    uuid(uuid-number), 
    nonextensible 
    [, optional-attribute-list]
] 
interface | dispinterface interface-name 
{
    interface-definition
}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*UUID-Number* 
</dt> <dd>

Spécifie un numéro d’identification unique universel pour l' [**interface**](interface.md).

</dd> <dt>

*Optional-attribute-List* 
</dt> <dd>

Spécifie une liste de zéro, un ou plusieurs attributs d’interface MIDL.

</dd> <dt>

*nom de l’interface* 
</dt> <dd>

Spécifie le nom de l' [**interface**](interface.md) ou de [**dispinterface**](dispinterface.md).

</dd> <dt>

*définition d’interface* 
</dt> <dd>

Spécifie les instructions IDL qui forment la définition de l' [**interface**](interface.md) ou de [**dispinterface**](dispinterface.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

Vous pouvez appliquer l’attribut non **\[ extensible \]** à une interface ou une dispinterface. Toutefois, une interface doit également avoir les **\[** attributs [**Dual**](dual.md) **\]** et **\[** [**oleautomation**](oleautomation.md) **\]** .

### <a name="flags"></a>Indicateurs

TYPEFLAG \_ FNONEXTENSIBLE

## <a name="examples"></a>Exemples

``` syntax
library Hello
{
    [
        uuid(12345678-1234-1234-1234-123456789ABC), 
        helpstring("A helpful description."),
        oleautomation, 
        dual, 
        nonextensible
    ] 
    interface IHello : IDispatch
    {
        // Interface definition statements.
    }
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contenu d’une bibliothèque de types](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**double**](dual.md)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 