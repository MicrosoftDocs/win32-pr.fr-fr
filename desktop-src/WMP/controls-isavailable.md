---
title: Controls. isAvailable
description: La propriété isAvailable indique si un type spécifié d’informations est disponible ou si une action spécifiée peut être exécutée. | Controls. isAvailable
ms.assetid: d2bfaa67-eac9-4fc4-9424-636ddb4b35d6
keywords:
- Controls. isAvailable lecteur Windows Media
topic_type:
- apiref
api_name:
- Controls.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61afa07596a55208be63bd29759fd5f9f3e10170
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539951"
---
# <a name="controlsisavailable"></a>Controls. isAvailable

La propriété **isAvailable** indique si un type spécifié d’informations est disponible ou si une action spécifiée peut être exécutée.

``` syntax
player.controls.isAvailable(
        name
        )
```

## <a name="parameters"></a>Paramètres

*name*

**Chaîne** contenant l’une des valeurs suivantes.



| String          | Description                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| currentItem     | Détermine si l’utilisateur peut définir la propriété **CurrentItem** .                                                                                                 |
| currentMarker   | Détermine si l’utilisateur peut effectuer une recherche sur un marqueur spécifique.                                                                                                        |
| currentPosition | Détermine si l’utilisateur peut rechercher une position spécifique dans le fichier. Certains fichiers ne prennent pas en charge la recherche.                                                       |
| fastForward     | Détermine si le fichier prend en charge le transfert rapide et si cette fonctionnalité peut être appelée. De nombreux types de fichiers (ou flux en direct) ne prennent pas en charge fastForward. |
| fastReverse     | Détermine si le fichier prend en charge fastReverse et si cette fonctionnalité peut être appelée. De nombreux types de fichiers (ou flux en direct) ne prennent pas en charge fastReverse.     |
| Suivant            | Détermine si l’utilisateur peut Rechercher l’entrée suivante dans une sélection.                                                                                             |
| pause           | Détermine si la méthode **Pause** est disponible.                                                                                                             |
| répétition            | Détermine si la méthode de **lecture** est disponible.                                                                                                              |
| previous        | Détermine si l’utilisateur peut Rechercher l’entrée précédente dans une sélection.                                                                                         |
| étape            | Détermine si la méthode **Step** est disponible pendant la lecture.                                                                                              |
| stop            | Détermine si la méthode **Stop** est disponible.                                                                                                              |



 

## <a name="return-values"></a>Valeurs de retour

Cette méthode retourne une valeur **booléenne** .

## <a name="examples"></a>Exemples

L’exemple suivant crée un élément bouton HTML qui cherche à la position de départ de l’élément multimédia actuel. Le code JScript utilise **isAvailable** pour vérifier que le fichier prend en charge l’opération de recherche. L’objet **Player** a été créé avec ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "START"  NAME = "START"  VALUE = "Seek To Zero"

    /* If supported, seek to position zero. */
    onClick = "if (Player.controls.isAvailable('CurrentPosition'))
        Player.controls.currentPosition = 0;
">
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Controls (objet)**](controls-object.md)
</dt> </dl>

 

 





