---
title: Network. sourceProtocol
description: La propriété sourceProtocol récupère le protocole source utilisé pour recevoir des données.
ms.assetid: f09bbcd0-9c34-49d1-8080-247aed2548d5
keywords:
- Lecteur Windows Media Network. sourceProtocol
topic_type:
- apiref
api_name:
- Network.sourceProtocol
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29e3f0ad63827605eb79a89325877e4bb83bfc62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535917"
---
# <a name="networksourceprotocol"></a>Network. sourceProtocol

La propriété **sourceProtocol** récupère le protocole source utilisé pour recevoir des données.

## <a name="syntax"></a>Syntaxe

*lecteur*. *réseau*. **sourceProtocol**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture seule.

## <a name="remarks"></a>Notes

Cette propriété a la valeur "" (chaîne vide) lors de la diffusion de contenu multimédia à partir d’un CD ou d’un DVD.

## <a name="examples"></a>Exemples

L’exemple JScript suivant utilise le *réseau*. **sourceProtocol** pour afficher le protocole source utilisé pour recevoir des données. Les informations s’affichent dans une balise DIV HTML créée avec ID = « SP ». L’objet **Player** a été créé avec ID = "Player".


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   if (3 == NewState){
     SP.innerHTML = "Source protocol: " + Player.network.sourceProtocol;
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
</dt> </dl>

 

 





