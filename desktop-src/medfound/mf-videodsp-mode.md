---
description: Définit le mode de traitement de la Stabilisation vidéo MFT.
ms.assetid: 0D49892A-8628-4F2B-B41B-51160A19DC9B
title: Attribut MF_VIDEODSP_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88383e6bdd197e4912c660657eefa6b9e812fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114011"
---
# <a name="mf_videodsp_mode-attribute"></a>\_Attribut de \_ mode VIDEODSP MF

Définit le mode de traitement de la [**stabilisation vidéo MFT**](video-stabilization-mft.md).

## <a name="data-type"></a>Type de données

**MFVideoDSPMode** stocké en tant que **UIINT32**

## <a name="remarks"></a>Notes

La valeur de cet attribut est une valeur d’énumération [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) . Cet attribut peut être utilisé pour activer ou désactiver la stabilisation d’image et peut être mis à jour pour chaque exemple de sortie.

Pour définir cet attribut :

1.  Appelez [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) sur la MFT de stabilisation vidéo pour recevoir un pointeur [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
2.  Appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) pour définir l’attribut.

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

[**Stabilisation vidéo MFT**](video-stabilization-mft.md)
</dt> </dl>

 

 




