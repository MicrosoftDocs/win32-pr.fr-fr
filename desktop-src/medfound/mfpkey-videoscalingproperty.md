---
description: Spécifie si le codec utilise l’optimisation de la mise à l’échelle vidéo.
ms.assetid: a21d0100-e020-4e74-b8e3-bb7071194828
title: MFPKEY_VIDEOSCALING, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da2dc069d70b167dd8da6cb308d70149aec1028f3aaf4e50b5c1cc8ab11104c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887650"
---
# <a name="mfpkey_videoscaling-property"></a>MFPKEY \_ propriété VIDEOSCALING

Spécifie si le codec utilise l’optimisation de la mise à l’échelle vidéo.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCVideoScaling g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

0

## <a name="remarks"></a>Remarques

La mise à l’échelle vidéo est un type d’optimisation de perception qui peut améliorer la qualité visuelle de la vidéo encodée à des vitesses de transmission faibles. L’optimisation de la mise à l’échelle vidéo réduit les artefacts prononcés, mais peut sacrifier les détails de l’image. Cette optimisation affecte la plage de luminance de la vidéo encodée comme décrit ci-dessous, mais n’affecte pas la résolution physique de la vidéo de sortie.

Cette propriété peut être définie sur l’une des valeurs suivantes.



| Valeur | Description                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------|
| 0     | La mise à l’échelle vidéo ne sera pas utilisée.                                                                                       |
| 1     | L’encodeur utilise l’optimisation de la mise à l’échelle vidéo classique. La plage de luminance sera mise à l’échelle de 0... 255 à 26... 229. |
| 2     | L’encodeur utilise l’optimisation de la mise à l’échelle vidéo agressive. La plage de luminance sera mise à l’échelle de 0... 255 à 31... 224.   |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




