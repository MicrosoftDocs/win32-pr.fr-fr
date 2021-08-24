---
description: Spécifie si un exemple de média contient une image vidéo 3D.
ms.assetid: 1B0B9DBD-80EB-4876-B2F2-BE419AC84265
title: Attribut MFSampleExtension_3DVideo (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb959accfb3326e90068a26247eeab25e9aeaddacb720a0dfd64aa6e5b237a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722799"
---
# <a name="mfsampleextension_3dvideo-attribute"></a>\_Attribut MFSampleExtension 3DVideo

Spécifie si un exemple de média contient une image vidéo 3D.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="remarks"></a>Remarques

Si cet attribut a la **valeur true**, l’exemple de média contient une image vidéo qui comporte deux vues stéréoscopiques ou plus. La valeur par défaut est **FALSE**.

Un composant qui génère des images vidéo 3D doit affecter la **valeur true** à cet attribut sur chaque échantillon de média qui contient un frame 3D.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFSampleExtension \_ 3DVideo \_ SampleFormat](mfsampleextension-3dvideo-sampleformat.md)
</dt> </dl>

 

 




