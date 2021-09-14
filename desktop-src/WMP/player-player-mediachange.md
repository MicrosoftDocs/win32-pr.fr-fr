---
title: Événement Player. MediaChange
description: L’événement MediaChange se produit lorsqu’un élément multimédia change. | Événement Player. MediaChange
ms.assetid: c4bdd2ae-c51f-4577-b762-bc84aaf52f76
keywords:
- Lecteur Windows Media d’événements MediaChange
- Lecteur Windows Media d’événements MediaChange, classe Player
- Lecteur Windows Media de classe Player, événement MediaChange
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010978"
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

## <a name="return-value"></a>Valeur de retour

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

la valeur des paramètres d’événement est spécifiée par Lecteur Windows Media, et est accessible ou passée à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise un élément DIV HTML, nommé MediaName, pour afficher le nom de l’élément multimédia en cours. Le code met à jour le texte de la balise DIV avec chaque occurrence de l’événement **mediaChange** . L’objet **Player** a été créé avec ID = "Player".


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



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> </dl>

 

 





