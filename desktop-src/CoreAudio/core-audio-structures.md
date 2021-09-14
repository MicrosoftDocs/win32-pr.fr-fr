---
description: Structures audio principales
ms.assetid: 92585cd4-baa9-4f75-816e-b83f5badad37
title: Structures audio principales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078f49ac7abce8fc2773549df26431b780550c1b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115029"
---
# <a name="core-audio-structures"></a>Structures audio principales

cette section décrit les structures utilisées par les api Audio principales dans Windows Vista et versions ultérieures.



| Structure                                                                     | Description                                                                                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_données de \_ notification du volume audio \_**](/windows/desktop/api/Endpointvolume/ns-endpointvolume-audio_volume_notification_data)   | Décrit une modification du niveau de volume ou de l’État muet d’un périphérique de point de terminaison audio.                                                                                 |
| [**paramètres d’activation de DIRECTX \_ audio \_ \_**](/windows/win32/api/mmdeviceapi/ns-mmdeviceapi-directx_audio_activation_params) | Spécifie les paramètres d’initialisation d’un flux DirectSound.                                                                                                   |
| [**Description de KSJACK \_**](/windows/win32/api/devicetopology/ns-devicetopology-ksjack_description)                             | Récupéré par le biais de [**IKsJackDescription :: GetJackDescription**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription-getjackdescription); décrit une prise jack audio.                                 |
| [**KSJACK \_ Description2**](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_description2)<br/>                | Récupéré par le biais de [**IKsJackDescription2 :: GetJackDescription2**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription2-getjackdescription2); décrit une prise jack audio. <br/>                 |
| [**\_informations sur le récepteur KSJACK \_**](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_sink_information)<br/>       | Récupéré par le biais de [**IKsJackSinkInformation :: GetJackSinkInformation**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjacksinkinformation-getjacksinkinformation); décrit un récepteur Jack audio.<br/> |
| [**LUID**](/windows/desktop/api/Devicetopology/ns-devicetopology-luid)<br/>                                               | Stocke l’identificateur de port vidéo.<br/>                                                                                                                        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de référence de programmation](programming-reference.md)
</dt> </dl>

 

 




