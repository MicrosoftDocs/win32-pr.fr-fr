---
description: Utilisation des rôles d’appareil
ms.assetid: 3b2cb1fe-0f11-4509-a6f3-513d2755cd29
title: Utilisation des rôles d’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c21ea667a6974634c1f9f0657dd02c13a621641c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114997"
---
# <a name="working-with-device-roles"></a>Utilisation des rôles d’appareil

L' [API MMDevice](mmdevice-api.md) prend en charge les rôles d’appareil. L’énumération [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) définit les rôles d’appareil pris en charge par l’API MMDevice.

> [!Note]  
> bien que l' [API MMDevice](mmdevice-api.md) prenne en charge les rôles d’appareil, l’interface utilisateur dans Windows Vista n’implémente pas la prise en charge de cette fonctionnalité.

 

Une application peut utiliser l’API MMDevice pour prendre en charge les [rôles d’appareil](device-roles.md) via les méthodes [**IMMDeviceEnumerator :: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) et [**IMMNotificationClient :: OnDefaultDeviceChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged) . toutefois, l’interface utilisateur de Windows Vista ne prend pas en charge l’affectation de rôles individuels à différents appareils. dans Windows Vista, l’interface utilisateur permet à l’utilisateur de sélectionner un périphérique audio par défaut pour le rendu et un périphérique audio par défaut pour la capture. Lorsque l’utilisateur sélectionne un appareil de rendu ou de capture par défaut, le système affecte les trois rôles d’appareil (eConsole, eMultimedia et eCommunications) à cet appareil. Les applications ne peuvent pas modifier les rôles affectés aux périphériques de point de terminaison audio. Le système d’exploitation permet uniquement à l’utilisateur d’attribuer des rôles d’appareil.

Un client peut s’inscrire pour recevoir une notification de l’API MMDevice chaque fois qu’une modification intervient dans l’attribution de rôles aux périphériques de point de terminaison audio. Lorsqu’un rôle passe d’un appareil à un autre, le client peut choisir de continuer ou d’enregistrer ses flux sur le même appareil ou de basculer les flux vers un autre appareil. Par défaut, les flux continuent à être lus (ou enregistrés) via l’appareil d’origine. dans Windows Vista, pour basculer les flux vers un autre appareil, le client doit supprimer les flux sur l’appareil d’origine et créer des flux de remplacement sur le nouvel appareil. dans Windows 7, le client peut écouter les nouvelles notifications pour implémenter un commutateur transparent sans interrompre la lecture ou la session de capture. Pour plus d’informations, consultez [routage de flux](stream-routing.md).

si vous envisagez d’utiliser Windows Vista pour tester votre application, vous pouvez configurer un environnement de test pour vérifier que l’application se comporte comme prévu lorsque l’utilisateur peut affecter des rôles d’appareil individuels à différents appareils. Pour plus d‘informations, envoyez un e-mail à uaa@microsoft.com.

## <a name="communication-devices"></a>Appareils de communication

l’interface utilisateur de Windows 7 a la possibilité d’ajouter des *appareils de communication*. Le panneau de contrôle du **son** permet à l’utilisateur de sélectionner un appareil de communication par défaut pour le rendu et la capture du flux audio. Par défaut, lorsqu’un nouvel appareil est connecté à l’ordinateur, le système d’exploitation effectue une détection automatique des rôles et détermine si l’appareil est adapté au rôle eCommunication. En ciblant les appareils de communication, vous pouvez développer des applications qui utilisent des API audio de base pour implémenter des solutions de communication PC-Phone. Par exemple, une application VoIP peut affecter ses flux d’entrée et de sortie vocaux aux appareils de point de terminaison de capture et de rendu par défaut avec le rôle eCommunications. Comme tout autre flux, une application de communication doit obtenir une référence au point de terminaison de l’appareil de communication en appelant [**IMMDeviceEnumerator :: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). Dans cet appel, l’application doit spécifier **eCommunications** dans le paramètre *role* . Les opérations de flux WASAPI sur un flux, ouvertes sur un appareil de communication, sont similaires à tout autre flux audio. L’application de communication peut améliorer l’expérience utilisateur en implémentant des comportements tels que l’utilisation de notifications à partir du point de terminaison de l’appareil. Pour plus d’informations, consultez [utilisation d’un appareil de communication](using-the-communication-device.md).

## <a name="automatic-device-role-detection"></a>Détection automatique du rôle d’appareil

Prenons l’exemple d’un scénario dans lequel un ordinateur possède un appareil de rendu par défaut, les haut-parleurs et un périphérique de capture par défaut, un microphone. L’utilisateur connecte un casque USB à l’ordinateur. Une fois les pilotes appropriés installés, le système d’exploitation tente de détecter un rôle à attribuer pour le nouveau périphérique audio.

dans Windows 7, la fonctionnalité de détection des rôles d’appareils a été considérablement améliorée pour déterminer les rôles appropriés adaptés aux périphériques audio. Tous les périphériques audio contiennent un ensemble de paramètres de configuration remplis par le fabricant de l’appareil, ce qui permet au système de décider de l’utilisation de l’appareil. Ces paramètres incluent des informations telles que l’emplacement physique du jack audio, le sous-type de prise Jack et les fonctionnalités de détection, afin que le système puisse déterminer si l’appareil est branché. En extrayant ces valeurs de l’appareil, le système d’exploitation détermine le rôle à attribuer à l’appareil. Dans ce scénario, le système a interrogé le périphérique du casque USB, a effectué la détection automatique des rôles et a décidé que l’appareil est le mieux adapté pour être un appareil de communication.

Une application peut également recevoir des informations de Jack à l’aide des API audio de base. Pour plus d’informations, consultez [**IKsJackDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription) et [**IKsJackDescription2**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rôles d’appareil](device-roles.md)
</dt> </dl>

 

 



