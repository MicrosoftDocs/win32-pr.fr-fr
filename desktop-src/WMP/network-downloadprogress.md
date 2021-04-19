---
title: Network. downloadProgress
description: La propriété downloadProgress récupère le pourcentage de téléchargement effectué.
ms.assetid: bb57ce84-babb-4dc2-bc2b-c40cbb587e91
keywords:
- Lecteur Windows Media Network. downloadProgress
topic_type:
- apiref
api_name:
- Network.downloadProgress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 605d7d08b346c5cc279176098b2a6d593a2fb925
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539597"
---
# <a name="networkdownloadprogress"></a>Network. downloadProgress

La propriété **downloadProgress** récupère le pourcentage de téléchargement effectué.

## <a name="syntax"></a>Syntaxe

*lecteur*. *réseau*. **downloadProgress**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture seule (**long**).

## <a name="remarks"></a>Notes

Lorsque le contrôle du lecteur Windows Media est connecté à un fichier multimédia qui peut être lu et téléchargé en même temps, la propriété **downloadProgress** retourne le pourcentage du fichier total téléchargé. Cette fonctionnalité n’est actuellement prise en charge que sur les serveurs Web. Les formats de fichier suivants peuvent être téléchargés et lus simultanément :

-   ASF (Advanced Systems Format)
-   Audio Windows Media (WMA)
-   Vidéo Windows Media (WMV)
-   MP3
-   MPEG4
-   WAV
-   Certains fichiers AVI

Utilisez le *lecteur*. Événement de **mise en mémoire tampon** pour déterminer à quel moment le téléchargement commence et se termine.

## <a name="examples"></a>Exemples

L’exemple JScript suivant utilise le *réseau*. **downloadProgress** pour afficher le pourcentage de téléchargement effectué. Les informations s’affichent dans une balise DIV HTML créée avec ID = « DP ». L’exemple utilise un minuteur avec un intervalle de 1 seconde pour mettre à jour l’affichage. L’objet **Player** a été créé avec ID = "Player".


```JScript
<!-- Create an event handler for buffering. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   var idI; // Variable for the interval id.
   
   // Test whether downloading has started or stopped.
   if (true == Start){ 
      // Start the timer. Call the function to update the display.
      idI = window.setInterval("UpdateDP()", 1000);
   }
   else{
      // Downloading is complete. Stop the timer.
      window.clearInterval(idI);
   }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateDP(){
   DP.innerHTML = "";
   DP.innerHTML = "Download progress: " + Player.network.downloadProgress;
   DP.innerHTML += " percent complete";
}
</SCRIPT>

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet réseau**](network-object.md)
</dt> <dt>

[**Player. Buffering (événement)**](player-player-buffering.md)
</dt> </dl>

 

 





