---
title: nonbrowsable (attribut)
description: Utilisez l’attribut \ non Browsable \ pour baliser une interface ou un membre dispinterface qui ne doit pas être affiché dans un Explorateur de propriétés.
ms.assetid: 94e868cc-8d9c-4b8a-ac18-1ea513a103da
keywords:
- MIDL d’attribut ne pouvant être exploré
topic_type:
- apiref
api_name:
- nonbrowsable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e24c39511df9637c352245b98b237fe8fd451eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093321"
---
# <a name="nonbrowsable-attribute"></a>nonbrowsable (attribut)

Utilisez l’attribut non **\[ navigable \]** pour baliser une interface ou un membre dispinterface qui ne doit pas être affiché dans un Explorateur de propriétés.

``` syntax
[property-attribute-list, nonbrowsable]return-type property-name(prop-param-list)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*property-attribute-List* 
</dt> <dd>

Autres attributs qui s’appliquent à la propriété.

</dd> <dt>

*type de retour* 
</dt> <dd>

Type des données retournées par la méthode.

</dd> <dt>

*property-name* 
</dt> <dd>

Nom de la propriété ou de la méthode.

</dd> <dt>

*prop-param-List* 
</dt> <dd>

Zéro, un ou plusieurs paramètres à passer à la méthode.

</dd> </dl>

## <a name="remarks"></a>Notes

Certaines propriétés ne doivent pas être affichées dans un Explorateur de propriétés. Cela peut être dû au fait que la récupération de la valeur prend beaucoup de temps. L’exemple empêche l’utilisateur de tenter de récupérer la propriété *Count* , qui retourne le nombre de lignes dans la feuille de réponse dynamique. Ce nombre peut représenter les résultats d’une requête très volumineuse.

D’autres propriétés peuvent avoir des effets inattendus sur le navigateur. Par exemple, considérez un contrôle avec la propriété « IsSelected » pour indiquer si le contrôle est sélectionné. Si « IsSelected » est défini sur false, un navigateur de propriétés basé sur une sélection parcourt un autre objet.

Notez qu’une propriété marquée comme non **\[ consultable \]** apparaît toujours dans un Explorateur d’objets, qui n’affiche pas les valeurs de propriété.

### <a name="typeflag-representation"></a>Représentation TYPEFLAG

Présence de FUNCFLAG \_ FNONBROWSABLE ou VARFLAG \_ FNONBROWSABLE.

## <a name="examples"></a>Exemples

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IDynaset:IDispatch
{
    [propget, nonbrowsable]HRESULT Count([out, retval] long *Value);
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 