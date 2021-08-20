---
description: Valeur spécifiant la taille, en octets, du type d’objet de métadonnées audio spatiales que le décodeur produira.
ms.assetid: C133693D-A8D5-4520-B561-57BF11074257
title: Attribut MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_LENGTH (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 784e1b210b616f4c42c2c3d410a207adc9c8c8ccaf751432cb027a7cc30cf951
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876810"
---
# <a name="mf_mt_spatial_audio_object_metadata_length-attribute"></a>\_Attribut de \_ \_ longueur des \_ métadonnées de l’objet audio spatial \_ \_ MF

Valeur spécifiant la taille, en octets, du type d’objet de métadonnées audio spatiales que le décodeur produira.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

L’objet blob de métadonnées avec le format spécifié est écrit à l’aide de l’interface [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) et lu à l’aide de l’interface [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) . L’objet blob de métadonnées est opaque pour le pipeline Media Foundation et les composants. L’attribut est appliqué au type de média audio spatial.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1703 \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 
