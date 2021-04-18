---
title: Événement Player. MediaChange
description: L’événement MediaChange se produit lorsqu’un élément multimédia change. | Événement Player. MediaChange
ms.assetid: c4bdd2ae-c51f-4577-b762-bc84aaf52f76
keywords:
- Événement MediaChange lecteur Windows Media
- Événement MediaChange lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement MediaChange
topic_type:
- apiref
api_name:
- Player.MediaChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99a63e087356b5d39ae8d751236b8128330c4f3c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533431"
---
# <a name="playermediachange-event"></a>Événement Player. MediaChange

L’événement **MediaChange** se produit lorsqu’un élément multimédia change.

## <a name="syntax"></a>Syntaxe


```JScript
Player.MediaChange(
  Item
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Item* 
</dt> <dd>

Objet **multimédia** représentant l’élément qui a été modifié.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.

## <a name="examples"></a>Exemples

L’exemple JScript suivant utilise un élément HTML DIV, nommé MediaName, pour afficher le nom de l’élément multimédia actuel. Le code met à jour le texte de la balise DIV avec chaque occurrence de l’événement **mediaChange** . L’objet **Player** a été créé avec ID = "Player".


```JScript
<!-- Create an event handler for media change. -->
<SCRIPT FOR = "Player" EVENT = "mediaChange(Item)">
   // Test whether a valid currentMedia object exists.
   if (Player.currentMedia){
      // Display the name of the current media item.
      MediaName.innerHTML = Player.currentMedia.name;
   }
</SCRIPT>

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> </dl>

 

 





