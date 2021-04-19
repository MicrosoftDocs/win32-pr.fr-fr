---
title: Méthode MediaCollection. getStringCollectionByQuery
description: La méthode getStringCollectionByQuery récupère un objet StringCollection contenant toutes les chaînes qui correspondent aux conditions de la requête.
ms.assetid: 17442151-7eb1-4256-ac5f-142b11645216
keywords:
- méthode getStringCollectionByQuery lecteur Windows Media
- méthode getStringCollectionByQuery lecteur Windows Media, classe MediaCollection
- Classe MediaCollection lecteur Windows Media, méthode getStringCollectionByQuery
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
ms.openlocfilehash: 4bf304d22cb207d8a2bfb046522e8704e900d508
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545437"
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

 

 





