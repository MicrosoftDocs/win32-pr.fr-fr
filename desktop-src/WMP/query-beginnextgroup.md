---
title: Query. beginNextGroup, méthode
description: La méthode beginNextGroup commence un nouveau groupe de conditions. | Query. beginNextGroup, méthode
ms.assetid: e0c59bd0-0789-413e-ade8-8d53c6f3e19b
keywords:
- Lecteur Windows Media de la méthode beginNextGroup
- méthode beginNextGroup Lecteur Windows Media, classe Query
- Lecteur Windows Media de classe de requête, méthode beginNextGroup
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010951"
---
# <a name="querybeginnextgroup-method"></a>Query. beginNextGroup, méthode

La méthode **beginNextGroup** commence un nouveau groupe de conditions.

## <a name="syntax"></a>Syntaxe


```JScript
Query.beginNextGroup()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Le démarrage d’un nouveau groupe de conditions implique que vous avez terminé le groupe de conditions actuel. Le nouveau groupe de conditions est toujours concaténé au groupe de conditions précédent à l’aide de ou de la logique.

## <a name="requirements"></a>Spécifications



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

 

 





