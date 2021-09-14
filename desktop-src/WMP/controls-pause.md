---
title: Controls. pause, méthode
description: La méthode pause interrompt la lecture de l’élément multimédia. | Controls. pause, méthode
ms.assetid: 7307a3b2-e5d6-4067-bdb5-38011565142a
keywords:
- pause, méthode Lecteur Windows Media
- pause, méthode Lecteur Windows Media, classe controls
- controls, classe Lecteur Windows Media, pause, méthode
topic_type:
- apiref
api_name:
- Controls.pause
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 898efb51355a1301bc76717f6d0184d0b30d619d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919335"
---
# <a name="controlspause-method"></a>Controls. pause, méthode

La méthode **Pause** interrompt la lecture de l’élément multimédia.

## <a name="syntax"></a>Syntaxe


```JScript
Controls.pause()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

lorsqu’un fichier est en pause, Lecteur Windows Media n’accorde aucune ressource système, telle que le périphérique audio.

Certains types de média ne peuvent pas être suspendus, tels que les flux en direct. Pour déterminer si un type de média particulier peut être suspendu, utilisez des *contrôles*. **isAvailable ('Pause')**.

## <a name="examples"></a>Exemples

L’exemple suivant crée un élément bouton HTML qui utilise **Pause** pour suspendre la lecture. L’objet **Player** a été créé avec ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "PAUSE"  NAME = "PAUSE"  VALUE = "||"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Pause'))

            /* Pause the Player. */
            Player.controls.pause();
">
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Controls (objet)**](controls-object.md)
</dt> <dt>

[**Controls. isAvailable**](controls-isavailable.md)
</dt> </dl>

 

 





