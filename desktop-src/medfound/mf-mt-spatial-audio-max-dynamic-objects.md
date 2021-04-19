---
description: Spécifie le nombre maximal d’objets audio dynamiques qui peuvent être rendus par le point de terminaison audio simulataneously.
ms.assetid: 6B6D73C1-C2E6-4C23-BBAD-7B51E8441C71
title: Attribut MF_MT_SPATIAL_AUDIO_MAX_DYNAMIC_OBJECTS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358045079fb9cf52ad1fd0c8969f54723c7f02d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518721"
---
# <a name="mf_mt_spatial_audio_max_dynamic_objects-attribute"></a>\_ \_ \_ \_ \_ Attribut objets dynamiques Max audio spatial \_ MF

Spécifie le nombre maximal d’objets audio dynamiques qui peuvent être rendus par le point de terminaison audio simulataneously.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Un [**IMFSpatialAudioSample**](/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample) peut contenir moins d’échantillons que le nombre spécifié par cet attribut. Si un exemple contient plus d’objets audio que ce qui est spécifié par cet attribut, le comportement n’est pas défini.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1703 \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




