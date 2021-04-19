---
title: Network. encodedFrameRate
description: La propriété encodedFrameRate récupère la fréquence d’images vidéo spécifiée par l’auteur du contenu en images par seconde.
ms.assetid: 7dad5c90-f750-48d7-9dda-3fc07394edcc
keywords:
- Lecteur Windows Media Network. encodedFrameRate
topic_type:
- apiref
api_name:
- Network.encodedFrameRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0008eb5d648dc7d3f51b40329ca3d830c3590c49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521626"
---
# <a name="networkencodedframerate"></a>Network. encodedFrameRate

La propriété **encodedFrameRate** récupère la fréquence d’images vidéo spécifiée par l’auteur du contenu en images par seconde.

## <a name="syntax"></a>Syntaxe

*lecteur*. *réseau*. **encodedFrameRate**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture seule (**long**).

## <a name="examples"></a>Exemples

L’exemple JScript suivant utilise le *réseau*. **encodedFrameRate** pour afficher la fréquence d’images spécifiée lors de l’encodage du fichier. Les informations sont affichées dans une balise DIV HTML créée avec ID = "FR". L’objet **Player** a été créé avec ID = "Player".


```JScript
<!-- Create an event handler for play state. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   switch (NewState){
      case 3:
          // Display the encoded frame rate.
          FR.innerHTML = "Encoded Frame Rate: ";
          FR.innerHTML += Player.network.encodedFrameRate;
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

[**Réseau. cadence**](network-framerate.md)
</dt> </dl>

 

 





