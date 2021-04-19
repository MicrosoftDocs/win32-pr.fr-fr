---
description: Contient l’horodatage de décodage (DTS) pour l’exemple.
ms.assetid: 4E0B8266-FF48-49A1-AB7B-A47C4F96AECD
title: Attribut MFSampleExtension_DecodeTimestamp (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9676b295eb16e7cb2bb607ef4a5074d24b276d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517582"
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
| Client minimal pris en charge<br/> | Applications Windows 8 \[ Desktop Apps \| UWP\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ \| apps UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Exemples d’attributs](sample-attributes.md)
</dt> </dl>

 

 




