---
title: Player. uiMode
description: La propriété uiMode spécifie ou récupère une valeur indiquant les contrôles qui sont affichés dans l’interface utilisateur.
ms.assetid: 6297d22b-e8ed-4f28-83f6-b74d3265c520
keywords:
- Lecteur Windows Media Player. uiMode
topic_type:
- apiref
api_name:
- Player.uiMode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b1fd2e8e3a2ac6314255cd6ebc350b2ace8cb63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541079"
---
# <a name="playeruimode"></a>Player. uiMode

La propriété **UIMODE** spécifie ou récupère une valeur indiquant les contrôles qui sont affichés dans l’interface utilisateur.

## <a name="syntax"></a>Syntaxe

*lecteur* . **UIMODE**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture/écriture.



| Valeur     | Description                                                                                                                                                                                                           | Exemple audio                                          | Exemple de vidéo                                          |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|--------------------------------------------------------|
| invisibles | Le lecteur Windows Media est incorporé sans aucune interface utilisateur visible (fenêtre contrôles, vidéo ou visualisation).                                                                                                        | (Rien ne s’affiche.)                                | (Rien ne s’affiche.)                                |
| aucun      | Le lecteur Windows Media est incorporé sans contrôles, et seule la fenêtre vidéo ou visualisation s’affiche.                                                                                                         | ![« aucune » avec l’audio](images/uimode-none-audio-v11.png) | ![« aucune » avec vidéo](images/uimode-none-video-v11.png) |
| minimales      | Le lecteur Windows Media est incorporé avec la fenêtre d’État, les commandes lecture/pause, arrêter, muet et volume affichées en plus de la fenêtre vidéo ou visualisation.                                                          | ![« mini » avec l’audio](images/uimode-mini-audio-v11.png) | ![« mini » avec vidéo](images/uimode-mini-video-v11.png) |
| complet      | Par défaut. Le lecteur Windows Media est intégré à la fenêtre d’État, à la barre de recherche, aux commandes lecture/pause, arrêter, muet, suivant, précédent, avance rapide, inversée rapide et volume, en plus de la fenêtre vidéo ou de visualisation. | ![« Full » avec l’audio](images/uimode-full-audio-v11.png) | ![« Full » avec vidéo](images/uimode-full-video-v11.png) |
| custom    | Le lecteur Windows Media est incorporé avec une interface utilisateur personnalisée. Ne peut être utilisé que dans les programmes C++.                                                                                                                      | (L’interface utilisateur personnalisée s’affiche.)                  | (L’interface utilisateur personnalisée s’affiche.)                  |



 

## <a name="remarks"></a>Notes

Cette propriété spécifie l’apparence du lecteur Windows Media incorporé. Lorsque **UIMODE** a la valeur « None », « mini » ou « Full », une fenêtre est présente pour l’affichage des clips vidéo et des visualisations audio. Cette fenêtre peut être masquée en mode mini ou en mode complet en affectant à l’attribut **Height** de la balise **OBJECT** la valeur 40, qui est mesurée à partir du bas et laisse la partie Controls de l’interface utilisateur visible. Si aucune interface incorporée n’est souhaitée, affectez la valeur zéro aux attributs **Width** et **Height** .

Si **UIMODE** est défini sur « invisible », aucune interface utilisateur n’est affichée, mais l’espace est toujours réservé sur la page, comme indiqué par **Width** et **Height**. Cela est utile pour conserver la mise en page quand **UIMODE** peut changer. En outre, l’espace réservé est transparent, de sorte que tous les éléments superposés derrière le contrôle sont visibles.

Si **UIMODE** a la valeur « Full » ou « mini », le lecteur Windows Media affiche les contrôles de transport en mode plein écran. Si **UIMODE** a la valeur « None », aucun contrôle n’est affiché en mode plein écran.

Si la fenêtre est visible et que le contenu audio est lu, la visualisation affichée sera celle qui est la plus récemment utilisée dans le lecteur Windows Media.

Si **UIMODE** a la valeur « Custom » dans un programme C++ qui implémente **IWMPRemoteMediaServices**, le fichier d’apparence indiqué par **IWMPRemoteMediaServices :: GetCustomUIMode** s’affiche.

Pendant la lecture en plein écran, le lecteur Windows Media masque le curseur de la souris quand **enableContextMenu** est égal à false et **UIMODE** est égal à « None ».

## <a name="examples"></a>Exemples

L’exemple suivant crée un élément SELECT HTML qui permet à l’utilisateur de modifier l’interface utilisateur d’un objet **lecteur** incorporé. L’objet **Player** a été créé avec ID = "Player".


```
<!-- Create an HTML SELECT element. -->
<SELECT  ID = UI  LANGUAGE="JScript"

         /* Specify the UI mode the user selects. */
         onChange = "Player.uiMode = UI.value">

/* These are the four UI mode options. */
<OPTION VALUE="invisible">Invisible
<OPTION VALUE="none">No Controls
<OPTION VALUE="mini">Mini Player
<OPTION VALUE="full">Full Player
</SELECT>

```



Windows Media Player 10 Mobile : cette propriété accepte ou retourne uniquement les valeurs « None » ou « Full ». Sur les périphériques Smartphone, seul l’état de lecture et un compteur s’affichent lorsque *UIMODE* est défini sur « Full ».

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure. Lecteur Windows Media série 9 ou version ultérieure pour « invisible » ou « personnalisé ».<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPRemoteMediaServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
</dt> <dt>

[**IWMPRemoteMediaServices::GetCustomUIMode**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getcustomuimode)
</dt> <dt>

[**Objet Player**](player-object.md)
</dt> </dl>

 

 





