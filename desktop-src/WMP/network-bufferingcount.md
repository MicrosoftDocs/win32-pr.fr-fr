---
title: Network. bufferingCount
description: La propriété bufferingCount récupère le nombre de fois que la mise en mémoire tampon s’est produite lors de la lecture du clip.
ms.assetid: 25a58795-161e-4290-8ea7-51acca968ef9
keywords:
- Lecteur Windows Media Network. bufferingCount
topic_type:
- apiref
api_name:
- Network.bufferingCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d19c80715ca04965927bb0a50450213d707beeb124fd671fd8071e2cdd90e3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901759"
---
# <a name="networkbufferingcount"></a>Network. bufferingCount

La propriété **bufferingCount** récupère le nombre de fois que la mise en mémoire tampon s’est produite lors de la lecture du clip.

## <a name="syntax"></a>Syntaxe

*lecteur*. *réseau*. **bufferingCount**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture seule (**long**).

## <a name="remarks"></a>Remarques

Chaque fois que la lecture est arrêtée et redémarrée, cette propriété est définie sur zéro. Elle n’est pas réinitialisée si la lecture est suspendue.

La mise en mémoire tampon s’applique uniquement au contenu de diffusion en continu. Cette propriété retourne des informations valides uniquement au moment de l’exécution lorsque le *joueur*. La propriété **URL** est définie.

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise le *réseau*. **bufferingCount** pour afficher le nombre de fois que la mise en mémoire tampon se produit pendant la lecture. Les informations sont affichées dans une balise DIV HTML créée avec ID = "CB". L’objet **Player** a été créé avec ID = "Player".


```JScript
<!-- Create an event handler. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   if (true == Start) 
      CB.innerHTML = "Buffering count: " + Player.network.bufferingCount;
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

 

 





