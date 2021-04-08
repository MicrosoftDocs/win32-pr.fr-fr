---
title: Arrêt, suspension et redémarrage de la lecture
description: Arrêt, suspension et redémarrage de la lecture
ms.assetid: 39751342-63bc-4e68-bf9e-38665db8a05c
keywords:
- Wave audio, arrêt de la lecture
- Waveform-interface audio, arrêt de la lecture
- lecture des fichiers Waveform-Audio, arrêt de la lecture
- Wave audio, suspension de la lecture
- Waveform-interface audio, suspension de la lecture
- lecture de fichiers Waveform-Audio, suspension de la lecture
- audio Wave, redémarrage de la lecture
- Wave-interface audio, redémarrage de la lecture
- lecture de fichiers wave-audio, redémarrage de la lecture
- waveOutPause fonction)
- waveOutReset fonction)
- waveOutRestart fonction)
- arrêt de la lecture des données Waveform
- suspension de la lecture des signaux audio
- redémarrage de la lecture Waveform-Audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6a4756a08317923056114259588a95bc62e97f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101492"
---
# <a name="stopping-pausing-and-restarting-playback"></a>Arrêt, suspension et redémarrage de la lecture

Vous pouvez arrêter ou suspendre la lecture pendant la lecture de l’audio Wave. Une fois la lecture suspendue, vous pouvez la redémarrer. Windows fournit les fonctions suivantes pour contrôler la lecture des signaux Wave-audio.



| Fonction                                 | Description                                                                                 |
|------------------------------------------|---------------------------------------------------------------------------------------------|
| [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)     | Suspend la lecture sur un appareil de sortie Waveform-Audio.                                          |
| [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)     | Arrête la lecture sur un périphérique de sortie Waveform-Audio et marque tous les blocs de données en attente comme terminés. |
| [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart) | Reprend la lecture sur un appareil de sortie Waveform-Audio suspendu.                                  |



 

La suspension d’un périphérique Wave-audio à l’aide de [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause) peut ne pas être instantanée. le pilote peut terminer la lecture du bloc actuel avant la suspension de la lecture.

En général, dès que le premier bloc de données Waveform Audio est envoyé à l’aide de la fonction [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) , le périphérique Waveform-Audio commence à fonctionner. Si vous ne souhaitez pas que le son commence immédiatement, appelez **waveOutPause** avant d’appeler **waveOutWrite**. Ensuite, lorsque vous souhaitez commencer à émettre des données Waveform-Audio, appelez [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart).

Vous ne pouvez pas utiliser **waveOutRestart** pour redémarrer un appareil qui a été arrêté avec [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset); vous devez utiliser **waveOutWrite** pour envoyer le premier bloc de données afin de reprendre la lecture sur l’appareil.

 

 