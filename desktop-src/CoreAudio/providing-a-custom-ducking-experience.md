---
description: Une application peut refuser l’expérience de l’utilisation des canards par défaut gérée par le système et la remplacer par une implémentation personnalisée.
ms.assetid: 18290d05-b114-476b-8365-6bbb5fe6cffc
title: Fournir un comportement de canard personnalisé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4051dc7b79f698f10d007beaafa97e90d79f3b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111310"
---
# <a name="providing-a-custom-ducking-behavior"></a>Fournir un comportement de canard personnalisé

Une application peut refuser l’expérience de l' [utilisation des canards par défaut](stream-attenuation.md) gérée par le système et la remplacer par une implémentation personnalisée.

Une application peut fournir une expérience de canard personnalisée. Par exemple, le lecteur Windows Media offre sa propre expérience en matière de mise en suspens en suspendant le flux multimédia actuel pendant une session de communication et en reprenant la lecture lorsque la session est fermée. Un exemple d’application multimédia qui implémente un canard est inclus dans SDK Windows exemples ; Pour plus d’informations, consultez [DuckingMediaPlayer](duckingmediaplayer.md). Pour simuler l’expérience de l’ouverture et de la fermeture des flux de communication et la génération d’événements de canard, consultez [DuckingCaptureSample](duckingcapturesample.md), qui est également inclus avec SDK Windows exemples.

Une application multimédia qui lit des sons à atténuer doit être consciente des flux de communication, lorsqu’ils sont ouverts et fermés dans le système. L’implémentation personnalisée peut être fournie à l’aide de MediaFoundation, DirectShow ou DirectSound, qui utilisent les API audio de base. Un client direct WASAPI peut également remplacer la gestion par défaut s’il sait à quel moment la session de communication démarre et se termine.

**Pour fournir une expérience de canard personnalisée, un client WASAPI doit effectuer les tâches suivantes :**

1.  Inscrivez-vous pour recevoir des événements de notification du *Gestionnaire de canards*, un composant du système audio qui gère les notifications relatives aux modifications du flux de communication. Pour plus d’informations, vous [obtenez des événements de canard](handling-audio-ducking-events-from-communication-devices.md).
    > [!Note]  
    > Si le client est inscrit pour recevoir des notifications d’inversion, le gestionnaire de canards désactive le comportement par défaut fourni par le système. Si le comportement par défaut est désactivé de manière explicitement (voir [désactivation de l’expérience de l’utilisation de l’environnement par défaut](disabling-the-ducking-experience.md)) et que le client ne fournit pas de comportement de remplacement, l’application ne rencontre pas de comportement d’inversion.

     

2.  Écoutez les notifications d’événement Duck envoyées par le gestionnaire de canards et effectuez le comportement de l’encadrement souhaité. Pour plus d’informations sur l’implémentation d’un comportement de mise en œuvre, consultez [considérations relatives à l’implémentation pour l’installation de notifications](handling-audio-ducking-events-from-communication-devices.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation d’un appareil de communication](using-the-communication-device.md)
</dt> <dt>

[Expérience de l’utilisation des canards par défaut](stream-attenuation.md)
</dt> <dt>

[Désactivation de l’expérience de l’utilisation des canards par défaut](disabling-the-ducking-experience.md)
</dt> <dt>

[Considérations relatives à l’implémentation pour l’installation de notifications](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[Obtention d’événements de canard](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



