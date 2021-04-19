---
title: Méthode MediaCollection. getAttributeStringCollection
description: La méthode getAttributeStringCollection récupère un objet StringCollection représentant l’ensemble de toutes les valeurs d’un attribut spécifié dans un type de média spécifié.
ms.assetid: 75563a75-88f5-419e-983b-d105bce02511
keywords:
- méthode getAttributeStringCollection lecteur Windows Media
- méthode getAttributeStringCollection lecteur Windows Media, classe MediaCollection
- Classe MediaCollection lecteur Windows Media, méthode getAttributeStringCollection
topic_type:
- apiref
api_name:
- MediaCollection.getAttributeStringCollection
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d50d25488a05e6076c99802ce738edf02298ade
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539969"
---
# <a name="mediacollectiongetattributestringcollection-method"></a>Méthode MediaCollection. getAttributeStringCollection

La méthode **getAttributeStringCollection** récupère un objet **StringCollection** représentant l’ensemble de toutes les valeurs d’un attribut spécifié dans un type de média spécifié.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = MediaCollection.getAttributeStringCollection(
  attribute,
  mediaType
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*attribut* \[ dans\]
</dt> <dd>

**Chaîne** spécifiant l’attribut.

</dd> <dt>

*MediaType* \[ dans\]
</dt> <dd>

**Chaîne** représentant le type de média. Contient l’une des valeurs suivantes : « audio », « Video », « playlist » ou « other ».

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un objet **StringCollection** .

## <a name="remarks"></a>Notes

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la section [référence des attributs](attribute-reference.md) .

## <a name="examples"></a>Exemples

L’exemple JScript suivant utilise *MediaCollection*. **getAttributeStringCollection** pour afficher une liste de valeurs qui correspondent à un attribut particulier pour les éléments audio de la collection de supports. Un élément SELECT HTML, créé avec ID = "attribute", permet à l’utilisateur de sélectionner un attribut, tel qu’un artiste, un genre ou un album. Un élément TEXTAREA HTML, créé avec ID = "AttributeVals", affiche le résultat. L’objet **Player** a été créé avec ID = "Player".


```JScript
// Clear the text in the display area.
AttributeVals.value = "";

// Store the mediaCollection object.
var library = Player.mediaCollection;

// Get the string collection for the attribute type the user selects.
var all = library.getAttributeStringCollection(Attribute.value, "Audio");

// Loop through the string collection.
for (i = 0; i < all.count; i++){

    // Display the items one line at a time.
    AttributeVals.value += all.item(i);
    AttributeVals.value += "\n";
}

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> <dt>

[**StringCollection, objet**](stringcollection-object.md)
</dt> </dl>

 

 





