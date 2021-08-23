---
title: Réseau. bande passante
description: La propriété bandWidth récupère la bande passante actuelle du clip.
ms.assetid: 2ef86f2a-98e9-4544-a740-c2237f06c135
keywords:
- réseau. bande passante Lecteur Windows Media
topic_type:
- apiref
api_name:
- Network.bandWidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40bd97ae2efe7513bc69d308a29356cfc7b141ecc84b816bdc7fad68d79aa785
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616876"
---
# <a name="networkbandwidth"></a>Réseau. bande passante

La propriété **Bandwidth** récupère la bande passante actuelle du clip.

## <a name="syntax"></a>Syntaxe

*lecteur*. *réseau*. **bande passante**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture seule (**long**).

## <a name="remarks"></a>Remarques

Cette propriété retourne zéro si le *joueur*. La propriété **URL** n’est pas définie. Cette propriété n’est valide que pour la diffusion multimédia en continu.

## <a name="examples"></a>Exemples

l’exemple de JScript Microsoft suivant utilise le *réseau*. **bande passante** pour afficher la bande passante du support actuel. Les informations s’affichent dans une balise DIV HTML créée avec ID = « BW ». L’objet **Player** a été créé avec ID = "Player".


```JScript
<!-- Create an event handler for play state.-->
<SCRIPT FOR = Player EVENT = PlayStateChange()>

   switch (Player.playState){

      case 3:

         if (Player.network.bandwidth != 0){
  
            BW.innerHTML = "Current Bandwidth: " + Player.network.bandWidth;
            BW.innerHTML += " K bits/second";
         }

         else
            BW.innerHTML = "Bandwidth is only available for streaming media.";

            break;

      default:
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

 

 





