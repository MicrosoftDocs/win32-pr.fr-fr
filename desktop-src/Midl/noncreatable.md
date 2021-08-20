---
title: noncreatable (attribut)
description: L’attribut \ noncreatable \ définit un objet qui ne peut pas être instancié par lui-même.
ms.assetid: 75d7b978-0f82-4e8a-89c2-ffd5b9a691d6
keywords:
- MIDL d’attribut noncreatable
topic_type:
- apiref
api_name:
- noncreatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e59c53d8e4c05d15d55a6ccd9d7fb2b5cd8783463d1f59d439c74240fdd93a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066939"
---
# <a name="noncreatable-attribute"></a>noncreatable (attribut)

L’attribut **\[ noncreatable \]** définit un objet qui ne peut pas être instancié par lui-même.

``` syntax
[
  coclass-attribute-list, 
    noncreatable
]
coclass coclass-name
{
  coclass-interface-list
}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*coclass-attribute-List* 
</dt> <dd>

Autres attributs qui s’appliquent à la classe.

</dd> <dt>

*nom de la coclasse* 
</dt> <dd>

Nom de la classe.

</dd> <dt>

*coclass-interface-List* 
</dt> <dd>

Liste des interfaces pour la classe.

</dd> </dl>

## <a name="remarks"></a>Remarques

Utilisez l’attribut **\[ noncreatable \]** sur une instruction [**coclass**](coclass.md) pour indiquer aux utilisateurs qu’ils ne peuvent pas créer un nouvel objet de cette classe au niveau supérieur, c’est-à-dire en appelant **CreateInstance** ou **CoCreateInstance**. L’instanciation d’un objet de cette classe requiert un appel de méthode à un autre objet. par exemple, dans Microsoft Excel, l’objet « Cell » ne peut pas être créé et doit être obtenu à partir d’un objet de feuille de calcul Microsoft Excel.

Les méthodes qui retournent des instances de classes pouvant être créées doivent retourner le type exact de l’objet, plutôt que des types **Variant** ou **IDispatch** \* .

### <a name="typeflag-representation"></a>Représentation TYPEFLAG :

Absence de FCANCREATE TYPEFLAG \_ .

## <a name="examples"></a>Exemples

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("This is MyCOClass"),
    noncreatable
]
coclass MyCoClass
{
    [default] interface IMyClass;
    [default, source] dispinterface IMyClassEvents;
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**coclasse**](coclass.md)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 