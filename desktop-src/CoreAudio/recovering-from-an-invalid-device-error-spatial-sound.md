---
description: Récupération à partir d’une erreur de Invalid-Device (son spatial)
title: Récupération à partir d’une erreur de Invalid-Device (son spatial)
ms.topic: article
ms.date: 10/29/2020
ms.openlocfilehash: 1ec4f040aff10f2d118b20c489e74d792c907113
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519421"
---
# <a name="recovering-from-an-invalid-device-error-spatial-sound"></a>Récupération à partir d’une erreur de Invalid-Device (son spatial)

La plupart des méthodes de l’API Microsoft spatiale audio, telles que [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient), [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream)et [ISpatialAudioObject](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), renvoient des codes d’erreur si l’appareil de point de terminaison audio utilisé par l’application cliente n’est pas valide ou si le format de rendu audio spatial est modifié sur le point de terminaison. Ces codes d’erreur indiquent que l’appareil de point de terminaison a été débranché, ou que le matériel audio ou les ressources matérielles associées ont été reconfigurés, désactivés, supprimés, que le mode audio spatial est modifié ou qu’il n’est pas possible de l’utiliser. Souvent, l’application peut récupérer à partir de cette erreur.

Les codes d’erreur qui indiquent une erreur de périphérique non valide sont les suivants :

- SPTLAUDCLNT_E_DESTROYED
- AUDCLNT_E_DEVICE_INVALIDATED
- AUDCLNT_E_RESOURCES_INVALIDATED
- AUDCLNT_E_UNSUPPORTED_FORMAT
- SPTLAUDCLNT_E_INTERNAL

## <a name="strategies-for-handling-invalid-device-errors"></a>Stratégies de gestion des erreurs de périphérique non valide

La stratégie recommandée pour la récupération à partir d’une erreur d’appareil non valide varie selon que l’application sélectionne automatiquement un appareil spécifique en fonction des exigences internes ou qu’il permet à l’utilisateur de sélectionner explicitement un appareil dans une liste d’appareils disponibles. 

### <a name="default-audio-device"></a>Périphérique audio par défaut

Si l’application sélectionne automatiquement l’appareil par défaut, procédez comme suit pour effectuer la récupération.

1. Libérez l’interface [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream) et [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) et toutes les autres interfaces audio spatiales utilisées pour le rendu. 
1. Appelez [IMMDeviceEnumerator :: GetDefaultAudioEndpoint](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) pour récupérer le périphérique audio par défaut actuel.
1. Essayez d’activer **ISpatialAudioClient** sur le périphérique audio.
1. Activez **ISpatialAudioObjectRenderStream**. 

### <a name="specifically-selected-audio-device"></a>Périphérique audio spécifiquement sélectionné

Si l’application sélectionne un périphérique audio spécifique, procédez comme suit pour effectuer la récupération.

1. Libérez l’interface ISpatialAudioObjectRenderStream et toutes les autres interfaces audio spatiales utilisées pour le rendu, mais ne libérez pas **ISpatialAudioClient**.
1. Utilisez l’instance **ISpatialAudioClient** actuelle pour activer **ISpatialAudioObjectRenderStream**.

Notez que pour les deux stratégies mentionnées ci-dessus, les mêmes étapes peuvent être appliquées aux applications qui utilisent les interfaces [ISpatialAudioObjectRenderStreamForMetadata](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata) ou [ISpatialAudioObjectRenderStreamForHrtf](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) . Remplacez simplement **ISpatialAudioObjectRenderStream** dans les étapes ci-dessus par les interfaces de métadonnées ou HRTF.


## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>
[Récupération à partir d’une erreur Invalid-Device](recovering-from-an-invalid-device-error.md) 
 [Gestion de flux](stream-management.md)
</dt> </dl>

 

 



