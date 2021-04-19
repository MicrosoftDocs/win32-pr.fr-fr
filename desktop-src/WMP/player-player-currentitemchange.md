---
title: Événement Player. CurrentItemChange
description: L’événement CurrentItemChange se produit lorsque Controls. currentItem change.
ms.assetid: e6f68aeb-d7e7-460b-adc9-647f28c678a1
keywords:
- Événement CurrentItemChange lecteur Windows Media
- Événement CurrentItemChange lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement CurrentItemChange
topic_type:
- apiref
api_name:
- Player.CurrentItemChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4c425184bf4b338177ec892ed5362c085dd8cb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542757"
---
# <a name="playercurrentitemchange-event"></a>Événement Player. CurrentItemChange

L’événement **CurrentItemChange** se produit lorsque *contrôle*. modifications de **CurrentItem** .

## <a name="syntax"></a>Syntaxe


```JScript
Player.CurrentItemChange()
```



## <a name="parameters"></a>Paramètres

Cet événement n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="examples"></a>Exemples

L’exemple JScript suivant montre un gestionnaire d’événements pour le *lecteur*. événement **currentItemChange** . L’objet **Player** a été créé avec ID = "Player".


```JScript
<!-- Create an HTML text box to display the media item name. -->
<INPUT TYPE="TEXT" NAME="MEDIA">

<!-- Create an event handler. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player EVENT = currentItemChange()>

   // Display the name of the new media item.
   MEDIA.value = Player.currentMedia.name;

</SCRIPT>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Controls. currentItem**](controls-currentitem.md)
</dt> <dt>

[**Objet Player**](player-object.md)
</dt> </dl>

 

 





