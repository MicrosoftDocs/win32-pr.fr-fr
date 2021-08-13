---
title: Player. Close, méthode
description: la méthode close libère Lecteur Windows Media ressources.
ms.assetid: 15bd5a05-dbfa-4bea-90c2-afd9f69631e0
keywords:
- fermer la méthode Lecteur Windows Media
- close, méthode Lecteur Windows Media, classe Player
- Player, classe Lecteur Windows Media, close, méthode
topic_type:
- apiref
api_name:
- Player.close
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29e68aed11b095dff80c8c91c88410f98b9a236bbcadcbff75da0fc0de392fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119467879"
---
# <a name="playerclose-method"></a>Player. Close, méthode

la méthode **close** libère Lecteur Windows Media ressources.

## <a name="syntax"></a>Syntaxe


```JScript
Player.close()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

cette méthode ferme le fichier multimédia numérique en cours, et non Lecteur Windows Media lui-même.

## <a name="examples"></a>Exemples

l’exemple suivant crée un élément bouton HTML qui, lorsque vous cliquez dessus, arrête la lecture dans Lecteur Windows Media et libère les ressources en cours d’utilisation. L’objet **Player** a été créé avec ID = "Player".


```JScript
<INPUT  TYPE = "BUTTON"  ID = "CLOSEIT"  VALUE = "Close it"  onClick = "

        /* Close the Player object. */
        Player.close();
">

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> </dl>

 

 





