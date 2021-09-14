---
description: Chaînes ID du point de terminaison
ms.assetid: 3c955e2d-daaa-4b77-8ca5-890383bb2d39
title: Chaînes ID du point de terminaison
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f04c07da78b92795ebadd7d8f9731f7188ae8dc3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114954"
---
# <a name="endpoint-id-strings"></a>Chaînes ID du point de terminaison

dans Windows Vista, le système génère des chaînes d’ID de point de terminaison pour identifier les [périphériques de point de terminaison audio](audio-endpoint-devices.md) dans le système. Une chaîne d’ID de point de terminaison est une chaîne de caractères larges se terminant par un caractère null. La chaîne d’ID de point de terminaison pour un périphérique de point de terminaison audio spécifique identifie de façon unique l’appareil parmi tous les périphériques de point de terminaison audio du système.

Si un système contient deux ou plusieurs périphériques de carte audio identiques, les périphériques de point de terminaison audio correspondants auront des noms conviviaux identiques, mais chaque périphérique de point de terminaison aura une chaîne d’ID de point de terminaison unique. Pour plus d’informations sur l’obtention du nom convivial d’un appareil de point de terminaison, consultez Propriétés de l' [appareil](device-properties.md).

Après avoir obtenu une instance d’interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) pour un périphérique de point de terminaison audio, un client peut appeler la méthode [**IMMDevice :: GetId**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) pour obtenir la chaîne d’ID de point de terminaison de l’appareil. Un client peut utiliser la chaîne d’ID de point de terminaison pour créer une instance du périphérique de point de terminaison audio ultérieurement ou dans un processus différent en appelant la méthode [**IMMDeviceEnumerator :: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) .

Un client peut organiser pour recevoir une notification lorsque l’état d’un périphérique de point de terminaison audio change. Pour recevoir des notifications, le client implémente une interface [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) et enregistre cette interface avec l’API MMDevice. Lorsque l’état d’un périphérique de point de terminaison change, l’API MMDevice appelle la méthode appropriée dans l’interface [**EDataFlow**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) du client. L’un des paramètres d’entrée de la méthode est la chaîne d’ID de point de terminaison qui identifie l’appareil de point de terminaison dont l’État a changé. Pour plus d’informations sur **EDataFlow**, consultez [événements d’appareil](device-events.md).

les api audio héritées telles que DirectSound et les fonctions multimédias Windows disposent de leurs propres interfaces pour l’énumération et l’identification des périphériques audio. dans Windows Vista, ces interfaces ont été étendues pour fournir les chaînes d’ID de point de terminaison qui identifient les appareils de point de terminaison qui sous-tendent les abstractions d’appareil présentées par les api.

Au cours de l’énumération d’appareils DirectSound, DirectSound fournit la chaîne d’ID de point de terminaison pour chaque appareil qu’elle énumère. Pour plus d’informations, consultez [événements audio pour les applications audio héritées](audio-events-for-legacy-audio-applications.md).

Pour obtenir la chaîne d’ID de point de terminaison pour un périphérique Waveform hérité, utilisez la fonction [**waveOutMessage**](/previous-versions//dd743865(v=vs.85)) ou [**waveInMessage**](/previous-versions//dd743846(v=vs.85)) pour envoyer un \_ message DRV QUERYFUNCTIONINSTANCEID au pilote de périphérique Waveform. pour obtenir un exemple de code illustrant l’utilisation de ce message, consultez [rôles d’appareil pour les Applications multimédias héritées Windows](device-roles-for-legacy-windows-multimedia-applications.md).

Pour plus d’informations sur l’utilisation des fonctionnalités des API audio de base pour améliorer les applications qui utilisent des API audio héritées, consultez [interopérabilité avec les API audio héritées](interoperability-with-legacy-audio-apis.md).

Les clients doivent traiter le contenu de la chaîne d’ID de point de terminaison comme opaque. Autrement dit, les clients ne doivent pas tenter d’analyser le contenu de la chaîne pour obtenir des informations sur l’appareil. La raison en est que le format de chaîne n’est pas défini et peut passer d’une implémentation du module système de l’API MMDevice à la suivante.

La durée de vie d’une chaîne d’ID de point de terminaison est liée à l’installation de l’appareil. La chaîne d’ID de point de terminaison d’un appareil change si l’utilisateur met à niveau le pilote de périphérique, ou si l’utilisateur désinstalle l’appareil et l’installe à nouveau. Toutefois, la chaîne d’ID de point de terminaison reste inchangée entre les redémarrages du système et la chaîne d’ID de point de terminaison d’un périphérique audio USB reste inchangée si l’utilisateur déconnecte l’appareil et le réintègre.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Périphériques de point de terminaison audio](audio-endpoint-devices.md)
</dt> </dl>

 

 
