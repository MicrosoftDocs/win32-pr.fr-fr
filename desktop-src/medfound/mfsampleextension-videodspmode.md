---
description: Indique si la stabilisation vidéo a été appliquée à une image vidéo.
ms.assetid: 13F877A3-7600-400F-9071-FE1B83027355
title: Attribut MFSampleExtension_VideoDSPMode (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 309d4b5b68455e78ba63074b9d8ec5e4cbde4fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534445"
---
# <a name="mfsampleextension_videodspmode-attribute"></a>\_Attribut MFSampleExtension VideoDSPMode

Indique si la stabilisation vidéo a été appliquée à une image vidéo.

## <a name="data-type"></a>Type de données

**MFVideoDSPMode** stocké en tant que **UInt32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>S’applique à

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Notes

La [**stabilisation vidéo MFT**](video-stabilization-mft.md) définit cet attribut sur les exemples de sortie qu’il produit. La valeur de l’attribut est une valeur d’énumération [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) . Si la valeur est **MFVideoDSPMode \_ stabilisation**, cela signifie que la table MFT a appliqué la stabilisation de l’image au frame.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Exemples d’attributs](sample-attributes.md)
</dt> <dt>

[Exemples de supports](media-samples.md)
</dt> <dt>

[**Stabilisation vidéo MFT**](video-stabilization-mft.md)
</dt> </dl>

 

 




