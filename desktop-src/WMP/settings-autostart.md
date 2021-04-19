---
title: Paramètres. démarrage automatique
description: La propriété AutoStart spécifie ou récupère une valeur indiquant si l’élément multimédia actuel commence à être lu automatiquement.
ms.assetid: 553f8534-9e3e-4fdc-bfc1-551939969289
keywords:
- Paramètres. démarrage automatique du lecteur Windows Media
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
ms.openlocfilehash: 0d08b8f84f4a0b51225ed5692a25fa41cab809ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523493"
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



 

## <a name="remarks"></a>Notes

Si le **démarrage automatique** est défini sur true, l’élément multimédia commence à s’exécuter quand *joueur*. **URL**, *Player*. **currentPlaylist** ou *Player*. **currentMedia** est défini. Dans le cas contraire, il ne démarrera pas avant les *contrôles*. la méthode **Play** est appelée.

Étant donné que la propriété **AutoStart** pour le mode complet du lecteur Windows Media peut être définie globalement par des événements externes (tels que le chargement d’un CD), il n’existe pas de valeur par défaut fiable pour les apparences et les contrôles de lecteur à distance. Cela est dû au fait que le moteur de lecture du lecteur en mode complet est utilisé dans les deux cas.

Vous devez définir **AutoStart** sur false immédiatement avant de définir *Player*. **URL**, *Player*. **currentPlaylist** ou *Player*. **currentMedia** dans les apparences et les contrôles du lecteur Windows Media à distance si vous souhaitez vous assurer que l’élément multimédia ne démarre pas immédiatement. En outre, sauf si vous définissez **AutoStart** sur true juste avant de spécifier un élément multimédia, vous ne devez pas compter sur ce paramètre en remplacement de l’utilisation des *contrôles*. méthode **Play** .

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

[**Settings (objet)**](settings-object.md)
</dt> </dl>

 

 





