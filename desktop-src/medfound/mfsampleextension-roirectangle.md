---
description: Spécifie les limites de la zone d’intérêt qui indique la région du cadre qui requiert une qualité différente.
ms.assetid: F06CACF0-AE75-4707-8CD0-7BA7D51BB80A
title: Attribut MFSampleExtension_ROIRectangle (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71d84d2054caa96feaf7bfb4ccc7a91ecf4ac9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543487"
---
# <a name="mfsampleextension_roirectangle-attribute"></a>\_Attribut MFSampleExtension ROIRectangle

Spécifie les limites de la zone d’intérêt qui indique la région du cadre qui requiert une qualité différente.

## <a name="data-type"></a>Type de données

**[**Roi \_ ZONE**](/windows/desktop/api/mfapi/ns-mfapi-roi_area)** stockée en tant qu' **objet BLOB**

## <a name="remarks"></a>Notes

Après avoir correctement défini [CODECAPI \_ AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) sur une valeur différente de zéro sur une table MFT d’encodeur, l’application peut définir cet attribut sur les exemples d’entrée et s’attendre à ce qu’elle soit respectée.

Si [CODECAPI \_ AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) n’est pas défini sur une valeur différente de zéro, l' \_ attribut MFSampleExtension ROIRectangle est ignoré sur les exemples d’entrée.

MFSampleExtension \_ ROIRectangle est défini sur un exemple d’entrée et est appliqué uniquement à l’exemple d’entrée actuel.

Le champ **QPDelta** de la structure de la [**\_ zone roi**](/windows/desktop/api/mfapi/ns-mfapi-roi_area) spécifie le delta du paramètre de quantification pour la région spécifiée à partir du reste du cadre. Si **QPDelta** est positif, cela indique que l’application souhaite que le rectangle ait une qualité inférieure à celle du reste du cadre.

**Encodeurs H. 264/AVC :** **QPDelta** doit être compris entre \[ -25, + 25 \] . L’encodeur doit s’assurer que le QP final est dans une plage valide pour la norme vidéo.

La région spécifiée n’a pas besoin d’être alignée en Mo. Les encodeurs ont la possibilité de choisir la limite réelle. Il est recommandé de couvrir la totalité de la région spécifiée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[Applications Windows 8.1 Desktop Apps \| UWP\]<br/>                                |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]<br/>                     |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




