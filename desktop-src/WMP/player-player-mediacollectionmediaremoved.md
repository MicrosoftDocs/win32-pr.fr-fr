---
title: Événement Player. MediaCollectionMediaRemoved
description: L’événement MediaCollectionMediaRemoved se produit lorsqu’un élément multimédia est supprimé de la bibliothèque locale. | Événement Player. MediaCollectionMediaRemoved
ms.assetid: a1df6faf-38dc-4f5f-8f8a-953c91ea026c
keywords:
- Lecteur Windows Media d’événements MediaCollectionMediaRemoved
- Lecteur Windows Media d’événements MediaCollectionMediaRemoved, classe Player
- Lecteur Windows Media de classe Player, événement MediaCollectionMediaRemoved
topic_type:
- apiref
api_name:
- Player.MediaCollectionMediaRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72af5fe4c5e90effeb34745ea71e3edb457da357
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010971"
---
# <a name="playermediacollectionmediaremoved-event"></a>Événement Player. MediaCollectionMediaRemoved

L’événement MediaCollectionMediaRemoved se produit lorsqu’un élément multimédia est supprimé de la bibliothèque locale.

## <a name="syntax"></a>Syntaxe


```JScript
Player.MediaCollectionMediaRemoved(
  pdispMedia
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pdispMedia* 
</dt> <dd>

Objet **multimédia** qui a été supprimé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cet événement se produit uniquement pour la bibliothèque locale.

**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Objet Player**](player-object.md)
</dt> <dt>

[**Player. mediaCollection**](player-mediacollection.md)
</dt> </dl>

 

 





