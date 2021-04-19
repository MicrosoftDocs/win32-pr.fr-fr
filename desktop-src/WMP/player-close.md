---
title: Player. Close, méthode
description: La méthode Close libère les ressources du lecteur Windows Media.
ms.assetid: 15bd5a05-dbfa-4bea-90c2-afd9f69631e0
keywords:
- méthode Close lecteur Windows Media
- méthode Close lecteur Windows Media, classe Player
- Classe player lecteur Windows Media, méthode Close
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
ms.openlocfilehash: debc2667c42da92b3a2639e0f14c767d2b5b0651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542634"
---
# <a name="playerclose-method"></a>Player. Close, méthode

La méthode **Close** libère les ressources du lecteur Windows Media.

## <a name="syntax"></a>Syntaxe


```JScript
Player.close()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode ferme le fichier multimédia numérique en cours, et non le lecteur Windows Media lui-même.

## <a name="examples"></a>Exemples

L’exemple suivant crée un élément bouton HTML qui, lorsque vous cliquez dessus, arrête la lecture dans le lecteur Windows Media et libère les ressources en cours d’utilisation. L’objet **Player** a été créé avec ID = "Player".


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

 

 





