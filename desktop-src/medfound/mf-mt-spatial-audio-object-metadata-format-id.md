---
description: GUID défini par décodeur qui identifie le format de métadonnées audio spatial, en avertissant les composants en aval du type d’objet de métadonnées que le décodeur produira.
ms.assetid: 9714A2C7-25A1-4735-A0AC-22329ECBBC46
title: Attribut MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_FORMAT_ID (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed16188a24b4c61facf1e325867d093b9b5cc869
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203110"
---
# <a name="mf_mt_spatial_audio_object_metadata_format_id-attribute"></a>\_Attribut d' \_ \_ ID de \_ \_ format de métadonnées d’objet audio \_ spatial \_ MF

GUID défini par décodeur qui identifie le format de métadonnées audio spatial, en avertissant les composants en aval du type d’objet de métadonnées que le décodeur produira.

## <a name="data-type"></a>Type de données

**GUID**

## <a name="remarks"></a>Notes

L’objet blob de métadonnées avec le format spécifié est écrit à l’aide de l’interface [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) et lu à l’aide de l’interface [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) . L’objet blob de métadonnées est opaque pour le pipeline Media Foundation et les composants. L’attribut est appliqué au type de média audio spatial. Si un composant en aval ne prend pas en charge le format de métadonnées spécifié par le GUID, le composant doit rejeter le type de média d’entrée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1703 \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 
