---
description: La méthode SaveBookmark enregistre la position actuelle du disque et l’état de l’objet MSWebDVD afin que l’utilisateur puisse retourner au même endroit ultérieurement.
ms.assetid: 975687c5-f93e-4473-b23b-63e0ae6bbb5d
title: Méthode SaveBookmark (segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f45fec3a109b97c0ccbcb9a98736a01bba625537f1369fa7986cb6b5a669d35b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072713"
---
# <a name="savebookmark-method"></a>Méthode SaveBookmark

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `SaveBookmark` méthode enregistre la position actuelle du disque et l’état de l’objet **mswebdvd** pour permettre à l’utilisateur de revenir ultérieurement au même endroit.

``` syntax
MSWebDVD.SaveBookmark()
```

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Un signet est un instantané de l’état actuel du navigateur DVD. Cela comprend des informations telles que l’emplacement de lecture sur le disque et les flux audio et sous-images qui sont sélectionnés. En enregistrant un signet, l’utilisateur peut fermer l’application, arrêter l’ordinateur, puis revenir ultérieurement pour continuer à afficher le disque là où il s’était arrêté, avec tous les paramètres comme auparavant. Un seul signet peut être enregistré à un moment donné. Lorsque vous appelez `SaveBookmark` , l’ancien signet est remplacé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Segment. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RestoreBookmark**](restorebookmark-method.md)
</dt> </dl>

 

 




