---
description: XAudio2 peut appeler des fonctions fournies par le client pour le notifier de façon asynchrone de certains événements qui se produisent dans le thread de traitement audio.
ms.assetid: 4fbd4229-f7ac-33b3-b4b7-f09150a60598
title: Rappels XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3377bd029cc2e21971748eaca7309dd44390a5bd3420d772c45264dfdbd075c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054289"
---
# <a name="xaudio2-callbacks"></a>Rappels XAudio2

XAudio2 peut appeler des fonctions fournies par le client pour le notifier de façon asynchrone de certains événements qui se produisent dans le thread de traitement audio. Ces rappels peuvent être globaux ou spécifiques à une voix source donnée. Pour recevoir des rappels de moteur globaux, le client doit fournir une instance d’une classe qui implémente l’interface [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) lors de l’initialisation de XAudio2. Pour recevoir des rappels vocaux sources, le client doit fournir une instance d’une classe qui implémente l’interface [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) lors de la création de voix source. Pour plus d’informations, consultez **IXAudio2EngineCallback** et **IXAudio2VoiceCallback**.

Vous devez implémenter les rappels avec précaution pour éviter de provoquer des interruptions dans l’audio. À chaque fois qu’un rappel est en cours d’exécution, XAudio2 ne peut pas générer de données audio. Des retards de plus de quelques millisecondes peuvent entraîner un problème audio. Les retards de cette nature génèrent également la sortie du débogueur. Cela indique des problèmes de performances potentiels. Au minimum, les fonctions de rappel ne doivent pas effectuer les opérations suivantes :

-   Accéder au disque dur ou à un autre stockage permanent
-   Effectuer des appels d’API coûteux ou bloquants
-   Synchroniser avec d’autres parties du code client
-   Exiger une utilisation importante du processeur

Si la conception du client requiert un rappel pour déclencher des actions telles que celles indiquées précédemment, le rappel doit signaler un thread client différent pour effectuer le travail. Vous pouvez le faire avec un mécanisme **SetEvent** simple ou des mécanismes plus sophistiqués comme une file d’attente de commandes non bloquante qui est consommée par un autre thread.

## <a name="ixaudio2enginecallback"></a>IXAudio2EngineCallback

La classe [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) contient des méthodes qui notifient le client lorsque certains événements se produisent dans le moteur XAudio2. Ces méthodes doivent être implémentées par le client XAudio2. XAudio2 appelle ces méthodes au moyen d’un pointeur d’interface fourni par le client à l’aide de la méthode [**IXAudio2 :: RegisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) . Toutes ces méthodes retournent **void**, plutôt qu’un **HRESULT**.

## <a name="ixaudio2voicecallback"></a>IXAudio2VoiceCallback

La classe [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) contient des méthodes qui informent le client lorsque certains événements se produisent dans une voix source XAudio2 spécifique. XAudio2 appelle ces méthodes au moyen d’un pointeur d’interface fourni par le client dans [**IXAudio2 :: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice). Comme avec [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback), ces méthodes doivent être implémentées par le client XAudio2 et retourner **void** plutôt qu’un **HRESULT**.

Comme mentionné précédemment, il est essentiel que les implémentations fournies par le client de ces rappels retournent aussi rapidement que possible, de préférence en quelques millisecondes. Les rappels sont exécutés dans le thread de traitement audio, et tout le traitement est interrompu jusqu’à ce que le rappel soit retourné. Un délai dans un rappel peut facilement entraîner un problème audio.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rappels](callbacks.md)
</dt> <dt>

[Guide de programmation XAudio2](programming-guide.md)
</dt> <dt>

[Procédure : utiliser des rappels de voix source](how-to--use-source-voice-callbacks.md)
</dt> <dt>

[Procédure : utiliser des rappels de moteur](how-to--use-engine-callbacks.md)
</dt> <dt>

[Procédure : diffuser un son en continu à partir du disque](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 
