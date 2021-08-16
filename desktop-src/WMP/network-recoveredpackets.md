---
title: Network. recoveredPackets
description: La propriété recoveredPackets récupère le nombre de paquets récupérés.
ms.assetid: ce10b906-2e8b-4b9f-83d0-56ba67cacd3f
keywords:
- Lecteur Windows Media Network. recoveredPackets
topic_type:
- apiref
api_name:
- Network.recoveredPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 464f7ad27603e506632d87254eaa4f76cbedf39ed15e353050cd13da0fa46204
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134932"
---
# <a name="networkrecoveredpackets"></a>Network. recoveredPackets

La propriété **recoveredPackets** récupère le nombre de paquets récupérés.

## <a name="syntax"></a>Syntaxe

*lecteur*. *réseau*. **recoveredPackets**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture seule (**long**).

## <a name="remarks"></a>Remarques

Chaque fois que la lecture est arrêtée et redémarrée, cette propriété est définie sur zéro. Elle n’est pas réinitialisée si la lecture est suspendue.

Cette propriété retourne des informations valides uniquement au moment de l’exécution et uniquement si le *joueur*. La propriété **URL** est également définie. Elle sera égale à zéro lors de l’utilisation du protocole HTTP, qui est sans perte.

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise le *réseau*. **recoveredPackets** pour afficher le nombre de paquets récupérés. Les informations s’affichent dans une balise DIV HTML créée avec ID = « PR ». L’exemple utilise un minuteur avec un intervalle de 1 seconde pour mettre à jour l’affichage. L’objet **Player** a été créé avec ID = "Player".


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   var idI; // Variable for the interval id.

   // Test whether content is playing.
   if (3 == NewState){
      // Start the timer. Call the function to update the display every second.
      idI = window.setInterval("UpdatePR()", 1000);
   }
   else{
      // Not playing; stop the timer.
      window.clearInterval(idI);
   }   
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdatePR(){
   PR.innerHTML = "";
   PR.innerHTML = "Packets recovered: " + Player.network.recoveredPackets;
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

 

 





