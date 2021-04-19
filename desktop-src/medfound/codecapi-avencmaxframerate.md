---
description: Définit la vitesse d’entrée maximale en temps réel des trames vidéo en cours d’alimentation sur l’encodeur.
ms.assetid: ACBE8799-A81C-44C3-B985-88ADFB1E51B4
title: CODECAPI_AVEncMaxFrameRate, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c04d1fd1297f299db133cd98bd493c968fcc29c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513339"
---
# <a name="codecapi_avencmaxframerate-property"></a>CODECAPI \_ propriété AVEncMaxFrameRate

Définit la vitesse d’entrée maximale en temps réel des trames vidéo en cours d’alimentation sur l’encodeur.

## <a name="data-type"></a>Type de données

**ULONGULONG** (VT \_ UI8)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncMaxFrameRate**

## <a name="remarks"></a>Notes

Cette propriété permet à l’appelant de spécifier la vitesse d’entrée maximale en temps réel des trames vidéo en cours d’alimentation sur l’encodeur. Cela donne à l’encodeur une indication de la fréquence nécessaire au traitement des trames entrantes. Cela est utile pour les encodeurs qui se définissent eux-mêmes dans une configuration d’état d’alimentation particulière en fonction de la résolution et de la fréquence d’images de la vidéo source.

La fréquence d’images est exprimée sous la forme d’un rapport. Les 32 bits supérieurs de la valeur de l’attribut contiennent le numérateur et les 32 inférieurs contiennent le dénominateur. Par exemple, si la fréquence d’images est de 30 images par seconde (FPS), le ratio est de 30/1. Si la fréquence d’images est de 29,97 fps, le ratio est de 30000/1001.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

