---
title: Méthode MediaCollection. getPlaylistByQuery
description: La méthode getPlaylistByQuery récupère un objet de sélection contenant des objets multimédias qui correspondent aux conditions de requête.
ms.assetid: 3487d442-a5bb-4519-ac45-d0138516305e
keywords:
- méthode getPlaylistByQuery lecteur Windows Media
- méthode getPlaylistByQuery lecteur Windows Media, classe MediaCollection
- Classe MediaCollection lecteur Windows Media, méthode getPlaylistByQuery
topic_type:
- apiref
api_name:
- MediaCollection.getPlaylistByQuery
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50b57d4303ba8784f912db9570faacb26d01677d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537466"
---
# <a name="mediacollectiongetplaylistbyquery-method"></a>Méthode MediaCollection. getPlaylistByQuery

La méthode **getPlaylistByQuery** récupère un objet de **sélection** contenant des objets **multimédias** qui correspondent aux conditions de requête.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = MediaCollection.getPlaylistByQuery(
  query,
  mediaType,
  sortAttribute,
  sortAscending
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*requête* \[ dans\]
</dt> <dd>

Objet de **requête** qui définit les conditions utilisées pour créer la sélection.

</dd> <dt>

*MediaType* \[ dans\]
</dt> <dd>

**Chaîne** contenant le type de média. Doit contenir l’une des valeurs suivantes : « audio », « Video », « photo », « playlist » ou « other ».

</dd> <dt>

*sortAttribute* \[ dans\]
</dt> <dd>

**Chaîne** contenant le nom d’attribut utilisé pour le tri. Une chaîne vide ("") signifie qu’aucun tri n’est appliqué.

</dd> <dt>

*sortAscending* \[ dans\]
</dt> <dd>

Valeur **booléenne** qui indique que la sélection doit être triée dans l’ordre croissant.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un objet **playlist** .

## <a name="remarks"></a>Notes

Les requêtes composées à l’aide de la **requête** ne respectent pas la casse.

Lorsque la requête composée spécifiée par le paramètre de *requête* contient une condition construite sur l’attribut **MediaType** , cette condition est ignorée. La valeur du paramètre *MediaType* est toujours utilisée. Par exemple, si la requête composée contient la condition « MediaType est égal à audio » et que la valeur du paramètre *MediaType* est « Video », la sélection résultante contient uniquement les éléments vidéo.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**MediaType (attribut)**](mediatype-attribute.md)
</dt> <dt>

[**Objet Query**](query-object.md)
</dt> </dl>

 

 





