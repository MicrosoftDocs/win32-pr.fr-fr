---
description: Les \_ \_ constantes audio spatiale xxx définissent les valeurs relatives aux fonctions de son spatial.
ms.assetid: F1A01BDB-0CC2-45ED-A423-8CC7F54D4E55
title: Constantes SPATIAL_AUDIO_XXX (SpatialAudioMetadata. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db363260b21f47676c12aeb5eaf3c10149b571ed2771a4d9f907e98b0ba17aed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018247"
---
# <a name="spatial_audio_xxx-constants"></a>\_ \_ Constantes audio spatiale xxx

Les \_ \_ constantes audio spatiale xxx définissent les valeurs relatives aux fonctions de son spatial.



| Constante/valeur                                                                                                                                                                                                                                                                                       | Description                                                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPATIAL_AUDIO_POSITION"></span><span id="spatial_audio_position"></span><dl> <dt>**Spatial \_ \_Position AUDIO**</dt> <dt>200</dt> </dl>                                                   | Commande de métadonnées audio spatiales standard définie par Microsoft qui représente la position de l’écouteur dans le modèle standard utilisé par [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) où l’en-tête de l’écouteur est positionné au niveau des coordonnées (0, 0, 0), défini en mètres.<br/> |
| <span id="SPATIAL_AUDIO_POSITION_BYTE_COUNT"></span><span id="spatial_audio_position_byte_count"></span><dl> <dt>**Spatial \_ \_Nombre d' \_ octets \_ de position audio**</dt> <dt>sizeof (float) \* 3</dt> </dl> | Spécifie la taille de la valeur de **\_ \_ position audio spatiale** .<br/>                                                                                                                                                                                                        |
| <span id="SPATIAL_AUDIO_STANDARD_COMMANDS_START"></span><span id="spatial_audio_standard_commands_start"></span><dl> <dt>**Spatial \_ \_Commandes audio \_ STANDARD \_ Start**</dt> <dt>200</dt> </dl>    | Spécifie le début de la plage de commandes de métadonnées audio spatiales réservées par Microsoft. Les commandes de métadonnées personnalisées sont limitées à l’ID de commande 0-199. Les commandes 200 à 255 sont réservées à une utilisation par Microsoft.<br/>                                                           |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>SpatialAudioMetadata. h</dt> </dl> |



 

 




