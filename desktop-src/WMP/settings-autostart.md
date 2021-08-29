---
title: Paramètres. démarrage automatique
description: La propriété AutoStart spécifie ou récupère une valeur indiquant si l’élément multimédia actuel commence à être lu automatiquement.
ms.assetid: 553f8534-9e3e-4fdc-bfc1-551939969289
keywords:
- Paramètres. autostart Lecteur Windows Media
topic_type:
- apiref
api_name:
- Settings.autoStart
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a12d8cf63fdf4d9652bf895f9110e233fb3f3665314e81a9d5aa5c6e1516b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123099"
---
# <a name="settingsautostart"></a>Paramètres. démarrage automatique

La propriété **AutoStart** spécifie ou récupère une valeur indiquant si l’élément multimédia actuel commence à être lu automatiquement.

## <a name="syntax"></a>Syntaxe

Player. Settings. AutoStart

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **valeur booléenne** en lecture/écriture.



| Valeur | Description                                                         |
|-------|---------------------------------------------------------------------|
| true  | Par défaut. La diffusion de l’élément multimédia commence automatiquement (consultez la section Notes). |
| false | La diffusion de l’élément multimédia ne commence pas automatiquement.                |



 

## <a name="remarks"></a>Remarques

Si le **démarrage automatique** est défini sur true, l’élément multimédia commence à s’exécuter quand *joueur*. **URL**, *Player*. **currentPlaylist** ou *Player*. **currentMedia** est défini. Dans le cas contraire, il ne démarrera pas avant les *contrôles*. la méthode **Play** est appelée.

étant donné que la propriété **autostart** pour le mode complet de Lecteur Windows Media peut être définie globalement par des événements externes (tels que le chargement d’un CD), il n’existe pas de valeur par défaut fiable pour les apparences et les contrôles de lecteur à distance. Cela est dû au fait que le moteur de lecture du lecteur en mode complet est utilisé dans les deux cas.

Vous devez définir **AutoStart** sur false immédiatement avant de définir *Player*. **URL**, *Player*. **currentPlaylist** ou *Player*. **currentMedia** dans les apparences et les contrôles de Lecteur Windows Media distants si vous souhaitez vous assurer que l’élément multimédia ne démarre pas immédiatement. En outre, sauf si vous définissez **AutoStart** sur true juste avant de spécifier un élément multimédia, vous ne devez pas compter sur ce paramètre en remplacement de l’utilisation des *contrôles*. méthode **Play** .

## <a name="examples"></a>Exemples

L’exemple suivant crée un élément de case à cocher HTML qui permet à l’utilisateur de spécifier si le contrôle du lecteur doit lire l’élément multimédia en cours automatiquement. L’objet **Player** a été créé avec ID = "Player".


```
<!-- Create an HTML CHECKBOX control. -->
<INPUT  TYPE = "CHECKBOX" ID = AS
              onClick = "
    /* Use the CHECKBOX state to specify the value 
       of the autoStart property. */
    Player.settings.autoStart = AS.checked;
"> 

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> <dt>

[**Paramètres Dessin**](settings-object.md)
</dt> </dl>

 

 





