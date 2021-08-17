---
title: VIDEO. Cursor
description: L’attribut Cursor spécifie ou récupère la valeur de curseur utilisée lorsque la souris se trouve sur une zone cliquable de la vidéo.
ms.assetid: 2faaf9cd-47be-47d5-ad4e-8f3bb322d812
keywords:
- VIDEO. cursor Lecteur Windows Media
topic_type:
- apiref
api_name:
- VIDEO.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73c39b40412a02e145b8063f473272184e1d7cf03caaa170de19bde7fad37a50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134242"
---
# <a name="videocursor"></a>VIDEO. Cursor

L’attribut **Cursor** spécifie ou récupère la valeur de curseur utilisée lorsque la souris se trouve sur une zone cliquable de la vidéo.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture.



| Valeur            | Description                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| système           | Curseur dépendant de la plateforme (généralement une flèche).                                               |
| Toutefois             | Toutefois.                                                                                       |
| help             | Flèche avec un point d’interrogation indiquant que l’aide est disponible.                                      |
| sizeall          | Flèche à quatre pointes pointant vers le Nord, le sud, l’est et l’Ouest.                                   |
| sizenesw         | Flèche à deux pointes pointant vers le nord-est et le sud-ouest.                                      |
| sizens           | Flèche à deux pointes pointant vers le Nord et le sud.                                              |
| sizenwse         | Flèche à deux pointes pointant vers le Nord-Ouest et le sud-est.                                      |
| sizewe           | Flèche à deux pointes pointant vers l’Ouest et l’est.                                                |
| haut          | Flèche verticale pointant vers le haut.                                                             |
| \*. ani ou \* . cur | Tout fichier. ani ou. cur (doit se trouver dans le même répertoire que le fichier. WMS ou dans le fichier. WMZ). |



 

## <a name="remarks"></a>Remarques

À des fins de rendu, System est le curseur par défaut. La valeur par défaut Récupérée à partir de cet attribut est "" (chaîne vide).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément VIDEO**](video-element.md)
</dt> </dl>

 

 





