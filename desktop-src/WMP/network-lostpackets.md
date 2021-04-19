---
title: Network. lostPackets
description: La propriété lostPackets récupère le nombre de paquets perdus.
ms.assetid: b90faaaf-656a-4b9b-abfe-370e6f7c7c4b
keywords:
- Lecteur Windows Media Network. lostPackets
topic_type:
- apiref
api_name:
- Network.lostPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a780afaea1ba46c5e2d5c7eb55b9476f68c9570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525261"
---
# <a name="networklostpackets"></a>Network. lostPackets

La propriété **lostPackets** récupère le nombre de paquets perdus.

## <a name="syntax"></a>Syntaxe

*lecteur*. *réseau*. **lostPackets**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture seule (**long**).

## <a name="remarks"></a>Notes

Cette propriété n’est valide que pour la diffusion multimédia en continu et sera égale à zéro lors de l’utilisation du protocole HTTP, qui est sans perte.

Les paquets peuvent être perdus pour plusieurs raisons, telles que le type et la qualité de la connexion réseau.

Chaque fois que la lecture est arrêtée et redémarrée, cette propriété est définie sur zéro. Elle n’est pas réinitialisée si la lecture est suspendue et redémarrée. Cette propriété retourne des informations valides uniquement au moment de l’exécution, et uniquement si le *joueur*. La propriété **URL** est définie.

## <a name="examples"></a>Exemples

L’exemple JScript suivant utilise le *réseau*. **lostPackets** pour afficher le nombre total de paquets perdus lors de la lecture lorsque l’utilisateur clique sur un bouton. Les informations s’affichent dans une balise DIV HTML créée avec ID = « LP ». L’objet **Player** a été créé avec ID = "Player".


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "lostpkts" NAME = "lostpkts"
       VALUE = "Count lost packets" 
       onClick = "LP.innerHTML = 'Packets lost: ' + Player.network.lostPackets;">

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

 

 





