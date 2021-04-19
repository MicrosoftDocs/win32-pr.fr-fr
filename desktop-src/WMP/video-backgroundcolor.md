---
title: VIDEO. backgroundColor
description: L’attribut backgroundColor spécifie ou récupère la couleur d’arrière-plan du contrôle Video.
ms.assetid: 7acf7dc8-80c3-4620-ad89-4c8de20d17ee
keywords:
- VIDEO. backgroundColor lecteur Windows Media
topic_type:
- apiref
api_name:
- VIDEO.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 992ffd881498c3670eaaf5c075db9c6432cc1496
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542407"
---
# <a name="videobackgroundcolor"></a>VIDEO. backgroundColor

L’attribut **backgroundColor** spécifie ou récupère la couleur d’arrière-plan du contrôle Video.

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant toute valeur de couleur Microsoft Internet Explorer ou la valeur « None ». Sa valeur par défaut est « None », ce qui signifie que si aucune vidéo n’est associée au contrôle Video, le contrôle Video est transparent et l’arrière-plan est affiché.

## <a name="remarks"></a>Notes

Lorsque la vidéo est plus petite que la fenêtre et que **stretchToFit** a la valeur false, la couleur d’arrière-plan apparaît autour de la vidéo.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence de couleur**](color-reference.md)
</dt> <dt>

[**Élément VIDEO**](video-element.md)
</dt> <dt>

[**VIDÉO. stretchToFit**](video-stretchtofit.md)
</dt> </dl>

 

 





