---
description: Spécifie les informations de trame de référence à long terme et est retourné sur l’exemple de sortie.
ms.assetid: 0632D780-C56B-4FDB-8A76-B7A7DE414242
title: Attribut MFSampleExtension_LongTermReferenceFrameInfo (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3af85ffa5876cdf58a21a6933c46f460c23e7456
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414064"
---
# <a name="mfsampleextension_longtermreferenceframeinfo-attribute"></a>\_Attribut MFSampleExtension LongTermReferenceFrameInfo

Spécifie les informations de trame de référence à long terme et est retourné sur l’exemple de sortie.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

**Encodeurs H. 264/AVC :**

Les encodeurs retournent cet attribut sur l’exemple de sortie lorsque l’application contrôle les frames LTR, qui est spécifié par [CODECAPI \_ AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).

MFSampleExtension \_ LongTermReferenceFrameInfo retourne jusqu’à deux champs.

Le premier champ, bits \[ 0.. 15 \] , est *LongTermFrameIdx* associé au frame de sortie s’il est marqué comme cadre LTR. La première valeur est 0xFFFF, si ce frame de sortie est une trame de référence à bref terme ou un frame non-référence.

Le deuxième champ, bits \[ 16.. 31 \] , est une image bitmap composée de *MaxNumLTRFrames* de nombreux bits qui indiquent le ou les frames LTR utilisés pour l’encodage de ce frame de sortie, à partir du bit 16. Le reste de bits doit être défini sur 0. La deuxième valeur est 0 si cette trame de sortie n’est pas encodée à l’aide d’une trame LTR. *MaxNumLTRFrames* est le nombre maximal de frames LTR définis via [CODECAPI \_ AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[applications Windows 8.1 desktop apps \| UWP\]<br/>                                |
| Serveur minimal pris en charge<br/> | Windows Server 2012 Applications de \[ Bureau R2 \| applications UWP\]<br/>                     |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




