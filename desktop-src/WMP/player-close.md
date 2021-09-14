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
ms.openlocfilehash: debc2667c42da92b3a2639e0f14c767d2b5b0651
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192735"
---
# <a name="playerclose-method"></a>Player. Close, méthode

la méthode **close** libère Lecteur Windows Media ressources.

## <a name="syntax"></a>Syntaxe


```JScript
Player.close()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

cette méthode ferme le fichier multimédia numérique en cours, et non Lecteur Windows Media lui-même.

## <a name="examples"></a>Exemples

l’exemple suivant crée un élément bouton HTML qui, lorsque vous cliquez dessus, arrête la lecture dans Lecteur Windows Media et libère les ressources en cours d’utilisation. L’objet **Player** a été créé avec ID = "Player".


```JScript
<INPUT  TYPE = "BUTTON"  ID = "CLOSEIT"  VALUE = "Close it"  onClick = "

        /* Close the Player object. */
        Player.close();
">

```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> </dl>

 

 





