---
title: Network. framesSkipped
description: La propriété framesSkipped récupère le nombre total de trames ignorées lors de la lecture.
ms.assetid: fc7561a4-1e52-4192-b8df-ed2fb407fb78
keywords:
- Lecteur Windows Media Network. framesSkipped
topic_type:
- apiref
api_name:
- Network.framesSkipped
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f33b778fffce071c47cb455f09e468243abab6a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413333"
---
# <a name="networkframesskipped"></a>Network. framesSkipped

La propriété **framesSkipped** récupère le nombre total de trames ignorées lors de la lecture.

## <a name="syntax"></a>Syntaxe

*lecteur*. *réseau*. **framesSkipped**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture seule (**long**).

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise le *réseau*. **framesSkipped** pour afficher le nombre total de trames ignorées lors de la lecture lorsque l’utilisateur clique sur un bouton. Les informations s’affichent dans une balise DIV HTML créée avec ID = « FS ». L’objet **Player** a été créé avec ID = "Player".


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "skipped" NAME = "skipped"
       VALUE = "Count frames skipped" 
       onClick = "FS.innerHTML = 'Frames skipped: ' + Player.network.framesSkipped;">

```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet réseau**](network-object.md)
</dt> </dl>

 

 





