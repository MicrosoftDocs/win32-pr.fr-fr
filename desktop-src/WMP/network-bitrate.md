---
title: Réseau. débit binaire
description: La propriété de débit binaire récupère la vitesse de transmission actuelle en cours de réception.
ms.assetid: e970a43a-1773-4dc0-ac2f-115f698bc1f4
keywords:
- Lecteur Windows Media Network. debit binaire
topic_type:
- apiref
api_name:
- Network.bitRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec142885bdd718903e956f8e86b59c3753cb024ecccc5efb2f8494797ea6a818
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901779"
---
# <a name="networkbitrate"></a>Réseau. débit binaire

La propriété de **débit** binaire récupère la vitesse de transmission actuelle en cours de réception.

## <a name="syntax"></a>Syntaxe

*lecteur*. *réseau*. **débit binaire**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture seule (**long**).

## <a name="remarks"></a>Remarques

Cette valeur est une combinaison des vitesses de transmission des flux vidéo et audio actuels.

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise le *réseau*. **débit** binaire pour afficher la vitesse de transmission actuelle du média. Les informations sont affichées dans une balise DIV HTML créée avec ID = "BR". L’objet **Player** a été créé avec ID = "Player".


```JScript
<!<entity type="mdash"/>-Create an event handler. -->
<SCRIPT FOR = Player EVENT = PlayStateChange()>
   switch (Player.playState){

      case 3:

         if (Player.network.bitRate){

            BR.innerHTML = "Current Bit Rate: " + Player.network.bitRate;
            BR.innerHTML += " K bits/second";
          }

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
</dt> </dl>

 

 





