---
title: Événement Player. MediaCollectionMediaAdded
description: L’événement MediaCollectionMediaAdded se produit lorsqu’un élément multimédia est ajouté à la bibliothèque locale. | Événement Player. MediaCollectionMediaAdded
ms.assetid: 01696d28-e83b-4fd2-8e88-2871831b61e7
keywords:
- Lecteur Windows Media d’événements MediaCollectionMediaAdded
- Lecteur Windows Media d’événements MediaCollectionMediaAdded, classe Player
- Lecteur Windows Media de classe Player, événement MediaCollectionMediaAdded
topic_type:
- apiref
api_name:
- Player.MediaCollectionMediaAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d18dd0536f508090c46f9fc5a9059c809f50091d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010973"
---
# <a name="playermediacollectionmediaadded-event"></a>Événement Player. MediaCollectionMediaAdded

L’événement MediaCollectionMediaAdded se produit lorsqu’un élément multimédia est ajouté à la bibliothèque locale.

## <a name="syntax"></a>Syntaxe


```JScript
Player.MediaCollectionMediaAdded(
  pdispMedia
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pdispMedia* 
</dt> <dd>

Objet **multimédia** qui a été ajouté.

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

 

 





