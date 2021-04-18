---
title: Network. receptionQuality
description: La propriété receptionQuality récupère le pourcentage de paquets reçus au cours des 30 dernières secondes.
ms.assetid: 432f7f0a-0130-4485-b4a3-daa80ce9bb36
keywords:
- Lecteur Windows Media Network. receptionQuality
topic_type:
- apiref
api_name:
- Network.receptionQuality
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3706ba4d953f80c4a9e799971a7e73d49553c709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526815"
---
# <a name="networkreceptionquality"></a>Network. receptionQuality

La propriété **receptionQuality** récupère le pourcentage de paquets reçus au cours des 30 dernières secondes.

## <a name="syntax"></a>Syntaxe

*lecteur*. *réseau*. **receptionQuality**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture seule (**long**).

## <a name="remarks"></a>Notes

Le nombre de paquets reçus, perdus et récupérés pendant la diffusion en continu est analysé une fois par seconde. **receptionQuality** est le pourcentage de paquets qui n’ont pas été perdus au cours des 30 dernières secondes.

Chaque fois que la lecture est arrêtée et redémarrée, cette propriété est définie sur zéro. Elle n’est pas réinitialisée si la lecture est suspendue.

Cette propriété retourne des informations valides uniquement au moment de l’exécution et uniquement si le *joueur*. La propriété **URL** est également définie.

## <a name="examples"></a>Exemples

L’exemple JScript suivant utilise le *réseau*. **receptionQuality** pour afficher le pourcentage de paquets reçus. Les informations sont affichées dans une balise DIV HTML créée avec ID = "RQ". L’exemple utilise un minuteur avec un intervalle de 30 secondes pour mettre à jour l’affichage. L’objet **Player** a été créé avec ID = "Player".


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   var idI; // Variable for the interval id.

   // Test whether content is playing.
   if (3 == NewState){
         // Start the timer. Update the display every 30 seconds.
         idI = window.setInterval("UpdateRQ()", 30000);
   }

      else{
         // Not playing; stop the timer.
         window.clearInterval(idI);
      }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateRQ(){
         RQ.innerHTML = "";
         RQ.innerHTML = "Reception quality: " + Player.network.receptionQuality;
         RQ.innerHTML += "%";         
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

[**Player. URL**](player-url.md)
</dt> </dl>

 

 





