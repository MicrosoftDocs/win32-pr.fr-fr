---
description: L’attribut pafréquence spécifie un cadence, en images par seconde.
ms.assetid: 541a86e3-7736-4de4-b509-f8d61ef9bc58
title: Attribut de fréquence d’images (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2939126dbd849538bb30fcf7729e5f91dafa292b6db512398c915c8f8de2c9a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015657"
---
# <a name="framerate-attribute-directshow"></a>Attribut de fréquence d’images (DirectShow)

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

L' `framerate` attribut spécifie une cadence, en images par seconde.

## <a name="possible-values"></a>Valeurs possibles

Valeur à virgule flottante. La valeur doit inclure le zéro non significatif avant la décimale. Par exemple, 0,3, pas. 3. N’utilisez pas plus de sept chiffres décimaux.

## <a name="applies-to"></a>S'applique à

[**clip**](clip-element.md), [**groupe**](group-element.md), [**chronologie**](timeline-element.md)

## <a name="remarks"></a>Remarques

Pour l’élément **clip** , cet attribut spécifie la fréquence d’images par défaut de la source. Spécifiez l’attribut pour les séquences andDIB d’images fixes. Pour une image continue, définissez la valeur sur zéro. Pour une séquence DIB, utilisez une valeur différente de zéro. La valeur par défaut est zéro.

Pour l’élément **Group** , cet attribut spécifie la fréquence d’images de sortie pour le groupe.

Pour l’élément **Timeline** , cet attribut spécifie la fréquence d’images par défaut pour tous les groupes.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Attributs XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md)
</dt> <dt>

[**IAMTimelineGroup::SetOutputFPS**](iamtimelinegroup-setoutputfps.md)
</dt> <dt>

[**IAMTimeline::SetDefaultFPS**](iamtimeline-setdefaultfps.md)
</dt> </dl>

 

 



