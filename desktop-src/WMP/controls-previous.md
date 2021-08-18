---
title: Controls. Previous, méthode
description: La méthode précédente définit l’élément actuel à l’élément précédent dans la sélection.
ms.assetid: 09f83306-5e82-4384-ad28-38e406a401d8
keywords:
- méthode précédente Lecteur Windows Media
- méthode previous Lecteur Windows Media, classe controls
- controls, classe Lecteur Windows Media, méthode previous
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
ms.openlocfilehash: f67dbc80fb731f32eefb36f2a0f66c852da3da69dbc6b7ae56c03ebafb06e07e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119328"
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

## <a name="remarks"></a>Remarques

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

 

 





