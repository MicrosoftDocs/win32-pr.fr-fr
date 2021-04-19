---
title: Controls. fastForward, méthode
description: La méthode fastForward démarre la lecture rapide de l’élément multimédia dans le sens avant. | Controls. fastForward, méthode
ms.assetid: 69cee803-f76b-4a8c-a2c2-1870665afaf9
keywords:
- méthode fastForward lecteur Windows Media
- méthode fastForward lecteur Windows Media, classe de contrôles
- Classe Controls lecteur Windows Media, méthode fastForward
topic_type:
- apiref
api_name:
- Controls.fastForward
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20d033b8b025955e57a9c3ebed00a6d7a92a666e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523976"
---
# <a name="controlsfastforward-method"></a>Controls. fastForward, méthode

La méthode **fastForward** démarre la lecture rapide de l’élément multimédia dans le sens avant.

## <a name="syntax"></a>Syntaxe


```JScript
Controls.fastForward()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La méthode **fastForward** lit le clip à cinq fois la vitesse normale. L’appel de **fastForward** modifie les *paramètres*. propriété **rate** sur 5,0. Si le **taux** est modifié par la suite ou si la **lecture** ou l' **arrêt** est appelé, le lecteur Windows Media arrête le transfert rapide.

La méthode **fastForward** ne fonctionne pas pour les diffusions en direct et certains types de média. Pour déterminer si vous pouvez avancer rapidement dans un clip, appelez **isAvailable**(« Fastforward »).

## <a name="examples"></a>Exemples

L’exemple suivant crée un élément BUTTON HTML qui utilise **fastForward** pour démarrer la lecture rapide de l’élément multimédia. L’objet **Player** a été créé avec ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "FF"  NAME = "FF"  VALUE = ">>"  

    /* Execute JScript when the BUTTON is clicked. 
       Check first to make sure fast-forward mode is available
       for this particular media item */
    onClick = "if (Player.controls.isAvailable('FastForward'))
        Player.controls.fastForward();
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

[**Controls. isAvailable**](controls-isavailable.md)
</dt> <dt>

[**Controls. Play**](controls-play.md)
</dt> <dt>

[**Controls. Stop**](controls-stop.md)
</dt> <dt>

[**Settings. rate**](settings-rate.md)
</dt> </dl>

 

 





