---
title: aggregatable (attribut)
description: L’attribut \ Aggregatable \ indique que la classe prend en charge l’agrégation.
ms.assetid: 3b680692-fbf7-4aeb-b11a-c3a87ddaea67
keywords:
- MIDL d’attribut agrégeables
topic_type:
- apiref
api_name:
- aggregatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5091815cf38060c30b82aa33fd05ad6be9d6c390
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093809"
---
# <a name="aggregatable-attribute"></a>aggregatable (attribut)

L’attribut **\[ agrégeables \]** indique que la classe prend en charge l’agrégation.

``` syntax
[
   coclass-attribute-list,
   aggregatable
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

## <a name="remarks"></a>Notes

Utilisez l’attribut **\[ agrégeables \]** sur une instruction [**coclass**](coclass.md) pour permettre aux utilisateurs de savoir que la classe prend en charge les agrégations. Autrement dit, la classe autorise l’exposition de ses interfaces par une classe de conteneur comme si ces interfaces étaient les propres interfaces du conteneur.

La représentation TYPEFLAG de cet attribut est TYPEFLAG \_ FAGGREGATABLE.

## <a name="examples"></a>Exemples

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    aggregatable
]
coclass Form
{
    [default] interface IForm;
    [default, source] interface IFormEvents;
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**coclasse**](coclass.md)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 