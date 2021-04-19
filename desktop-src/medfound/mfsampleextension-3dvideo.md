---
description: Spécifie si un exemple de média contient une image vidéo 3D.
ms.assetid: 1B0B9DBD-80EB-4876-B2F2-BE419AC84265
title: Attribut MFSampleExtension_3DVideo (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e30ea247f6f12f05414df0ae4305ecaaa6e3e283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524093"
---
# <a name="mfsampleextension_3dvideo-attribute"></a>\_Attribut MFSampleExtension 3DVideo

Spécifie si un exemple de média contient une image vidéo 3D.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="remarks"></a>Notes

Si cet attribut a la **valeur true**, l’exemple de média contient une image vidéo qui comporte deux vues stéréoscopiques ou plus. La valeur par défaut est **FALSE**.

Un composant qui génère des images vidéo 3D doit affecter la **valeur true** à cet attribut sur chaque échantillon de média qui contient un frame 3D.

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

[MFSampleExtension \_ 3DVideo \_ SampleFormat](mfsampleextension-3dvideo-sampleformat.md)
</dt> </dl>

 

 




