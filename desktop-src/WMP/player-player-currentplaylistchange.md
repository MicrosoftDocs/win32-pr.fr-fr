---
title: Événement Player. CurrentPlaylistChange
description: L’événement CurrentPlaylistChange se produit en cas de modification de la sélection actuelle. | Événement Player. CurrentPlaylistChange
ms.assetid: 5270373e-e401-40c6-bf8c-ef0557610372
keywords:
- Lecteur Windows Media d’événements CurrentPlaylistChange
- Lecteur Windows Media d’événements CurrentPlaylistChange, classe Player
- Lecteur Windows Media de classe Player, événement CurrentPlaylistChange
topic_type:
- apiref
api_name:
- Player.CurrentPlaylistChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4722db224285587198e3ddb021022ec5d8f2cea6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011001"
---
# <a name="playercurrentplaylistchange-event"></a>Événement Player. CurrentPlaylistChange

L’événement **CurrentPlaylistChange** se produit en cas de modification de la sélection actuelle.

## <a name="syntax"></a>Syntaxe


```JScript
Player.CurrentPlaylistChange(
  change
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*change* 
</dt> <dd>

**Nombre** (**long**) indiquant le type de modification qui s’est produite dans la sélection. Consultez le *lecteur*. Événement **PlaylistChange** pour une table de valeurs possibles.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cet événement ne se produit pas lorsqu’une sélection différente devient la sélection actuelle. Il se produit uniquement lorsqu’une modification se produit dans la sélection actuelle, par exemple un élément multimédia ajouté à la sélection.

la valeur des paramètres d’événement est spécifiée par Lecteur Windows Media, et est accessible ou passée à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

## <a name="examples"></a>Exemples

l’exemple de JScript suivant met à jour le texte d’un élément DIV HTML, nommé PlItems, pour afficher les noms des éléments multimédias dans la sélection actuelle. L’objet **Player** a été créé avec ID = "Player".


```JScript
<!-- Create an event handler for current playlist change. -->
<SCRIPT FOR = "Player" EVENT = "currentPlaylistChange(change)">
   switch (change){
      // Only update for move, delete, insert, and append events.
      case 3, 4, 5, 6:

         // Clear the contents of the DIV.
         PlItems.innerHTML = "";

         // Loop through the playlist and display each item name.
         for (var i = 0; i < Player.currentPlaylist.count; i++){
            PlItems.innerHTML += Player.currentPlaylist.item(i).name;
            PlItems.innerHTML += "<br>";
         }
         break;
      
      default:
   } 
</SCRIPT>

```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> <dt>

[**Player. currentPlaylist**](player-currentplaylist.md)
</dt> <dt>

[**Player. PlaylistChange**](player-player-playlistchange.md)
</dt> </dl>

 

 





