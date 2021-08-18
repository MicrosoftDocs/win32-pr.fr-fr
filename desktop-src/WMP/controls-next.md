---
title: Controls. Next, méthode
description: La méthode suivante définit l’élément actuel à l’élément suivant dans la sélection.
ms.assetid: 67436c76-8fb9-4350-86f3-67f5e9e6dca1
keywords:
- méthode suivante Lecteur Windows Media
- next, méthode Lecteur Windows Media, classe controls
- controls, classe Lecteur Windows Media, next, méthode
topic_type:
- apiref
api_name:
- Controls.next
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83a40c063163b0dadaa3db2d0d6281ace64312f68ee999763e6b27d4bd98f84d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997469"
---
# <a name="controlsnext-method"></a>Controls. Next, méthode

La méthode **suivante** définit l’élément actuel à l’élément suivant dans la sélection.

## <a name="syntax"></a>Syntaxe


```JScript
Controls.next()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Si la sélection se trouve sur la dernière entrée **lors de** l’appel de la méthode, la première entrée de la sélection devient la dernière.

Pour les sélections côté serveur, cette méthode passe à l’élément suivant dans la sélection côté serveur, et non à la sélection du client.

Lors de la lecture d’un DVD, cette méthode passe au chapitre logique suivant dans la séquence de lecture, qui peut ne pas être le chapitre suivant de la sélection. Quand le DVD est toujours en cours d’exécution, cette méthode passe à l’étape suivante.

## <a name="examples"></a>Exemples

L’exemple suivant crée un élément bouton HTML qui utilise **Next** pour passer à l’élément suivant dans la sélection actuelle. L’objet **Player** a été créé avec ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "NEXT"  NAME = "NEXT"  VALUE = ">>|"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Next'))

            /* Move to the next item in the playlist. */
            Player.controls.next();
">

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Controls (objet)**](controls-object.md)
</dt> <dt>

[**Contrôles. Previous**](controls-previous.md)
</dt> <dt>

[**Controls. Stop**](controls-stop.md)
</dt> </dl>

 

 





