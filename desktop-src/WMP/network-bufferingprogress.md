---
title: Network. bufferingProgress
description: La propriété bufferingProgress récupère le pourcentage d’achèvement de la mise en mémoire tampon.
ms.assetid: d604159b-7c42-47f8-8085-53f859f24703
keywords:
- Lecteur Windows Media Network. bufferingProgress
topic_type:
- apiref
api_name:
- Network.bufferingProgress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e3a4f37f8f6b8ffe8ff93ca72b0c9551d7e314
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414568"
---
# <a name="networkbufferingprogress"></a>Network. bufferingProgress

La propriété **bufferingProgress** récupère le pourcentage d’achèvement de la mise en mémoire tampon.

## <a name="syntax"></a>Syntaxe

*lecteur*. *réseau*. **bufferingProgress**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture seule (**long**).

## <a name="remarks"></a>Notes

Chaque fois que la lecture est arrêtée et redémarrée, cette propriété est définie sur zéro. Elle n’est pas réinitialisée si la lecture est suspendue.

La mise en mémoire tampon s’applique uniquement au contenu de diffusion en continu. Cette propriété retourne des informations valides uniquement au moment de l’exécution, lorsque le *joueur*. La propriété **URL** est définie.

Utilisez l’événement *Player*. * * * * Buffering * * * * pour déterminer à quel moment la mise en mémoire tampon démarre ou s’arrête.

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise le *réseau*. **bufferingProgress** pour afficher le pourcentage de la mise en mémoire tampon terminée. Les informations s’affichent dans une balise DIV HTML créée avec ID = « BP ». L’exemple utilise un minuteur avec un intervalle de 1 seconde pour mettre à jour l’affichage. L’objet **Player** a été créé avec ID = "Player".


```JScript
<!-- Create an event handler for buffering. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   var idI; // Variable for the interval id.

   // Test whether buffering has started or stopped.
   if (true == Start){ 
      // Start the timer. Call the function to update the display every second.
      idI = window.setInterval("UpdateBP()", 1000);
   }

   else{
      // Buffering is complete. Stop the timer.
      window.clearInterval(idI);
   }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateBP(){
   BP.innerHTML = "";
   BP.innerHTML = "Buffering progress: " + Player.network.bufferingProgress;
   BP.innerHTML += " percent complete";
}
</SCRIPT>

```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet réseau**](network-object.md)
</dt> <dt>

[**Player. Buffering (événement)**](player-player-buffering.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 





