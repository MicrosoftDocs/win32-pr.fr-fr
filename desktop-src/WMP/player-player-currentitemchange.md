---
title: Événement Player. CurrentItemChange
description: L’événement CurrentItemChange se produit lorsque Controls. currentItem change.
ms.assetid: e6f68aeb-d7e7-460b-adc9-647f28c678a1
keywords:
- Lecteur Windows Media d’événements CurrentItemChange
- Lecteur Windows Media d’événements CurrentItemChange, classe Player
- Lecteur Windows Media de classe Player, événement CurrentItemChange
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
ms.openlocfilehash: 5ed0ca3c8333c7261c8332bcc124c905c5540f5cdf0dbefe3f34f121eb901cc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338124"
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

l’exemple de JScript suivant montre un gestionnaire d’événements pour le *lecteur*. événement **currentItemChange** . L’objet **Player** a été créé avec ID = "Player".


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

 

 





