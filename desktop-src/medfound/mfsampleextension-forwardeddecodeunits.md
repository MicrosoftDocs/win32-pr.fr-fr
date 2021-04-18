---
description: Obtient un objet de type IMFCollection contenant des objets IMFSample qui contiennent des unités de couche d’abstraction de réseau (NALUs) et des unités SEI (Supplémental addition information) transmises par un décodeur.
ms.assetid: F9FD7959-A78A-4C72-8326-EE8FF9066E6C
title: Attribut MFSampleExtension_ForwardedDecodeUnits (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2ab5c10a4a7fb4dfd201f9c494c1bc65e14c162
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519834"
---
# <a name="mfsampleextension_forwardeddecodeunits-attribute"></a>\_Attribut MFSampleExtension ForwardedDecodeUnits

Obtient un objet de type [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) contenant des objets [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) qui contiennent des unités de couche d’abstraction de réseau (NALUs) et des unités SEI (Supplémental addition information) transmises par un décodeur.

## <a name="data-type"></a>Type de données

**IUnknown**

## <a name="remarks"></a>Notes

La collection contient toutes les unités NALU/SEI personnalisées depuis la suppression du frame précédent avec les octets de prévention de l’émulation.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1709 \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




