---
description: Spécifie la manière dont une image vidéo 3D est stockée dans un échantillon de média.
ms.assetid: 1B996B22-C76B-47E5-8937-1E5E672E32EC
title: Attribut MFSampleExtension_3DVideo_SampleFormat (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14829c879c151149edc48bf1635b3a5591ddeac5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115011"
---
# <a name="mfsampleextension_3dvideo_sampleformat-attribute"></a>MFSampleExtension \_ 3DVideo \_ SampleFormat, attribut

Spécifie la manière dont une image vidéo 3D est stockée dans un échantillon de média.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

La valeur de cet attribut est un membre de l’énumération [**MFVideo3DSampleFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dsampleformat) .

Un composant qui génère des images vidéo 3D doit affecter la **valeur true** à cet attribut sur chaque échantillon de média qui contient un frame 3D. L’attribut est ignoré si l’attribut [MFSampleExtension \_ 3DVideo](mfsampleextension-3dvideo.md) a la **valeur false** ou n’est pas défini.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 8 \[ Desktop Apps \| UWP\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ \| apps UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFSampleExtension \_ 3DVideo](mfsampleextension-3dvideo.md)
</dt> </dl>

 

 




