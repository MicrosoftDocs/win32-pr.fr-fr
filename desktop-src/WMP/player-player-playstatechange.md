---
title: Événement Player. PlayStateChange
description: L’événement PlayStateChange se produit lorsqu’une modification est apportée à la propriété lecture.
ms.assetid: d4c4b114-04b6-4079-b6a2-52b336fc6dc1
keywords:
- Lecteur Windows Media d’événements PlayStateChange
- Lecteur Windows Media d’événements PlayStateChange, classe Player
- Lecteur Windows Media de classe Player, événement PlayStateChange
topic_type:
- apiref
api_name:
- Player.PlayStateChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e621d8698a5379b0d39a55db141fc0012f6ef969
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008363"
---
# <a name="playerplaystatechange-event"></a>Événement Player. PlayStateChange

L’événement **PlayStateChange** se produit lorsqu’une modification est apportée à la propriété **lecture** .

## <a name="syntax"></a>Syntaxe


```JScript
Player.PlayStateChange(
  NewState
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NewState* 
</dt> <dd>

Nombre (**long**) qui spécifie le nouveau **lecture**. Pour obtenir un tableau des valeurs possibles, consultez [lecture](player-playstate.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

la valeur des paramètres d’événement est spécifiée par Lecteur Windows Media, et est accessible ou passée à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

il n’est pas garanti que les états de Lecteur Windows Media se produisent dans un ordre particulier. En outre, tous les États ne se produisent pas nécessairement au cours d’une séquence d’événements. Vous ne devez pas écrire du code qui s’appuie sur l’ordre de l’État.

## <a name="examples"></a>Exemples

L’exemple suivant montre un gestionnaire d’événements pour le *lecteur*. événement **playStateChange** . Un élément de texte HTML, nommé « myText », affiche le nouvel état de lecture. L’objet Player a été créé avec ID = "Player".


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player EVENT = playStateChange(NewState)>

// Test for the player current state, display a message for each.
switch (NewState){
    case 1:
        myText.value = "Stopped";
        break;

    case 2:
        myText.value = "Paused";
        break;

    case 3:
        myText.value = "Playing";
        break;

    // Other cases go here.

    default:
        myText.value = "";
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
</dt> <dt>

[**Player. lecture**](player-playstate.md)
</dt> </dl>

 

 





