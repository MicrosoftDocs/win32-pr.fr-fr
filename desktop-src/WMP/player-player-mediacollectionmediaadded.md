---
title: Événement Player. MediaCollectionMediaAdded
description: L’événement MediaCollectionMediaAdded se produit lorsqu’un élément multimédia est ajouté à la bibliothèque locale. | Événement Player. MediaCollectionMediaAdded
ms.assetid: 01696d28-e83b-4fd2-8e88-2871831b61e7
keywords:
- Événement MediaCollectionMediaAdded lecteur Windows Media
- Événement MediaCollectionMediaAdded lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement MediaCollectionMediaAdded
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545621"
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

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cet événement se produit uniquement pour la bibliothèque locale.

**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.

## <a name="requirements"></a>Configuration requise



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

 

 





