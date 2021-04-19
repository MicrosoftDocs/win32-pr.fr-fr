---
title: Controls. Previous, méthode
description: La méthode précédente définit l’élément actuel à l’élément précédent dans la sélection.
ms.assetid: 09f83306-5e82-4384-ad28-38e406a401d8
keywords:
- méthode précédente lecteur Windows Media
- méthode Previous lecteur Windows Media, classe de contrôles
- Controls, classe Windows Media Player, méthode Previous
topic_type:
- apiref
api_name:
- Controls.previous
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b8fcfacd93412f467e6ef1def5afa6305a6bc0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530995"
---
# <a name="controlsprevious-method"></a>Controls. Previous, méthode

La méthode **précédente** définit l’élément actuel à l’élément précédent dans la sélection.

## <a name="syntax"></a>Syntaxe


```JScript
Controls.previous()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Si la sélection se trouve sur la première entrée lors de l’appel de la méthode **précédente** , la dernière entrée de la sélection deviendra celle en cours.

## <a name="examples"></a>Exemples

L’exemple suivant crée un élément BUTTON HTML qui utilise **Previous** pour accéder à l’élément précédent dans la sélection actuelle. L’objet **Player** a été créé avec ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "PREV"  NAME = "PREV"  VALUE = "|<<"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Previous'))

            /* Move to the preceding item in the playlist. */
            Player.controls.previous();
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

[**Contrôles. Next**](controls-next.md)
</dt> <dt>

[**Controls. Stop**](controls-stop.md)
</dt> </dl>

 

 





