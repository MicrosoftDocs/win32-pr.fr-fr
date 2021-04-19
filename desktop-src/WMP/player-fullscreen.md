---
title: Player. fullScreen
description: La propriété fullScreen spécifie ou récupère une valeur indiquant si le contenu vidéo est lu en mode plein écran.
ms.assetid: 43eeeddd-13a6-44d8-9cff-a60e976fc189
keywords:
- Lecteur Windows Media Player. fullScreen
topic_type:
- apiref
api_name:
- Player.fullScreen
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3f71b4100c359effd95f79c574a52b5a5bae28c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542454"
---
# <a name="playerfullscreen"></a>Player. fullScreen

La propriété **fullscreen** spécifie ou récupère une valeur indiquant si le contenu vidéo est lu en mode plein écran.

## <a name="syntax"></a>Syntaxe

*lecteur* . **plein écran**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **valeur booléenne** en lecture/écriture.



| Valeur | Description                                                    |
|-------|----------------------------------------------------------------|
| true  | Le contenu vidéo est lu en mode plein écran.              |
| false | Par défaut. Le contenu vidéo n’est pas lu en mode plein écran. |



 

## <a name="remarks"></a>Notes

Pour que le mode plein écran fonctionne correctement quand vous incorporez le contrôle du lecteur Windows Media, la zone d’affichage de la vidéo doit avoir une hauteur et une largeur d’au moins un pixel. Si **UIMODE** a la valeur « mini » ou « Full », la hauteur du contrôle lui-même doit être supérieure ou égale à 65 pour s’adapter à la zone d’affichage vidéo en plus de l’interface utilisateur.

Si **UIMODE** a la valeur « invisible », l’affectation de la valeur true à cette propriété génère une erreur et n’affecte pas le comportement du contrôle.

Pendant la lecture en plein écran, le lecteur Windows Media masque le curseur de la souris quand **enableContextMenu** est égal à false et **UIMODE** est égal à « None ».

Si **UIMODE** a la valeur « Full » ou « mini », le lecteur Windows Media affiche les contrôles de transport en mode plein écran lorsque le curseur de la souris se déplace. Après un bref intervalle d’absence de mouvement de la souris, les contrôles de transport sont masqués. Si **UIMODE** a la valeur « None », aucun contrôle n’est affiché en mode plein écran.

**Remarque**

L’affichage des contrôles de transport en mode plein écran nécessite le système d’exploitation Windows XP.

Si les contrôles de transport ne s’affichent pas en mode plein écran, le lecteur Windows Media quitte automatiquement le mode plein écran lorsque la lecture s’arrête.

**Remarque**

Veillez à toujours informer l’utilisateur sur la manière de revenir en mode plein écran.

## <a name="examples"></a>Exemples

L’exemple suivant crée un bouton d’entrée HTML qui utilise *Player*. **plein** écran pour faire basculer un objet lecteur incorporé en mode plein écran. L’objet **Player** a été créé avec ID = "Player".


```
<INPUT type = button 
       value = "Full Screen" 
       name = FSBUTTON
       onclick = "
               /* Check to be sure the player is playing. */
               if (Player.playState == 3) 
                  Player.fullScreen = 'true';
               ">
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> </dl>

 

 





