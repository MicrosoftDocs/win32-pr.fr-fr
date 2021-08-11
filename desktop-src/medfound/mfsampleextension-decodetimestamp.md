---
description: Contient l’horodatage de décodage (DTS) pour l’exemple.
ms.assetid: 4E0B8266-FF48-49A1-AB7B-A47C4F96AECD
title: Attribut MFSampleExtension_DecodeTimestamp (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e0d72ea69f487efe24148fa8ce60ad05eb7a124673f02a78e70c67f604a51bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241480"
---
# <a name="mfsampleextension_decodetimestamp-attribute"></a>\_Attribut MFSampleExtension DecodeTimestamp

Contient l’horodatage de décodage (DTS) pour l’exemple.

## <a name="data-type"></a>Type de données

**UINT64**

## <a name="remarks"></a>Notes

La valeur de l’attribut est le DTS en unités de 100 nanosecondes. Le DTS est défini dans certaines normes d’encodage, y compris MPEG. Le DTS spécifie le moment où l’image encodée doit être décodée. Si la vidéo encodée contient des frames B, les DTS peuvent différer de l’heure de la présentation, car les images B apparaissent hors de l’ordre temporel dans le flux binaire.

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

[Exemples d’attributs](sample-attributes.md)
</dt> </dl>

 

 




