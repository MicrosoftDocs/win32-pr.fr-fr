---
title: attribut id
description: L’attribut \ ID \ spécifie un DISPID pour une fonction membre (une propriété ou une méthode, dans une interface ou une dispinterface).
ms.assetid: 6f1be049-81b4-4aa2-a893-5dd79bb4d63c
keywords:
- ID MIDL de l’attribut ID
topic_type:
- apiref
api_name:
- id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07c57d8ea818bbd7b8fd5bd35816e6b7227eb917
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381814"
---
# <a name="id-attribute"></a>attribut id

L’attribut **\[ ID \]** spécifie un DISPID pour une fonction membre (une propriété ou une méthode, dans une interface ou une dispinterface).

``` syntax
[id(id-num) [,optional-attribute-list]] return-type function-name(optional-parameter-list)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*ID-num* 
</dt> <dd>

DISPID pour la fonction.

</dd> <dt>

*Optional-attribute-List* 
</dt> <dd>

Spécifie une liste de zéro, un ou plusieurs attributs d’interface MIDL.

</dd> <dt>

*type de retour* 
</dt> <dd>

Spécifie le type de retour de la fonction.

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Spécifie le nom de la fonction dans le fichier IDL.

</dd> <dt>

*liste de paramètres facultatifs* 
</dt> <dd>

Zéro, un ou plusieurs paramètres de fonction.

</dd> </dl>

## <a name="remarks"></a>Notes

Utilisez l’attribut **\[ ID \]** lorsque vous souhaitez assigner un DISPID standard (tel que \_ value DISPID, DISPID NEWENUM, \_ etc.) à une méthode ou une propriété, ou lorsque vous implémentez votre propre **IDispatch :: Invoke** au lieu de le déléguer à **DispInvoke** / **ITypeInfo :: Invoke**.

Si vous n’utilisez pas l’attribut **\[ ID \]** sur une interface, le compilateur MIDL assigne un DISPID pour vous. Toutefois, lorsque vous spécifiez une dispinterface à l’aide de propriétés et de méthodes, vous devez spécifier un DISPID pour chaque propriété et méthode.

L' *ID-num* est une valeur intégrale positive 32 bits. Les ID négatifs sont réservés pour une utilisation par Automation.

## <a name="examples"></a>Exemples

``` syntax
interface IKnown : IUnknown
{
    properties:
        [id(90), propget, 
         helpstring("A meaningful comment."] long Func1(void);

    /* Other interface statements */
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

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

 

 