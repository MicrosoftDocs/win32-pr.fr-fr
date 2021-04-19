---
title: Controls. fastReverse, méthode
description: La méthode fastReverse démarre une analyse rapide de l’élément multimédia dans le sens inverse.
ms.assetid: 4fc61739-9006-4d62-b2c1-2b8e8830f2d9
keywords:
- méthode fastReverse lecteur Windows Media
- méthode fastReverse lecteur Windows Media, classe de contrôles
- Classe Controls lecteur Windows Media, méthode fastReverse
topic_type:
- apiref
api_name:
- Controls.fastReverse
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73e5a63c4299bf08c25e36e2d61924f3fb171792
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525438"
---
# <a name="controlsfastreverse-method"></a>Controls. fastReverse, méthode

La méthode **fastReverse** démarre une analyse rapide de l’élément multimédia dans le sens inverse.

## <a name="syntax"></a>Syntaxe


```JScript
Controls.fastReverse()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La méthode **fastReverse** analyse le clip en sens inverse à cinq fois la vitesse normale, en affichant uniquement les images clés s’il s’agit d’un fichier vidéo. L’appel de **fastReverse** modifie les *paramètres*. propriété **rate** sur 5,0. Si la **fréquence** est modifiée par la suite, ou si la **lecture** ou l' **arrêt** est appelé, le lecteur Windows Media arrête rapidement l’opération inverse.

Si l’élément fait partie d’une sélection, **fastReverse** s’arrête au début de la piste actuelle. Par exemple, si Track 3 se trouve dans **fastReverse**, lorsque le début de la piste 3 est atteint, le lecteur Windows Media ne passe pas à Track 2. Le nombre de lecture n’est pas incrémenté lors de l’appel de **fastReverse**.

Si vous appelez **fastForward** alors que **fastReverse** est en vigueur, **fastReverse** sera arrêté et **fastForward** démarrera.

Cette méthode ne fonctionne pas pour les diffusions en direct et certains types de média. Pour déterminer si vous pouvez utiliser l’inverse rapide dans un clip, appelez **isAvailable**(« FastReverse »).

## <a name="examples"></a>Exemples

L’exemple suivant crée un élément BUTTON HTML qui utilise **fastReverse** pour démarrer la lecture rapide et inversée de l’élément multimédia. L’objet **Player** a été créé avec ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "REW"  NAME = "REW"  VALUE = "<<"  

    /* Run JScript when the BUTTON is clicked. 
       Check first to make sure fast-reverse mode is available
       for this particular media item */
    onClick = "if (Player.controls.isAvailable('FastReverse'))
        Player.controls.fastReverse();
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

[**Controls. fastForward**](controls-fastforward.md)
</dt> <dt>

[**Controls. isAvailable**](controls-isavailable.md)
</dt> <dt>

[**Controls. Play**](controls-play.md)
</dt> <dt>

[**Controls. Stop**](controls-stop.md)
</dt> <dt>

[**Settings. rate**](settings-rate.md)
</dt> </dl>

 

 





