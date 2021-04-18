---
title: Controls. Stop, méthode
description: La méthode Stop arrête la lecture de l’élément multimédia. | Controls. Stop, méthode
ms.assetid: ace95fde-9c94-4737-88f2-94321cbc687c
keywords:
- méthode Stop lecteur Windows Media
- méthode Stop lecteur Windows Media, classe Controls
- Controls, classe Windows Media Player, stop, méthode
topic_type:
- apiref
api_name:
- Controls.stop
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1ffc581fffbce0a341559e82c6bd196f712149
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533039"
---
# <a name="controlsstop-method"></a>Controls. Stop, méthode

La méthode **Stop** arrête la lecture de l’élément multimédia.

## <a name="syntax"></a>Syntaxe


```JScript
Controls.stop()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode force le lecteur Windows Media à libérer toutes les ressources système qu’il utilise, telles que le périphérique audio. Toutefois, l’élément multimédia actuel n’est pas libéré.

Lorsque le joueur est arrêté, le suivi se rembobine au début. L' **appel de la lecture commence** ensuite la lecture du clip à partir du début. Pour arrêter une opération de lecture sans modifier la position actuelle, utilisez la méthode **Pause** .

## <a name="examples"></a>Exemples

L’exemple suivant crée un élément BUTTON HTML qui utilise **Stop** pour arrêter la lecture. L’objet **Player** a été créé avec ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "STOP"  NAME = "STOP"  VALUE = "Stop"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Stop'))

            /* Stop the Player. */
            Player.controls.stop();
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
</dt> <dt>

[**Contrôles. Next**](controls-next.md)
</dt> <dt>

[**Controls. pause**](controls-pause.md)
</dt> <dt>

[**Contrôles. Previous**](controls-previous.md)
</dt> </dl>

 

 





