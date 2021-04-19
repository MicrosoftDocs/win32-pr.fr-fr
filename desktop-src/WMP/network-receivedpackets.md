---
title: Network. receivedPackets
description: La propriété receivedPackets récupère le nombre de paquets reçus.
ms.assetid: db4f6f08-c248-4db8-ab19-fdd5d2794085
keywords:
- Lecteur Windows Media Network. receivedPackets
topic_type:
- apiref
api_name:
- Network.receivedPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bc792330cd107ca428ad0fbec930fe262a2f131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535329"
---
# <a name="networkreceivedpackets"></a>Network. receivedPackets

La propriété **receivedPackets** récupère le nombre de paquets reçus.

## <a name="syntax"></a>Syntaxe

*lecteur*. *réseau*. **receivedPackets**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture seule (**long**).

## <a name="remarks"></a>Notes

Chaque fois que la lecture du clip est arrêtée et redémarrée, cette propriété est définie sur zéro. Elle n’est pas réinitialisée si la lecture du fichier est suspendue.

## <a name="examples"></a>Exemples

L’exemple JScript suivant utilise le *réseau*. **receivedPackets** pour afficher le nombre de paquets reçus. Les informations sont affichées dans une balise DIV HTML créée avec l’ID = « RP ». L’exemple utilise un minuteur avec un intervalle de 1 seconde pour mettre à jour l’affichage. L’objet **Player** a été créé avec ID = "Player".


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>

   var idI; // Variable for the interval id.

   // Test whether packets may be arriving.
   switch (NewState){
      case 1, 2, 4, 5, 7, 8, 9:
          window.clearInterval(idI);
          break;

      default:
         idI = window.setInterval("UpdateRP()", 1000);

   }</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateRP(){
   RP.innerHTML = "";
   RP.innerHTML = "Packets received: " + Player.network.receivedPackets;         
}

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet réseau**](network-object.md)
</dt> </dl>

 

 





