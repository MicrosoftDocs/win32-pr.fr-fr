---
description: Contrôle la signalisation de MFSampleExtension \_ MeanAbsoluteDifference par le biais de IMFAttribute sur chaque échantillon de sortie.
ms.assetid: 61C0F431-FBF5-4B17-8F3A-0F6AD2BA33B7
title: CODECAPI_AVEncVideoMeanAbsoluteDifference, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f58a7bc0da9fce88c0b8137d800d527d4717801c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516199"
---
# <a name="codecapi_avencvideomeanabsolutedifference-property"></a>CODECAPI \_ propriété AVEncVideoMeanAbsoluteDifference

Contrôle la signalisation de [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) par le biais de [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) sur chaque échantillon de sortie.

## <a name="data-type"></a>Type de données

**ULong** (VT \_ UI4)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncVideoMeanAbsoluteDifference**

## <a name="remarks"></a>Notes

Si l’application définit une valeur différente de zéro, l’encodeur doit ajouter l’exemple d’attribut [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) à chaque exemple de sortie. L' \_ attribut MFSampleExtension MeanAbsoluteDifference indique la différence absolue moyenne entre les échantillons source et les échantillons prédits dans le plan Y.

Si l’encodeur retourne 0 pour **GetParameterRange**, l’encodeur ne prend pas en charge la sortie de [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) sur les exemples de sortie.

La valeur par défaut doit être 0.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




