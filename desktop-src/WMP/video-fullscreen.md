---
title: VIDEO. fullScreen
description: L’attribut fullScreen spécifie ou récupère une valeur indiquant si la vidéo est affichée en mode plein écran.
ms.assetid: de74d95a-31a2-4f65-811c-4e8018ee484a
keywords:
- VIDEO. fullScreen Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c27fa1bde6437b55689494751410145995862d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533375"
---
# <a name="videofullscreen"></a>VIDEO. fullScreen

L’attribut **fullscreen** spécifie ou récupère une valeur indiquant si la vidéo est affichée en mode plein écran.

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **valeur booléenne** en lecture/écriture.



| Valeur | Description                                          |
|-------|------------------------------------------------------|
| true  | La vidéo s’affiche en mode plein écran.                  |
| false | Par défaut. La vidéo ne s’affiche pas en mode plein écran. |



 

## <a name="remarks"></a>Notes

Cette propriété ne peut être spécifiée qu’au moment de l’exécution, une fois qu’un fichier a été chargé. Il doit donc être défini dans un gestionnaire d’événements de script. Le bouton d’échappement est utilisé pour revenir à un affichage normal.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément VIDEO**](video-element.md)
</dt> <dt>

[**VIDÉO. maintainAspectRatio**](video-maintainaspectratio.md)
</dt> <dt>

[**VIDÉO. shrinkToFit**](video-shrinktofit.md)
</dt> <dt>

[**VIDÉO. stretchToFit**](video-stretchtofit.md)
</dt> </dl>

 

 





