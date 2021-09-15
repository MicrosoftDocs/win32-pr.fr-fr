---
title: Réseau. cadence
description: La propriété cadencer récupère la fréquence d’images vidéo actuelle en images par centaines de secondes. Par exemple, une valeur de 2998 indique 29,98 images par seconde.
ms.assetid: ee30dce5-a42e-4be5-ab4b-0d5f8869d23a
keywords:
- réseau. cadence Lecteur Windows Media
topic_type:
- apiref
api_name:
- Network.frameRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30ec6e16a3cef86a385525a793d73a50c3124e21
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413334"
---
# <a name="networkframerate"></a>Réseau. cadence

La propriété **cadencer** récupère la fréquence d’images vidéo actuelle en images par centaines de secondes. Par exemple, une valeur de 2998 indique 29,98 images par seconde.

## <a name="syntax"></a>Syntaxe

*lecteur*. *réseau*. **fréquence** d’images

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture seule (**long**).

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise le *réseau*. **cadence** d’images pour afficher la fréquence d’images actuelle. Les informations sont affichées dans une balise DIV HTML créée avec ID = "FR". L’objet **Player** a été créé avec ID = "Player".


```JScript
<!-- Create an event handler for play state. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   switch (NewState){
      case 3:
          // Display the current frame rate.
          FR.innerHTML = "Frame Rate: ";
          FR.innerHTML += Player.network.frameRate;
          break;

      default:
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

[**Network. encodedFrameRate**](network-encodedframerate.md)
</dt> </dl>

 

 





