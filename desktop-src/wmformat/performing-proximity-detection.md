---
title: Détection de proximité en cours
description: Détection de proximité en cours
ms.assetid: 73207c4c-2d8d-4ec3-b3d0-78f55ee0a754
keywords:
- Windows Media Format SDK, détection de proximité
- Windows Media Format SDK, détection de proximité
- ASF (Advanced Systems Format), en effectuant la détection de proximité
- ASF (format avancé des systèmes), exécution de la détection de proximité
- ASF (Advanced Systems Format), détection de proximité
- ASF (format de systèmes avancés), détection de proximité
- gestion des droits numériques (DRM), réalisation de la détection de proximité
- DRM (Digital Rights Management), réalisation de la détection de proximité
- gestion des droits numériques (DRM), détection de proximité
- DRM (gestion des droits numériques), détection de proximité
- détection de proximité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9628a6c33832b56858e5c457f15fd0935c2c436
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381465"
---
# <a name="performing-proximity-detection"></a>Détection de proximité en cours

Avant de pouvoir diffuser en continu des données chiffrées sur un appareil inscrit dans le protocole Windows Media DRM 10 pour les périphériques réseau, vous devez effectuer un processus appelé détection de proximité (également appelé validation). Ce processus implique l’envoi de messages à l’appareil et la réception de réponses. Le temps nécessaire à la réception d’une réponse est utilisé pour déterminer si l’appareil est suffisamment « proche » de l’ordinateur sur le réseau pour recevoir des données sécurisées. En confirmant que l’appareil est physiquement proche de l’ordinateur client sur le réseau, vous pouvez empêcher l’usurpation d’identité et d’autres accès non autorisés.

Lorsque la détection de proximité s’est terminée avec succès, l’appareil est considéré comme valide. Vous pouvez vérifier si un appareil est valide en appelant la méthode [**IWMRegisteredDevice :: IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) . Les appareils doivent être validés toutes les 48 heures. Un appareil qui a été validé plus de 48 heures avant l’exécution de votre programme doit être revalidé en effectuant à nouveau le processus de détection de proximité.

Pour effectuer la détection de proximité, vous devez établir des communications avec l’appareil, puis appeler la méthode [**IWMProximityDetection :: StartDetection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmproximitydetection-startdetection) . Le processus de détection est exécuté de façon asynchrone par les composants DRM internes du kit de développement logiciel (SDK) du format Windows Media. Votre application doit inclure une implémentation de l’interface [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) pour traiter les messages de détection de proximité.

Deux messages sont envoyés par le processus de détection de proximité : un message de résultat et un message d’achèvement.

Le message de résultat, le \_ résultat de proximité WMT \_ , est envoyé lorsque le processus de détection est terminé. Le paramètre *HR* de la méthode de rappel [**OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) indique si l’appareil est suffisamment proche de l’ordinateur client. Si le paramètre *HR* du message de résultat indique une réussite, le paramètre *PValue* contient une **valeur DWORD** qui spécifie la latence mesurée sur le périphérique en millisecondes.

Le message d’achèvement, la \_ proximité WMT \_ terminée, est envoyé lorsque la détection est finalisée. Vous ne devez libérer l’interface [**IWMProximityDetection**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) qu’après avoir reçu ce message.

Lorsque la détection de proximité d’un appareil est réussie, la base de données d’inscription des appareils est automatiquement mise à jour. Les appels suivants à [**IWMRegisteredDevice :: IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) retournent la **valeur TRUE** jusqu’à 48 heures, et l’appareil doit être revalidé.

**Remarque** DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation du protocole Windows Media DRM 10 pour les périphériques réseau**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




