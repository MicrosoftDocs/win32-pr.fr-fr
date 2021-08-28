---
description: Obtient un objet de type IMFCollection contenant des objets IMFSample qui contiennent des unités de couche d’abstraction de réseau (NALUs) et des unités SEI (Supplémental addition information) transmises par un décodeur.
ms.assetid: F9FD7959-A78A-4C72-8326-EE8FF9066E6C
title: Attribut MFSampleExtension_ForwardedDecodeUnits (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2298a29d722c118fb79d5f0b49aa9d3d94fd735150a65772eb15e6da7638445
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713729"
---
# <a name="mfsampleextension_forwardeddecodeunits-attribute"></a>\_Attribut MFSampleExtension ForwardedDecodeUnits

Obtient un objet de type [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) contenant des objets [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) qui contiennent des unités de couche d’abstraction de réseau (NALUs) et des unités SEI (Supplémental addition information) transmises par un décodeur.

## <a name="data-type"></a>Type de données

**IUnknown**

## <a name="remarks"></a>Remarques

La collection contient toutes les unités NALU/SEI personnalisées depuis la suppression du frame précédent avec les octets de prévention de l’émulation.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




