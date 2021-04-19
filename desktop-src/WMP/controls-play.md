---
title: Controls. Play, méthode
description: La méthode Play entraîne le démarrage de la lecture de l’élément multimédia actuel ou reprend la lecture d’un élément suspendu.
ms.assetid: 2218a13b-6294-45f5-bb6f-c5a1e433e0c6
keywords:
- Play, méthode lecteur Windows Media
- méthode Play lecteur Windows Media, classe Controls
- Controls, classe Windows Media Player, Play, méthode
topic_type:
- apiref
api_name:
- Controls.play
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea66f3bc4cf01d194dc44bcdf7b7cc838e1f3799
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537822"
---
# <a name="controlsplay-method"></a>Controls. Play, méthode

La méthode **Play** entraîne le démarrage de la lecture de l’élément multimédia actuel ou reprend la lecture d’un élément suspendu.

## <a name="syntax"></a>Syntaxe


```JScript
Controls.play()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Si cette méthode est appelée pendant le transfert rapide ou le rembobinage, il s’agit de la valeur des *paramètres*. la valeur **rate** est définie sur 1,0.

## <a name="examples"></a>Exemples

L’exemple suivant crée un élément BUTTON HTML qui utilise **Play** pour lire l’élément multimédia en cours. L’objet **Player** a été créé avec ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "PLAY"  NAME = "PLAY"  VALUE = "Play"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Play'))

            /* Start playback. */
            Player.controls.play();
">

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Controls (objet)**](controls-object.md)
</dt> </dl>

 

 





