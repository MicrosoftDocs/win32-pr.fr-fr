---
title: Query. beginNextGroup, méthode
description: La méthode beginNextGroup commence un nouveau groupe de conditions. | Query. beginNextGroup, méthode
ms.assetid: e0c59bd0-0789-413e-ade8-8d53c6f3e19b
keywords:
- méthode beginNextGroup lecteur Windows Media
- méthode beginNextGroup lecteur Windows Media, classe Query
- Classe de requête lecteur Windows Media, méthode beginNextGroup
topic_type:
- apiref
api_name:
- Query.beginNextGroup
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46c043b9a0ea506e054877b4d8122304ced75e28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543878"
---
# <a name="querybeginnextgroup-method"></a>Query. beginNextGroup, méthode

La méthode **beginNextGroup** commence un nouveau groupe de conditions.

## <a name="syntax"></a>Syntaxe


```JScript
Query.beginNextGroup()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Le démarrage d’un nouveau groupe de conditions implique que vous avez terminé le groupe de conditions actuel. Le nouveau groupe de conditions est toujours concaténé au groupe de conditions précédent à l’aide de ou de la logique.

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

[**Query. addCondition**](query-addcondition.md)
</dt> </dl>

 

 





