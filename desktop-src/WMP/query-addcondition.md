---
title: Query. addCondition, méthode
description: La méthode addCondition ajoute une condition à l’objet de requête à l’aide de et de la logique.
ms.assetid: 29b5d372-eddf-4b70-882b-d2dde79d9287
keywords:
- méthode addCondition lecteur Windows Media
- méthode addCondition lecteur Windows Media, classe Query
- Classe de requête lecteur Windows Media, méthode addCondition
topic_type:
- apiref
api_name:
- Query.addCondition
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4035d2877cf0081e9153277c88feb545a529568d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540216"
---
# <a name="queryaddcondition-method"></a>Query. addCondition, méthode

La méthode **addCondition** ajoute une condition à l’objet de **requête** à l’aide de et de la logique.

## <a name="syntax"></a>Syntaxe


```JScript
Query.addCondition(
  attribute,
  operator,
  value
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*attribut* \[ dans\]
</dt> <dd>

**Chaîne** contenant le nom de l’attribut.

</dd> <dt>

*opérateur* \[ dans\]
</dt> <dd>

**Chaîne** contenant l’opérateur. Consultez la section Notes pour connaître les valeurs prises en charge.

</dd> <dt>

*valeur* \[ dans\]
</dt> <dd>

**Chaîne** contenant la valeur de l’attribut.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Les requêtes composées à l’aide de la **requête** ne respectent pas la casse.

Vous trouverez une liste de valeurs pour le paramètre *attribut* dans la section [référence des attributs alphabétiques](alphabetical-attribute-reference.md) .

Les conditions contenues dans un objet de **requête** sont organisées en groupes de conditions. Plusieurs conditions au sein d’un groupe de conditions sont toujours concaténées à l’aide de et de la logique. Les groupes de conditions sont toujours concaténés entre eux à l’aide de ou logique. Pour démarrer un nouveau groupe de conditions, appelez **query. beginNextGroup**.

Le tableau suivant répertorie les valeurs prises en charge pour l' *opérateur*.



| Opérateur            | S’applique à     |
|---------------------|----------------|
| BeginsWith          | Chaînes        |
| Contient            | Chaînes        |
| Égal à              | Tous les types      |
| GreaterThan         | Nombres, dates |
| Supérieur ou égal à | Nombres, dates |
| LessThan            | Nombres, dates |
| Inférieur ou égal à    | Nombres, dates |
| NotBeginsWith       | Chaînes        |
| NotContains         | Chaînes        |
| NotEquals           | Tous les types      |



 

## <a name="examples"></a>Exemples

L’exemple JScript suivant utilise **query. addCondition** et **query. beginNextGroup** pour exécuter un exemple de requête.


```JScript
// Perform an example query for media for which:
// The genre contains "jazz"
// and the title begins with "a"
// OR the genre contains "jazz"
// and the author begins with "b".

// Create the query object.
var Query = Player.mediaCollection.createQuery();

// Add the first condition group.
Query.addCondition("WM/Genre", "Contains", "jazz");
Query.addCondition("Title", "BeginsWith", "a");

// Begin the new condition group ("or").
Query.beginNextGroup();

// Add the second condition group.
Query.addCondition("WM/Genre", "Contains", "jazz");
Query.addCondition("Author", "BeginsWith", "b");

// Perform the query on "audio" media.
var Playlist = Player.mediaCollection.getPlaylistByQuery(
    Query,      // query
    "audio",    // mediaType
    "",         // sortAttribute
    false);     // sortAscending
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MediaCollection. createQuery**](mediacollection-createquery.md)
</dt> <dt>

[**MediaCollection.getPlaylistByQuery**](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[**MediaCollection.getStringCollectionByQuery**](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[**Objet Query**](query-object.md)
</dt> <dt>

[**Query. beginNextGroup**](query-beginnextgroup.md)
</dt> </dl>

 

 





