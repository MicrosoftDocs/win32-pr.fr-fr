---
title: Méthode MediaCollection. getStringCollectionByQuery
description: La méthode getStringCollectionByQuery récupère un objet StringCollection contenant toutes les chaînes qui correspondent aux conditions de la requête.
ms.assetid: 17442151-7eb1-4256-ac5f-142b11645216
keywords:
- Lecteur Windows Media de la méthode getStringCollectionByQuery
- méthode getStringCollectionByQuery Lecteur Windows Media, classe MediaCollection
- Lecteur Windows Media de la classe MediaCollection, méthode getStringCollectionByQuery
topic_type:
- apiref
api_name:
- MediaCollection.getStringCollectionByQuery
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d9e8f2eae2ce52a566d4db6b8298187df1d4d444432e99dda22d3cacc0ed3ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390109"
---
# <a name="mediacollectiongetstringcollectionbyquery-method"></a>Méthode MediaCollection. getStringCollectionByQuery

La méthode **getStringCollectionByQuery** récupère un objet **StringCollection** contenant toutes les chaînes qui correspondent aux conditions de la requête.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = MediaCollection.getStringCollectionByQuery(
  attribute,
  query,
  mediaType,
  sortAttribute,
  sortAscending
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*attribut* \[ dans\]
</dt> <dd>

**Chaîne** contenant le nom de l’attribut.

</dd> <dt>

*requête* \[ dans\]
</dt> <dd>

Objet de **requête** .

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

**Boolean**, true indiquant que **StringCollection** doit être trié dans l’ordre croissant.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un objet **StringCollection** .

## <a name="remarks"></a>Remarques

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

 

 





